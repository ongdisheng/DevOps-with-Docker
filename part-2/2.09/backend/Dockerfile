# start from base image
FROM golang:1.16

# set working directory in container 
WORKDIR /usr/src/app

# define container port 
EXPOSE 8080

# set environment variable
ENV REQUEST_ORIGIN=http://127.0.0.1:5000

# copy source code to /usr/src/app
COPY . .

# build project
RUN go build

# execute during docker run 
CMD ["./server"]