# Laravel Artisan Commands

> **List of all artisan commands of Laravel**

```
    composer create-project laravel/laravel YOUR_PROJECT_NAME 
    composer create-project laravel/laravel="5.8.*" YOUR_PROJECT_NAME
    composer create-project laravel/laravel=8.*.* YOUR_PROJECT_NAME --prefer-dist
    composer create-project laravel/laravel=4.1.27 YOUR_PROJECT_NAME --prefer-dist
```
```
    php artisan --version
    php artisan -V
    
    php artisan serve
    php artisan serve --port=YOUR_PORT
    
    php artisan key:generate
    
    composer dump-autoload

    php artisan list
```
```
    php artisan cache:clear

    php artisan config:clear
    php artisan config:cache
    
    php artisan view:clear
    php artisan view:cache

    php artisan route:clear
    php artisan route:cache

    php artisan event:clear
    php artisan event:cache

    php artisan optimize:clear
```
```
    php artisan migrate

    php artisan migrate:status
    
    php artisan migrate --force
    
    php artisan migrate:rollback
    php artisan migrate:rollback --step=5
    
    php artisan migrate:reset
    
    php artisan migrate:refresh
    
    php artisan migrate:refresh --seed
    php artisan migrate:refresh --step=5
    
    php artisan migrate:fresh
    php artisan migrate:fresh --seed
    
    php artisan db:seed
    php artisan db:seed --class=UserSeeder
    php artisan db:seed --force
```
```
    php artisan make:migration create_YOUR_TABLE_NAME_table 
    php artisan make:migration create_users_table --create=users
    php artisan make:migration add_votes_to_users_table --table=users

    php artisan make:seeder YOUR_TABLE_NAMESeeder
    
    php artisan make:controller YOUR_CONTROLLER_NAMEController
    
    php artisan make:model YOUR_MODEL_NAME
    
    php artisan make:middleware YOUR_MIDDLEWARE_NAME
    
    php artisan make:event YOUR_EVENT_NAME
    
    php artisan make:listener YOUR_LISTENER_NAME
    
    php artisan queue:table
```
```
    php artisan make:command YOUR_COMMAND_NAME

    php artisan make:mail YOUR_MAILABLE_NAME
```

```
    php artisan tinker
    User::factory()->count(3)->make();
    User::factory()->count(3)->create();
```

```
    composer require laravel/ui
    composer require laravel/ui:^3.4 (for 8)
    composer require laravel/ui:^2.4 (for 7)
    composer require laravel/ui:^1.0 --dev (for 6)
    
    php artisan ui vue
    
    php artisan ui vue --auth

    php artisan ui bootstrap --auth
    
    npm install
    npm run dev
    npm run prod
    npm run watch
    
    step1: npm cache clear --force
    step2: delete package-lock.json
    step3: again run - "npm run dev"
```

```
php artisan queue:table
php artisan queue:failed-table
php artisan queue:batches-table
```

```
php artisan vendor:publish --tag=laravel-errors
```

```
{!! $all_products->withQueryString()->links() !!}
{{ $allImages->appends(request()->query())->links() }}
```

```
$users = User::paginate()->withQueryString();
$users = User::paginate()->appends([
    'role' => $request->role,
    'group' => $request->group,
]);
```

```
$data = ProcurementItems::with(['procurement' => function($itemQry) {
    $itemQry->with(['cartOrders' => function($cartQry) {
        $cartQry->with(['cartItems' => function($cartItmQry) {
            $cartItmQry->with(['productVariant']);
        }]);
    }]);
}])
->where('procurement_id', $procurementId)
->orderBy('id', 'desc')
->get();
```
