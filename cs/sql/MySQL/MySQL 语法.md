# MySQL 语法

* 注释  
    * 三种注释方法
        1. `# `  
        2. `-- `
        3. `/* */`
    * 注意
        * a
        ```
        /*!50001 DROP TABLE IF EXISTS `count_yysbh`*/; 
        ```
        表示假如 数据库版本是5.00.01以上版本，“DROP TABLE IF EXISTS `count_yysbh”才会被执行。
        * b
* join
    - `using (xxx)`  一定要加括号
* union 与 union all
    - union 会去重
* using 与 on
    - using 是 两个表的字段相同时使用
* having 与 where
    - 因为 where 无法与 mysql 的统计函数一起使用
    如
    ```
    SELECT  customer,SUM(price) FROM order
    WHERE customer=’…’ OR customer = ‘…’
    GROUP BY customer
    HAVING SUM(price) > 1500
    ```
