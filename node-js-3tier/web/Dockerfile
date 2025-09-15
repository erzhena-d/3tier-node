#set base image
FROM node:18 AS builder
# set working directory
WORKDIR /usr/src/app
# copy file with packages to the working directory 
COPY package.json .
#install necessary packages
RUN npm install
#copy rest of the files 
COPY . .

# next stage
FROM node:18-slim
WORKDIR /usr/src/app

COPY --from=builder /usr/src/app .

ENV PORT=3000 \
    API_HOST=http://34.58.129.251:3001

EXPOSE 3000

CMD ["npm", "start"]

