# Explain

* expain 出来的信息有 10 列，分别是
    ```
    id、select_type、table、type、possible_keys、key、key_len、ref、rows、Extra
    ```
* id 是 SQL 执行的顺序的标识, SQL 从大到小的执行
    1. id 相同时，执行顺序由上至下
    2. 如果是子查询，id 的序号会递增，id 值越大优先级越高，越先被执行
    3.id 如果相同，可以认为是一组，从上往下顺序执行；在所有组中，id 值越大，优先级越高，越先执行
* select_type 是查询中每个 select 子句的类型
    (1) SIMPLE(简单 SELECT, 不使用 UNION 或子查询等)
    (2) PRIMARY(查询中若包含任何复杂的子部分, 最外层的 select 被标记为 PRIMARY)
    (3) UNION(UNION 中的第二个或后面的 SELECT 语句)
    (4) DEPENDENT UNION(UNION 中的第二个或后面的 SELECT 语句，取决于外面的查询)
    (5) UNION RESULT(UNION 的结果)
    (6) SUBQUERY(子查询中的第一个 SELECT)
    (7) DEPENDENT SUBQUERY(子查询中的第一个 SELECT，取决于外面的查询)
    (8) DERIVED(派生表的 SELECT, FROM 子句的子查询)
    (9) UNCACHEABLE SUBQUERY(一个子查询的结果不能被缓存，必须重新评估外链接的第一行)

## 参考文章
* [MySQL Explain 详解](http://www.cnblogs.com/xuanzhi201111/p/4175635.html)
