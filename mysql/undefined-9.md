# 데이터 테이블 업데이트

```sql
UPDATE <테이블 이름> SET <컬럼 이름> = <변경할 값> WHERE <컬럼 이름> = <변경할 대상 컬럼 이름>;
-- 예시
UPDATE people SET age = 20 WHERE name = "Kim";
-- 예시
UPDATE people SET address = "한국" WHERE name = "Kim";
```

\*\* 선택한 대상의 컬럼의 값을 변경할 수 있다.

### 중요 !! WHERE문을 쓰지 않는다면??

```sql
UPDATE <테이블 이름> SET <컬럼 이름> = <변경할 값>;
-- 예시
UPDATE people SET age = 20;
```

이처럼 WHERE 문을 쓰지 않는다면,\
people 테이블의 모든 age가 20으로 변경된다.

특별한 상황이 아니라면 무조건! WHERE을 붙여서 원하는 대상만 변경해야한다.
