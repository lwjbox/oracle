## 实验3：创建分区表

### 实验目的：

掌握分区表的创建方法，掌握各种分区方式的使用场景。

### 实验内容：
- 本实验使用3个表空间：USERS,USERS02,USERS03。在表空间中创建两张表：订单表(orders)与订单详表(order_details)。
- 使用自己的账号**dasenlin**创建本实验的表，表创建在上述3个分区，自定义分区策略。
- 你需要使用system用户给你自己的账号分配上述分区的使用权限。你需要使用system用户给你的用户分配可以查询执行计划的权限。
- 表创建成功后，插入数据，数据能并平均分布到各个分区。每个表的数据都应该大于1万行，对表进行联合查询。
- 写出插入数据的语句和查询数据的语句，并分析语句的执行计划。
- 进行分区与不分区的对比实验。
### 实验结果

创建orders表的实验截图：

![图1-1](https://github.com/lwjbox/oracle/blob/master/test3/1-1.png?raw=true) 
</br></br></br></br></br>

创建order_details表的实验截图：

![图1-2](https://github.com/lwjbox/oracle/blob/master/test3/1-2.png?raw=true) 
</br></br></br></br></br>

通过system给WANFENG分配权限的实验截图：

![图1-3](https://github.com/lwjbox/oracle/blob/master/test3/1-3.png?raw=true) 
</br></br></br></br></br>

![图1-4](https://github.com/lwjbox/oracle/blob/master/test3/1-4.PNG?raw=true) 
</br></br></br></br></br>

查看表空间的数据文件的实验截图：

![图1-5](https://github.com/lwjbox/oracle/blob/master/test3/1-5.png?raw=true) 
</br></br></br></br></br>

查看数据使用情况的实验截图：

![图1-6](https://github.com/lwjbox/oracle/blob/master/test3/1-6.png?raw=true) 
</br></br></br>

### 实验总结
Oracle的表分区功能通过改善可管理性、性能和可用性，从而为各式应用程序带来了极大的好处。没有分配权限普通用户只能创建表，读写会报错，所有创建表用要分配权限。

