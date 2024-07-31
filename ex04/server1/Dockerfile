# 생성할 이미지의 베이스가 될 이미를 결정하는 명령어.
# 사용하려는 이미지가 도커 엔진에 없으면 자동으로 도커 허브에서 pull을 시도한다.
FROM nginx 

# 현재 디렉토리 경로의 모든 파일과 디렉토리를 해당 디렉토리에 복사하는 명령어
COPY webapp /usr/share/nginx/html

# 도커 컨테이너가 실행할 때 고정적으로 실행되는 스크립트 혹은 명령어.
# 아래의 경우
# nginx : 실행할 프로그램의 이름 , Nginx 웹 서버를 실행하는 명령어
# -g "daemon off;" : Nginx의 설정 옵션, -g는 글로벌 설정을 뜻하고, daemon off 는 Nginx가 데몬모드(백그라운드_를 사용하지 않고 포그라운드로 실행되도록 지시
ENTRYPOINT ["nginx", "-g", "daemon off;"]



# build 명령어
# docker build -t server1 ./server1
# -t : 생설될 이미지의 이름을 설정한다.

# docker run 명령어
# docker run -d -p 8001:80 server1
# -d(detached mode) : 백그라운드에서 도커 컨테이너가 실행.
# -p(포트포워딩) : 8001로 요청하면 80으로 포트포워딩 해라
