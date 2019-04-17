# 安装悟空环境  

## 资源  

- https://wukong.hahack.com/#/install?id=%E6%96%B9%E5%BC%8F%E4%BA%8C%EF%BC%9A%E6%89%8B%E5%8A%A8%E5%AE%89%E8%A3%85  

## 安装流程   


### 安装问题

1. 错误   （问题已解决）
fatal error: portaudio.h: 没有那个文件或目录   
error: command 'arm-linux-gnueabihf-gcc' failed with exit status 1  

通过安装 运行代码：`sudo apt-get install portaudio19-dev python-all-dev python3-all-dev` 
以及`pip3 install pyaudio`  解决问题  
更多参考 ：Issue -PyAudio??  


参考资料：  
- 安装pyaudio找不到portaudio.h的问题（https://blog.csdn.net/qq_23729557/article/details/78956602）     
	- sudo apt-get install portaudio19-dev python-all-dev python3-all-dev
	- pip install pyaudio
- 记录：针对这个问题，本来以为是PIP安装的时候下载的包错了，后来对着文件名进行搜索了下，原来是pyaudio的运行需要依赖于portaudio这个库。 
    - https://blog.csdn.net/sparkexpert/article/details/56495891 
    
-  安装pyaudio出现错误：没有portaudio.h （已解决）  https://blog.csdn.net/qq_34638161/article/details/80383914
  
  
  2. 安装错误    
  
  运行：`pip3 install -r requirements.txt`错误     
  
  
  再次尝试发现新问题
  ```
Cannot uninstall 'PyYAML'. It is a distutils installed project and thus we cannot accurately determine which files belong to it which would lead to only a partial uninstall.
  ``` 
  
翻译： 不能卸载“PyYAML”。这是一个安装了distutils的项目，因此我们不能准确地确定哪些文件属于它，这只会导致部分卸载。



  
  ```  
  pi@raspberrypi:~ $ cd /home/pi
pi@raspberrypi:~ $ ls
aawukong-robot  Documents  MagPi  Pictures  Templates  wukong-robot
Desktop         Downloads  Music  Public    Videos
pi@raspberrypi:~ $ cd wukong-robot
pi@raspberrypi:~/wukong-robot $ pip3 install -r requirements.txt
Collecting pyyaml>=4.2b1 (from -r requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/9f/2c/9417b5c774792634834e730932745bc09a7d36754ca00acf1ccd1ac2594d/PyYAML-5.1.tar.gz (274kB)
    100% |████████████████████████████████| 276kB 30kB/s 
Collecting requests==2.21.0 (from -r requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/7d/e3/20f3d364d6c8e5d2353c72a67778eb189176f08e873c9900e10c0287b84b/requests-2.21.0-py2.py3-none-any.whl (57kB)
    100% |████████████████████████████████| 61kB 16kB/s 
Collecting baidu-aip==2.0.0.1 (from -r requirements.txt (line 3))
  Downloading https://www.piwheels.org/simple/baidu-aip/baidu_aip-2.0.0.1-py3-none-any.whl
Collecting pydub==0.23.1 (from -r requirements.txt (line 4))
  Downloading https://files.pythonhosted.org/packages/79/db/eaf620b73a1eec3c8c6f8f5b0b236a50f9da88ad57802154b7ba7664d0b8/pydub-0.23.1-py2.py3-none-any.whl
Collecting python-dateutil==2.7.5 (from -r requirements.txt (line 5))
  Downloading https://files.pythonhosted.org/packages/74/68/d87d9b36af36f44254a8d512cbfc48369103a3b9e474be9bdfe536abfc45/python_dateutil-2.7.5-py2.py3-none-any.whl (225kB)
    100% |████████████████████████████████| 235kB 12kB/s 
Collecting watchdog==0.9.0 (from -r requirements.txt (line 6))
  Downloading https://www.piwheels.org/simple/watchdog/watchdog-0.9.0-py3-none-any.whl (67kB)
    100% |████████████████████████████████| 71kB 104kB/s 
Collecting pytz==2018.9 (from -r requirements.txt (line 7))
  Downloading https://files.pythonhosted.org/packages/61/28/1d3920e4d1d50b19bc5d24398a7cd85cc7b9a75a490570d5a30c57622d34/pytz-2018.9-py2.py3-none-any.whl (510kB)
    100% |████████████████████████████████| 512kB 11kB/s 
Collecting fire==0.1.3 (from -r requirements.txt (line 8))
  Downloading https://www.piwheels.org/simple/fire/fire-0.1.3-py2.py3-none-any.whl (50kB)
    100% |████████████████████████████████| 51kB 77kB/s 
Collecting tornado==5.1.1 (from -r requirements.txt (line 9))
  Downloading https://www.piwheels.org/simple/tornado/tornado-5.1.1-cp35-cp35m-linux_armv7l.whl (462kB)
    100% |████████████████████████████████| 471kB 122kB/s 
Collecting markdown==3.0.1 (from -r requirements.txt (line 10))
  Downloading https://files.pythonhosted.org/packages/7a/6b/5600647404ba15545ec37d2f7f58844d690baf2f81f3a60b862e48f29287/Markdown-3.0.1-py2.py3-none-any.whl (89kB)
    100% |████████████████████████████████| 92kB 12kB/s 
Collecting semver==2.8.1 (from -r requirements.txt (line 11))
  Downloading https://files.pythonhosted.org/packages/21/18/a0de8cda637ba3efee1b3617ded00601507ce15bd70a39399740e0fd415f/semver-2.8.1-py2.py3-none-any.whl
Collecting chardet<3.1.0,>=3.0.2 (from requests==2.21.0->-r requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/bc/a9/01ffebfb562e4274b6487b4bb1ddec7ca55ec7510b22e4c51f14098443b8/chardet-3.0.4-py2.py3-none-any.whl (133kB)
    100% |████████████████████████████████| 143kB 22kB/s 
Collecting idna<2.9,>=2.5 (from requests==2.21.0->-r requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/14/2c/cd551d81dbe15200be1cf41cd03869a46fe7226e7450af7a6545bfc474c9/idna-2.8-py2.py3-none-any.whl (58kB)
    100% |████████████████████████████████| 61kB 22kB/s 
Collecting certifi>=2017.4.17 (from requests==2.21.0->-r requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/60/75/f692a584e85b7eaba0e03827b3d51f45f571c2e793dd731e598828d380aa/certifi-2019.3.9-py2.py3-none-any.whl (158kB)
    100% |████████████████████████████████| 163kB 20kB/s 
Collecting urllib3<1.25,>=1.21.1 (from requests==2.21.0->-r requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/62/00/ee1d7de624db8ba7090d1226aebefab96a2c71cd5cfa7629d6ad3f61b79e/urllib3-1.24.1-py2.py3-none-any.whl (118kB)
    100% |████████████████████████████████| 122kB 17kB/s 
Collecting six>=1.5 (from python-dateutil==2.7.5->-r requirements.txt (line 5))
  Downloading https://files.pythonhosted.org/packages/73/fb/00a976f728d0d1fecfe898238ce23f502a721c0ac0ecfedb80e0d88c64e9/six-1.12.0-py2.py3-none-any.whl
Collecting pathtools>=0.1.1 (from watchdog==0.9.0->-r requirements.txt (line 6))
  Downloading https://www.piwheels.org/simple/pathtools/pathtools-0.1.2-py3-none-any.whl
Collecting argh>=0.24.1 (from watchdog==0.9.0->-r requirements.txt (line 6))
Exception:
Traceback (most recent call last):
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/connection.py", line 138, in _new_conn
    (self.host, self.port), self.timeout, **extra_kw)
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/util/connection.py", line 75, in create_connection
    for res in socket.getaddrinfo(host, port, family, socket.SOCK_STREAM):
  File "/usr/lib/python3.5/socket.py", line 733, in getaddrinfo
    for res in _socket.getaddrinfo(host, port, family, type, proto, flags):
socket.gaierror: [Errno -3] 域名解析暂时失败

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/connectionpool.py", line 594, in urlopen
    chunked=chunked)
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/connectionpool.py", line 350, in _make_request
    self._validate_conn(conn)
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/connectionpool.py", line 837, in _validate_conn
    conn.connect()
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/connection.py", line 281, in connect
    conn = self._new_conn()
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/connection.py", line 147, in _new_conn
    self, "Failed to establish a new connection: %s" % e)
requests.packages.urllib3.exceptions.NewConnectionError: <requests.packages.urllib3.connection.VerifiedHTTPSConnection object at 0x74ace2d0>: Failed to establish a new connection: [Errno -3] 域名解析暂时失败

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/lib/python3/dist-packages/pip/basecommand.py", line 215, in main
    status = self.run(options, args)
  File "/usr/lib/python3/dist-packages/pip/commands/install.py", line 353, in run
    wb.build(autobuilding=True)
  File "/usr/lib/python3/dist-packages/pip/wheel.py", line 749, in build
    self.requirement_set.prepare_files(self.finder)
  File "/usr/lib/python3/dist-packages/pip/req/req_set.py", line 380, in prepare_files
    ignore_dependencies=self.ignore_dependencies))
  File "/usr/lib/python3/dist-packages/pip/req/req_set.py", line 554, in _prepare_file
    require_hashes
  File "/usr/lib/python3/dist-packages/pip/req/req_install.py", line 278, in populate_link
    self.link = finder.find_requirement(self, upgrade)
  File "/usr/lib/python3/dist-packages/pip/index.py", line 465, in find_requirement
    all_candidates = self.find_all_candidates(req.name)
  File "/usr/lib/python3/dist-packages/pip/index.py", line 423, in find_all_candidates
    for page in self._get_pages(url_locations, project_name):
  File "/usr/lib/python3/dist-packages/pip/index.py", line 568, in _get_pages
    page = self._get_page(location)
  File "/usr/lib/python3/dist-packages/pip/index.py", line 683, in _get_page
    return HTMLPage.get_page(link, session=self.session)
  File "/usr/lib/python3/dist-packages/pip/index.py", line 792, in get_page
    "Cache-Control": "max-age=600",
  File "/usr/share/python-wheels/requests-2.12.4-py2.py3-none-any.whl/requests/sessions.py", line 501, in get
    return self.request('GET', url, **kwargs)
  File "/usr/lib/python3/dist-packages/pip/download.py", line 386, in request
    return super(PipSession, self).request(method, url, *args, **kwargs)
  File "/usr/share/python-wheels/requests-2.12.4-py2.py3-none-any.whl/requests/sessions.py", line 488, in request
    resp = self.send(prep, **send_kwargs)
  File "/usr/share/python-wheels/requests-2.12.4-py2.py3-none-any.whl/requests/sessions.py", line 609, in send
    r = adapter.send(request, **kwargs)
  File "/usr/share/python-wheels/CacheControl-0.11.7-py2.py3-none-any.whl/cachecontrol/adapter.py", line 47, in send
    resp = super(CacheControlAdapter, self).send(request, **kw)
  File "/usr/share/python-wheels/requests-2.12.4-py2.py3-none-any.whl/requests/adapters.py", line 423, in send
    timeout=timeout
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/connectionpool.py", line 643, in urlopen
    _stacktrace=sys.exc_info()[2])
  File "/usr/share/python-wheels/urllib3-1.19.1-py2.py3-none-any.whl/urllib3/util/retry.py", line 315, in increment
    total -= 1
TypeError: unsupported operand type(s) for -=: 'Retry' and 'int'

  ```      
  
  3. 错误3  在安装 构建snowboy 
  
  背景 
