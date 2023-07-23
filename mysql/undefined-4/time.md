---
description: 시간 HH:MM:SS
---

# TIME

```sql
CREATE TABLE <테이블 이름> (<열 이름> TIME);
```

```sql
INSERT INTO <테이블 이름> (<열 이름>) VALUES ("hh:mm:ss");
```



## CURTIME() CURRENT\_TIME()

현재 시간 보기

```sql
SELECT CURTIME();
-- 또는
SELECT CURRENT_TIME();
```



### 현재 시간 삽입

```sql
INSERT INTO <테이블 이름> (<열 이름>) VALUES (CURTIME());
```



### 시간 가져오기  HOUR()

```sql
SELECT <열 이름>, HOUR(<열 이름>) FROM <테이블 이름>;
```



### 분 가져오기 MINUTE()

```sql
SELECT <열 이름>, MINUTE(<열 이름>) FROM <테이블 이름>;
```

### 초 가져오기 SECOND()

```sql
SELECT <열 이름>, SECOND(<열 이름>) FROM <테이블 이름>;
```
