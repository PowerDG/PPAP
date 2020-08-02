





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



### 对宿主授权

GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'root' WITH GRANT OPTION;



\---------------------

本文著作权归作者所有。

商业转载请联系作者获得授权，非商业转载请注明出处。

来源地址：https://www.php.cn/docker/445365.html

来源：php中文网(www.php.cn)

© 版权声明：转载请附上原文链接！



### 重启改名字



===

**使用管理员身份打开命令行**

　　①重启mysql：

　　　　1、**net stop mysql**  2、**net start mysql** 
 　②进入mysql，登录
 　　　mysql -u root -p
 　　　不用输入密码，直接回车（出现Enter Password 也一样直接回车，即可登陆成功）
 　③输入**use mysql**，修改root的密码：
 　　　update user set authentication_string=password('新密码') where user='root';
 　　　flush privileges;
 　④退出：

　　　　quit;
 　⑤再次重启mysql：

　　　　1、net stop mysql   2、net start mysql
 　⑥测试是否成功就是是否登陆成功咯。
 　　　mysql -u root -p

　　　　Enter Password>'新密码'





### End

