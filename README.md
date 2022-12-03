# Laravel docker шаблон
## Установка и конфигурация
#### 1. Устанавливаем laravel в директорию app
```
docker exec template-php-1 composer create-project laravel/laravel app
```
#### 2. Устанавливаем имя базы данных в .env.example DB_DATABASE=

#### 3. Копируем файл .env.example в директорию app. Переименовываем файл в .env.
```
docker exec template-php-1 cp .env.example app/.env
```
#### 4. Генерируем key
```
docker exec template-php-1 php artisan key:generate
```
#### 5. Открываем доступ к storage в app
```
docker exec template-php-1 chown -R www-data:www-data /var/www
```

