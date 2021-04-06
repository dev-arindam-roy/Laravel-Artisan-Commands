# Laravel Artisan Commands

> **List of all artisan commands of Laravel**

**Create Project**
```
    composer create-project laravel/laravel YOUR_PROJECT_NAME 
    composer create-project laravel/laravel="5.8.*" YOUR_PROJECT_NAME 
```
```
    php artisan --version
    php artisan -V
    
    php artisan serve
    php artisan serve --port=YOUR_PORT
    
    php artisan key:generate
    composer dump-autoload
    
    php artisan cache:clear
    php artisan config:clear
    php artisan config:cache
    
    php artisan view:clear
    php artisan view:cache

    php artisan route:clear
    php artisan route:cache

    php artisan migrate
    php artisan db:seed
    
    php artisan make:controller YOUR_CONTROLLER_NAME
    php artisan make:model YOUR_MODEL_NAME
    php artisan make:middleware YOUR_MIDDLEWARE_NAME
    php artisan make:migration create_YOUR_TABLE_NAME_table 
```