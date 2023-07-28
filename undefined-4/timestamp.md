# TIMESTAMP

DATETIME과 비슷한 약간의 차이가 있다.

* TIMESTAMP가 메모리를 더 적게 차지한다.
* 더 작은 날짜의 범위를 지원한다.
* 최소 1970-01-01 00:00:01 부터 최대 2038-01-19 03:14:07 까지

{% hint style="info" %}
TIMESTAMPS는 제한적인 범위가 있기때문에 비교적 최신날짜에 사용해야한다.

생일이나 태어난 날 등은 1970년 이전의 사람이 있을수 있기 때문에

이럴때는 TIMESTAMPS를 사용하지 않고 DATETIME을 사용해야한다.
{% endhint %}



## TIMESTAMP 추가하기

```sql
-- 예시
CREATE TABLE <테이블 이름>(
	<열 이름> VARCHAR(150),
	<열 이름> TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

INSERT가 추가될때마다 현재 시간이 찍힌다.



### 업데이트 TIMESTAMP 추가하기

```sql
-- 예시
CREATE TABLE <테이블 이름>(
	<열 이름> VARCHAR(150),
	<열 이름> TIMESTAMP DEFAULT CURRENT_TIMESTAMP
	<열 이름> TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
-- DEFAULT는 현재시간이 찍힌다.
```

ON UPDATE를 사용하면, 테이블이 UPDATE될때 업데이트 된 시간이 찍힌다.

업데이트가 되지 않은 최초의 값은 NULL

업데이트로 인해 수정되면 자동으로 UPDATE TIMESTAMP의 값이 변경된다.

{% embed url="https://dev.mysql.com/doc/refman/5.7/en/timestamp-initialization.html" %}
