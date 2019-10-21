# base image
FROM node:12.2.0-alpine

# set working directory
RUN mkdir /app
WORKDIR /app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# install and cache app dependencies
COPY package.json /app/package.json
COPY . /app
RUN npm install --silent
RUN npm install react-scripts@3.0.1 -g --silent
RUN npm run build
# start app
CMD ["npm", "start"]
# Expose PORT 3000 on our virtual machine so we can run our server
EXPOSE 3000
