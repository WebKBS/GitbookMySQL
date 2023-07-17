# CHAR\_LENGTH()

글자의 길이수를 반환한다.&#x20;

시작부터 중요!

{% hint style="warning" %}
LENGTH()와는 전혀 다르다!\
LENGTH()는 바이트수를 반환하고

글자수를 반환하려면 반드시 CHAR\_LENGTH()를 사용해야한다.
{% endhint %}



### 사용방법.

```sql
SELECT CHAR_LENGTH("HELLO WORLD");
-- 결과: 11
```

```sql
-- 예시
SELECT CHAR_LENGTH(<열 이름>) AS <변경할 열 이름>, <부분 보기 열 이름> FROM <테이블이름>;
```
