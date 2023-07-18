# DISTINCT

```sql
SELECT DISTINCT <열 이름> FROM <테이블 이름>;
```

DISTINCT는 중복된 열의 문자열 값을 제외하고 보여준다.



### 조합해서 사용하기

```sql
SELECT DISTINCT <열 이름>, <열 이름> FROM <테이블 이름>;
--열 이름 추가로 가능하다.
```



### CONCAT과 조합해서 사용하기

```sql
SELECT DISTINCT CONCAT(<열 이름>, ' ',<열 이름>) FROM <테이블 이름>;
-- 열 이름과 조합해서 중복된 값이 제거 된다.
```

