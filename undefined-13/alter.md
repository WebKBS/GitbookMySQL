---
description: 이미 생성된 테이블에 추가로 해당 테이블의 열을 CRUD를 할 수 있다.
---

# ALTER

{% hint style="info" %}
이미 생성된 테이블에 사용한다.
{% endhint %}

## 테이블 열 추가하기

```sql
ALTER TABLE <생성된 테이블 이름>
ADD COLUMN <열 이름> VARCHAR(15);
```

### 기타 속성도 추가 가능하다.

```sql
ALTER TABLE <생성된 테이블 이름>
ADD COLUMN <열 이름> INT NOT NULL DEFAULT 1;
```



## 테이블 열 삭제하기

```sql
ALTER TABLE <테이블 이름> DROP COLUMN <열 이름>;
```



## 테이블 이름 변경하기

```sql
RENAME TABLE <현재 테이블 이름> TO <변경할 테이블 이름>;
-- 기존 방식

ALTER TABLE <현제 테이블 이름> RENAME TO <변경할 테이블 이름>;
-- ALTER 방식
```



## 테이블 열 이름 변경하기

```sql
ALTER TABLE <테이블 이름>
RENAME COLUMN <현재 열 이름> TO <변경할 열 이름>;
```



## 테이블 열 속성 변경하기

```sql
ALTER TABLE <테이블 이름>
MODIFY <현재 열 이름> VARCHAR(100) DEFAULT 'unknown';
-- 현재 열이름 뒤에 변경하고싶은 속성을 넣으면 된다.
```
