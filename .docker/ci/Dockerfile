#Phase 1 : Production Build
FROM node:14-alpine3.12 as builder

WORKDIR /var/app
ENV NODE_ENV=production
COPY package.json .
RUN npm install
COPY . .

#

