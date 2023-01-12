FROM nginx:1.22-alpine

RUN set -x ; \
    adduser -u 82 -D -S -G www-data www-data && \
    sed 's/user  nginx;/user  www-data;/g' -i /etc/nginx/nginx.conf

COPY nginx/default.conf /etc/nginx/conf.d
COPY --chown=82:82 ./flatpress-1.2.1/ /var/www/html
