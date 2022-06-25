
## 1. Initialize the project by, using the command:
```
composer create-project symfony/skeleton my-project
```
## 2. Install Twig template engine:
```
composer require twig
```
![twig on IDEs.](https://notejoy.s3.amazonaws.com/note_images/2216881.1.Image%202022-06-23%20at%2009.03.24%20undefined.png)
## 3. Create controller:
Install library to create controller:
```
composer require --dev symfony/maker-bundle
```
Install Doctrine Annotations to implement custom function annotations for classes and PHP functions.
```
composer require doctrine/annotations
```
Make controller:
```
php bin/console make:
```
![Result of make controller](https://notejoy.s3.amazonaws.com/note_images/2216881.1.Image%202022-06-23%20at%2009.10.17%20undefined.png)

## 4. Setup database:
Modify the DATABASE_URL variable to connect to the database:
```
DATABASE_URL="mysql://root:@127.0.0.1:3306/symf4?serverVersion=mariadb-10.4.24"
```
Symfony provides tools for use with databases thanks to Doctrine. These tools support relational databases like MySQL and PostgreSQL and also NoSQL databases like MongoDB.
```
 composer require symfony/orm-pack
```
Create database:
```
php bin/console make:entity
```
Next, execute the create migration file command, which will generate the instruction file containing the SQL query.
```
php bin/console make:migration
```
To create a table in PHPMyAdmin , we have to run the following command:
```
php bin/console doctrine:migrations:migrate
```
