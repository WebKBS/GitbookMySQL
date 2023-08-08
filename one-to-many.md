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



{% hint style="warning" %}
FOREIGN KEY로 연결된 행의 값은 DELETE로 삭제시 지워지지 않는다.
{% endhint %}

만약 삭제를 가능 하게 하려면 ON DELETE CASCADE를 추가해 줘야한다.

```sql
CREATE TABLE <주문>(
    id INT PRIMARY KEY AUTO_INCREMENT,
    order_date DATE,
    amount DECIMAL(8,2),
    customer_id INT,
    FOREIGN KEY (customer_id) REFERENCES <고객>(id),
    ON DELETE CASCADE
);
```

{% hint style="warning" %}
ON DELETE CASCADE 를 설정하고

DELETE로 해당 데이터를 삭제하면

FOREIGN KEY 와 연결된 모든 데이터도 함께 삭제된다.
{% endhint %}
