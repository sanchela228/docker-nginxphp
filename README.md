# docker-nginxphp

Просто Nginx + php8.3

# Cron
Так же отдельно здесь добавлено phpmyadmin на 8080 порт
и крон.
Для настройки крон заданий идем в `/docker/server/crontabs/root`

Изначально `/etc/crontabs/root` не выполняется в nginx:alpine, поэтому я запускаю это отдельным контейнером и в докер файле уже запускаю крон
```Dockerfile
RUN crontab /etc/crontabs/root
CMD ["crond", "-f"]
```

Сама рабочая область проекта находится в `/www/`

# Xdebug
Так же здесь есть дебаг. 
Для phpStorm нужно будет добавить хост сервер в `Settings/PHP/Servers`.
Host:localhost
Так же укажите маппинг для папки www - /var/www/html


> Ну было и было, сидим пердим

<img src="https://itstruct.ru/monkey.gif" alt="description" style="width: 100%;">