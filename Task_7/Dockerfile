# Використання базового образу Alpine
ARG NGINX_VERSION=latest
FROM nginx:${NGINX_VERSION}-alpine

# Встановлення пакетів Nginx та supervisord
RUN apk update && apk add nginx supervisor

# Копіювання конфігураційних файлів в образ
COPY nginx.conf /etc/nginx/nginx.conf
COPY supervisord.conf /etc/supervisord.conf

# Вказання команд, які будуть виконані при старті контейнера
CMD ["supervisord", "-c", "/etc/supervisord.conf"]
