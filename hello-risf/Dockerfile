FROM nginx:alpine

RUN mkdir -p /var/cache/nginx/client_temp && \
    chown -R nginx:nginx /var/cache/nginx && \
    chmod -R 755 /var/cache/nginx && \
    touch /var/run/nginx.pid && \
    chown -R nginx:nginx /var/run/nginx.pid

RUN sed -i '/access_log/d' /etc/nginx/nginx.conf && \
    sed -i '/error_log/d' /etc/nginx/nginx.conf

COPY index.html /usr/share/nginx/html/

RUN chown nginx:nginx /usr/share/nginx/html/index.html

USER root