还没有获得 ` _snowboydetect.so `   
上面的 

  
  
 
### 安装细节 

安装了  
- sox  sox 已经是最新版 (14.4.1-5+deb9u1) 
- ffmpeg 已经是最新版 (7:3.2.12-1~deb9u1+rpt1)。 

``` 
pi@raspberrypi:~ $ cd /home/pi/wukong
pi@raspberrypi:~ $ cd wukong-robot
pi@raspberrypi:~/wukong-robot $ sudo apt-get install python-pyaudio python3-pyaudio sox pulseaudio libsox-fmt-all ffmpeg
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
没有可用的软件包 sox，但是它被其它的软件包引用了。
这可能意味着这个缺失的软件包可能已被废弃，
或者只能在其他发布源中找到

没有可用的软件包 libsox-fmt-all，但是它被其它的软件包引用了。
这可能意味着这个缺失的软件包可能已被废弃，
或者只能在其他发布源中找到

没有可用的软件包 pulseaudio，但是它被其它的软件包引用了。
这可能意味着这个缺失的软件包可能已被废弃，
或者只能在其他发布源中找到

E: 无法定位软件包 python-pyaudio
E: 无法定位软件包 python3-pyaudio
E: 软件包 sox 没有可安装候选
E: 软件包 pulseaudio 没有可安装候选
E: 软件包 libsox-fmt-all 没有可安装候选 

pi@raspberrypi:~/wukong-robot $ sudo apt-get install sox
正在读取软件包列表... 完成
正在分析软件包的依赖关系树        
正在读取状态信息... 完成       
您也许需要运行“apt --fix-broken install”来修正上面的错误。
下列软件包有未满足的依赖关系：
 remarkable : 依赖: gir1.2-gtksource-3.0 但是它将不会被安装
              依赖: python3-markdown 但是它将不会被安装
              依赖: python3-bs4 但是它将不会被安装
              依赖: gir1.2-webkit-3.0 但是它将不会被安装
              依赖: yelp 但是它将不会被安装
              依赖: wkhtmltopdf 但是它将不会被安装
 sox : 依赖: libsox-fmt-alsa (= 14.4.1-5+deb9u1) 但是它将不会被安装 或
               libsox-fmt-ao (= 14.4.1-5+deb9u1) 但是它将不会被安装 或
               libsox-fmt-oss (= 14.4.1-5+deb9u1) 但是它将不会被安装 或
               libsox-fmt-pulse (= 14.4.1-5+deb9u1) 但是它将不会被安装
       依赖: libsox-fmt-base (= 14.4.1-5+deb9u1) 但是它将不会被安装
       依赖: libsox2 (= 14.4.1-5+deb9u1) 但是它将不会被安装
E: 有未能满足的依赖关系。请尝试不指明软件包的名字来运行“apt --fix-broken install”(也可以指定一个解决办法)。
pi@raspberrypi:~/wukong-robot $ sudo apt-get install sox
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
下列软件包是自动安装的并且现在不需要了：
  realpath
使用'sudo apt autoremove'来卸载它(它们)。
将会同时安装下列软件：
  libopencore-amrnb0 libopencore-amrwb0 libsox-fmt-alsa libsox-fmt-base libsox2
建议安装：
  libsox-fmt-all
下列【新】软件包将被安装：
  libopencore-amrnb0 libopencore-amrwb0 libsox-fmt-alsa libsox-fmt-base libsox2 sox
升级了 0 个软件包，新安装了 6 个软件包，要卸载 0 个软件包，有 86 个软件包未被升级。
需要下载 600 kB 的归档。
解压缩后会消耗 1,291 kB 的额外空间。
您希望继续执行吗？ [Y/n] y
获取:1 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libopencore-amrnb0 armhf 0.1.3-2.1 [80.4 kB]
获取:2 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libopencore-amrwb0 armhf 0.1.3-2.1 [42.0 kB]
获取:3 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox2 armhf 14.4.1-5+deb9u1 [231 kB]
获取:4 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox-fmt-alsa armhf 14.4.1-5+deb9u1 [46.9 kB]
获取:5 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox-fmt-base armhf 14.4.1-5+deb9u1 [64.6 kB]
获取:6 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf sox armhf 14.4.1-5+deb9u1 [135 kB]
已下载 600 kB，耗时 5秒 (114 kB/s)
正在选中未选择的软件包 libopencore-amrnb0:armhf。
(正在读取数据库 ... 系统当前共安装有 147864 个文件和目录。)
正准备解包 .../0-libopencore-amrnb0_0.1.3-2.1_armhf.deb  ...
正在解包 libopencore-amrnb0:armhf (0.1.3-2.1) ...
正在选中未选择的软件包 libopencore-amrwb0:armhf。
正准备解包 .../1-libopencore-amrwb0_0.1.3-2.1_armhf.deb  ...
正在解包 libopencore-amrwb0:armhf (0.1.3-2.1) ...
正在选中未选择的软件包 libsox2:armhf。
正准备解包 .../2-libsox2_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox2:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 libsox-fmt-alsa:armhf。
正准备解包 .../3-libsox-fmt-alsa_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox-fmt-alsa:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 libsox-fmt-base:armhf。
正准备解包 .../4-libsox-fmt-base_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox-fmt-base:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 sox。
正准备解包 .../5-sox_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 sox (14.4.1-5+deb9u1) ...
正在处理用于 mime-support (3.60) 的触发器 ...
正在设置 libsox2:armhf (14.4.1-5+deb9u1) ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...
正在设置 libopencore-amrnb0:armhf (0.1.3-2.1) ...
正在处理用于 man-db (2.7.6.1-2) 的触发器 ...
正在设置 libopencore-amrwb0:armhf (0.1.3-2.1) ...
正在设置 libsox-fmt-base:armhf (14.4.1-5+deb9u1) ...
正在设置 libsox-fmt-alsa:armhf (14.4.1-5+deb9u1) ...
正在设置 sox (14.4.1-5+deb9u1) ...
```    
 安装  
 
 
 ```
 pi@raspberrypi:~ $ sudo apt-get install python-pyaudio python3-pyaudio sox pulseaudio libsox-fmt-all ffmpeg
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
sox 已经是最新版 (14.4.1-5+deb9u1)。
ffmpeg 已经是最新版 (7:3.2.12-1~deb9u1+rpt1)。
ffmpeg 已设置为手动安装。
下列软件包是自动安装的并且现在不需要了：
  libqt5quickwidgets5 realpath
使用'sudo apt autoremove'来卸载它(它们)。
将会同时安装下列软件：
  libao-common libao4 libasound2-plugins libpulsedsp libsox-fmt-ao
  libsox-fmt-mp3 libsox-fmt-oss libsox-fmt-pulse pulseaudio-utils rtkit
建议安装：
  pavumeter pavucontrol paman paprefs python-pyaudio-doc
下列【新】软件包将被安装：
  libao-common libao4 libasound2-plugins libpulsedsp libsox-fmt-all
  libsox-fmt-ao libsox-fmt-mp3 libsox-fmt-oss libsox-fmt-pulse pulseaudio
  pulseaudio-utils python-pyaudio python3-pyaudio rtkit
升级了 0 个软件包，新安装了 14 个软件包，要卸载 0 个软件包，有 86 个软件包未被升级。
需要下载 1,581 kB 的归档。
解压缩后会消耗 7,088 kB 的额外空间。
您希望继续执行吗？ [Y/n] y
获取:1 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libao-common armhf 1.2.2-1 [11.3 kB]
获取:2 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libao4 armhf 1.2.2-1 [36.4 kB]
获取:3 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libasound2-plugins armhf 1.1.1-1 [72.9 kB]
获取:4 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libpulsedsp armhf 10.0-1+deb9u1 [52.0 kB]
获取:5 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox-fmt-ao armhf 14.4.1-5+deb9u1 [43.8 kB]
获取:6 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox-fmt-mp3 armhf 14.4.1-5+deb9u1 [52.2 kB]
获取:7 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox-fmt-oss armhf 14.4.1-5+deb9u1 [44.1 kB]
获取:8 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox-fmt-pulse armhf 14.4.1-5+deb9u1 [43.6 kB]
获取:9 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libsox-fmt-all armhf 14.4.1-5+deb9u1 [41.3 kB]
获取:10 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf pulseaudio-utils armhf 10.0-1+deb9u1 [82.8 kB]
获取:11 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf pulseaudio armhf 10.0-1+deb9u1 [1,020 kB]
获取:12 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf python-pyaudio armhf 0.2.11-1 [24.3 kB]
获取:13 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf python3-pyaudio armhf 0.2.11-1 [24.3 kB]
获取:14 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf rtkit armhf 0.11-4+deb9u1 [32.2 kB]
已下载 1,581 kB，耗时 3分 3秒 (8,628 B/s)                                      
正在选中未选择的软件包 libao-common。
(正在读取数据库 ... 系统当前共安装有 147890 个文件和目录。)
正准备解包 .../00-libao-common_1.2.2-1_armhf.deb  ...
正在解包 libao-common (1.2.2-1) ...
正在选中未选择的软件包 libao4。
正准备解包 .../01-libao4_1.2.2-1_armhf.deb  ...
正在解包 libao4 (1.2.2-1) ...
正在选中未选择的软件包 libasound2-plugins:armhf。
正准备解包 .../02-libasound2-plugins_1.1.1-1_armhf.deb  ...
正在解包 libasound2-plugins:armhf (1.1.1-1) ...
正在选中未选择的软件包 libpulsedsp:armhf。
正准备解包 .../03-libpulsedsp_10.0-1+deb9u1_armhf.deb  ...
正在解包 libpulsedsp:armhf (10.0-1+deb9u1) ...
正在选中未选择的软件包 libsox-fmt-ao:armhf。
正准备解包 .../04-libsox-fmt-ao_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox-fmt-ao:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 libsox-fmt-mp3:armhf。
正准备解包 .../05-libsox-fmt-mp3_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox-fmt-mp3:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 libsox-fmt-oss:armhf。
正准备解包 .../06-libsox-fmt-oss_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox-fmt-oss:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 libsox-fmt-pulse:armhf。
正准备解包 .../07-libsox-fmt-pulse_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox-fmt-pulse:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 libsox-fmt-all:armhf。
正准备解包 .../08-libsox-fmt-all_14.4.1-5+deb9u1_armhf.deb  ...
正在解包 libsox-fmt-all:armhf (14.4.1-5+deb9u1) ...
正在选中未选择的软件包 pulseaudio-utils。
正准备解包 .../09-pulseaudio-utils_10.0-1+deb9u1_armhf.deb  ...
正在解包 pulseaudio-utils (10.0-1+deb9u1) ...
正在选中未选择的软件包 pulseaudio。
正准备解包 .../10-pulseaudio_10.0-1+deb9u1_armhf.deb  ...
正在解包 pulseaudio (10.0-1+deb9u1) ...
正在选中未选择的软件包 python-pyaudio。
正准备解包 .../11-python-pyaudio_0.2.11-1_armhf.deb  ...
正在解包 python-pyaudio (0.2.11-1) ...
正在选中未选择的软件包 python3-pyaudio。
正准备解包 .../12-python3-pyaudio_0.2.11-1_armhf.deb  ...
正在解包 python3-pyaudio (0.2.11-1) ...
正在选中未选择的软件包 rtkit。
正准备解包 .../13-rtkit_0.11-4+deb9u1_armhf.deb  ...
正在解包 rtkit (0.11-4+deb9u1) ...
正在设置 libsox-fmt-pulse:armhf (14.4.1-5+deb9u1) ...
正在设置 libpulsedsp:armhf (10.0-1+deb9u1) ...
正在设置 pulseaudio-utils (10.0-1+deb9u1) ...
正在设置 libasound2-plugins:armhf (1.1.1-1) ...
正在设置 libao-common (1.2.2-1) ...
正在设置 libsox-fmt-oss:armhf (14.4.1-5+deb9u1) ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...
正在设置 rtkit (0.11-4+deb9u1) ...
Created symlink /etc/systemd/system/graphical.target.wants/rtkit-daemon.service → /lib/systemd/system/rtkit-daemon.service.
正在设置 python-pyaudio (0.2.11-1) ...
正在处理用于 man-db (2.7.6.1-2) 的触发器 ...
正在处理用于 dbus (1.10.26-0+deb9u1) 的触发器 ...
正在设置 python3-pyaudio (0.2.11-1) ...
正在设置 libsox-fmt-mp3:armhf (14.4.1-5+deb9u1) ...
正在设置 pulseaudio (10.0-1+deb9u1) ...
正在将用户“pulse”加入到“audio”组中
正在设置 libao4 (1.2.2-1) ...
正在设置 libsox-fmt-ao:armhf (14.4.1-5+deb9u1) ...
正在设置 libsox-fmt-all:armhf (14.4.1-5+deb9u1) ...
正在处理用于 dbus (1.10.26-0+deb9u1) 的触发器 ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...
```     

