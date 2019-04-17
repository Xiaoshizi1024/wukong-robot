# PyAudio 安装没有portaudio.h文件？

## 背景    

在利用wukong项目时， 需要安装  PyAudio ,但是用官方提供的方法出现了错误  

```  
fatal error: portaudio.h: 没有那个文件或目录   
error: command 'arm-linux-gnueabihf-gcc' failed with exit status 1   
```   

## 行动  

通过 `pip list` 发现电脑上已经有 `PyAudio`的最新版&通过官方看系统内也有最新的了，那么为什么还能出错了...  

官网： https://pypi.org/project/PyAudio/
  
 

``` 
pi@raspberrypi:~ $ pip list
DEPRECATION: The default format will switch to columns in the future. You can use --format=(legacy|columns) (or define a format=(legacy|columns) in your pip.conf under the [list] section) to disable this warning.
automationhat (0.1.0)
blinker (1.3)
blinkt (0.1.2)
buttonshim (0.0.2)
Cap1xxx (0.1.3)
chardet (2.3.0)
click (6.6)
colorama (0.3.7)
colorzero (1.1)
cryptography (1.7.1)
drumhat (0.1.0)
enum34 (1.1.6)
envirophat (1.0.0)
ExplorerHAT (0.4.2)
Flask (0.12.1)
fourletterphat (0.1.0)
gpiozero (1.5.0)
idna (2.2)
ipaddress (1.0.17)
itsdangerous (0.24)
Jinja2 (2.8)
keyring (10.1)
keyrings.alt (1.3)
MarkupSafe (0.23)
mcpi (0.1.1)
microdotphat (0.2.1)
mote (0.0.4)
motephat (0.0.2)
numpy (1.12.1)
oauthlib (2.0.1)
pantilthat (0.0.7)
phatbeat (0.1.1)
pianohat (0.1.0)
picamera (1.13)
picraft (1.0)
piglow (1.2.4)
pigpio (1.38)
Pillow (4.0.0)
pip (9.0.1)
pyasn1 (0.1.9)
PyAudio (0.2.11)
pycrypto (2.6.1)
pygame (1.9.3)
pygobject (3.22.0)
pyinotify (0.9.6)
PyJWT (1.4.2)
pyOpenSSL (16.2.0)
pyserial (3.2.1)
pyxdg (0.25)
rainbowhat (0.1.0)
requests (2.12.4)
requests-oauthlib (0.7.0)
RPi.GPIO (0.6.5)
RTIMULib (7.2.1)
scrollphat (0.0.7)
scrollphathd (1.2.1)
SecretStorage (2.3.1)
sense-emu (1.1)
sense-hat (2.2.0)
setuptools (33.1.1)
simplejson (3.10.0)
six (1.12.0)
skywriter (0.0.7)
sn3218 (1.2.7)
spidev (3.3)
touchphat (0.0.1)
twython (3.4.0)
unicornhathd (0.0.4)
urllib3 (1.19.1)
Werkzeug (0.11.15)
wheel (0.29.0)
pi@raspberrypi:~ $ python3 -v
```     

在一个文档中说
> 对于Ubuntu/Debian而言： 
> 我们使用包管理工具apt来安装： 
> sudo apt-get install python-pyaudio python3-pyaudio 
> 如果最新版的pyaudio不能获得的话我们可以使用pip来进行安装： 
> pip install pyaudio 
> 注意： 
> pip会下载pyaudio的源码并且为你的系统构建。所以请确保你提前安装了portaudio库开发包（portaudio19-dev）以及python开发包（python-all-dev）。 
> 为了使pyaudio独立于系统的包，请考虑在virtualenv中安装PyAudio。
> --------------------- 
> 作者：顶杰 
> 来源：CSDN 
>  原文：https://blog.csdn.net/qq_23729557/article/details/78956602 
> 版权声明：本文为博主原创文章，转载请附上博文链接！  
> 原文： http://people.csail.mit.edu/hubert/pyaudio/#downloads     
 
 
 基于该文档进行尝试  
 运行代码：`sudo apt-get install portaudio19-dev python-all-dev python3-all-dev` 
 
然后在运行：`pip3 install pyaudio`     

问题已解决...    



### 详细代码记录  

 运行代码：`sudo apt-get install portaudio19-dev python-all-dev python3-all-dev`   
 
