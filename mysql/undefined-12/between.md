---
description: 원하는 값의 범위를 좁혀 값을 검색한다.
---

# BETWEEN

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> BETWEEN <값> AND <값>
```



### 원하는 값을 제외 NOT BETWEEN

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> NOT BETWEEN <값> AND <값>
```

BETWEEN 앞에 NOT을 붙이면 된다.
