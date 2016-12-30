# pandas 开发笔记

* dataframe 操作
    - dataframe 删除某些列
        ```
        ticket_mc_data.drop([
            'user_name',
            'group_name',
            'operate_time',
            'operator',
        ], axis=1, inplace=True)
        ```
    - dataframe 给列重命名
        ```
        first_response_data_date_group_rtx_sum.rename(columns={
                'is_this_queue_first_response':'first_response_count',
            }, inplace=True)
        ```
