# ORDER BY

```sql
SELECT * FROM <테이블 이름> ORDER BY <정렬할 열 이름>;
```

열을 알파벳 순으로 오름차순 순서대로 정렬한다.



```sql
SELECT <열 이름> FROM <테이블 이름> ORDER BY <정렬할 열 이름>;
```

\*을 사용하면 전체 목록이 나오듯이 열 이름을 SELECT 다음에 추가하면 선택한 정렬된 열만 나타난다.

ORDER BY 다음에 오는 열 이름을 정렬한다.

{% hint style="warning" %}
ORDER BY 뒤에오는 정렬할 열 이름은 하나만 있어야한다.
{% endhint %}



### 반대로 정렬하기 (내림 차순)

```sql
SELECT * FROM <테이블 이름> ORDER BY <정렬할 열 이름> DESC;
```

마지막에 DESC만 붙여 주면 된다.&#x20;

```sql
SELECT <열 이름> FROM <테이블 이름> ORDER BY <정렬할 열 이름> DESC;
```



{% hint style="info" %}
DESC의 반대는 ASCE. (기본값)
{% endhint %}

