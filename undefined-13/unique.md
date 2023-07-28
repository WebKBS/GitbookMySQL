---
description: 테이블 생성시 컬럼에 고유한 특성을 부여
---

# UNIQUE

{% hint style="warning" %}
UNIQUE로 지정된 값은 한번만 사용할 수 있다. (중복 불가)
{% endhint %}

```
CREATE TABLE <테이블 이름>(
    <열 이름> VARCHAR(<값>) NOT NULL UNIQUE
)'
```



```sql
-- 예시
CREATE TABLE <테이블 이름> (
    name VARCHAR (100) NOT NULL,
    phone VARCHAR (15) NOT NULL UNIQUE
);

-- name은 변경될수 있으나 
-- name이 달라도 phone의 값은 중복이 불가하다.
```
