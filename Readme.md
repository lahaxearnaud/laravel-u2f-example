#Example of usage of lahaxearnaud/laravel-u2f

Hello world application of the library [lahaxearnaud/laravel-u2f](https://github.com/lahaxearnaud/laravel-u2f).


## Installation

    git clone https://github.com/lahaxearnaud/laravel-u2f-example.git
    
    cd laravel-u2f-example
    
    composer install
    
    cp .env.example .env
    
    touch database.sqlite

Edit .env file and change the DB_DATABASE sqlite path

    php artisan migrate

The output should be:

    Migration table created successfully.
    Migrating: 2014_10_12_000000_create_users_table
    Migrated:  2014_10_12_000000_create_users_table (0 seconds)
    Migrating: 2014_10_12_100000_create_password_resets_table
    Migrated:  2014_10_12_100000_create_password_resets_table (0 seconds)
    Migrating: 2015_05_17_031822_create_u2f_key_table
    Migrated:  2015_05_17_031822_create_u2f_key_table (0 seconds)

The easiest way to test the app is [Valet](https://laravel.com/docs/5.8/valet)

    valet park
    valet secure

    php artisan key:generate

Now you can go to the [homepage](https://laravel-u2f-example.test/): https://laravel-u2f-example.test/

## Create an account

Create an account on the [register page](https://laravel-u2f-example.test/register): https://laravel-u2f-example.test/register


## Register new devices

If you use the commande ```php artisan route:list``` you should see some u2f routes.

Go to [U2F Register page](https://laravel-u2f-example.test/u2f/register): https://laravel-u2f-example.test/u2f/register

Follow instruction to add a new u2f key to your account.

![Register](/doc/register.png?raw=true)

## Second factor login

Once you have registred a device you can logout.
If you try to login in again you will have an additionnal steps with your u2f key.

![Register](/doc/login.png?raw=true)



## After coding

What better way to relax, after spending hours coding, than a good [mojito](https://cocktailand.fr/cocktail/recette/mojito-26) on a terrace?