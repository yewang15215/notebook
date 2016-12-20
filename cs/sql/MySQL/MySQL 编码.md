# MySQL 编码


* SET NAMES
    > SET NAMES utf8
    相当于
    SET character_set_client = utf8 用来设置客户端送给MySQL服务器的数据的 字符集
    SET character_set_results = utf8 服务器返回查询结果时使用的字符集
    SET character_set_connection = utf8
    MySQL 服务器 把客户端传来的数据，从character_set_client字符集转换成character_set_connection字符集
