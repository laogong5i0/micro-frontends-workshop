FROM node:11

# Create app directory
RUN mkdir -p /code
WORKDIR /code

# Install app dependencies
COPY package.json /code/
RUN npm install

# Bundle app source
COPY ./src /code/src
COPY ./static /code/static

EXPOSE 3001
CMD [ "./node_modules/.bin/nodemon", "--watch", "./static", "--exec", "npm", "start" ]