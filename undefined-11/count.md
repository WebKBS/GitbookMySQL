---
description: 데이터 개수 구하기
---

# COUNT()

```sql
SELECT COUNT(*) FROM <테이블 이름>;
```

### 원하는 열만 사용

```sql
SELECT COUNT(<열 이름>) FROM <테이블 이름>;
```

{% hint style="info" %}
중복된 이름도 COUNT 에 포함된다.\
하지만 NULL값은 포함되지 않는다.
{% endhint %}



### 중복 제거와 함께 사용 (DISTINCT)

```sql
SELECT COUNT(DISTINCT <열 이름>) FROM <테이블 이름>;
-- 중복을 제거하고 카운트 개수를 보여준다.
```



### LIKE 와 함께 사용 (문자열이 포함된것이 몇개인지)

```sql
 SELECT COUNT(*) FROM <테이블 이름> WHERE <열 이름> LIKE '%<검색문자>%';
```

