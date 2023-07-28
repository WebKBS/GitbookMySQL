---
description: 합계를 구한다.
---

# SUM()

```sql
SELECT SUM(<열 이름>) FROM <테이블 이름>;
```

\*\* 문자는 합치지 않는다.

### GROUP BY 조합해서 사용하기

```sql
SELECT <열 이름>, SUM(<합칠 열 이름>) FROM <테이블 이름> GROUP BY <열 이름>;
```

<열 이름>은 추가해서 볼 열 이름이다. GROUP BY와 열 이름이 같아야 한다.\
합계와 대상의 열 이름을 동시에 볼수 있다.



### 카운트와 조합해서 사용하기

```sql
SELECT <열 이름>, COUNT(*),SUM(<합칠 열 이름>) FROM <테이블 이름> GROUP BY <열 이름>;
```
