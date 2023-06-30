# start from base image
FROM node:16

# set working directory in container
WORKDIR /usr/src/app

# define container port 
EXPOSE 5000

# copy source code to /usr/src/app
COPY . .

# build project
RUN npm install
RUN npm run build
RUN npm install -g serve

# execute during docker run 
CMD ["serve", "-s", "-l", "5000", "build"]