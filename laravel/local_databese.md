## Laravel + XAMPP + MySql
What I wanted to do: To launch a database by a Laravel project provided by my current client.

1. Run MySqpl server with XAMPP
2. Run `mysql -u root -p` to log in to MySql
3. Run `CREATE DATABASE your_db_name CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;` to create a database
4. Run this command to create a database user
  ```
  CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
  GRANT ALL PRIVILEGES ON online_regist.* TO 'poas'@'localhost';
  FLUSH PRIVILEGES;
  ```
* To identify the username and password, see settings in .env
  ```
  DB_USERNAME=*****
  DB_PASSWORD=******
  ```
5. Run `php artisan migrate` in Laravel folder

### Connection verification command
```
php artisan tinker
> DB::connection()->getPdo();
```

### Encountered error
```
SQLSTATE[HY000] [1045] Access denied for user 'poas'@'localhost' (using password: YES)
```
Laravel attempted to connect to the database, but the username or password was incorrect.
