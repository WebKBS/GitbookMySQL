# 데이터 테이블 읽기

## 테이블 모든 column 내용보기

```sql
SELECT * FROM <테이블 이름>;
```

테이블 column의 모든 값이 표시된다.



## 개별  column 값만 보기

```sql
SELECT <열 이름> FROM <테이블 이름>;
```

### 조합해서 보기

```sql
SELECT <열 이름>, <열 이름> FROM <테이블 이름>;
```

column 이름을 "," 콤마로 구분해서 사용한다.



## WHERE, 해당하는 특정 값만 보기

```sql
SELECT * FROM <테이블 이름> WHERE <열이름> = <값>;

-- 예시 
SELECT * FROM people WHERE age = 10;
-- 예시 
SELECT * FROM people WHERE name = "Kim";
```

모든 열에 열 이름의 값을 볼때 사용한다.

\*\* number는 숫자를 사용하고, string은 "" 및 '' 을 사용하되, 대소문자를 가리지 않는다.

### 원하는 열만 보기

```sql
SELECT <열 이름>, <열 이름> FROM <테이블 이름> WHERE <열이름> = <값>;

-- 예시
SELECT name FROM people WHERE age = 10;
-- 예시
SELECT name, age FROM people WHERE name = "Kim";
```



## Alias, 이름 변경해서 보기

```sql
SELECT <열 이름> AS <변경할 열 이름> FROM <테이블 이름>;
-- 예시
SELECT name AS first_name FROM people;
```

열 이름을 불러올때 이름을 변경해서 불러온다.\
\*\* 불러올때 이름을 변경하더라도 실제 테이블에서 변경되는것은 아니다.
