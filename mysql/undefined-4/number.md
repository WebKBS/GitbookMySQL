# NUMBER

## INT

max size가 최대 -2147483648 \~ 2147483647 사이의 정수

양수의 값만 받으려면 생성시 UNSIGNED를 붙여야한다.

```sql
CREATE TABLE <테이블 이름> (<컬럼 이름> INT UNSIGNED);
```

음수를 받는것을 제거하고, 양수만 받을시

TITNYINT의 최소 최대값은 0 \~ 4294967295 사이의 값이 된다.

## TINYINT

\-128 \~ 127 사이의 정수

양수의 값만 받으려면 생성시 UNSIGNED를 붙여야한다.

```sql
CREATE TABLE <테이블 이름> (<컬럼 이름> TINYINT UNSIGNED);
```

음수를 받는것을 제거하고, 양수만 받을시

TITNYINT의 최소 최대값은 0 \~ 255 사이의 값이 된다.



{% embed url="https://dev.mysql.com/doc/refman/5.7/en/integer-types.html" %}



## DECIMAL

정확한 소수를 저장할때 사용한다.
