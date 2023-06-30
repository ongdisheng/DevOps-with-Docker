# start from base image (java 8)
FROM openjdk:8

# set working directory in container
WORKDIR /usr/src/app

# define container port 
EXPOSE 8080

# copy source code to /usr/src/app
COPY . .

# fix line ending issue
RUN apt-get update && apt-get -y install dos2unix
RUN dos2unix mvnw

# build project
RUN ./mvnw package

# execute during docker run
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]