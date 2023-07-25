# 비교 연산자

## >, <

```sql
-- 원하는 값보다 큰 값을 출력할 때
SELECT * FROM <테이블 이름> WHERE <열 이름> > <원하는 값>;

-- 원하는 값보다 작은 값을 출력할 때
SELECT * FROM <테이블 이름> WHERE <열 이름> < <원하는 값>;
```



## >=, <=

```sql
-- 원하는 값보다 크거나 같은 값을 출력할 때
SELECT * FROM <테이블 이름> WHERE <열 이름> >= <원하는 값>;

-- 원하는 값보다 작거나 같은 값을 출력할 때
SELECT * FROM <테이블 이름> WHERE <열 이름> <= <원하는 값>;
```



{% hint style="warning" %}
값이 NULL인 값은 출력이 되지 않는다.
{% endhint %}

