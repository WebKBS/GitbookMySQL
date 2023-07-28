---
description: 날짜 YYYY-MM-DD
---

# DATE

```sql
CREATE TABLE <테이블 이름> (<열 이름> DATE);
```

```sql
INSERT INTO <테이블 이름> (<열 이름>) VALUES ("YYYY-MM-DD");
```



## CURDATE() CURRENT\_DATE()

현재 날짜 보기

```sql
SELECT CURDATE();
-- 또는
SELECT CURRENT_DATE();
```



### 현재 날짜 삽입

```sql
INSERT INTO <테이블 이름> (<열 이름>) VALUES (CURDATE());
```



### 특정 일 만 선택하기 DAY()

```sql
SELECT <열 이름>, DAY(<열 이름>) FROM <테이블 이름>;
```



### 특정 요일 선택하기 DAYOFWEEK()

```sql
SELECT <열 이름>, DAYOFWEEK(<열 이름>) FROM <테이블 이름>;
```

숫자료 표시된다.

{% hint style="info" %}
일요일부터 1,2,3,4,5,6,7

일요일: 1, 월요일: 2, 화요일: 3 .... 토요일: 7
{% endhint %}



### 월 이름 추출 MONTHNAME()

```sql
SELECT <열 이름>, MONTHNAME(<열 이름>) FROM <테이블 이름>;
```



{% embed url="https://dev.mysql.com/doc/refman/5.7/en/datetime.html" %}

## DATE\_FORMAT() 날짜 양식 바꾸기

```sql
SELECT <열 이름>, DATE_FORMAT(<열 이름>, '%a') FROM <테이블 이름>;
-- '%'를 사용해서 특정 DATE를 FORMAT할 수 있다.
SELECT <열 이름>, DATE_FORMAT(<열 이름>, '%a %b') FROM <테이블 이름>;
-- 여러 조합으로도 사용할 수 있다.

-- 글자와 조합해서 원하는 텍스트를 추가할수도 있다.
SELECT <열 이름>, DATE_FORMAT(<열 이름>, '시간: %a %b') FROM <테이블 이름>;
```

아래 자료에서 사용할것을 찾아보자.

{% embed url="https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html" %}



## 날짜 계산방법&#x20;



{% hint style="info" %}
예시의 CURDATE()는 현재 기준이며, 정해진 DATE가 있으면 기준을 바꿀수 있으며 그 기준으로 출력된다.
{% endhint %}

### DATEDIFF()

현재날짜에서 지정 날짜 사이의 총 일수를 출력한다.

```sql
SELECT <열 이름> DATEDIFF(CURDATE(), <계산할 열이름>) FROM <테이블 이름>;
-- 출력: 현재날짜 - 지정날짜 = 경과된 날짜
```



### DATE\_ADD()

현재 날짜에서 원하는 년,월,일을 추가하여 추가된 날짜를 출력한다.

```sql
SELECT DATE_ADD(CURDATE(), INTERVAL 1 YEAR);
-- 현재 날짜 2023년 7월 23일 기준 1년후인 2024년 7월 23일이 출력된다.

-- 월
SELECT DATE_ADD(CURDATE(), INTERVAL 1 MONTH);
-- 일
SELECT DATE_ADD(CURDATE(), INTERVAL 1 DAY);
```



### DATE\_SUB()

현재 날짜에서 원하는 년,월,일을 추가하여 이전의 날짜를 출력한다.

```sql
SELECT DATE_SUB(CURDATE(), INTERVAL 1 YEAR);
-- 현재 날짜 2023년 7월 23일 기준 1년후인 2022년 7월 23일이 출력된다.

-- 월
SELECT DATE_SUB(CURDATE(), INTERVAL 1 MONTH);
-- 일
SELECT DATE_SUB(CURDATE(), INTERVAL 1 DAY);
```

