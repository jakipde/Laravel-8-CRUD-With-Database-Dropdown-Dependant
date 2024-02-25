# Laravel-8-CRUD-With-Database-Dropdown-Dependant
Simple Laravel 8 CRUD Template with Database Dropdown Dependant (Seed Based)

Project Details:
This small template was created using Laravel 8, Composer 2, and PHP 8.2.

Database Configuration:
This project uses a SQL Server Database. Make sure you have the necessary drivers and configurations installed.

Setup Guide:

1. Login to your SQL Server and create a new user (username: jaki, password: 123). You can change the username and password if needed.

2. Create a new database named "GoodRecord". You can also change the database name if desired.

3. Open your terminal in VS Code.

4. Run the following commands:

php artisan migration --path=database/migrations/2024_02_24_223956_shift_grup_choices_table.php
php artisan migration --path=database/migrations/2024_02_24_224006_part_no_choices_table.php
php artisan migration --path=database/migrations/2024_02_24_224017_customer_choices_table.php

5. Run the following command to create the products table:

php artisan migration --path=database/migrations/2024_02_22_121111_create_products_table.php

6. It's important to migrate the options tables first, then the products table to avoid foreign key errors.

7. Seed the tables with the following commands:

php artisan db:seed --class=ShiftGroupChoicesSeeder
php artisan db:seed --class=PartNoChoicesSeeder
php artisan db:seed --class=CustomerChoicesSeeder

8. You can also use "**php artisan db:seed**" to seed all tables.

9. Check the tables **dbo.customer_choices**, **dbo.part_no_choices**, **dbo.shift_grup_choices**. Right-click and select "Select Top 1000 Rows" to verify that the tables are populated.

10. If you have Valet-Windows installed, you can test the application by accessing laravel8crudgr.test in your browser's URL column, if not then just run "**php artisan serve**".
