---
description: 열을 그룹을 지음
---

# GROUP BY()

```sql
SELECT <열 이름> FROM <테이블 이름> GROUP BY <열 이름>;
```

동일 데이터의 그룹을 묶는다.

단 출력되는 데이터에는 DISTINCT처럼 중복된 열이 나타나는데, 실제론 그룹이 만들어져있다.

이를 확인하기위해서 COUNT를 사용해보자.

```sql
SELECT <열 이름>, COUNT(*) FROM <테이블 이름> GROUP BY <열 이름>;
```

COUNT에 그룹으로 지어진 개수가 나타난다.



{% hint style="info" %}
GROUP BY는 모든 열 "\*" 을 SELECT하면 에러가난다.

보통 개별 열을 GROUP을 만들고

COUNT(\*)를 사용한다.
{% endhint %}



## 조합해서 다중 열 만드는 방법

다중 열은 혹시나 중복된 열을 피할때 사용한다.

```sql
SELECT <열 이름>, <열 이름>, COUNT(*) 
FROM <테이블 이름> 
GROUP BY <열 이름>, <열 이름>;
```



### CONCAT을 이용한 방법

```sql
SELECT CONCAT(<열 이름>, ' ', <열 이름>) AS <변경할 열 이름>,  COUNT(*)
FROM <테이블 이름>
GROUP BY <변경할 열이름>;
```
