FROM openjdk:11-jdk-slim

WORKDIR /app

# ADD 압축파일.zip ./ # 이렇게 하면 압축이 풀린다.

# buil
COPY build/aws-v3-0.0.3.jar ./application.jar

# 실행할 명령어를 넣는다.
# java -jar -Dspring.prifiles.active=dev application.jar 를 터미널에 치는것과 같음
# 근간이 되는 명령어 "목적"
ENTRYPOINT ["java", "-jar", "-Dspring.profiles.active=dev", "application.jar"] 
# 옵션
CMD ["--server.port=3000"]




