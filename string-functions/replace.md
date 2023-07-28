# REPLACE()

### 사용방법.

```sql
SELECT REPLACE("HELLO WORLD", " ", " and ");
-- 결과: HELLO and WORLD
```

첫번째 인자는 변경할 값을 받고, 두번째는 첫번째의 변경할 대상 문자, 세번째는 변경할 문자를 추가한다.

{% hint style="warning" %}
\*\* 중요!! REPLACE는 대소문자를 구분한다.

실제 테이블의 값은 변경되지 않는다.
{% endhint %}
