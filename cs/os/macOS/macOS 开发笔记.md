# macOS 开发笔记


* **~/.bashrc 的设置**，新开一个终端都要 source 一下才起作用
    * 原因
        - 在 Linux 下，当用户登录到一个图形界面，然后打开一个终端 terminal，那些 shell 是 **non-login shell**。
        - **non-login shell** 读取~/.bashrc 来应用新的环境变量。
        - 在 OS X 登录的时候，并没有运行着一个 shell，所以，在运行 Terminal.app 的时候，其实那是一个 **login shell**。
        - **login shell** 读取 / etc/profile 和~/.bash_profile 来应用新的环境变量。
    * 解决方法
        新建了 **.bash_profile** 加载一次 .bashrc
        ```
        if ["${BASH-no}" != "no" ]; then  
            [-r ~/.bashrc] && . ~/.bashrc  
        fi  
        ```