安装  PyAudio  
```   	
pi@raspberrypi:~ $ pip3 install pyaudio
Collecting pyaudio
  Downloading https://files.pythonhosted.org/packages/ab/42/b4f04721c5c5bfc196ce156b3c768998ef8c0ae3654ed29ea5020c749a6b/PyAudio-0.2.11.tar.gz
Building wheels for collected packages: pyaudio
  Running setup.py bdist_wheel for pyaudio ... error
  Complete output from command /usr/bin/python3 -u -c "import setuptools, tokenize;__file__='/tmp/pip-build-kspcfq_x/pyaudio/setup.py';f=getattr(tokenize, 'open', open)(__file__);code=f.read().replace('\r\n', '\n');f.close();exec(compile(code, __file__, 'exec'))" bdist_wheel -d /tmp/tmp2c_b3di3pip-wheel- --python-tag cp35:
  running bdist_wheel
  running build
  running build_py
  creating build
  creating build/lib.linux-armv7l-3.5
  copying src/pyaudio.py -> build/lib.linux-armv7l-3.5
  running build_ext
  building '_portaudio' extension
  creating build/temp.linux-armv7l-3.5
  creating build/temp.linux-armv7l-3.5/src
  arm-linux-gnueabihf-gcc -pthread -DNDEBUG -g -fwrapv -O2 -Wall -Wstrict-prototypes -g -fdebug-prefix-map=/build/python3.5-6waWnr/python3.5-3.5.3=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -fPIC -I/usr/include/python3.5m -c src/_portaudiomodule.c -o build/temp.linux-armv7l-3.5/src/_portaudiomodule.o
  src/_portaudiomodule.c:29:23: fatal error: portaudio.h: 没有那个文件或目录
   #include "portaudio.h"
                         ^
  compilation terminated.
  error: command 'arm-linux-gnueabihf-gcc' failed with exit status 1
  
  ----------------------------------------
  Failed building wheel for pyaudio
  Running setup.py clean for pyaudio
Failed to build pyaudio
Installing collected packages: pyaudio
  Running setup.py install for pyaudio ... error
    Complete output from command /usr/bin/python3 -u -c "import setuptools, tokenize;__file__='/tmp/pip-build-kspcfq_x/pyaudio/setup.py';f=getattr(tokenize, 'open', open)(__file__);code=f.read().replace('\r\n', '\n');f.close();exec(compile(code, __file__, 'exec'))" install --record /tmp/pip-czs_6emc-record/install-record.txt --single-version-externally-managed --compile --user --prefix=:
    running install
    running build
    running build_py
    creating build
    creating build/lib.linux-armv7l-3.5
    copying src/pyaudio.py -> build/lib.linux-armv7l-3.5
    running build_ext
    building '_portaudio' extension
    creating build/temp.linux-armv7l-3.5
    creating build/temp.linux-armv7l-3.5/src
    arm-linux-gnueabihf-gcc -pthread -DNDEBUG -g -fwrapv -O2 -Wall -Wstrict-prototypes -g -fdebug-prefix-map=/build/python3.5-6waWnr/python3.5-3.5.3=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -fPIC -I/usr/include/python3.5m -c src/_portaudiomodule.c -o build/temp.linux-armv7l-3.5/src/_portaudiomodule.o
    src/_portaudiomodule.c:29:23: fatal error: portaudio.h: 没有那个文件或目录
     #include "portaudio.h"
                           ^
    compilation terminated.
    error: command 'arm-linux-gnueabihf-gcc' failed with exit status 1
    
    ----------------------------------------
Command "/usr/bin/python3 -u -c "import setuptools, tokenize;__file__='/tmp/pip-build-kspcfq_x/pyaudio/setup.py';f=getattr(tokenize, 'open', open)(__file__);code=f.read().replace('\r\n', '\n');f.close();exec(compile(code, __file__, 'exec'))" install --record /tmp/pip-czs_6emc-record/install-record.txt --single-version-externally-managed --compile --user --prefix=" failed with error code 1 in /tmp/pip-build-kspcfq_x/pyaudio/

```  
     
安装 swig 
``` 
wget http://hahack-1253537070.file.myqcloud.com/misc/swig-3.0.10.tar.gz
tar xvf swig-3.0.10.tar.gz
cd swig-3.0.10
sudo apt-get -y update
sudo apt-get install -y libpcre3 libpcre3-dev
./configure --prefix=/usr --without-clisp --without-maximum-compile-warnings
make
make install
install -v -m755 -d /usr/share/doc/swig-3.0.10
sudo cp -v -R Doc/* /usr/share/doc/swig-3.0.10
sudo apt-get install -y libatlas-base-dev
```  

反馈： 反馈太长了，没有了下载以及解压的代码了 

