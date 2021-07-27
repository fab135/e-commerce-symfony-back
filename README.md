# Requirements 
```
- php ^7.2
- symfony cli
```

## Clone this reposiroty

`git clone https://github.com/mickaelnambs/e-commerce-symfony-back.git`

Go inside 

`cd e-commerce-symfony-back`

Update composer

`composer install`

Update database configuration, edit this line in `.env` file with your own configuration

`DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=5.7`

Generate two keypairs

`mkdir -p config/jwt`
`php bin/console lexik:jwt:generate-keypair`

Create database:

`php bin/console doctrine:database:create`

Then update schema by running:

`php bin/console d:s:u -f`

Load fixtures:

`php bin/console doctrine:fixtures:load --no-interaction`

Run symfony server

`symfony serve`

