#Phase 1 : Production Build
FROM node:14-alpine3.12 as builder

WORKDIR /var/app
ENV NODE_ENV=production
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

#

FROM nginx
EXPOSE 80
COPY --from=builder /var/app/build /usr/share/nginx/html


#sudo docker run -d -p 3000:80 react-docker-travis:prod

