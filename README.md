<style>
	blockquote {
    background-color: #000000;
}
</style>
# Laravel-Artisan-Commands
List of all artisan commands of Laravel

> **1. How to create or install a new Laravel project with latest version?**
```
composer create-project laravel/laravel YOUR_PROJECT_NAME 
```

> **2. How to create or install a new Laravel project with specific version?**
```
composer create-project laravel/laravel="5.8.*" YOUR_PROJECT_NAME 
```

> **3. How to create or install a new Laravel project with stable specific version?**
```
composer create-project laravel/laravel="5.8.*" YOUR_PROJECT_NAME 
```

> **4. How to check Laravel version?**
```
php artisan --version
OR
php artisan -V
```

> **5. How to start Laravel project in default port?**
```
php artisan serve
Defatlt port is 8000
```

> **6. How to start Laravel project in a specific port?**
```
php artisan serve --port=YOUR_PORT
```

```
1. composer create-project laravel/laravel YOUR_PROJECT_NAME 
2. composer create-project laravel/laravel="5.8.*" YOUR_PROJECT_NAME
3. composer create-project --prefer-dist laravel/laravel YOUR_PROJECT_NAME "5.5.*"

4.  php artisan --version
5.  php artisan serve
6.  php artisan serve --port=YOUR_PORT

7.  php artisan key:generate

8.  php artisan cache:clear
9.  php artisan config:cache
10. php artisan view:clear
11. php artisan route:clear
12. php artisan route:cache

13. composer dump-autoload
14. php artisan migrate
15. php artisan db:seed
```
