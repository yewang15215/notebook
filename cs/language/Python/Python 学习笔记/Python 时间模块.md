# Pthon 时间模块

* Python 时间模块常用类
    - datetime.date
    - datetime.time
    - datetime.datetime
    - datetime.timedelta

* Python 时间类型
    - 时间戳
        + 获取时间戳
            ```
            time.time()
            ```
        + 时间戳 -> datetime 对象
            ```
            datetime.datetime.fromtimestamp(timestamp)
            ```
        + 时间戳 -> struct_time
            ```
            time.localtime(timestamp) 
            ```
        + 时间戳 -> 字符串
            ```
            datetime.datetime.fromtimestamp(timestamp).strftime('%Y-%m-%d %H:%M:%S')  
            ```
    - 字符串
        + 获取字符串
            ```
            '2016-12-28'
            ```
        + 字符串 -> datetime 对象
            ```
            datetime.datetime.strptime('2016-12-28', '%Y-%m-%d')
            ```
        + 字符串 -> 时间戳
            ```
            time.mktime(time.strptime('2016-12-28', '%Y-%m-%d %H:%M:%S'))
            ```
        + 字符串 -> struct_time
            ```
            time.strptime('2016-12-28', '%Y-%m-%d %H:%M:%S') 
            ```
    - 时间元组 struct_time
        + 获取 struct_time
            ```
            time.strptime('2016-12-28', '%Y-%m-%d %H:%M:%S') 
            ```
        + struct_time -> datetime 对象
            ```
            datetime.datetime.fromtimestamp(time.mktime(struct_time))
            ```
        + struct_time -> 时间戳
            ```
            time.mktime(struct_time)  
            ```
        + struct_time -> 字符串
            ```
            time.strftime('%Y-%m-%d %H:%M:%S', struct_time) 
            ```
    - datetime 对象
        + 获取 datetime 对象
            ```
            datetime.datetime(2016, 12, 28) 
            ```
        + datetime -> 时间戳
            ```
            time.mktime(datetime.datetime.timetuple()) 
            ```
        + datetime -> struct_time
            ```
            datetime.datetime.timetuple()  
            ```
        + datetime -> 字符串
            ```
            datetime.datetime.strftime()  
            ```
* Python 时间运算 
    - 加减
        ```
        import datetime
        now = datetime.datetime.now()
        date = now + datetime.timedelta(days = 1)
        ```
