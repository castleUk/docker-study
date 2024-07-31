# MYSQL 도커파일 생성방법

```txt
FROM mysql

ENV MYSQL_USER=ssar
ENV MYSQL_PASSWORD=ssar1234
ENV MYSQL_ROOT_PASSWORD=root1234
ENV MYSQL_DATABASE=ssardb

CMD ["--character-set-server=utf8mb4", "--collation-server=utf8mb4_unicode_ci"]

```

## UTF 8 설정확인
```sh
show variables like 'character_set_%';
```

## 터미널 접속법
```txt
docker exec -it [container id] bash
```

## 볼륨 옵션으로 호스트 폴더 연결해서 실행하는 법
```sh
docker run -d -v /Users/castleuk/study/docker/DOCKER_LAB/ex05/mysql-volume:/var/lib/mysql -p 3307:3306 --name mysql-container mysql-image
```

## 이름있는 볼륨으로 사용법 (컨테이너 삭제해도 볼륨이 살아있음)
```sh
docker run -d -v mysql-volume:/var/lib/mysql -p 3307:3306 --name mysql-container mysql-image
```