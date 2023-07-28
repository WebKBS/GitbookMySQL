---
description: 원하는 값의 범위를 좁혀 값을 검색한다.
---

# BETWEEN

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> BETWEEN <값> AND <값>;
```



### 원하는 값을 제외 NOT BETWEEN

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> NOT BETWEEN <값> AND <값>;
```

BETWEEN 앞에 NOT을 붙이면 된다.



## BETWEEN으로 날짜 및 시간 검색

```sql
-- 시간 검색
SELECT * FROM <테이블 이름> WHERE <열 이름>
    BETWEEN CAST(<시간> AS TIME)
    AND CAST(<시간> AS TIME);
-- 예시
SELECT * FROM <테이블 이름> WHERE <열 이름>
    BETWEEN CAST("09:00:00" AS TIME) 
    AND CAST("14:00:00" AS TIME);
    
-- 또 다른 방법
SELECT * FROM <테이블 이름> WHERE HOUR(<열 이름>)
BETWEEN <시간> AND <시간>;
-- 예시
SELECT * FROM <테이블 이름> WHERE HOUR(<열 이름>)
BETWEEN 9 AND 14;
```

시간 뿐 아니라 연도, 날짜 등도 유사한 방식으로 가능하다.
