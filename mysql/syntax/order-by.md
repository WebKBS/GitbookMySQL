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



```sql
SELECT <열 이름>, <열 이름> FROM <테이블 이름> ORDER BY <정렬할 열 이름>, <정렬할 열 이름>;
```

{% hint style="info" %}
ORDER BY 뒤에 여러 열 이름을 추가하면 첫번째 두번째 순으로 순서대로 정렬한다. \
\* 첫번째 열 정렬후 동일 이름이 있을시, 두번째 열에도 순서대로 정렬됨.
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



### CONCAT 조합해서 사용하기

```sql
SELECT CONCAT(<열 이름>, ' ', <열 이름>) AS <변경할 열이름> FROM <테이블 이름> ORDER BY <정렬할 열이름>;
```
