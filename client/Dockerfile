# FROM node:18.13-alpine as builder
#
# WORKDIR /app
# COPY package.json /usr/src/app/package.json
#
# RUN npm install --force
#
# COPY . /app
# RUN npm run build
#
# FROM nginx:alpine
#
# COPY --from=builder /app/build /usr/share/nginx/html
#
# EXPOSE 80
#
# CMD ["nginx", "-g", "daemon off;"]

FROM node:18.13-alpine as builder

WORKDIR /app
COPY ./package.json .

RUN npm install --force

COPY . .

RUN npm run build

FROM nginx:alpine
RUN rm /etc/nginx/conf.d/default.conf
RUN pwd
COPY /var/jenkins_home/workspace/docker/fe/default.conf /etc/nginx/conf.d
COPY --from=builder /app/build /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]

