# macOS 学习笔记

* 修改终端提示符
    - 修改共享名
        ```bash
        sudo scutil --set ComputerName newName
        ```
    - 修改主机名
        ```bash
        sudo scutil --set HostName newName
        ```

* 隐藏/显示文件夹
    - 隐藏
        ```
        chflags hidden xxx
        ```
    - 显示
        ```
        chflags nohidden xxx
        ```
