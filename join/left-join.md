---
description: 왼쪽 테이블의 모든 정보와 교집합을 포함한 데이터를 출력한다.
---

# LEFT JOIN

```sql
SELECT * FROM <테이블1>
LEFT JOIN <테이블2> ON <테이블2>.<열 이름> = <테이블1>.<열 이름>;
```

{% hint style="info" %}
inner JOIN과 다른점은 \
inner JOIN은 서로 다른 테이블의 오로지 교집합만 데이터를 출력하기때문에\
한쪽의 NULL체크 된 값 등은 볼수가 없다.\
\
공통된 교집합을 포함하면서 한쪽의 모든 데이터 값을 볼수 있기때문에

NULL(없는 값) 값등을 찾아낼수 있다.
{% endhint %}



### RIGHT JOIN

LEFT JOIN과 동일하나 테이블 순서를 반대로 보면된다.

