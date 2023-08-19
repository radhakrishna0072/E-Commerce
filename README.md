# **Laravel E-Commerce Project**
1) Update the EC2 instance
2) Install php & check version using
# _sudo apt install php -y_ 
php - -version
 ![image](https://github.com/bvenkydevops/E-Commerce/assets/104990262/a6cd268b-9670-4d9b-9b27-83334f2ffd7b)


3) Install php extensions like FastCGI Process Manager (fpm), Binary Calculator Math(bcmath), mysql, xml, zip, gd, intl, pdo   by using
# sudo apt install php8.1-fpm php8.1-curl php8.1-bcmath php8.1-mysql  php8.1-xml php8.1-zip php8.1-gd php8.1-intl php8.1-pdo

4) Install Apache HTTP server using
# _sudo apt install apache2 –y_

5) Install My-SQL server using 
# _sudo apt install mysql-server_

6) To Provide the security to My-SQL DB Server  using 
# _sudo mysql_secure_installation_
Connecting to MySQL using a blank password. == Enter ‘Y’
There are three levels of password validation policy: = Enter ‘0(Zero)’
Remove anonymous users? = Enter ‘Y’ 
Disallow root login remotely? = Enter ‘n’
Remove test database and access to it? = ‘y’
Reload privilege tables now? = Enter ‘y’

7) To directly interact with MYSQL DB with super user privileges  
# _Sudo mysql_
i) To change the authentication method and password for the 'root' user in MySQL
# _ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';_
ii) apply any changes made to the user privileges
# _FLUSH PRIVILEGES;_
iii) To exit, Enter
exit

8) go to 
# _cd /var/www/html/_

9) remove index.html file
  # _rm –rf  index.html_

10) Clone the repository
# _git clone https://github.com/bvenkydevops/E-Commerce.git_

11) To connect MYSQL server using CLI
 # _mysql -u root –p_
i)password: password
ii) To create the ‘ecommerce_marolix’ database using
# _CREATE DATABASE ecommerce_marolix;_
iii) To check data base is created (or) not
CREATE DATABASE ecommerce_marolix;
  it shows like this
  ![image](https://github.com/bvenkydevops/E-Commerce/assets/104990262/19fefe0c-6593-422e-8f32-901c2d61628e)

 
iv) To exit from the MYSQL database using
exit

12) go to 
# _cd  /var/www/html/E-Commerce-project/database/database/_

13) To import from “ecommerce_marolix.sql”  DB  to  newly created “ecommerce_marolix” DB with password using 
# _mysql -u root -p ecommerce_marolix < ecommerce_marolix.sql_
Enter password: password

15) To connect the MYSQL DB with password
   # _ mysql -u root -p_
i)Enter password: password
ii) To see the databases using 
# _show databases;_
iii) Select a specific database as the active database for your current session using 
   # _use ecommerce_marolix;_
iv) To see the what are the tables present in DB using 
    # _show tables;_
v) To exit from the MYSQL DB
     exit

16)Go to 
# cd /var/www/html/E-Commerce-project/E-commerce-7June

17) To change ‘’.env.example”  file to “.env” file
  # mv  .env.example .env

18) Go to “.env”  file and configure as follows
     #  vi  .env 
               DB_CONNECTION=mysql 
               DB_HOST=localhost 
               DB_PORT=3306 
               DB_DATABASE=ecommerce_marolix 
               DB_USERNAME=root 
               DB_PASSWORD=password

19) To download the Composer installation script and save it as composer-setup.php using the PHP command-line interpreter.
Cd ~
    #  _php -r "copy('http://getcomposer.org/installer', 'composer-setup.php');"_
20) To run the composer installation Script using
 #  _php composer-setup.php_

21) To execute the Composer tool, which is responsible for managing dependencies and packages for PHP projects using?
   #  _php composer.phar_

22) To move the Composer executable (PHAR file) to a directory that is in your system's PATH, making it globally accessible from the command line.
#  _sudo mv composer.phar /usr/local/bin/composer_

23) To declare and manage project dependencies in a “composer.json” file and install the required packages from various sources
 Composer

24)To change the “user” & “group” ownership to “www-data”( This is a common operation in web server configurations to ensure that the web server process has the necessary permissions to access and modify the files and directories of a web application.)
# sudo chown -R www-data:www-data /var/www/html/E-Commerce-project
# sudo chmod -R 775 /var/www/html/E-Commerce-project/

25) go to 
# cd /var/www/html/E-Commerce-project/E-commerce-7June/

26) To update the dependencies, based on version present in “composer.json” file
 # composer update

27)  To install the dependencies defined in your project's “composer.json” file.
# composer install

28) Laravel will generate a new random key and update the APP_KEY value in your application's .env file 
 # php artisan key:generate

29) Laravel will execute any pending migrations that haven't been run yet by using
#  php artisan migrate

30) To restart the Apache HTTP Serve
  #  sudo service apache2 restart

31) Update the security group with “All traffic” in Inbound rules & copy the EC2 instance public IP and past in Chrome. Finally get an output like below 

![image](https://github.com/bvenkydevops/E-Commerce/assets/104990262/ce4cb05e-81d5-48fc-9592-8c7ccc8ebf9c)


ii) After click on  E-Commerce-project

 ![image](https://github.com/bvenkydevops/E-Commerce/assets/104990262/96f4653c-8b62-4645-bb52-46110504099e)


iii) After Click on E-commerce-7June & final output is like this
 
![image](https://github.com/bvenkydevops/E-Commerce/assets/104990262/db140f53-503f-4182-bb45-fe7559848e5a)

