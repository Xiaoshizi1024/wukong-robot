# 树莓派安装nodejs 

## 背景 
为了获得 获得 ` _snowboydetect.so `      
安装之后的下个行动

https://github.com/wzpan/snowboy#precompiled-node-module

## 步骤 
1. 查看系统内核 
2. 下载 nodejs文件
3. 解压安装 nodejs文件
4. 将nodejs&npm配置成全局
5. 重启？  


参考资料：
- Linux系统中常见查看自己系统版本和内核命令  https://blog.csdn.net/fengye_wuqi/article/details/80348844	  
- 官方下载链接 https://nodejs.org/en/download/  
- Linux 上安装 Node.js


  安装步骤   http://www.runoob.com/nodejs/nodejs-install-setup.html


实际运行代码：
```
uname -r  
wget https://nodejs.org/dist/v10.15.3/node-v10.15.3-linux-armv7l.tar.xz
  
tar xf node-v10.15.3-linux-armv7l.tar.xz
     
cd node-v10.15.3-linux-armv7l 
./bin/node -v 
``` 
反馈： 
v10.15.3  


运行
``` 
 sudo ln -s /usr/software/nodejs/bin/npm   /usr/local/bin/ 
sudo ln -s /usr/software/nodejs/bin/node   /usr/local/bin/ 
```  

重启来检测是否安装成功 
`reboot`  
## 自检 
查看是否完成配置，使node &npm全局可用 

发现 node全局可用， npm完全不能用... 

参考https://blog.csdn.net/xiongtm/article/details/77620005  
在显示 npm版本， 但是全局中还是不可查看版本， 并且在这个文件中还是不可用... 

```
pi@raspberrypi:~ $ ls
aawukong-robot  MagPi     Public           swig-3.0.10.tar.gz
Desktop         Music     snowboy          Templates
Documents       node      snowboy.tar.bz2  Videos
Downloads       Pictures  swig-3.0.10      wukong-robot
pi@raspberrypi:~ $ cd node
pi@raspberrypi:~/node $ cd bin
pi@raspberrypi:~/node/bin $ ./node -v
v10.15.3
pi@raspberrypi:~/node/bin $ ./npm -v
6.4.1
pi@raspberrypi:~/node/bin $ sudo ln -s /usr/software/nodejs/bin/npm   /usr/local/bin/ 
ln: 无法创建符号链接'/usr/local/bin/npm': 文件已存在
pi@raspberrypi:~/node/bin $ npm
bash: npm: 未找到命令
```   
尝试着用重启  

不可用，尝试着卸载重装试试。。。  
  
  ```
  pi@raspberrypi:// $ sudo apt-get purge --auto-remove nodejs
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
下列软件包将被【卸载】：
  erlang-base* erlang-crypto* erlang-syntax-tools* fonts-lato* libboost-thread1.62.0* libc-ares2* libhttp-parser2.8* libqt5quickwidgets5* libqt5scintilla2-12v5*
  libqt5scintilla2-l10n* libqwt-qt5-6* libruby2.3* libscsynth1* libsctp1* libuv1* nodejs* nodejs-doc* nodered* rake* realpath* ruby* ruby-did-you-mean* ruby-minitest*
  ruby-net-telnet* ruby-power-assert* ruby-test-unit* ruby2.3* rubygems-integration*
升级了 0 个软件包，新安装了 0 个软件包，要卸载 28 个软件包，有 81 个软件包未被升级。
解压缩后将会空出 131 MB 的空间。
您希望继续执行吗？ [Y/n] y
(正在读取数据库 ... 系统当前共安装有 134198 个文件和目录。)
正在卸载 erlang-crypto (1:19.2.1+dfsg-2+deb9u1) ...
正在卸载 erlang-syntax-tools (1:19.2.1+dfsg-2+deb9u1) ...
正在卸载 erlang-base (1:19.2.1+dfsg-2+deb9u1) ...
Searching for services which depend on erlang and should be stopped...none found.
Killing epmd...it is not running.
正在卸载 fonts-lato (2.0-1) ...
正在卸载 libscsynth1 (1:3.7.0~repack-4) ...
正在卸载 libboost-thread1.62.0:armhf (1.62.0+dfsg-4) ...
正在卸载 nodered (0.19.4) ...
正在卸载 nodejs (8.11.1~dfsg-2~bpo9+1) ...
正在卸载 libc-ares2:armhf (1.14.0-1~bpo9+1) ...
正在卸载 libhttp-parser2.8:armhf (2.8.1-1~bpo9+1) ...
正在卸载 libqt5quickwidgets5:armhf (5.7.1-2+rpi1) ...
正在卸载 libqt5scintilla2-12v5 (2.9.3+dfsg-4) ...
正在卸载 libqt5scintilla2-l10n (2.9.3+dfsg-4) ...
正在卸载 libqwt-qt5-6 (6.1.2-6) ...
正在卸载 libsctp1:armhf (1.0.17+dfsg-1) ...
正在卸载 libuv1:armhf (1.18.0-3~bpo9+1) ...
正在卸载 nodejs-doc (8.11.1~dfsg-2~bpo9+1) ...
正在卸载 realpath (8.26-3) ...
正在卸载 ruby (1:2.3.3) ...
正在卸载 ruby2.3 (2.3.3-1+deb9u3+rpi1) ...
正在卸载 libruby2.3:armhf (2.3.3-1+deb9u3+rpi1) ...
正在卸载 rake (10.5.0-2) ...
正在卸载 ruby-did-you-mean (1.0.0-2) ...
正在卸载 ruby-minitest (5.9.0-1) ...
正在卸载 ruby-net-telnet (0.1.1-2) ...
正在卸载 ruby-test-unit (3.1.7-2) ...
正在卸载 ruby-power-assert (0.3.0-1) ...
正在卸载 rubygems-integration (1.11) ...
正在处理用于 mime-support (3.60) 的触发器 ...
正在处理用于 desktop-file-utils (0.23-1) 的触发器 ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...
正在处理用于 man-db (2.7.6.1-2) 的触发器 ...
正在处理用于 gnome-menus (3.13.3-9) 的触发器 ...
正在处理用于 hicolor-icon-theme (0.15-1) 的触发器 ...
正在处理用于 fontconfig (2.11.0-6.7) 的触发器 ...
(正在读取数据库 ... 系统当前共安装有 124968 个文件和目录。)
正在清除 erlang-base (1:19.2.1+dfsg-2+deb9u1) 的配置文件 ...
正在清除 nodered (0.19.4) 的配置文件 ...
```     

