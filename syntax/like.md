---
description: 찾고 싶은 문자를 찾을때 사용
---

# LIKE

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE <문자열>;
```

원하는 문자열을 찾을때 사용한다.



LIKE에는 특수한 기능이 있다.

<문자열>에는 %(퍼센트) 기호와 \_(언더바) 기호를 사용할 수 있다.

%, \_ 를 사용하지 않으면 아무것도 반환하지 않는다.



### 기호 %

사용방법

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '%<원하는 문자>%';

-- 예시
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '%Hello%';
-- 결과 Hello가 포함된 모든 데이터를 나타낸다.

-- 하나만 사용도 가능하다.
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '%lo';
-- %가 앞쪽에 하나만 쓰면 끝나는 문자를 검색한다.

SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE 'He%';
-- %가 뒤쪽에 하나만 쓰면 시작하는 문자를 검색한다.
```



### 기호 \_

사용방법

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '___';
-- _언더바는 _언더바 개당 하나의 글자수를 의미한다.
-- '___' 3개이면 문자가 3개인 문자를 모두 출력한다.

SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE 'H_l';
-- _언더바와 문자를 조합하면 언더바는 아무 문자가 포함되기에 문자 순서에 대해 일치하는것을 출력한다.

--예시
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '__ab__';
-- '__ab__' 문자열 6개중 중간 ab가 일치하는 데이터를 찾아서 출력한다.
```



### 예외적으로 %가 있는 문자를 검색할때

이스케이프 처리를 해야한다.

예시) 10%, Hello\_world

```sql
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '%\%%';
-- 역슬래시 \를 사용해야한다. \%
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '%10\%%';

SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '%\_%';
SELECT * FROM <테이블 이름> WHERE <열 이름> LIKE '%\_world%';
```



{% hint style="warning" %}
LIKE 사용시 찾는 문자열은 대소문자를 구분하지 않는다!
{% endhint %}
