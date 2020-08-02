





docker pull mysql:5.6.34



docker run --name mysql5634 -p 3316:3306 -e MYSQL_ROOT_PASSWORD=root -d mysql:5.6.34



docker run --name mysql8016 -p 3318:3306 -e MYSQL_ROOT_PASSWORD=root -d mysql:8.0.16