```  
swig-3.0.10/Examples/test-suite/schemerunme/overload_extend_c.scm
swig-3.0.10/Examples/test-suite/schemerunme/contract.scm
swig-3.0.10/Examples/test-suite/schemerunme/global_vars_proxy.scm
swig-3.0.10/Examples/test-suite/schemerunme/global_vars.scm
swig-3.0.10/Examples/test-suite/schemerunme/constover.scm
swig-3.0.10/Examples/test-suite/schemerunme/class_ignore.scm
swig-3.0.10/Examples/test-suite/schemerunme/name.scm
swig-3.0.10/Examples/test-suite/schemerunme/dynamic_cast.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_complicated.scm
swig-3.0.10/Examples/test-suite/schemerunme/li_std_string.scm
swig-3.0.10/Examples/test-suite/schemerunme/multiple_inheritance_proxy.scm
swig-3.0.10/Examples/test-suite/schemerunme/inherit_missing.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_simple.scm
swig-3.0.10/Examples/test-suite/schemerunme/list_vector.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_extend.scm
swig-3.0.10/Examples/test-suite/schemerunme/cpp_namespace.scm
swig-3.0.10/Examples/test-suite/schemerunme/unions.scm
swig-3.0.10/Examples/test-suite/schemerunme/typename.scm
swig-3.0.10/Examples/test-suite/schemerunme/pointer_in_out.scm
swig-3.0.10/Examples/test-suite/schemerunme/reference_global_vars.scm
swig-3.0.10/Examples/test-suite/schemerunme/li_typemaps.scm
swig-3.0.10/Examples/test-suite/schemerunme/typedef_inherit.scm
swig-3.0.10/Examples/test-suite/schemerunme/casts.scm
swig-3.0.10/Examples/test-suite/langobj.i
swig-3.0.10/Examples/test-suite/template_typemaps.i
swig-3.0.10/Examples/test-suite/member_pointer.i
swig-3.0.10/Examples/test-suite/python_nondynamic.i
swig-3.0.10/Examples/test-suite/packageoption.h
swig-3.0.10/Examples/test-suite/template_specialization_defarg.i
swig-3.0.10/Examples/test-suite/smart_pointer_ignore.i
swig-3.0.10/Examples/test-suite/array_typedef_memberin.i
swig-3.0.10/Examples/test-suite/preproc_include_h2.i
swig-3.0.10/Examples/test-suite/smart_pointer_template_defaults_overload.i
swig-3.0.10/Examples/test-suite/implicittest.i
swig-3.0.10/Examples/test-suite/li_cpointer_cpp.i
swig-3.0.10/Examples/test-suite/abstract_typedef.i
swig-3.0.10/Examples/test-suite/overload_complicated.i
swig-3.0.10/Examples/test-suite/funcptr_cpp.i
swig-3.0.10/Examples/test-suite/const_const_2.i
swig-3.0.10/Examples/test-suite/preproc_include_h3.i
swig-3.0.10/Examples/test-suite/template_basic.i
swig-3.0.10/Examples/test-suite/template_tbase_template.i
swig-3.0.10/Examples/test-suite/extend_typedef_class.i
swig-3.0.10/Examples/test-suite/constructor_value.i
swig-3.0.10/Examples/test-suite/features.i
swig-3.0.10/Examples/test-suite/ret_by_value.i
swig-3.0.10/Examples/test-suite/simple_array.i
swig-3.0.10/Examples/test-suite/constant_directive.i
swig-3.0.10/Examples/test-suite/sizeof_pointer.i
swig-3.0.10/Examples/test-suite/smart_pointer_template_const_overload.i
swig-3.0.10/Examples/test-suite/ignore_parameter.i
swig-3.0.10/Examples/test-suite/scilab_enums.i
swig-3.0.10/Examples/test-suite/scilab_pointer_conversion_functions.i
swig-3.0.10/Examples/test-suite/multiple_inheritance_interfaces.i
swig-3.0.10/Examples/test-suite/refcount.h
swig-3.0.10/Examples/test-suite/typemap_delete.i
swig-3.0.10/Examples/test-suite/friends.i
swig-3.0.10/Examples/test-suite/director_unroll.i
swig-3.0.10/Examples/test-suite/director_property.i
swig-3.0.10/Examples/test-suite/operator_pointer_ref.i
swig-3.0.10/Examples/test-suite/typemap_namespace.i
swig-3.0.10/Examples/test-suite/empty_c.i
swig-3.0.10/Examples/test-suite/director_stl.i
swig-3.0.10/Examples/test-suite/cpp11_hash_tables.i
swig-3.0.10/Examples/test-suite/li_cmalloc.i
swig-3.0.10/Examples/test-suite/inout.i
swig-3.0.10/Examples/test-suite/special_variable_macros.i
swig-3.0.10/Examples/test-suite/li_std_deque.i
swig-3.0.10/Examples/test-suite/overload_numeric.i
swig-3.0.10/Examples/test-suite/typemap_global_scope.i
swig-3.0.10/Examples/test-suite/template_typedef_rec.i
swig-3.0.10/Examples/test-suite/using_directive_and_declaration_forward.i
swig-3.0.10/Examples/test-suite/li_std_list.i
swig-3.0.10/Examples/test-suite/li_swigtype_inout.i
swig-3.0.10/Examples/test-suite/cpp11_default_delete.i
swig-3.0.10/Examples/test-suite/rename.h
swig-3.0.10/Examples/test-suite/java_throws.i
swig-3.0.10/Examples/test-suite/li_boost_intrusive_ptr.i
swig-3.0.10/Examples/test-suite/template_typedef_import.i
swig-3.0.10/Examples/test-suite/allowexcept.i
swig-3.0.10/Examples/test-suite/typemap_manyargs.i
swig-3.0.10/Examples/test-suite/java_nspacewithoutpackage.i
swig-3.0.10/Examples/test-suite/template_int_const.i
swig-3.0.10/Examples/test-suite/template_partial_arg.i
swig-3.0.10/Examples/test-suite/typemap_template.i
swig-3.0.10/Examples/test-suite/smart_pointer_const2.i
swig-3.0.10/Examples/test-suite/template_ns2.i
swig-3.0.10/Examples/test-suite/namespace_class.i
swig-3.0.10/Examples/test-suite/director_binary_string.i
swig-3.0.10/Examples/test-suite/function_typedef.i
swig-3.0.10/Examples/test-suite/unicode_strings.i
swig-3.0.10/Examples/test-suite/template_arg_replace.i
swig-3.0.10/Examples/test-suite/cpp11_inheriting_constructors.i
swig-3.0.10/Examples/java/
swig-3.0.10/Examples/java/index.html
swig-3.0.10/Examples/java/pointer/
swig-3.0.10/Examples/java/pointer/index.html
swig-3.0.10/Examples/java/pointer/example.i
swig-3.0.10/Examples/java/pointer/Makefile
swig-3.0.10/Examples/java/pointer/example.c
swig-3.0.10/Examples/java/pointer/runme.java
swig-3.0.10/Examples/java/class/
swig-3.0.10/Examples/java/class/index.html
swig-3.0.10/Examples/java/class/example.i
swig-3.0.10/Examples/java/class/example.cxx
swig-3.0.10/Examples/java/class/example.h
swig-3.0.10/Examples/java/class/Makefile
swig-3.0.10/Examples/java/class/runme.java
swig-3.0.10/Examples/java/class/example.dsp
swig-3.0.10/Examples/java/typemap/
swig-3.0.10/Examples/java/typemap/index.html
swig-3.0.10/Examples/java/typemap/example.i
swig-3.0.10/Examples/java/typemap/Makefile
swig-3.0.10/Examples/java/typemap/runme.java
swig-3.0.10/Examples/java/enum/
swig-3.0.10/Examples/java/enum/index.html
swig-3.0.10/Examples/java/enum/example.i
swig-3.0.10/Examples/java/enum/example.cxx
swig-3.0.10/Examples/java/enum/example.h
swig-3.0.10/Examples/java/enum/Makefile
swig-3.0.10/Examples/java/enum/runme.java
swig-3.0.10/Examples/java/template/
swig-3.0.10/Examples/java/template/index.html
swig-3.0.10/Examples/java/template/example.i
swig-3.0.10/Examples/java/template/example.h
swig-3.0.10/Examples/java/template/Makefile
swig-3.0.10/Examples/java/template/runme.java
swig-3.0.10/Examples/java/nested/
swig-3.0.10/Examples/java/nested/example.i
swig-3.0.10/Examples/java/nested/example.cxx
swig-3.0.10/Examples/java/nested/example.h
swig-3.0.10/Examples/java/nested/Makefile
swig-3.0.10/Examples/java/nested/runme.java
swig-3.0.10/Examples/java/nested/example.dsp
swig-3.0.10/Examples/java/funcptr/
swig-3.0.10/Examples/java/funcptr/index.html
swig-3.0.10/Examples/java/funcptr/example.i
swig-3.0.10/Examples/java/funcptr/example.h
swig-3.0.10/Examples/java/funcptr/Makefile
swig-3.0.10/Examples/java/funcptr/example.c
swig-3.0.10/Examples/java/funcptr/runme.java
swig-3.0.10/Examples/java/native/
swig-3.0.10/Examples/java/native/index.html
swig-3.0.10/Examples/java/native/example.i
swig-3.0.10/Examples/java/native/Makefile
swig-3.0.10/Examples/java/native/runme.java
swig-3.0.10/Examples/java/simple/
swig-3.0.10/Examples/java/simple/index.html
swig-3.0.10/Examples/java/simple/example.i
swig-3.0.10/Examples/java/simple/Makefile
swig-3.0.10/Examples/java/simple/example.c
swig-3.0.10/Examples/java/simple/runme.java
swig-3.0.10/Examples/java/simple/example.dsp
swig-3.0.10/Examples/java/reference/
swig-3.0.10/Examples/java/reference/index.html
swig-3.0.10/Examples/java/reference/example.i
swig-3.0.10/Examples/java/reference/example.cxx
swig-3.0.10/Examples/java/reference/example.h
swig-3.0.10/Examples/java/reference/Makefile
swig-3.0.10/Examples/java/reference/runme.java
swig-3.0.10/Examples/java/check.list
swig-3.0.10/Examples/java/callback/
swig-3.0.10/Examples/java/callback/index.html
swig-3.0.10/Examples/java/callback/example.i
swig-3.0.10/Examples/java/callback/example.cxx
swig-3.0.10/Examples/java/callback/example.h
swig-3.0.10/Examples/java/callback/Makefile
swig-3.0.10/Examples/java/callback/runme.java
swig-3.0.10/Examples/java/extend/
swig-3.0.10/Examples/java/extend/index.html
swig-3.0.10/Examples/java/extend/example.i
swig-3.0.10/Examples/java/extend/example.cxx
swig-3.0.10/Examples/java/extend/example.h
swig-3.0.10/Examples/java/extend/Makefile
swig-3.0.10/Examples/java/extend/runme.java
swig-3.0.10/Examples/java/variables/
swig-3.0.10/Examples/java/variables/index.html
swig-3.0.10/Examples/java/variables/example.i
swig-3.0.10/Examples/java/variables/example.h
swig-3.0.10/Examples/java/variables/Makefile
swig-3.0.10/Examples/java/variables/example.c
swig-3.0.10/Examples/java/variables/runme.java
swig-3.0.10/Examples/java/multimap/
swig-3.0.10/Examples/java/multimap/example.i
swig-3.0.10/Examples/java/multimap/Makefile
swig-3.0.10/Examples/java/multimap/example.c
swig-3.0.10/Examples/java/multimap/runme.java
swig-3.0.10/Examples/java/multimap/example.dsp
swig-3.0.10/Examples/java/constants/
swig-3.0.10/Examples/java/constants/index.html
swig-3.0.10/Examples/java/constants/example.i
swig-3.0.10/Examples/java/constants/Makefile
swig-3.0.10/Examples/java/constants/runme.java
swig-3.0.10/swig.spec.in
swig-3.0.10/appveyor.yml
swig-3.0.10/README
pi@raspberrypi:~ $ cd swig-3.0.10
pi@raspberrypi:~/swig-3.0.10 $ sudo apt-get -y update
命中:1 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch InRelease
命中:2 http://archive.raspberrypi.org/debian stretch InRelease                 
正在读取软件包列表... 完成                                                     
pi@raspberrypi:~/swig-3.0.10 $ sudo apt-get install -y libpcre3 libpcre3-dev
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
libpcre3 已经是最新版 (2:8.39-3)。
下列软件包是自动安装的并且现在不需要了：
  erlang-base erlang-crypto erlang-syntax-tools fonts-lato
  libboost-thread1.62.0 libqt5quickwidgets5 libqt5scintilla2-12v5
  libqt5scintilla2-l10n libqwt-qt5-6 libruby2.3 libscsynth1 libsctp1 rake
  realpath ruby ruby-did-you-mean ruby-minitest ruby-net-telnet
  ruby-power-assert ruby-test-unit ruby2.3 rubygems-integration
使用'sudo apt autoremove'来卸载它(它们)。
将会同时安装下列软件：
  libpcre32-3 libpcrecpp0v5
下列【新】软件包将被安装：
  libpcre3-dev libpcre32-3 libpcrecpp0v5
升级了 0 个软件包，新安装了 3 个软件包，要卸载 0 个软件包，有 85 个软件包未被升级。
需要下载 941 kB 的归档。
解压缩后会消耗 2,535 kB 的额外空间。
获取:1 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libpcrecpp0v5 armhf 2:8.39-3 [149 kB]
获取:2 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libpcre32-3 armhf 2:8.39-3 [227 kB]
获取:3 http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian stretch/main armhf libpcre3-dev armhf 2:8.39-3 [565 kB]
已下载 941 kB，耗时 3秒 (290 kB/s)    
正在选中未选择的软件包 libpcrecpp0v5:armhf。
(正在读取数据库 ... 系统当前共安装有 134055 个文件和目录。)
正准备解包 .../libpcrecpp0v5_2%3a8.39-3_armhf.deb  ...
正在解包 libpcrecpp0v5:armhf (2:8.39-3) ...
正在选中未选择的软件包 libpcre32-3:armhf。
正准备解包 .../libpcre32-3_2%3a8.39-3_armhf.deb  ...
正在解包 libpcre32-3:armhf (2:8.39-3) ...
正在选中未选择的软件包 libpcre3-dev:armhf。
正准备解包 .../libpcre3-dev_2%3a8.39-3_armhf.deb  ...
正在解包 libpcre3-dev:armhf (2:8.39-3) ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...
正在处理用于 man-db (2.7.6.1-2) 的触发器 ...
正在设置 libpcrecpp0v5:armhf (2:8.39-3) ...
正在设置 libpcre32-3:armhf (2:8.39-3) ...
正在设置 libpcre3-dev:armhf (2:8.39-3) ...
正在处理用于 libc-bin (2.24-11+deb9u3) 的触发器 ...
pi@raspberrypi:~/swig-3.0.10 $ ./configure --prefix=/usr --without-clisp --without-maximum-compile-warnings
checking build system type... 
armv7l-unknown-linux-gnueabihf
checking host system type... armv7l-unknown-linux-gnueabihf
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /bin/mkdir -p
checking for gawk... no
checking for mawk... mawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking for style of include used by make... GNU
checking dependency style of gcc... gcc3
checking for g++... g++
checking whether we are using the GNU C++ compiler... yes
checking whether g++ accepts -g... yes
checking dependency style of g++... gcc3
checking maximum warning verbosity option... no
checking how to run the C preprocessor... gcc -E
checking for grep that handles long lines and -e... /bin/grep
checking for egrep... /bin/grep -E
checking for ANSI C header files... yes
checking for popen... yes
checking whether to enable PCRE support... yes
checking whether to use local PCRE... no
checking for a sed that does not truncate output... /bin/sed
checking for pcre-config... /usr/bin/pcre-config
checking whether to enable ccache-swig... yes

Checking packages required for SWIG developers.
Note : None of the following packages are required for users to compile and install SWIG from the distributed tarball

checking for bison... no
checking for byacc... no

Checking for installed target languages and other information in order to compile and run
the examples and test-suite invoked by 'make check'.
Note : None of the following packages are required for users to compile and install SWIG from the distributed tarball

checking for boostlib >= 1.20.0... configure: We could not detect the boost libraries (version 1.20 or higher). If you have a staged boost library (still not installed) please specify $BOOST_ROOT in your environment and do not give a PATH to --with-boost option.  If you are sure you have boost installed, then check your version number looking in <boost/version.hpp>. See http://randspringer.de/boost for more documentation.
configure: ISYSTEM: -isystem 
checking SO... .so
checking LDSHARED... gcc -shared
checking CXXSHARED... gcc -shared
checking TRYLINKINGWITHCXX... CXXSHARED= g++ -shared 
checking CCSHARED... -fpic
checking RPATH... -Xlinker -rpath $(exec_prefix)/lib -Xlinker -rpath .
checking LINKFORSHARED... -Xlinker -export-dynamic
checking PLATCFLAGS... 
checking whether to enable C++11 testing... no
checking for dlopen in -ldl... yes
checking for shl_load in -ldld... no
checking for library containing t_open... no
checking for library containing gethostbyname... none required
checking for library containing socket... none required
checking for swill_init in -lswill... no
checking for main in -lieee... yes
checking for crypt in -lcrypt... yes
checking for pkg-config... pkg-config
checking for Tcl configuration... no
checking for Tcl header files... not found
checking for Tcl library... not found
checking for python... python
checking for python major version number... 2
checking for Python os.name... posix
checking for Python prefix... /usr
checking for Python exec-prefix... /usr
checking for Python version... python2.7
checking for Python lib dir... lib
checking for Python header files... -I/usr/include/python2.7 -I/usr/lib/python2.7/config
checking for Python library directory... Not found
checking for Python library... -lpython2.7
checking for python3... python3
checking for python3-config... python3-config
checking for python3 major version number... 3
checking for Python 3.x os.name... posix
checking for Python 3.x prefix... /usr
checking for Python 3.x exec-prefix... /usr
checking for Python 3.x version... python3.5
checking for Python 3.x lib dir... lib
checking for Python 3.x header files... -I/usr/include/python3.5m -I/usr/include/python3.5m
checking for Python 3.x library directory... Not found
checking for Python 3.x library... -lpython3.5
checking for pep8... no
checking for perl... perl
checking for Perl5 header files... /usr/lib/arm-linux-gnueabihf/perl/5.24/CORE
checking for Perl5 library... perl
checking for Perl5 ccflags... -D_REENTRANT -D_GNU_SOURCE -DDEBIAN -fwrapv -fno-strict-aliasing -pipe -isystem /usr/local/include -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
checking for Perl5 ccdlflags... -Wl,-E
checking for Perl5 cccdlflags... -fPIC
checking for Perl5 ldflags...  -fstack-protector-strong -L/usr/local/lib
checking for Perl5 Test::More module... found
checking for octave... no
checking for scilab... no
checking for java JDK... no (JAVA_HOME is not defined)
checking for java... java
checking for javac... javac
checking for java include file jni.h... not found
checking for nodejs... nodejs
checking for node-gyp... no
checking for JavaScriptCore/JavaScript.h... not found
checking for JavaScriptCore/Webkit library... not found
checking for V8 Javascript v8.h... not found
checking for V8 Javascript library... not found
checking for gcj... no
checking for gcjh... no
checking for android... no
checking for adb... no
checking for ant... ant
checking for ndk-build... no
checking for guile-config... no
checking for mzscheme... no
checking for mzc... no
checking for ruby... ruby
checking for Ruby header files... could not locate ruby.h
checking for Ruby library... not found... using /usr/include/ruby-2.3.0
checking for php5... no
checking for php... no
checking for PHP header files... could not find -config or obtain PHP version from it
checking for Ocaml DL load generator... checking for ocamldlgen... no
checking for Ocaml package tool... checking for ocamlfind... no
checking for Ocaml compiler... checking for ocamlc... no
checking for Ocaml toplevel creator... checking for ocamlmktop... no
checking for Ocaml Pre-Processor-Pretty-Printer... checking for camlp4... no
checking for pike... no
checking for pike7.8... no
checking for pike7.6... no
checking for pike7.4... no
checking for pike7.2... no
checking for chicken... no
checking for csc... no
checking for csi... no
checking for mono-csc... no
checking for gmcs... no
checking for mcs... no
checking for cscc... no
checking for lua5.4... no
checking for lua5.3... no
checking for lua5.2... no
checking for lua5.1... /usr/bin/lua5.1
checking Lua version... Lua 5.1 or later
checking whether Lua dynamic loading is enabled... yes
checking lua.h usability... no
checking lua.h presence... no
checking for lua.h... no
checking for lua.h in other locations... not found
checking for library containing lua_close... no
checking for alisp... no
configure: Disabling CLISP
checking for R... no
checking for go... no
checking for gccgo... no
checking for dmd... no
checking for ldmd... no
checking for gdmd... no
checking for dmd... no
checking for gdmd... no
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating Makefile
config.status: creating swig.spec
config.status: creating Examples/Makefile
config.status: creating Examples/d/example.mk
config.status: creating Examples/xml/Makefile
config.status: creating Examples/test-suite/errors/Makefile
config.status: creating Examples/test-suite/chicken/Makefile
config.status: creating Examples/test-suite/csharp/Makefile
config.status: creating Examples/test-suite/d/Makefile
config.status: creating Examples/test-suite/guile/Makefile
config.status: creating Examples/test-suite/java/Makefile
config.status: creating Examples/test-suite/javascript/Makefile
config.status: creating Examples/test-suite/mzscheme/Makefile
config.status: creating Examples/test-suite/ocaml/Makefile
config.status: creating Examples/test-suite/octave/Makefile
config.status: creating Examples/test-suite/perl5/Makefile
config.status: creating Examples/test-suite/php/Makefile
config.status: creating Examples/test-suite/pike/Makefile
config.status: creating Examples/test-suite/python/Makefile
config.status: creating Examples/test-suite/ruby/Makefile
config.status: creating Examples/test-suite/scilab/Makefile
config.status: creating Examples/test-suite/tcl/Makefile
config.status: creating Examples/test-suite/lua/Makefile
config.status: creating Examples/test-suite/allegrocl/Makefile
config.status: creating Examples/test-suite/clisp/Makefile
config.status: creating Examples/test-suite/cffi/Makefile
config.status: creating Examples/test-suite/uffi/Makefile
config.status: creating Examples/test-suite/r/Makefile
config.status: creating Examples/test-suite/go/Makefile
config.status: creating Source/Makefile
config.status: creating Tools/javascript/Makefile
config.status: creating preinst-swig
config.status: creating CCache/ccache_swig_config.h
config.status: creating Source/Include/swigconfig.h
config.status: executing depfiles commands
config.status: executing Examples commands
=== configuring in CCache (/home/pi/swig-3.0.10/CCache)
configure: running /bin/bash ./configure --disable-option-checking '--prefix=/usr'  '--without-clisp' '--without-maximum-compile-warnings' --cache-file=/dev/null --srcdir=.
configure: Configuring ccache
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking how to run the C preprocessor... gcc -E
checking for a BSD-compatible install... /usr/bin/install -c
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking whether time.h and sys/time.h may both be included... yes
checking for sys/wait.h that is POSIX.1 compatible... yes
checking for grep that handles long lines and -e... /bin/grep
checking for egrep... /bin/grep -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking ctype.h usability... yes
checking ctype.h presence... yes
checking for ctype.h... yes
checking for strings.h... (cached) yes
checking for stdlib.h... (cached) yes
checking for string.h... (cached) yes
checking pwd.h usability... yes
checking pwd.h presence... yes
checking for pwd.h... yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking for realpath... yes
checking for snprintf... yes
checking for vsnprintf... yes
checking for vasprintf... yes
checking for asprintf... yes
checking for mkstemp... yes
checking for gethostname... yes
checking for getpwuid... yes
checking for utimes... yes
checking for compar_fn_t in stdlib.h... yes
checking for C99 vsnprintf... yes
checking zlib.h usability... yes
checking zlib.h presence... yes
checking for zlib.h... yes
checking for gzdopen in -lz... yes
configure: creating ./config.status
config.status: creating Makefile
config.status: creating config.h

The SWIG test-suite and examples are configured for the following languages:
perl5 python 

pi@raspberrypi:~/swig-3.0.10 $ 
pi@raspberrypi:~/swig-3.0.10 $ make
make[1]: Entering directory '/home/pi/swig-3.0.10/Source'
make  all-am
make[2]: Entering directory '/home/pi/swig-3.0.10/Source'
depbase=`echo CParse/cscanner.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/cscanner.o -MD -MP -MF $depbase.Tpo -c -o CParse/cscanner.o CParse/cscanner.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo CParse/parser.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/parser.o -MD -MP -MF $depbase.Tpo -c -o CParse/parser.o CParse/parser.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo CParse/templ.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/templ.o -MD -MP -MF $depbase.Tpo -c -o CParse/templ.o CParse/templ.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo CParse/util.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/util.o -MD -MP -MF $depbase.Tpo -c -o CParse/util.o CParse/util.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/base.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/base.o -MD -MP -MF $depbase.Tpo -c -o DOH/base.o DOH/base.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/file.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/file.o -MD -MP -MF $depbase.Tpo -c -o DOH/file.o DOH/file.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/fio.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/fio.o -MD -MP -MF $depbase.Tpo -c -o DOH/fio.o DOH/fio.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/hash.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/hash.o -MD -MP -MF $depbase.Tpo -c -o DOH/hash.o DOH/hash.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/list.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/list.o -MD -MP -MF $depbase.Tpo -c -o DOH/list.o DOH/list.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/memory.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/memory.o -MD -MP -MF $depbase.Tpo -c -o DOH/memory.o DOH/memory.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/string.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/string.o -MD -MP -MF $depbase.Tpo -c -o DOH/string.o DOH/string.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/void.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/void.o -MD -MP -MF $depbase.Tpo -c -o DOH/void.o DOH/void.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/allegrocl.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/allegrocl.o -MD -MP -MF $depbase.Tpo -c -o Modules/allegrocl.o Modules/allegrocl.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/allocate.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/allocate.o -MD -MP -MF $depbase.Tpo -c -o Modules/allocate.o Modules/allocate.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/browser.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/browser.o -MD -MP -MF $depbase.Tpo -c -o Modules/browser.o Modules/browser.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/cffi.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/cffi.o -MD -MP -MF $depbase.Tpo -c -o Modules/cffi.o Modules/cffi.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/chicken.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/chicken.o -MD -MP -MF $depbase.Tpo -c -o Modules/chicken.o Modules/chicken.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/clisp.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/clisp.o -MD -MP -MF $depbase.Tpo -c -o Modules/clisp.o Modules/clisp.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/contract.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/contract.o -MD -MP -MF $depbase.Tpo -c -o Modules/contract.o Modules/contract.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/csharp.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/csharp.o -MD -MP -MF $depbase.Tpo -c -o Modules/csharp.o Modules/csharp.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/d.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/d.o -MD -MP -MF $depbase.Tpo -c -o Modules/d.o Modules/d.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/directors.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/directors.o -MD -MP -MF $depbase.Tpo -c -o Modules/directors.o Modules/directors.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/emit.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/emit.o -MD -MP -MF $depbase.Tpo -c -o Modules/emit.o Modules/emit.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/go.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/go.o -MD -MP -MF $depbase.Tpo -c -o Modules/go.o Modules/go.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/guile.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/guile.o -MD -MP -MF $depbase.Tpo -c -o Modules/guile.o Modules/guile.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/interface.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/interface.o -MD -MP -MF $depbase.Tpo -c -o Modules/interface.o Modules/interface.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/java.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/java.o -MD -MP -MF $depbase.Tpo -c -o Modules/java.o Modules/java.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/javascript.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/javascript.o -MD -MP -MF $depbase.Tpo -c -o Modules/javascript.o Modules/javascript.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/lang.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/lang.o -MD -MP -MF $depbase.Tpo -c -o Modules/lang.o Modules/lang.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/lua.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/lua.o -MD -MP -MF $depbase.Tpo -c -o Modules/lua.o Modules/lua.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/main.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/main.o -MD -MP -MF $depbase.Tpo -c -o Modules/main.o Modules/main.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/modula3.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/modula3.o -MD -MP -MF $depbase.Tpo -c -o Modules/modula3.o Modules/modula3.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/module.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/module.o -MD -MP -MF $depbase.Tpo -c -o Modules/module.o Modules/module.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/mzscheme.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/mzscheme.o -MD -MP -MF $depbase.Tpo -c -o Modules/mzscheme.o Modules/mzscheme.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/nested.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/nested.o -MD -MP -MF $depbase.Tpo -c -o Modules/nested.o Modules/nested.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/ocaml.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/ocaml.o -MD -MP -MF $depbase.Tpo -c -o Modules/ocaml.o Modules/ocaml.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/octave.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/octave.o -MD -MP -MF $depbase.Tpo -c -o Modules/octave.o Modules/octave.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/overload.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/overload.o -MD -MP -MF $depbase.Tpo -c -o Modules/overload.o Modules/overload.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/perl5.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/perl5.o -MD -MP -MF $depbase.Tpo -c -o Modules/perl5.o Modules/perl5.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/php.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/php.o -MD -MP -MF $depbase.Tpo -c -o Modules/php.o Modules/php.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/pike.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/pike.o -MD -MP -MF $depbase.Tpo -c -o Modules/pike.o Modules/pike.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/python.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/python.o -MD -MP -MF $depbase.Tpo -c -o Modules/python.o Modules/python.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/r.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/r.o -MD -MP -MF $depbase.Tpo -c -o Modules/r.o Modules/r.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/ruby.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/ruby.o -MD -MP -MF $depbase.Tpo -c -o Modules/ruby.o Modules/ruby.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/s-exp.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/s-exp.o -MD -MP -MF $depbase.Tpo -c -o Modules/s-exp.o Modules/s-exp.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/scilab.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/scilab.o -MD -MP -MF $depbase.Tpo -c -o Modules/scilab.o Modules/scilab.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/swigmain.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/swigmain.o -MD -MP -MF $depbase.Tpo -c -o Modules/swigmain.o Modules/swigmain.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/tcl8.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/tcl8.o -MD -MP -MF $depbase.Tpo -c -o Modules/tcl8.o Modules/tcl8.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/typepass.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/typepass.o -MD -MP -MF $depbase.Tpo -c -o Modules/typepass.o Modules/typepass.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/uffi.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/uffi.o -MD -MP -MF $depbase.Tpo -c -o Modules/uffi.o Modules/uffi.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/utils.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/utils.o -MD -MP -MF $depbase.Tpo -c -o Modules/utils.o Modules/utils.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/xml.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/xml.o -MD -MP -MF $depbase.Tpo -c -o Modules/xml.o Modules/xml.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Preprocessor/cpp.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Preprocessor/cpp.o -MD -MP -MF $depbase.Tpo -c -o Preprocessor/cpp.o Preprocessor/cpp.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Preprocessor/expr.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Preprocessor/expr.o -MD -MP -MF $depbase.Tpo -c -o Preprocessor/expr.o Preprocessor/expr.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/cwrap.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/cwrap.o -MD -MP -MF $depbase.Tpo -c -o Swig/cwrap.o Swig/cwrap.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/deprecate.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/deprecate.o -MD -MP -MF $depbase.Tpo -c -o Swig/deprecate.o Swig/deprecate.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/error.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/error.o -MD -MP -MF $depbase.Tpo -c -o Swig/error.o Swig/error.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/extend.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/extend.o -MD -MP -MF $depbase.Tpo -c -o Swig/extend.o Swig/extend.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/fragment.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/fragment.o -MD -MP -MF $depbase.Tpo -c -o Swig/fragment.o Swig/fragment.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/getopt.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/getopt.o -MD -MP -MF $depbase.Tpo -c -o Swig/getopt.o Swig/getopt.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/include.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/include.o -MD -MP -MF $depbase.Tpo -c -o Swig/include.o Swig/include.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/misc.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/misc.o -MD -MP -MF $depbase.Tpo -c -o Swig/misc.o Swig/misc.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/naming.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/naming.o -MD -MP -MF $depbase.Tpo -c -o Swig/naming.o Swig/naming.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/parms.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/parms.o -MD -MP -MF $depbase.Tpo -c -o Swig/parms.o Swig/parms.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/scanner.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/scanner.o -MD -MP -MF $depbase.Tpo -c -o Swig/scanner.o Swig/scanner.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/stype.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/stype.o -MD -MP -MF $depbase.Tpo -c -o Swig/stype.o Swig/stype.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/symbol.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/symbol.o -MD -MP -MF $depbase.Tpo -c -o Swig/symbol.o Swig/symbol.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/tree.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/tree.o -MD -MP -MF $depbase.Tpo -c -o Swig/tree.o Swig/tree.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/typeobj.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/typeobj.o -MD -MP -MF $depbase.Tpo -c -o Swig/typeobj.o Swig/typeobj.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/typemap.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/typemap.o -MD -MP -MF $depbase.Tpo -c -o Swig/typemap.o Swig/typemap.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/typesys.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/typesys.o -MD -MP -MF $depbase.Tpo -c -o Swig/typesys.o Swig/typesys.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Swig/wrapfunc.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Swig/wrapfunc.o -MD -MP -MF $depbase.Tpo -c -o Swig/wrapfunc.o Swig/wrapfunc.c &&\
mv -f $depbase.Tpo $depbase.Po
g++  -g -O2   -o eswig CParse/cscanner.o CParse/parser.o CParse/templ.o CParse/util.o DOH/base.o DOH/file.o DOH/fio.o DOH/hash.o DOH/list.o DOH/memory.o DOH/string.o DOH/void.o Modules/allegrocl.o Modules/allocate.o Modules/browser.o Modules/cffi.o Modules/chicken.o Modules/clisp.o Modules/contract.o Modules/csharp.o Modules/d.o Modules/directors.o Modules/emit.o Modules/go.o Modules/guile.o Modules/interface.o Modules/java.o Modules/javascript.o Modules/lang.o Modules/lua.o Modules/main.o Modules/modula3.o Modules/module.o Modules/mzscheme.o Modules/nested.o Modules/ocaml.o Modules/octave.o Modules/overload.o Modules/perl5.o Modules/php.o Modules/pike.o Modules/python.o Modules/r.o Modules/ruby.o Modules/s-exp.o Modules/scilab.o Modules/swigmain.o Modules/tcl8.o Modules/typepass.o Modules/uffi.o Modules/utils.o Modules/xml.o Preprocessor/cpp.o Preprocessor/expr.o Swig/cwrap.o Swig/deprecate.o Swig/error.o Swig/extend.o Swig/fragment.o Swig/getopt.o Swig/include.o Swig/misc.o Swig/naming.o Swig/parms.o Swig/scanner.o Swig/stype.o Swig/symbol.o Swig/tree.o Swig/typeobj.o Swig/typemap.o Swig/typesys.o Swig/wrapfunc.o  -ldl  -lpcre
cp -f ../Source/eswig ../swig
make[2]: Leaving directory '/home/pi/swig-3.0.10/Source'
make[1]: Leaving directory '/home/pi/swig-3.0.10/Source'
test -z "1" || (cd CCache && make)
make[1]: Entering directory '/home/pi/swig-3.0.10/CCache'
gcc -g -O2 -Wall -W -I.   -c -o ccache.o ccache.c
gcc -g -O2 -Wall -W -I.   -c -o mdfour.o mdfour.c
gcc -g -O2 -Wall -W -I.   -c -o hash.o hash.c
gcc -g -O2 -Wall -W -I.   -c -o execute.o execute.c
gcc -g -O2 -Wall -W -I.   -c -o util.o util.c
gcc -g -O2 -Wall -W -I.   -c -o args.o args.c
gcc -g -O2 -Wall -W -I.   -c -o stats.o stats.c
gcc -g -O2 -Wall -W -I.   -c -o cleanup.o cleanup.c
gcc -g -O2 -Wall -W -I.   -c -o snprintf.o snprintf.c
gcc -g -O2 -Wall -W -I.   -c -o unify.o unify.c
gcc -g -O2 -Wall -W -I.  -o ccache-swig ccache.o mdfour.o hash.o execute.o util.o args.o stats.o cleanup.o snprintf.o unify.o -lz 
make[1]: Leaving directory '/home/pi/swig-3.0.10/CCache'

