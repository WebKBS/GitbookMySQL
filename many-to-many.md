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

### JOIN으로 원하는 값 가져오기

```sql
SELECT 
    title, rating
FROM
    series
        JOIN
    reviews ON series.id = reviews.series_id;
```



### 오름차순

```sql
- 그룹짓기
SELECT title, ROUND(AVG(rating), 2) AS avg_rating FROM series -- AVG로 평균값 내기 ROUND로 소수점2자리까지
JOIN reviews ON series.id = reviews.series_id
GROUP BY title
ORDER BY avg_rating; -- 오름차순
```
