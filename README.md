Laravel Framework 8.83.27 node v20.3.0

### Запуск
- cp .env.example .env
- php artisan optimize
- npm run prod

- chmod -R 777 storage/logs
- docker-compose up -d --build

Нечего не работало множество проблем было при установке (windows 10 - phpstorm 2021.1.1) laravel-mix вот подробная инструкция:
1) composer create-project --prefer-dist laravel/laravel:^8.5 laravel-api
2) помогла статья Manually Setting up Vue without Using laravel/ui
3) composer require laravel/ui
4) php artisan ui vue
5) npm install && npm run dev
6) paсkage.json -> "laravel-mix": "^6.0.6", -> npm install
7) npm update vue-loader
8) npm i vue-loader
9) пробовать запустить впаралельно в терминалах php artisan serve и npm run wacth
10) создать компонент SpaController -> App.vue ( далее по видео)
11) web.php -> Route::get('/{any}',[\App\Http\Controllers\SpaController::class, 'index'])->where('any','.*');
12) тестировать))

    "devDependencies": {
    "@popperjs/core": "^2.10.2",
    "axios": "^0.19",
    "bootstrap": "^5.1.3",
    "cross-env": "^7.0",
    "laravel-mix": "^6.0.6",
    "lodash": "^4.17.19",
    "resolve-url-loader": "^3.1.2",
    "sass": "^1.32.11",
    "sass-loader": "^11.0.1",
    "vue": "^2.6.12",
    "vue-loader": "^15.9.8",
    "vue-template-compiler": "^2.6.12",
    "webpack-cli": "^4.9.2"
    }



