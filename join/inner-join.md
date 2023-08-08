---
description: 연결된 테이블의 교집합 부분을 추출한다.
---

# INNER JOIN

<figure><img src="../.gitbook/assets/Group 1.png" alt=""><figcaption></figcaption></figure>

```sql
SELECT * FROM <테이블1>
JOIN <테이블2> ON <테이블2>.<열 이름> = <테이블1>.<열 이름>;
```

#### 예시

```sql
-- id값을 join 해본다.
SELECT * FROM customers
JOIN orders ON orders.customer_id = customers.id;
```



### GROUP BY와 함께 사용하기

```sql
SELECT 
    <열이름1>, <열이름2>, SUM(<합할 값>) AS <변경할 이름>
FROM
    <테이블1>
        JOIN
    <테이블2> ON <테이블2>.<열 이름> = <테이블1>.<열 이름>;
GROUP BY <열이름1> , <열이름2>
ORDER BY <변경할 이름>;
```
