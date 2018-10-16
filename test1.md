### 教材中的查询语句

- 查询1：

```SQL
SELECT d.department_name，count(e.job_id)as "部门总人数"，
avg(e.salary)as "平均工资"
from hr.departments d，hr.employees e
where d.department_id = e.department_id
and d.department_name in ('IT'，'Sales')
GROUP BY department_name;
```

- 查询2：
```SQL
SELECT d.department_name，count(e.job_id)as "部门总人数"，
avg(e.salary)as "平均工资"
FROM hr.departments d，hr.employees e
WHERE d.department_id = e.department_id
GROUP BY department_name
HAVING d.department_name in ('IT'，'Sales');
```

##### 教材中的查询语句分析：
- 查询1中，通过avg函数求出职工的平均工资，通过count函数求出部门的总人数，用where子句和group by子句一起使用，分组查询可以消除非限定行的标准where子句d.department_id = e.department_id   and d.department_name in ('IT'，'Sales')，从而查询到两个部门('IT'和'Sales')的部门总人数和平均工资。
- 查询2中，也一样通过avg函数求出职工的平均工资，通过count函数求出部门的总人数，不同的是在group by子句之后使用having子句，限定条件d.department_name in ('IT'，'Sales')进行分组，这样系统仅对满足条件的组返回结果，having和where类似，唯一的差别是where过滤行，having过滤组。

### 自定义的查询语句：


~~~sql
SELECT department_name, count(job_id) as "部门总人数", 
avg(salary) as "平均工资"
FROM hr.employees e
JOIN
(SELECT d.department_id, d.department_name
FROM hr.departments d
WHERE d.department_name in ('IT', 'Sales'))
USING (department_id)
GROUP BY department_name;
~~~

##### 自定义的查询语句分析：
- 自定义的查询语句中首先执行id查询d.department_id = e.department_id， join 用于根据两个或多个表中的列之间的关系,从这些表中查询符合department_name='IT'和department_name='Sales'的部门的条件，通过avg函数求出职工的平均工资，通过count函数求出部门的总人数。


### 语句的执行结果：
- 查询语句1用时0.037秒
- 查询语句2用时0.062秒


从时间上判断，查询语句1更优。
自定义查询语句的sqldeveloper中截图：
![图片1]()
