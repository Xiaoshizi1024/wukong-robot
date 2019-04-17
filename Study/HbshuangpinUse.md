# Linux 如何使用fcitx输入法 小鹤双拼  

參考資料： 
- https://jingyan.baidu.com/article/1e5468f9288a06484861b767.html 
  
  
## 安裝流程 
 
 1. 卸載原有輸入法   
 2. 安裝 fcitx輸入法   `sudo apt-get install fcitx fcitx-pinyin`
 3. 配置输入法  
     -  点击 开始 ->> 首选向 ->> Fcitx配置   
  4. 重启输入法 
    - 点击开始 ->>  附件 ->> 任务管理器->> 找到 fc 文件，终止， 重启  
    
    
     
###  问题 
  
-   [Ubuntu安装Fcitx以及Fcitx输入中文不显示候选词框的解决办法](https://blog.csdn.net/qq_21397217/article/details/52447263)
      - 命令：`$ sudo apt remove fcitx-module-kimpanel`
      
      
``` 
pi@raspberrypi:~ $ sudo apt remove fcitx-module-kimpanel
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
下列软件包是自动安装的并且现在不需要了：
  libqt5quickwidgets5 realpath
使用'sudo apt autoremove'来卸载它(它们)。
下列软件包将被【卸载】：
  fcitx-module-kimpanel fcitx-ui-qimpanel
升级了 0 个软件包，新安装了 0 个软件包，要卸载 2 个软件包，有 86 个软件包未被升级。
解压缩后将会空出 690 kB 的空间。
您希望继续执行吗？ [Y/n] y
(正在读取数据库 ... 系统当前共安装有 147928 个文件和目录。)
正在卸载 fcitx-ui-qimpanel (2.1.2-2) ...
正在卸载 fcitx-module-kimpanel (1:4.2.9.1-6) ...
正在处理用于 mime-support (3.60) 的触发器 ...
正在处理用于 desktop-file-utils (0.23-1) 的触发器 ...
正在处理用于 gnome-menus (3.13.3-9) 的触发器 ...

```

 
  

命令：  

`sudo apt-get install fcitx fcitx-pinyin`    


190416 18：24   小狮子 
