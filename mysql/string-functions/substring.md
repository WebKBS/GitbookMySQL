# SUBSTRING()

### 사용방법.

```sql
SELECT SUBSTRING("HELLO WORLD", 1, 4);
-- 결과: HELL
```

첫번째 인자는 문자열, 두번째 인자는 시작 번호, 세번째 인자는 끊는 번호.

\*\* 중요한점은 시작번호 문자열 index는 0이 아닌 1부터 시작한다.\
\*\* 두번째 인자를 사용하지 않으면,  시작지점이 되고, 지정한 숫자 이전의 문자들은 삭제된다.

```sql
SELECT SUBSTRING("HELLO WORLD", 4);
-- 결과: LO WORLD
```

#### 음수를 사용하면 반대로 시작한다.

```sql
SELECT SUBSTRING("HELLO WORLD", -4);
-- 결과: ORLD
```

\
SUBSTRING도 마찬가지로 이름을 수정할 수 있다.

```sql
SELECT SUBSTRING(title, 1, 10) AS 'short title' FROM <테이블 이름>;
```

### 축약어 SUBSTR()
