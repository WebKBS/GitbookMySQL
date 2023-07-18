---
description: 행 표시 값 제한
---

# LIMIT

```sql
SELECT <열 이름> FROM <테이블 이름> LIMIT <표시할 행 수>;
```

보고싶은 행을 갯수 제한을 둔다.

```sql
-- 예시
SELECT <열 이름> FROM <테이블 이름> LIMIT 5;
-- 행을 5개까지만 표시한다.
```

### ORDER BY와 함께 사용

```sql
SELECT <열 이름> FROM <테이블 이름> ORDER BY <정렬할 열이름> LIMIT <표시할 행 수>;
-- 오름차순

SELECT <열 이름> FROM <테이블 이름> ORDER BY <정렬할 열이름> DESC LIMIT <표시할 행 수>;
-- 내림차순
```

### &#x20;표시할 행의 숫자 지정하기

```sql
SELECT <열 이름> FROM <테이블 이름> LIMIT <시작 숫자 지정>, <표시할 행 수>;
```

```sql
-- 예시
SELECT <열 이름> FROM <테이블 이름> LIMIT 4, 10;
-- 5번쨰 행 시작부터 10개의 행 데이터를 보여준다.
```

{% hint style="info" %}
LIMIT의 시작 숫자 지정은 0부터 시작한다. (LIMIT 0, 10)
{% endhint %}
