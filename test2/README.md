# 实验2：用户管理 - 掌握管理角色、权根、用户的能力，并在用户之间共享对象


## 1、实验前准备：
下载安装ssh客户端并登录。截图如下：

![](https://github.com/lwjbox/oracle/blob/master/test2/one.png?raw=true)
## 2、实验内容：
- 第一步：

以system登录到pdborcl，创建角色lwjbox和用户dasenlin，给用户分配表空间，设置限额为50M，授予lwjbox角色。截图如下：

![](https://github.com/lwjbox/oracle/blob/master/test2/two.png?raw=true)

- 第二步：

新用户dasenlin连接到pdborcl，创建表mytable和视图myview，插入数据，最后将myview的SELECT对象权限授予hr用户。截图如下：



![](https://github.com/lwjbox/oracle/blob/master/test2/three.png?raw=true)

- 第三步：

用户hr连接到pdborcl，查询new_user授予它的视图myview。截图如下：



![](https://github.com/lwjbox/oracle/blob/master/test2/four.png?raw=true)

## 3、查看数据库的使用情况

查看表空间的数据库文件，以及每个文件的磁盘占用情况。截图如下：


![](https://github.com/lwjbox/oracle/blob/master/test2/five.png?raw=true)


## 4、实验总结

通过本实验的学习我能够创建新角色和新用户，并且能用新用户连接数据库、创建表，插入数据，创建视图，查询表和视图的数据。