参考 [在树莓派上安装最新版本的NodeJS
](https://juejin.im/post/5ad0350d518825364001d7b1) 
尝试运用`apt-get`的方式来安装 ,发现问题   

```  
pi@raspberrypi:~ $ sudo apt-get install nodejs npm
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
nodejs 已经是最新版 (8.11.1~dfsg-2~bpo9+1)。
有一些软件包无法被安装。如果您用的是 unstable 发行版，这也许是
因为系统无法达到您要求的状态造成的。该版本中可能会有一些您需要的软件
包尚未被创建或是它们已被从新到(Incoming)目录移出。
下列信息可能会对解决问题有所帮助：

下列软件包有未满足的依赖关系：
 npm : 依赖: node-gyp (>= 0.10.9) 但是它将不会被安装
E: 无法修正错误，因为您要求某些软件包保持现状，就是它们破坏了软件包间的依赖关系。

```   


尝试-     

```
pi@raspberrypi:~ $ node -v
v8.11.1
pi@raspberrypi:~ $ npm -b
bash: npm: 未找到命令
pi@raspberrypi:~ $ sudo apt-get install  npm -y
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
有一些软件包无法被安装。如果您用的是 unstable 发行版，这也许是
因为系统无法达到您要求的状态造成的。该版本中可能会有一些您需要的软件
包尚未被创建或是它们已被从新到(Incoming)目录移出。
下列信息可能会对解决问题有所帮助：

下列软件包有未满足的依赖关系：
 npm : 依赖: node-gyp (>= 0.10.9) 但是它将不会被安装
E: 无法修正错误，因为您要求某些软件包保持现状，就是它们破坏了软件包间的依赖关系。
pi@raspberrypi:~ $ sudo apt-get install  nnod-gyp
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
E: 无法定位软件包 nnod-gyp
pi@raspberrypi:~ $ sudo apt-get install  node-gyp
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
有一些软件包无法被安装。如果您用的是 unstable 发行版，这也许是
因为系统无法达到您要求的状态造成的。该版本中可能会有一些您需要的软件
包尚未被创建或是它们已被从新到(Incoming)目录移出。
下列信息可能会对解决问题有所帮助：

下列软件包有未满足的依赖关系：
 node-gyp : 依赖: nodejs-dev 但是它将不会被安装
E: 无法修正错误，因为您要求某些软件包保持现状，就是它们破坏了软件包间的依赖关系。
pi@raspberrypi:~ $ sudo apt-get install  nodejs-dev
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
有一些软件包无法被安装。如果您用的是 unstable 发行版，这也许是
因为系统无法达到您要求的状态造成的。该版本中可能会有一些您需要的软件
包尚未被创建或是它们已被从新到(Incoming)目录移出。
下列信息可能会对解决问题有所帮助：

下列软件包有未满足的依赖关系：
 nodejs-dev : 依赖: libc-ares-dev (>= 1.7.5) 但是它将不会被安装
              依赖: nodejs (= 0.10.29~dfsg-2) 但是 8.11.1~dfsg-2~bpo9+1 正要被安装
E: 无法修正错误，因为您要求某些软件包保持现状，就是它们破坏了软件包间的依赖关系。
```

卸载 armV7版本的 nodejs, 尝试安装 Linux版本的... 
```
pi@raspberrypi:~ $ sudo apt-get remove nodejs npm
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
软件包 npm 未安装，所以不会被卸载
下列软件包是自动安装的并且现在不需要了：
  libc-ares2 libhttp-parser2.8 libuv1 nodejs-doc
使用'sudo apt autoremove'来卸载它(它们)。
下列软件包将被【卸载】：
  nodejs
升级了 0 个软件包，新安装了 0 个软件包，要卸载 1 个软件包，有 0 个软件包未被升级。
解压缩后将会空出 15.8 MB 的空间。
您希望继续执行吗？ [Y/n] y
(正在读取数据库 ... 系统当前共安装有 125178 个文件和目录。)
正在卸载 nodejs (8.11.1~dfsg-2~bpo9+1) ...
正在处理用于 man-db (2.7.6.1-2) 的触发器 ...

```  
运行代码 

从官网以及图形化界面下载 node-v10.15.3-linux-x64.tar.xz

``` 
tar xf node-v10.15.3-linux-x64.tar.xz
$ cd node-v10.15.3-linux-x64
~/node-v10.15.3-linux-x64 $ ./bin/node -v
``` 
细节反馈
```
pi@raspberrypi:~ $ tar xf node-v10.15.3-linux-x64.tar.xz
pi@raspberrypi:~ $ cd node-v10.15.3-linux-x64
pi@raspberrypi:~/node-v10.15.3-linux-x64 $ ./bin/node -v
bash: ./bin/node: 无法执行二进制文件: 可执行文件格式错误
```
尝试重启在安装  
`reboot`  

重复上面指令无效 ...  

尝试着用其他方式安装...  

node 跟npm完全不可用是否还要卸载？把本地的安装包跟文件夹删除 