``` 
pi@raspberrypi:~ $ sudo apt-get install portaudio19-dev python-all-dev python3-all-dev
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
python-all-dev 已经是最新版 (2.7.13-2)。
python-all-dev 已设置为手动安装。
下列软件包是自动安装的并且现在不需要了：
  erlang-base erlang-crypto erlang-syntax-tools fonts-lato
  libboost-thread1.62.0 libqt5quickwidgets5 libqt5scintilla2-12v5
  libqt5scintilla2-l10n libqwt-qt5-6 libruby2.3 libscsynth1 libsctp1 rake
  realpath ruby ruby-did-you-mean ruby-minitest ruby-net-telnet
  ruby-power-assert ruby-test-unit ruby2.3 rubygems-integration
使用'sudo apt autoremove'来卸载它(它们)。
将会同时安装下列软件：
  jackd1 libasound2-dev libjack-dev libjack0 libportaudiocpp0
  libpython3-all-dev libzita-alsa-pcmi0 libzita-resampler1 python3-all
  uuid-dev
建议安装：
  jack-tools meterbridge libasound2-doc portaudio19-doc
推荐安装：
  qjackctl
下列软件包将被【卸载】：
  jackd jackd2 libjack-jackd2-0 qjackctl sonic-pi supercollider-server
下列【新】软件包将被安装：
  jackd1 libasound2-dev libjack-dev libjack0 libportaudiocpp0
  libpython3-all-dev libzita-alsa-pcmi0 libzita-resampler1 portaudio19-dev
  python3-all python3-all-dev uuid-dev
升级了 0 个软件包，新安装了 12 个软件包，要卸载 6 个软件包，有 85 个软件包未被升级。
需要下载 985 kB 的归档。
解压缩后将会空出 2,313 kB 的空间。
您希望继续执行吗？ [Y/n] y
获取:1 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libjack0 armhf 1:0.125.0-2 [50.4 kB]
获取:2 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libzita-alsa-pcmi0 armhf 0.2.0-4 [11.7 kB]
获取:3 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libzita-resampler1 armhf 1.6.0-2 [10.3 kB]
获取:4 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf jackd1 armhf 1:0.125.0-2 [237 kB]
获取:5 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf uuid-dev armhf 2.29.2-1+deb9u1 [83.2 kB]
获取:6 http://archive.raspberrypi.org/debian stretch/main armhf libasound2-dev armhf 1.1.3-5+rpt4 [262 kB]
获取:7 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libjack-dev armhf 1:0.125.0-2 [211 kB]
获取:8 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libportaudiocpp0 armhf 19.6.0-1 [16.8 kB]
获取:9 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libpython3-all-dev armhf 3.5.3-1 [960 B]
获取:10 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf portaudio19-dev armhf 19.6.0-1 [98.6 kB]
获取:11 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf python3-all armhf 3.5.3-1 [934 B]
获取:12 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf python3-all-dev armhf 3.5.3-1 [962 B]
已下载 985 kB，耗时 3秒 (286 kB/s)                                             
正在预设定软件包 ...
(正在读取数据库 ... 系统当前共安装有 148276 个文件和目录。)
正在卸载 sonic-pi (1:3.0.1+1) ...
正在卸载 supercollider-server (1:3.7.0~repack-4) ...
正在卸载 qjackctl (0.4.4-1) ...
正在卸载 jackd (5) ...
正在卸载 jackd2 (1.9.10+20150825git1ed50c92~dfsg-5) ...
dpkg: libjack-jackd2-0:armhf：有依赖问题，但是如您所愿，将继续卸载：
 libfluidsynth1:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。
 timidity 依赖于 libjack-jackd2-0 (>= 1.9.5~dfsg-14) | libjack-0.116；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.116。
  提供了 libjack-0.116 的软件包 libjack-jackd2-0:armhf 即将被删除。
 gstreamer1.0-plugins-good:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libscsynth1 依赖于 libjack-jackd2-0 (>= 1.9.5~dfsg-14) | libjack-0.116；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.116。
  提供了 libjack-0.116 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libasound2-plugins:armhf 依赖于 libjack-jackd2-0 (>= 1.9.5~dfsg-14) | libjack-0.116；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.116。
  提供了 libjack-0.116 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libportaudio2:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libavdevice57:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。
 timidity 依赖于 libjack-jackd2-0 (>= 1.9.5~dfsg-14) | libjack-0.116；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.116。
  提供了 libjack-0.116 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libscsynth1 依赖于 libjack-jackd2-0 (>= 1.9.5~dfsg-14) | libjack-0.116；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.116。
  提供了 libjack-0.116 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libasound2-plugins:armhf 依赖于 libjack-jackd2-0 (>= 1.9.5~dfsg-14) | libjack-0.116；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.116。
  提供了 libjack-0.116 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libfluidsynth1:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。
 gstreamer1.0-plugins-good:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libportaudio2:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。
 libavdevice57:armhf 依赖于 libjack-jackd2-0 (>= 1.9.10+20150825) | libjack-0.125；然而：
  即将删除 libjack-jackd2-0:armhf。
  未安装软件包 libjack-0.125。
  提供了 libjack-0.125 的软件包 libjack-jackd2-0:armhf 即将被删除。

正在卸载 libjack-jackd2-0:armhf (1.9.10+20150825git1ed50c92~dfsg-5) ...
正在选中未选择的软件包 libjack0:armhf。
(正在读取数据库 ... 系统当前共安装有 133692 个文件和目录。)
正准备解包 .../00-libjack0_1%3a0.125.0-2_armhf.deb  ...
正在解包 libjack0:armhf (1:0.125.0-2) ...
正在选中未选择的软件包 libzita-alsa-pcmi0:armhf。
正准备解包 .../01-libzita-alsa-pcmi0_0.2.0-4_armhf.deb  ...
正在解包 libzita-alsa-pcmi0:armhf (0.2.0-4) ...
正在选中未选择的软件包 libzita-resampler1:armhf。
正准备解包 .../02-libzita-resampler1_1.6.0-2_armhf.deb  ...
正在解包 libzita-resampler1:armhf (1.6.0-2) ...
正在选中未选择的软件包 jackd1。
正准备解包 .../03-jackd1_1%3a0.125.0-2_armhf.deb  ...
正在解包 jackd1 (1:0.125.0-2) ...
正在选中未选择的软件包 libasound2-dev:armhf。
正准备解包 .../04-libasound2-dev_1.1.3-5+rpt4_armhf.deb  ...
正在解包 libasound2-dev:armhf (1.1.3-5+rpt4) ...
正在选中未选择的软件包 uuid-dev:armhf。
正准备解包 .../05-uuid-dev_2.29.2-1+deb9u1_armhf.deb  ...
正在解包 uuid-dev:armhf (2.29.2-1+deb9u1) ...
正在选中未选择的软件包 libjack-dev。
正准备解包 .../06-libjack-dev_1%3a0.125.0-2_armhf.deb  ...
正在解包 libjack-dev (1:0.125.0-2) ...
正在选中未选择的软件包 libportaudiocpp0:armhf。
正准备解包 .../07-libportaudiocpp0_19.6.0-1_armhf.deb  ...
正在解包 libportaudiocpp0:armhf (19.6.0-1) ...
正在选中未选择的软件包 libpython3-all-dev:armhf。
正准备解包 .../08-libpython3-all-dev_3.5.3-1_armhf.deb  ...
正在解包 libpython3-all-dev:armhf (3.5.3-1) ...
正在选中未选择的软件包 portaudio19-dev:armhf。
正准备解包 .../09-portaudio19-dev_19.6.0-1_armhf.deb  ...
正在解包 portaudio19-dev:armhf (19.6.0-1) ...
正在选中未选择的软件包 python3-all。
正准备解包 .../10-python3-all_3.5.3-1_armhf.deb  ...
正在解包 python3-all (3.5.3-1) ...
正在选中未选择的软件包 python3-all-dev。
正准备解包 .../11-python3-all-dev_3.5.3-1_armhf.deb  ...
正在解包 python3-all-dev (3.5.3-1) ...
正在设置 libasound2-dev:armhf (1.1.3-5+rpt4) ...
正在设置 libportaudiocpp0:armhf (19.6.0-1) ...
正在设置 libjack0:armhf (1:0.125.0-2) ...
正在处理用于 mime-support (3.60) 的触发器 ...
正在处理用于 desktop-file-utils (0.23-1) 的触发器 ...
正在设置 uuid-dev:armhf (2.29.2-1+deb9u1) ...
正在设置 libzita-resampler1:armhf (1.6.0-2) ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...
正在设置 libpython3-all-dev:armhf (3.5.3-1) ...
正在设置 python3-all (3.5.3-1) ...
正在处理用于 man-db (2.7.6.1-2) 的触发器 ...
正在设置 libzita-alsa-pcmi0:armhf (0.2.0-4) ...
正在处理用于 gnome-menus (3.13.3-9) 的触发器 ...
正在处理用于 hicolor-icon-theme (0.15-1) 的触发器 ...
正在设置 libjack-dev (1:0.125.0-2) ...
正在设置 portaudio19-dev:armhf (19.6.0-1) ...
正在设置 python3-all-dev (3.5.3-1) ...
正在设置 jackd1 (1:0.125.0-2) ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...

```  

