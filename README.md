# Laravel 10  & TailwindCSS 3 skeleton

## Requirements
•	PHP 8.1 or higher

## Version
This Laravel framework is running on a version of 10.10 and TailwindCSS is running on 3.3.5.

## Usage
Clone the repository
```
git clone git@github.com:tecnauta/laravel10-pack-skeleton.git
```

Rename the directory to new name
```
mv laravel10-pack-skeleton/ new-name-example/
```

Change directories into new-name-example
```
cd new-name-example/
```

Install composer
```
composer install
```

Create the .env file by duplicating the .env.example file
```
cp .env.example .env
```

Change/add values to database on .env
```
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=
```

Set the APP_KEY value
```
php artisan key:generate
```

Clear your cache & config (OPTIONAL)
``` 
php artisan cache:clear && php artisan config:clear
```

Change docker-compose.yml
- replace laravel10-pack-skeleton-app with the name of the project
- replace laravelskeleton network

Finally, run docker!
- docker-compose up --build
- npm run dev

Remember
- Run artisan commands that interact with the database from inside the app container
```
docker exec new-name-example-app php artisan migrate
```
