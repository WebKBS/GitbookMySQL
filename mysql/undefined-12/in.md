---
description: OR 연산자가 여러개일 때 대신해서 사용.
---

# IN 연산자

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> IN (<값>, <값>, <값>, ...);
```



### 원하는  결과외 반대의 데이터를 찾을때 NOT IN

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> NOT IN (<값>, <값>, <값>, ...);
```
