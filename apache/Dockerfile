FROM alpine:latest
ENV server_name=localhost
RUN apk add --no-cache apache2-proxy
RUN apk add --no-cache apache2-utils
RUN rm -rf /var/www/localhost/cgi-bin/
CMD exec /usr/sbin/httpd -D FOREGROUND -f /etc/apache2/httpd.conf