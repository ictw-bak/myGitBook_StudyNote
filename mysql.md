##### mysql添加用户方法

##### 建立数据库gamesp

##### create database gamesp;

##### 添加用户

##### grant all on 数据库名.\* to 用户名@localhost identified by '密码';

##### grant all on gamesp.\* to newuser@localhost identified by 'password';

##### 添加一个远程用户，名为username密码为password

##### GRANT ALL PRIVILEGES ON \*.\* TO username@"%" IDENTIFIED BY 'password'

##### 说明：

##### （1）grant all 赋予所有的权限

##### （2）gamesp.\* 数据库 gamesp 中所有的表

##### （3）newuser 用户名

##### （4）@localhost 在本地电脑上的 mysql server 服务器

##### （5）identfified by 'password' 设置密码



