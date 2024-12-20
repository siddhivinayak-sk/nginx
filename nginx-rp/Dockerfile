FROM nginx
COPY ./nginx/nginx.conf /etc/nginx/templates/nginx.conf.template
COPY ./public /usr/share/nginx/html

ENV TARGET_SERVER=host.docker.internal
ENV TARGET_SERVER_PORT=8081

CMD ["/bin/sh", "-c", "envsubst '$TARGET_SERVER $TARGET_SERVER_PORT' < /etc/nginx/templates/nginx.conf.template > /etc/nginx/conf.d/default.conf && exec nginx-debug -g 'daemon off;'"]

