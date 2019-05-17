# Docker_environment_Laravel
Base Environment for a laravel application/api

**Contents**
  * Docker environment that creates the following containers:
      * mysql
      * php-fpm (where along with composer you can create a Laravel API/Application)
      * Ngnix that will provide a webserver for the api/application in the application/ folder
      * phpmyadmin to manage the Database

**Prerequisites**

  *  Docker
  *  Docker-compose
  
**How To Use**

1 - Assuming you have docker and docker-compose at hand. Open a terminal at the root folder of the project ad use ```docker-compose up```

2 - Still in the terminal ```docker exec -it php-fpm bash ```

3 - ```composer create-project laravel/laravel=5.6.12 server — prefer-dist```

4 - Back at the root of the project you should have a folder named server where is your laravel folder and it is served at ```localhost:8081``` and phpmyadmin is served at ```localhost:8080``` as default.


**Helpfull References/External Documentations**
* Guide used : https://medium.com/@newaeonweb/laravel-restful-api-using-docker-in-three-steps-63a5b4c8f211
* phpmyadmin : https://hub.docker.com/r/phpmyadmin/phpmyadmin/
* Permissions for laravel folder : https://vijayasankarn.wordpress.com/2017/02/04/securely-setting-file-permissions-for-laravel-framework/