---
title: "MariaDB mac os에 세팅하기"
excerpt: "맥북에 MariaDB를 세팅해보자."

categories:
  - Blog
tags:
  - Blog
---



맥북에 MariaDB를 세팅해보기로 하자

```shell
brew install mariadb # MariaDB 설치
```

```shell
mysql.server start # 서버 실행
mysql -u root # 서버 접속
```



나의 경우에는 서버 접속시 권한이 없는 문제가 발생해서

```
sudo mysql -u root
```

사용했다. 그러나 비밀번호를 설정한적이 없는데 계속 비밀번호를 요구했다.

따라서, 비밀번호를 초기화할 필요가 있었다. 구글링을 해보면 다양한 방법이 나오는데 나는 다음과 같은 명령어로 비밀번호를 재설정했다.

```
sudo mariadb-secure-installation
```

다른 방법은 다음 블로그(https://bongjacy.tistory.com/entry/Mac%EC%97%90-MariaDB-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0)를 참고해도 된다.



이렇게 하면 맥에 mariadb는 이상없이 깔리고 실행된다.!