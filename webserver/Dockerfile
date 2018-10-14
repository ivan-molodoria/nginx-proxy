FROM alpine:3.6
RUN apk add --update \
     nginx \
     && rm -rf /var/cache/apk/*
RUN mkdir -p /run/nginx
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./nginx/index.html /usr/share/nginx/html/index.html
EXPOSE 80

ENTRYPOINT ["nginx", "-g", "daemon off;"]
