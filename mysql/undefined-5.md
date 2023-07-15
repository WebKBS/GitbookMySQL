# 테이블 생성하기

```sql
CREATE TABLE <테이블 이름> (
    name VARCHAR(50),
    age INT
);
```

위와 같이 사용하며 column을 구분지을땐 "," 콤마를 사용한다.



### 생성된 테이블 확인하기

```sql
SHOW TABLES;
```

생성된 테이블 목록이 나온다.



### 테이블 colum 확인하기

```sql
SHOW COLUMNS FROM <테이블 이름>
```

단축어로 사용하는 방법.

```sql
DESCRIBE <테이블 이름>;
DESC <테이블 이름>;
```

DESCRIBE 또는 DESC를 사용한다.



### NOT NULL

```sql
CREATE TABLE <테이블 이름> (
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL
);
```

NOT NULL은 반드시 값이 있어야 한다는것을 추가한다.

테이블 생성시 NOT NULL을 설정하면\
INSERT할때 값이 없으면 에러를 발생시킨다.

