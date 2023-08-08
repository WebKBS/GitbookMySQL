# 일 대 다 One To Many

## 테이블 만들기

```sql
CREATE TABLE <고객>(
    id  INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    email VARCHAR(50)
);

CREATE TABLE <주문>(
    id INT PRIMARY KEY AUTO_INCREMENT,
    order_date DATE,
    amount DECIMAL(8,2),
    customer_id INT,
    FOREIGN KEY (customer_id) REFERENCES <고객>(id)
    -- FOREIGN KEY로 customers id와 연결시켜줘야한다.
);
```

테이블 생성시 FOREIGN KEY로  제약조건 관계를 맺어줘야한다.
