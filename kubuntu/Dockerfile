### Base Image 지정
FROM ubuntu:20.04

### TimeZone 환경 변수 지정
ENV TZ Asia/Seoul

### TimeZone 설정
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

### /home/dev 폴더 생성
RUN mkdir /home/dev

### update 및 패키지 설치
RUN apt update && apt -y install nano git tar gzip build-essential curl alien openjdk-8-jdk nginx

### nodejs 설치
RUN curl -sL https://deb.nodesource.com/setup_17.x -o nodesource_setup.sh && bash nodesource_setup.sh && apt -y install nodejs

### 서비스 배포
EXPOSE 80 8080
