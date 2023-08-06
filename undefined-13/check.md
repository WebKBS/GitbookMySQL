---
description: 원하는 값의 범위를 제한한다.
---

# Check

```sql
CREATE TABLE <테이블 이름>(
    <열 이름> INT CHECK (<값>)
);

-- 0 또는 1을 반환한다.

-- 값 예시
-- age > 18
```

### Check 조건 이름 만들기

```sql
CREATE TABLE <테이블 이름>(
    <열 이름> INT,
    CONSTRAINT <만들 이름> CHECK (<값>)
);
```

제약 조건에는 이름을 따로 만들어주는게 좋다.

만약 제약된 조건에 실패한다면 만든 이름이 에러메세지로 출력된다.



## 다중 체크

```sql
CREATE TABLE <테이블 이름> (
  <첫번째 열이름> INT NOT NULL,
  <두번째 열이름> INT NOT NULL,
  CONSTRAINT <체크 이름> CHECK(<첫번쨰 열 이름> >= <두번째 열이름>)
);
```

