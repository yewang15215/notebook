# MySQL 编码


* SET NAMES
    ```
    SET NAMES utf8
    ```
    相当于
    
    ```
    -- 用来设置客户端送给 MySQL 服务器的数据的字符集 --
    SET character_set_client = utf8 
    
    -- 服务器返回查询结果时使用的字符集 --
    SET character_set_results = utf8 
    
    -- MySQL 服务器 把客户端传来的数据，从 character_set_client 字符集转换成 character_set_connection 字符集 --
    SET character_set_connection = utf8
    
    ```
