FROM nginxinc/nginx-unprivileged:stable-alpine

ARG DOCROOT=/usr/share/nginx/html

COPY --chown=nginx:nginx . ${DOCROOT}

RUN find ${DOCROOT} -type d -exec chmod 755 {} \; && \
    find ${DOCROOT} -type f -exec chmod 644 {} \;

USER nginx
EXPOSE 8080
