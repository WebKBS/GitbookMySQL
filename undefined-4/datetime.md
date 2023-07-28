---
description: 날짜와 시간
---

# DATETIME

```sql
CREATE TABLE <테이블 이름> (<열 이름> DATETIME);
```

```sql
INSERT INTO <테이블 이름> (<열 이름>) VALUES ("YYYY-MM-DD hh:mm:ss");
```



## NOW() CURRENT\_TIMESTAMP()

현재 날짜 및 시간 보기

```sql
SELECT NOW();
-- 또는
SELECT CURRENT_TIMESTAMP();
```

###

### 현재 날짜,시간 삽입

```sql
INSERT INTO <테이블 이름> (<열 이름>) VALUES (NOW());
```
