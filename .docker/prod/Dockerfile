#Phase 1 : Production Build
FROM node:14-alpine3.12 as builder

WORKDIR /usr/share/nginx/html
ENV NODE_ENV=production
COPY package.json .
RUN npm install
COPY . .
CMD ["npm","start"]

#

