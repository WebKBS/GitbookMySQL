# 다 대 다 Many TO Many

## 테이블 만들기

```sql
-- 예시
CREATE TABLE reviewers (
    id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL
);
 
CREATE TABLE series (
    id INT PRIMARY KEY AUTO_INCREMENT,
    title VARCHAR(100),
    released_year YEAR,
    genre VARCHAR(100)
);
 
CREATE TABLE reviews (
    id INT PRIMARY KEY AUTO_INCREMENT,
    rating DECIMAL(2 , 1 ),
    series_id INT,
    reviewer_id INT,
    FOREIGN KEY (series_id) -- 연결할 테이블 id를 지정해주자
        REFERENCES series (id),
    FOREIGN KEY (reviewer_id) -- 연결할 테이블 id를 지정해주자
        REFERENCES reviewers (id)
);

```

{% hint style="info" %}
다대다는 테이블과 테이블을 서로 이어줄 또 다른 테이블이 있어야한다.
{% endhint %}
