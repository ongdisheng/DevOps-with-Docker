# start from ubuntu image
FROM ubuntu:20.04

# set '/usr/src/app' as current working directory
WORKDIR /usr/src/app

# install curl
RUN apt-get update && apt-get -y install curl

# copy website.sh file to '/usr/src/app'
COPY website.sh .

# add execution permission
RUN chmod +x website.sh

# execute when using docker run command
CMD ./website.sh