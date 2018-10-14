FROM alpine:3.6
RUN apk add --update \
     nginx \
     && rm -rf /var/cache/apk/*
RUN mkdir -p /run/nginx

COPY ./nginx-proxy/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

ENTRYPOINT ["nginx", "-g", "daemon off;"]
