# 데이터 삽입하기

```sql
INSERT INTO <테이블 이름> (name, age)
VALUES ("Happy", 10); // 데이터 name age순서
```

반복해서 사용하면 테이블에 데이터가 추가로 삽입된다.

\*\* 테이블이름은 같아야한다.\
\


```sql
INSERT INTO <테이블 이름> (age, name)
VALUES (10, "Happy"); // 데이터 age name 순서
```

row의 삽입 순서가 바뀌어도 동일하게 작동한다.



### 다중 데이터 삽입.

```sql
INSERT INTO <테이블 이름> (name, age)
VALUES ("first", 1),
    ("second", 2),
    ("third", 3);
```

"," 콤마를 구분지어 여러 다중데이터를 삽입할 수 있다.
