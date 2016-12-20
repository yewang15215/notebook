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
