# pandas 开发笔记

* dataframe 删除某些列
    ```
    ticket_mc_data.drop([
        'user_name',
        'group_name',
        'operate_time',
        'operator',
    ], axis=1, inplace=True)
    ```
