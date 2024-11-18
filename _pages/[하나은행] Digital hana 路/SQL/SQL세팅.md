---
title: "MySQL"
date: "2024-11-18"
thumbnail: ""
---

# MySQL 개발환경세팅
---


```shell
1.
sql 폴더 생성
ex) mkdir sql

2. docker-compose.yml 파일을 sql 폴더 안에 생성하기

docker-compose.yml 내용 >
<<<
services:
 localdb:
 container_name: hana4db
 image: mysql:8.0
 ports:
 - 3309:3306
 environment:
 MYSQL_ROOT_PASSWORD: TestdbRoot
 MYSQL_DATABASE: testdb
 command:
 - --character-set-server=utf8mb4
 - --collation-server=utf8mb4_unicode_ci
 - --log_bin_trust_function_creators=1
 volumes:
 - ./mysql:/var/lib/mysql
 >>>

```

```shell

공유 디렉토리 만들기

sql 폴더 안에 mysql이라는 폴더를 만들어서(위의 volumes가 공유폴더이름)


```



``shell
$> docker compose up -d
# ⇐⇒ docker-compose up -d

# down (container 제거)
$> docker-compose down

# 확인
$> docker ps

# cf. 시작만 (docker compose stop)
$> docker compose start

# 완전삭제: -volumne, -stop, -force
volumes: $> docker compose rm -vsf


```

# mysql 접속하기
```shell
mysql -u root -p // 3306포트면
mysql -u root -p -P 3309 //포트가 다를경우 뒤에 -P 쓰고 포트 걸어주기
```