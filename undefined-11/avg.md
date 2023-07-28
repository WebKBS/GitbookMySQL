---
description: 평균을 구한다.
---

# AVG()

```sql
SELECT AVG(<열 이름>) FROM <테이블 이름>;
```

사용 방법은 SUM과 같다.



### GROUP BY와 조합해서 사용하기

```sql
SELECT <열 이름>, AVG(<합칠 열 이름>) FROM <테이블 이름> GROUP BY <열 이름>;
```

조합한 열과 평균을 내기에 편리하다.



조합된 평균 개수를 보려면 COUNT 사용하기

```sql
SELECT <열 이름>, COUNT(*),SUM(<합칠 열 이름>) FROM <테이블 이름> GROUP BY <열 이름>;
```

