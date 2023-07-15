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

### DEFAULT

```sql
CREATE TABLE <테이블 이름>  (    
    name VARCHAR(20) DEFAULT 'default value',    
    age INT DEFAULT 99  
);
```

default 설정을하면,\
공백 입력시

```sql
INSERT INTO <테이블 이름>() VALUES(); // 아무 값을 넣지 않았을때.
```

default에 설정된 값이 입력된다.&#x20;



#### NOT NULL과 DEFAULT는 조합하여 사용할 수 있다.

```sql
CREATE TABLE <테이블 이름>  (
        name VARCHAR(20) NOT NULL DEFAULT 'default value',
        age INT NOT NULL DEFAULT 99
 );
```

NOT NULL과 조합하여 사용시,\
NOT NULL은 값이 없으면 에러를 발생하지만,\
DEFAULT가 설정 되어있다면 값이 NULL이어도 DEFAULT의 값이 대체 되어 사용된다.\




### KEY

```sql
CREATE TABLE <테이블 이름> (
    id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL
);

-- 또 다른 방법
CREATE TABLE <테이블 이름> (
    id INT,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    PRIMARY KEY (cat_id)
);;l
```

key, 한마디로 id 설정이다. 고유한 id.

INSERT로 생성시 동일한 key가 있으면 에러를 발생시킨다.

동일한 이름과 age가 있을때, 중복된 사용자시 누가 누군지 인지하기 어렵기 때문에\
식별자를 추가하든 고유 id를 부여해야한다.



