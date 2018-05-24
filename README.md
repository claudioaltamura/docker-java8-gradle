[![Build Status](https://travis-ci.org/claudioaltamura/docker-java8-gradle.svg?branch=master)](https://travis-ci.org/claudioaltamura/docker-java8-gradle)

# docker-java8-gradle
docker-java8-gradle examples

##Gradle
Classical
Build app: ./gradlew build

Run app: ./gradlew run

##With Docker
Build image: ./gradlew dockerBuildImage

Run container: ./gradlew startContainer

##With Dockerfile

	FROM openjdk:latest
	COPY * /opt/app/
	WORKDIR /opt/app
	CMD ["java", "HelloWorld"]

### compile class
javac helloworld.java

### build image
docker build -t java8-helloworld .

### run image
docker run --name hellojava 67eca8c9dd66 
Hello World

docker logs hellojava
Hello World

docker rm hellojava
