





docker pull mysql:5.6.34



docker run --name mysql5634 -p 3316:3306 -e MYSQL_ROOT_PASSWORD=root -d mysql:5.6.34



docker run --name mysql8016 -p 3318:3306 -e MYSQL_ROOT_PASSWORD=root -d mysql:8.0.16



###  —5-6-7

update mysql.user set host="%" where user="root";

flush privileges;

### —8

update mysql.user set host="%" where user="root";

ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY '123456';

flush privileges;



flush privileges;



use mysql;



update user set authentication_string = password('root') where user = 'root';