```  

构建 snowboy 
运行  

```
wget http://hahack-1253537070.file.myqcloud.com/misc/snowboy.tar.bz2  # 使用我fork出来的版本以确保接口兼容
tar -xvjf snowboy.tar.bz2
cd snowboy/swig/Python3
make
cp _snowboydetect.so <wukon-robot的根目录/snowboy/>
```
反馈： 
``` 
pi@raspberrypi:~ $ wget http://hahack-1253537070.file.myqcloud.com/misc/snowboy.tar.bz2  # 使用我fork出来的版本以确保接口兼容
--2019-04-16 21:13:29--  http://hahack-1253537070.file.myqcloud.com/misc/snowboy.tar.bz2
正在解析主机 hahack-1253537070.file.myqcloud.com (hahack-1253537070.file.myqcloud.com)... 42.236.125.84, 182.118.11.193, 182.118.11.126
正在连接 hahack-1253537070.file.myqcloud.com (hahack-1253537070.file.myqcloud.com)|42.236.125.84|:80... 已连接。
已发出 HTTP 请求，正在等待回应... 200 OK
长度：26351700 (25M) [application/x-bzip2]
正在保存至: “snowboy.tar.bz2”

snowboy.tar.bz2     100%[===================>]  25.13M   178KB/s    in 2m 23s  