然后在运行：`pip3 install pyaudio`     

安装反馈： 
```  
pi@raspberrypi:~ $ pip3 install pyaudio
Collecting pyaudio
  Using cached https://files.pythonhosted.org/packages/ab/42/b4f04721c5c5bfc196ce156b3c768998ef8c0ae3654ed29ea5020c749a6b/PyAudio-0.2.11.tar.gz
Building wheels for collected packages: pyaudio
  Running setup.py bdist_wheel for pyaudio ... done
  Stored in directory: /home/pi/.cache/pip/wheels/f4/a8/a4/292214166c2917890f85b2f72a8e5f13e1ffa527c4200dcede
Successfully built pyaudio
Installing collected packages: pyaudio
Successfully installed pyaudio-0.2.11
  
```


## 参考

参考资料：  
- 安装pyaudio找不到portaudio.h的问题（  https://blog.csdn.net/qq_23729557/article/details/78956602）     
	- sudo apt-get install portaudio19-dev python-all-dev python3-all-dev
	- pip install pyaudio
- 记录：针对这个问题，本来以为是PIP安装的时候下载的包错了，后来对着文件名进行搜索了下，原来是pyaudio的运行需要依赖于portaudio这个库。 
    - https://blog.csdn.net/sparkexpert/article/details/56495891 
    
-  安装pyaudio出现错误：没有portaudio.h （已解决）  https://blog.csdn.net/qq_34638161/article/details/80383914  


190416   小狮子  发布并解决问题 
