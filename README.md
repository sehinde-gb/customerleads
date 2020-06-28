Laravel 6

This project uses Laravel 6

Installation

git clone https://github.com/sehinde-gb/customerleads.git

cd customerleads

Run composer install to ensure that Laravel knows what packages to use.

To generate your application key type the following command

php artisan key:generate

Create a MYSQL database using mysql -u root and provide a name for your SQL database.

Amend your env file so that it reflects the name of your newly added database name above.

php artisan migrate --seed to create and populate tables

Check to see if your tables have migrated successfully using your sql software application

Within our example we are using the Laravel Valet environment and we would suggest that you browse to http://customerleads.test/
