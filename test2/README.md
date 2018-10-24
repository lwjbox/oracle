# 实验2：用户管理 - 掌握管理角色、权根、用户的能力，并在用户之间共享对象


## 实验前准备：
下载安装ssh客户端并登录。截图如下：

![](https://github.com/lwjbox/oracle/blob/master/test2/one.png?raw=true)
## 实验内容：
- 第一步：

以system登录到pdborcl，创建角色lwjbox和用户dasenlin，给用户分配表空间，设置限额为50M，授予lwjbox角色。截图如下：

![](https://github.com/lwjbox/oracle/blob/master/test2/two.png?raw=true)

- 第二步：

新用户dasenlin连接到pdborcl，创建表mytable和视图myview，插入数据，最后将myview的SELECT对象权限授予hr用户。截图如下：



![](https://github.com/lwjbox/oracle/blob/master/test2/three.png?raw=true)


![](https://github.com/lwjbox/oracle/blob/master/test2/four.png?raw=true)
![](https://github.com/lwjbox/oracle/blob/master/test2/five.png?raw=true)
