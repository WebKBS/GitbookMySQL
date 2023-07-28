# CONCAT()

### 사용방법.

```sql
SELECT CONCAT("H", "I");

-- 결과: HI
```

인자로 들어온 값을 합하여 return한다.



### 테이블 column을 인자로 전달할수 있다.

```sql
SELECT CONCAT(name1, name2) FROM <테이블 이름>;
```

### 필요시 이름변경도 가능하다.

```sql
SELECT CONCAT(name1, name2) AS <변경할 이름> FROM <테이블 이름>;
```



## CONCAT\_WS

```sql
SELECT CONCAT_WS("@", "H", "I");
-- 결과 H@I
```

첫번째 인자가, 첫번째 이후에 오는 인자들 사이에 추가된다.
