# 맥북 터미널에서 설치

```bash
brew install mysql
```

homebrew가 설치되어있지 않으면 homebrew를 설치해야한다.



### mysql 서버를 실행하는 방법

```
mysql.server start
```



### mysql 터미널에서 실행

```
mysql -u root -p
```

비밀번호 창이 뜨는데, 생성시 설정한 비밀번호를 입력하면된다.

### 현재 사용중인 데이터베이스 보기

```sql
show databases;
```

\*\* sql은 문장 완성시 반드시 ; (세미콜론)으로 종료 지점을 표시해야한다.
