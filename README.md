# docker-nginxphp-laravel

В этой ветке уже сервер с laravel+vue так же для установки здесь есть композер,
но так как у нас папка vendor будет пустая вам самим нужно будет своими ручками маленькими установить это все дело через композер.

Подключайтесь к php контейнеру exec и там команду чтобы попасть в корень проекта

```php
cd /var/www/html/
```
Установить всю фигню
```php
php composer.phar install --working-dir=src
php src/artisan key:generate
php src/artisan migrate
```

Если при установке ошибка, возможно стоит отключить дебаг в IDE, во время выполнения установки

## Xdebug
Так же здесь есть дебаг.
Для phpStorm нужно будет добавить хост сервер в `Settings/PHP/Servers`.
Host:localhost
Так же укажите маппинг для папки www - /var/www/html

> Ну а хули, я че знать должен

<img src="https://itstruct.ru/monkey_thinking.gif" alt="description" style="width: 100%;">