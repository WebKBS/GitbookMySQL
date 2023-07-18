# DISTINCT

```sql
SELECT DISTINCT <열 이름> FROM <테이블 이름>;
```

DISTINCT는 중복된 열의 문자열 값을 제외하고 보여준다.



```sql
SELECT DISTINCT <열 이름>, <열 이름> FROM <테이블 이름>;
--열 이름 추가로 가능하다.
```

이 방법은 선택한 모든 열에 대한 중복을 검사하며 선택한 데이터의 row(행)이/가 하나라도 일치하지 않으면 중복을 제거하지 않는다.



### 조합해서 사용하기

#### CONCAT과 조합해서 사용하기

```sql
SELECT DISTINCT CONCAT(<열 이름>, ' ',<열 이름>) FROM <테이블 이름>;
-- 열 이름과 조합해서 중복된 값이 제거 된다.
```

