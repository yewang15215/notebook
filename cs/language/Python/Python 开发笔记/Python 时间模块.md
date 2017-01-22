# Python 时间模块

* 周
    - 周第一天
        ```
        the_date - timedelta(days=the_date.weekday())
        ```
    - 周最后一天
        ```
        the_date + timedelta(days=-the_date.weekday(), weeks=1) - timedelta(1)
        ```
* 月
    - 月最后一天
        ```
        from calendar import monthrange

        date(the_date.year, the_date.month, monthrange(the_date.year, the_date.month)[1])
        ```
