#set base image
FROM node:18
# set working directory
WORKDIR /usr/src/app
# copy file with packages to the working directory 
COPY package.json .
#install necessary packages
RUN npm install
#copy rest of the files 
COPY . .

ENV PORT=3001 \
    DB=beatles \
    DBUSER=john \
    DBPASS=Password123! \
    DBHOST=35.238.147.178 \
    DBPORT=3306 

EXPOSE 3001

CMD ["npm", "start"]

