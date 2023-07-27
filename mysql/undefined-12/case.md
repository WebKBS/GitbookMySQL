---
description: 개발언어 if else 및 switch문과 비슷한 조건문
---

# CASE

원하는 조건에 따라 값(별 & 순위)을 매길수 있다.

```sql
SELECT *
    CASE
        WHEN <열 이름> THEN <설정 값>
        ELSE <값>
    END AS <변경할 이름>
FROM <테이블 이름>;
```

WHEN을 사용해서 단계적으로 검색 조건을 찾아간다.

### 다른 연산자와 조합하는 방법

```sql
SELECT *
    CASE
        WHEN <열 이름> BETWEEN <값> AND <값> THEN <설정 값>
        WHEN <열 이름> BETWEEN <값> AND <값> THEN <설정 값>
        ELSE <값>
    END AS <변경할 이름>
FROM <테이블 이름>;

-- 예시
SELECT *
    CASE
        WHEN <열 이름> BETWEEN 0 AND 50 THEN "*"
        WHEN <열 이름> BETWEEN 50 AND 100 THEN "**"
        ELSE "***"
    END AS <변경할 이름>
FROM <테이블 이름>;
```

예시 처럼 \*표 개수로 조건에 따라 값을 매길수 있다.
