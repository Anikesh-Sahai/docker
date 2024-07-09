# FROM node:8.16.1-alpine
# WORKDIR /app
# COPY . /app
# RUN npm install
# EXPOSE 5000
# CMD node index.js


#ENTRYPOINT ["node", "index.js"]
#COPY package.json /app

# when we run it again it creates chache and if it finds changes then the belloow steps are not chached 
# for that mostly the code part changes and pakage file didnt change much so
# with that thebuild was very fast
FROM node:8.16.1-alpine
WORKDIR /app

COPY package.json /app

RUN npm install
EXPOSE 5000

COPY . /app
CMD node index.js

# entry point is used when the launching command should be constant