2019-04-16 21:15:53 (180 KB/s) - 已保存 “snowboy.tar.bz2” [26351700/26351700])

pi@raspberrypi:~ $ tar -xvjf snowboy.tar.bz2
snowboy/
snowboy/.npmignore
snowboy/README_commercial.md
snowboy/._.DS_Store
snowboy/.DS_Store
snowboy/swig/
snowboy/README_ZH_CN.md
snowboy/LICENSE
snowboy/binding.gyp
snowboy/include/
snowboy/resources/
snowboy/MANIFEST.in
snowboy/README.md
snowboy/setup.py
snowboy/.gitignore
snowboy/package.json
snowboy/examples/
snowboy/scripts/
snowboy/lib/
snowboy/tsconfig.json
snowboy/.travis.yml
snowboy/lib/ubuntu64/
snowboy/lib/osx/
snowboy/lib/aarch64-ubuntu1604/
snowboy/lib/rpi/
snowboy/lib/ios/
snowboy/lib/android/
snowboy/lib/node/
snowboy/lib/node/SnowboyDetectNative.d.ts
snowboy/lib/node/node-pre-gyp.d.ts
snowboy/lib/node/index.ts
snowboy/lib/android/armv8-aarch64/
snowboy/lib/android/armv7a/
snowboy/lib/android/armv7a/libsnowboy-detect.a
snowboy/lib/android/armv8-aarch64/libsnowboy-detect.a
snowboy/lib/ios/libsnowboy-detect.a
snowboy/lib/rpi/libsnowboy-detect.a
snowboy/lib/aarch64-ubuntu1604/libsnowboy-detect.a
snowboy/lib/osx/libsnowboy-detect.a
snowboy/lib/ubuntu64/libsnowboy-detect.a
snowboy/scripts/publish-node.sh
snowboy/scripts/install_swig.sh
snowboy/examples/C++/
snowboy/examples/Go/
snowboy/examples/._.DS_Store
snowboy/examples/.DS_Store
snowboy/examples/Python3/
snowboy/examples/Python/
snowboy/examples/Perl/
snowboy/examples/Java/
snowboy/examples/iOS/
snowboy/examples/Android/
snowboy/examples/Node/
snowboy/examples/C/
snowboy/examples/REST_API/
snowboy/examples/REST_API/training_service.py
snowboy/examples/REST_API/training_service.sh
snowboy/examples/C/snowboy-detect-c-wrapper.cc
snowboy/examples/C/Makefile
snowboy/examples/C/patches/
snowboy/examples/C/resources
snowboy/examples/C/demo.mk
snowboy/examples/C/snowboy-detect-c-wrapper.h
snowboy/examples/C/install_portaudio.sh
snowboy/examples/C/demo.c
snowboy/examples/C/patches/portaudio.patch
snowboy/examples/Node/resources
snowboy/examples/Node/microphone.js
snowboy/examples/Node/file.js
snowboy/examples/Android/SnowboyAlexaDemo/
snowboy/examples/Android/README.md
snowboy/examples/Android/SnowboyAlexaDemo/res/
snowboy/examples/Android/SnowboyAlexaDemo/ic_launcher-web.png
snowboy/examples/Android/SnowboyAlexaDemo/AndroidManifest.xml
snowboy/examples/Android/SnowboyAlexaDemo/project.properties
snowboy/examples/Android/SnowboyAlexaDemo/.classpath
snowboy/examples/Android/SnowboyAlexaDemo/gradle/
snowboy/examples/Android/SnowboyAlexaDemo/gradlew
snowboy/examples/Android/SnowboyAlexaDemo/.gitignore
snowboy/examples/Android/SnowboyAlexaDemo/.project
snowboy/examples/Android/SnowboyAlexaDemo/build.gradle
snowboy/examples/Android/SnowboyAlexaDemo/gradlew.bat
snowboy/examples/Android/SnowboyAlexaDemo/assets/
snowboy/examples/Android/SnowboyAlexaDemo/.idea/
snowboy/examples/Android/SnowboyAlexaDemo/src/
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/
snowboy/examples/Android/SnowboyAlexaDemo/src/main/
snowboy/examples/Android/SnowboyAlexaDemo/src/main/jniLibs
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/SnowboyVad.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/MsgEnum.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/SnowboyDetect.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/audio/
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/AppResCopy.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/Demo.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/Constants.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/snowboyJNI.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/audio/RecordingThread.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/audio/PlaybackThread.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/audio/AudioDataSaver.java
snowboy/examples/Android/SnowboyAlexaDemo/src/ai/kitt/snowboy/audio/AudioDataReceivedListener.java
snowboy/examples/Android/SnowboyAlexaDemo/.idea/encodings.xml
snowboy/examples/Android/SnowboyAlexaDemo/.idea/runConfigurations.xml
snowboy/examples/Android/SnowboyAlexaDemo/.idea/gradle.xml
snowboy/examples/Android/SnowboyAlexaDemo/.idea/modules.xml
snowboy/examples/Android/SnowboyAlexaDemo/.idea/.name
snowboy/examples/Android/SnowboyAlexaDemo/.idea/copyright/
snowboy/examples/Android/SnowboyAlexaDemo/.idea/misc.xml
snowboy/examples/Android/SnowboyAlexaDemo/.idea/compiler.xml
snowboy/examples/Android/SnowboyAlexaDemo/.idea/copyright/profiles_settings.xml
snowboy/examples/Android/SnowboyAlexaDemo/assets/snowboy/
snowboy/examples/Android/SnowboyAlexaDemo/assets/snowboy/alexa.umdl
snowboy/examples/Android/SnowboyAlexaDemo/assets/snowboy/common.res
snowboy/examples/Android/SnowboyAlexaDemo/assets/snowboy/ding.wav
snowboy/examples/Android/SnowboyAlexaDemo/gradle/wrapper/
snowboy/examples/Android/SnowboyAlexaDemo/gradle/wrapper/gradle-wrapper.jar
snowboy/examples/Android/SnowboyAlexaDemo/gradle/wrapper/gradle-wrapper.properties
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-mdpi/
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-hdpi/
snowboy/examples/Android/SnowboyAlexaDemo/res/drawable/
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-xxxhdpi/
snowboy/examples/Android/SnowboyAlexaDemo/res/layout/
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-xxhdpi/
snowboy/examples/Android/SnowboyAlexaDemo/res/values/
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-xhdpi/
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-xhdpi/ic_launcher.png
snowboy/examples/Android/SnowboyAlexaDemo/res/values/strings.xml
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-xxhdpi/ic_launcher.png
snowboy/examples/Android/SnowboyAlexaDemo/res/layout/main.xml
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-xxxhdpi/ic_launcher.png
snowboy/examples/Android/SnowboyAlexaDemo/res/drawable/icon.png
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-hdpi/ic_launcher.png
snowboy/examples/Android/SnowboyAlexaDemo/res/mipmap-mdpi/ic_launcher.png
snowboy/examples/iOS/Swift3/
snowboy/examples/iOS/Obj-C/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcworkspace/
snowboy/examples/iOS/Obj-C/SnowboyTestUITests/
snowboy/examples/iOS/Obj-C/Pods/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/
snowboy/examples/iOS/Obj-C/SnowboyTest/
snowboy/examples/iOS/Obj-C/Podfile
snowboy/examples/iOS/Obj-C/SnowboyTestTests/
snowboy/examples/iOS/Obj-C/Podfile.lock
snowboy/examples/iOS/Obj-C/SnowboyTestTests/SnowboyTestTests.m
snowboy/examples/iOS/Obj-C/SnowboyTestTests/Info.plist
snowboy/examples/iOS/Obj-C/SnowboyTest/ViewController.mm
snowboy/examples/iOS/Obj-C/SnowboyTest/AppDelegate.h
snowboy/examples/iOS/Obj-C/SnowboyTest/libsnowboy-detect.a
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/
snowboy/examples/iOS/Obj-C/SnowboyTest/Base.lproj/
snowboy/examples/iOS/Obj-C/SnowboyTest/main.m
snowboy/examples/iOS/Obj-C/SnowboyTest/alexa.umdl
snowboy/examples/iOS/Obj-C/SnowboyTest/snowboy-detect.h
snowboy/examples/iOS/Obj-C/SnowboyTest/common.res
snowboy/examples/iOS/Obj-C/SnowboyTest/AppDelegate.m
snowboy/examples/iOS/Obj-C/SnowboyTest/Info.plist
snowboy/examples/iOS/Obj-C/SnowboyTest/ViewController.h
snowboy/examples/iOS/Obj-C/SnowboyTest/Base.lproj/LaunchScreen.storyboard
snowboy/examples/iOS/Obj-C/SnowboyTest/Base.lproj/Main.storyboard
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/AppIcon.appiconset/
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/Contents.json
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/banner.imageset/
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/banner.imageset/snowboy-1.png
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/banner.imageset/snowboy.png
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/banner.imageset/Contents.json
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/banner.imageset/snowboy-2.png
snowboy/examples/iOS/Obj-C/SnowboyTest/Assets.xcassets/AppIcon.appiconset/Contents.json
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/project.pbxproj
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/xcuserdata/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/project.xcworkspace/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/project.xcworkspace/contents.xcworkspacedata
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/project.xcworkspace/xcuserdata/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/project.xcworkspace/xcuserdata/patrickquinn.xcuserdatad/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/project.xcworkspace/xcuserdata/patrickquinn.xcuserdatad/UserInterfaceState.xcuserstate
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/SnowboyTest.xcscheme
snowboy/examples/iOS/Obj-C/SnowboyTest.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/xcschememanagement.plist
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/
snowboy/examples/iOS/Obj-C/Pods/EZAudio/
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/
snowboy/examples/iOS/Obj-C/Pods/Manifest.lock
snowboy/examples/iOS/Obj-C/Pods/Headers/
snowboy/examples/iOS/Obj-C/Pods/TPCircularBuffer/
snowboy/examples/iOS/Obj-C/Pods/TPCircularBuffer/TPCircularBuffer.h
snowboy/examples/iOS/Obj-C/Pods/TPCircularBuffer/TPCircularBuffer+AudioBufferList.c
snowboy/examples/iOS/Obj-C/Pods/TPCircularBuffer/README.markdown
snowboy/examples/iOS/Obj-C/Pods/TPCircularBuffer/TPCircularBuffer.c
snowboy/examples/iOS/Obj-C/Pods/TPCircularBuffer/TPCircularBuffer+AudioBufferList.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/TPCircularBuffer/
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/TPCircularBuffer/TPCircularBuffer.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/TPCircularBuffer/TPCircularBuffer+AudioBufferList.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZPlot.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioOSX.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioUtilities.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudio.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/TPCircularBuffer.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioPlot.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioPlayer.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioFloatConverter.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZOutput.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZRecorder.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioPlotGL.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioFile.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioDisplayLink.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioDevice.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioFloatData.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZMicrophone.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioFFT.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Private/EZAudio/EZAudioiOS.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/TPCircularBuffer/
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/TPCircularBuffer/TPCircularBuffer.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/TPCircularBuffer/TPCircularBuffer+AudioBufferList.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZPlot.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioOSX.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioUtilities.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudio.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/TPCircularBuffer.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioPlot.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioPlayer.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioFloatConverter.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZOutput.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZRecorder.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioPlotGL.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioFile.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioDisplayLink.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioDevice.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioFloatData.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZMicrophone.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioFFT.h
snowboy/examples/iOS/Obj-C/Pods/Headers/Public/EZAudio/EZAudioiOS.h
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/EZAudio/
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/TPCircularBuffer/
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/TPCircularBuffer/TPCircularBuffer-prefix.pch
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/TPCircularBuffer/TPCircularBuffer.xcconfig
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/TPCircularBuffer/TPCircularBuffer-dummy.m
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/EZAudio/EZAudio-prefix.pch
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/EZAudio/EZAudio.xcconfig
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/EZAudio/EZAudio-dummy.m
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/Pods-SnowboyTest-resources.sh
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/Pods-SnowboyTest.debug.xcconfig
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/Pods-SnowboyTest-dummy.m
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/Pods-SnowboyTest.release.xcconfig
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/Pods-SnowboyTest-acknowledgements.plist
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/Pods-SnowboyTest-acknowledgements.markdown
snowboy/examples/iOS/Obj-C/Pods/Target Support Files/Pods-SnowboyTest/Pods-SnowboyTest-frameworks.sh
snowboy/examples/iOS/Obj-C/Pods/EZAudio/LICENSE
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/
snowboy/examples/iOS/Obj-C/Pods/EZAudio/README.md
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZPlot.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioOSX.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioUtilities.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudio.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZMicrophone.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFloatData.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/TPCircularBuffer.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioPlot.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioPlayer.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFloatConverter.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZOutput.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZRecorder.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFFT.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioPlotGL.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFile.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioDisplayLink.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioDevice.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZPlot.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioPlot.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioPlayer.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/TPCircularBuffer.c
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFloatData.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZMicrophone.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudio.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioUtilities.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZRecorder.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZOutput.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFloatConverter.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioDevice.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioDisplayLink.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFile.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioPlotGL.m
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioFFT.h
snowboy/examples/iOS/Obj-C/Pods/EZAudio/EZAudio/EZAudioiOS.h
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/project.pbxproj
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/xcuserdata/
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/TPCircularBuffer.xcscheme
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/EZAudio.xcscheme
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/Pods-SnowboyTest.xcscheme
snowboy/examples/iOS/Obj-C/Pods/Pods.xcodeproj/xcuserdata/patrickquinn.xcuserdatad/xcschemes/xcschememanagement.plist
snowboy/examples/iOS/Obj-C/SnowboyTestUITests/SnowboyTestUITests.m
snowboy/examples/iOS/Obj-C/SnowboyTestUITests/Info.plist
snowboy/examples/iOS/Obj-C/SnowboyTest.xcworkspace/contents.xcworkspacedata
snowboy/examples/iOS/Obj-C/SnowboyTest.xcworkspace/xcuserdata/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcworkspace/xcuserdata/patrickquinn.xcuserdatad/
snowboy/examples/iOS/Obj-C/SnowboyTest.xcworkspace/xcuserdata/patrickquinn.xcuserdatad/UserInterfaceState.xcuserstate
snowboy/examples/iOS/Swift3/README.md
snowboy/examples/iOS/Swift3/SnowboyTestUITests/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/
snowboy/examples/iOS/Swift3/SnowboyTest/
snowboy/examples/iOS/Swift3/SnowboyTestTests/
snowboy/examples/iOS/Swift3/SnowboyTestTests/SnowboyTestTests.swift
snowboy/examples/iOS/Swift3/SnowboyTestTests/Info.plist
snowboy/examples/iOS/Swift3/SnowboyTest/SnowboyTest-Bridging-Header.h
snowboy/examples/iOS/Swift3/SnowboyTest/ViewController.swift
snowboy/examples/iOS/Swift3/SnowboyTest/SnowboyTest.xcdatamodeld/
snowboy/examples/iOS/Swift3/SnowboyTest/SnowboyWrapper.h
snowboy/examples/iOS/Swift3/SnowboyTest/Assets.xcassets/
snowboy/examples/iOS/Swift3/SnowboyTest/Base.lproj/
snowboy/examples/iOS/Swift3/SnowboyTest/AppDelegate.swift
snowboy/examples/iOS/Swift3/SnowboyTest/Info.plist
snowboy/examples/iOS/Swift3/SnowboyTest/SnowboyWrapper.mm
snowboy/examples/iOS/Swift3/SnowboyTest/Base.lproj/LaunchScreen.storyboard
snowboy/examples/iOS/Swift3/SnowboyTest/Base.lproj/Main.storyboard
snowboy/examples/iOS/Swift3/SnowboyTest/Assets.xcassets/AppIcon.appiconset/
snowboy/examples/iOS/Swift3/SnowboyTest/Assets.xcassets/AppIcon.appiconset/Contents.json
snowboy/examples/iOS/Swift3/SnowboyTest/SnowboyTest.xcdatamodeld/.xccurrentversion
snowboy/examples/iOS/Swift3/SnowboyTest/SnowboyTest.xcdatamodeld/SnowboyTest.xcdatamodel/
snowboy/examples/iOS/Swift3/SnowboyTest/SnowboyTest.xcdatamodeld/SnowboyTest.xcdatamodel/contents
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/project.pbxproj
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/xcuserdata/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/project.xcworkspace/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/project.xcworkspace/contents.xcworkspacedata
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/project.xcworkspace/xcuserdata/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/project.xcworkspace/xcuserdata/shengbi.xcuserdatad/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/project.xcworkspace/xcuserdata/shengbi.xcuserdatad/UserInterfaceState.xcuserstate
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/xcuserdata/shengbi.xcuserdatad/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/xcuserdata/shengbi.xcuserdatad/xcdebugger/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/xcuserdata/shengbi.xcuserdatad/xcschemes/
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/xcuserdata/shengbi.xcuserdatad/xcschemes/SnowboyTest.xcscheme
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/xcuserdata/shengbi.xcuserdatad/xcschemes/xcschememanagement.plist
snowboy/examples/iOS/Swift3/SnowboyTest.xcodeproj/xcuserdata/shengbi.xcuserdatad/xcdebugger/Breakpoints_v2.xcbkptlist
snowboy/examples/iOS/Swift3/SnowboyTestUITests/SnowboyTestUITests.swift
snowboy/examples/iOS/Swift3/SnowboyTestUITests/Info.plist
snowboy/examples/Java/Makefile
snowboy/examples/Java/resources
snowboy/examples/Java/java
snowboy/examples/Java/Demo.java
snowboy/examples/Java/jniLibs
snowboy/examples/Perl/cpanfile
snowboy/examples/Perl/Snowboy.pm
snowboy/examples/Perl/resources
snowboy/examples/Perl/Snowboy.dylib
snowboy/examples/Perl/snowboy_unit_test.pl
snowboy/examples/Perl/snowboy_googlevoice.pl
snowboy/examples/Perl/Snowboy.so
snowboy/examples/Perl/snowboy_RESTful_train.pl
snowboy/examples/Python/requirements.txt
snowboy/examples/Python/snowboythreaded.py
snowboy/examples/Python/snowboydecoder_arecord.py
snowboy/examples/Python/snowboydecoder.py
snowboy/examples/Python/demo3.py
snowboy/examples/Python/resources
snowboy/examples/Python/demo_threaded.py
snowboy/examples/Python/demo2.py
snowboy/examples/Python/__init__.py
snowboy/examples/Python/demo_arecord.py
snowboy/examples/Python/_snowboydetect.so
snowboy/examples/Python/demo4.py
snowboy/examples/Python/snowboydetect.py
snowboy/examples/Python/demo.py
snowboy/examples/Python3/requirements.txt
snowboy/examples/Python3/snowboydecoder.py
snowboy/examples/Python3/demo3.py
snowboy/examples/Python3/resources
snowboy/examples/Python3/demo2.py
snowboy/examples/Python3/_snowboydetect.so
snowboy/examples/Python3/demo4.py
snowboy/examples/Python3/snowboydetect.py
snowboy/examples/Python3/demo.py
snowboy/examples/Go/detect/
snowboy/examples/Go/listen/
snowboy/examples/Go/listen/README.md
snowboy/examples/Go/listen/main.go
snowboy/examples/Go/detect/readme.md
snowboy/examples/Go/detect/main.go
snowboy/examples/C++/demo.cc
snowboy/examples/C++/Makefile
snowboy/examples/C++/patches/
snowboy/examples/C++/resources
snowboy/examples/C++/demo.mk
snowboy/examples/C++/demo2.cc
snowboy/examples/C++/install_portaudio.sh
snowboy/examples/C++/patches/portaudio.patch
snowboy/resources/._.DS_Store
snowboy/resources/.DS_Store
snowboy/resources/snowboy.raw
snowboy/resources/alexa/
snowboy/resources/models/
snowboy/resources/common.res
snowboy/resources/dong.wav
snowboy/resources/snowboy.wav
snowboy/resources/ding.wav
snowboy/resources/models/smart_mirror.umdl
snowboy/resources/models/jarvis.umdl
snowboy/resources/models/snowboy.umdl
snowboy/resources/models/subex.umdl
snowboy/resources/alexa/alexa-avs-sample-app/
snowboy/resources/alexa/alexa_02092017.umdl
snowboy/resources/alexa/SnowboyAlexaDemo.apk
snowboy/resources/alexa/alexa-avs-sample-app/alexa.umdl
snowboy/include/snowboy-detect.h
snowboy/swig/Go/
snowboy/swig/._.DS_Store
snowboy/swig/.DS_Store
snowboy/swig/Python3/
snowboy/swig/Python/
snowboy/swig/Perl/
snowboy/swig/Java/
snowboy/swig/Android/
snowboy/swig/Node/
snowboy/swig/Node/snowboy.cc
snowboy/swig/Android/snowboy-detect-swig.i
snowboy/swig/Android/install_openblas.sh
snowboy/swig/Android/Makefile
snowboy/swig/Android/install_ndk.sh
snowboy/swig/Java/snowboy-detect-swig.i
snowboy/swig/Java/Makefile
snowboy/swig/Perl/Makefile
snowboy/swig/Perl/snowboy-detect.i
snowboy/swig/Python/snowboy-detect-swig.i
snowboy/swig/Python/snowboy-detect-swig.o
snowboy/swig/Python/snowboy-detect-swig.cc
snowboy/swig/Python/Makefile
snowboy/swig/Python/_snowboydetect.so
snowboy/swig/Python/snowboydetect.py
snowboy/swig/Python3/snowboy-detect-swig.i
snowboy/swig/Python3/._.DS_Store
snowboy/swig/Python3/.DS_Store
snowboy/swig/Python3/Makefile
snowboy/swig/Go/snowboy.go
snowboy/swig/Go/snowboydetect.swigcxx  


pi@raspberrypi:~ $ cd snowboy/swig/Python3
pi@raspberrypi:~/snowboy/swig/Python3 $ make
/bin/sh: 1: swig: not found
expr: 语法错误
swig -I../../ -c++ -python -o snowboy-detect-swig.cc snowboy-detect-swig.i
make: swig：命令未找到
Makefile:67: recipe for target 'snowboy-detect-swig.cc' failed
make: *** [snowboy-detect-swig.cc] Error 127
-------------------------------------------------

```

参考资料：  
- 安装pyaudio找不到portaudio.h的问题（https://blog.csdn.net/qq_23729557/article/details/78956602）

190416 小獅子 17：39 init-