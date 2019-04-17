
## 背景  
在安装悟空程序中  

 运行：`pip3 install -r requirements.txt`错误   

  
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
## 参考资料 
- https://blog.csdn.net/cynthrial/article/details/82289585

安装上述文件采取的行动  错误

``` 
wget https://bootstrap.pypa.io/get-pip.py
python get-pip.py
```

代码
```  
pi@raspberrypi:~/wukong-robot $ pip -V
pip 9.0.1 from /usr/lib/python2.7/dist-packages (python 2.7)
pi@raspberrypi:~/wukong-robot $ wget https://bootstrap.pypa.io/get-pip.py
--2019-04-16 21:09:57--  https://bootstrap.pypa.io/get-pip.py
正在解析主机 bootstrap.pypa.io (bootstrap.pypa.io)... 151.101.228.175, 2a04:4e42:36::175
正在连接 bootstrap.pypa.io (bootstrap.pypa.io)|151.101.228.175|:443... 已连接。
已发出 HTTP 请求，正在等待回应... 200 OK
长度：1699325 (1.6M) [text/x-python]
正在保存至: “get-pip.py”

get-pip.py             100%[===========================>]   1.62M  10.6KB/s    in 2m 7s   

2019-04-16 21:12:05 (13.1 KB/s) - 已保存 “get-pip.py” [1699325/1699325])

pi@raspberrypi:~/wukong-robot $ python get-pip.py
DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 won't be maintained after that date. A future version of pip will drop support for Python 2.7.
Looking in indexes: https://pypi.org/simple, https://www.piwheels.org/simple
Collecting pip
  Downloading https://files.pythonhosted.org/packages/d8/f3/413bab4ff08e1fc4828dfc59996d721917df8e8583ea85385d51125dceff/pip-19.0.3-py2.py3-none-any.whl (1.4MB)
    9% |███                             | 122kB 1.7kB/s eta 0:12:00Exception:
Traceback (most recent call last):
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/cli/base_command.py", line 179, in main
    status = self.run(options, args)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/commands/install.py", line 315, in run
    resolver.resolve(requirement_set)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/resolve.py", line 131, in resolve
    self._resolve_one(requirement_set, req)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/resolve.py", line 294, in _resolve_one
    abstract_dist = self._get_abstract_dist_for(req_to_install)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/resolve.py", line 242, in _get_abstract_dist_for
    self.require_hashes
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/operations/prepare.py", line 334, in prepare_linked_requirement
    progress_bar=self.progress_bar
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/download.py", line 878, in unpack_url
    progress_bar=progress_bar
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/download.py", line 702, in unpack_http_url
    progress_bar)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/download.py", line 946, in _download_http_url
    _download_url(resp, link, content_file, hashes, progress_bar)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/download.py", line 639, in _download_url
    hashes.check_against_chunks(downloaded_chunks)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/utils/hashes.py", line 62, in check_against_chunks
    for chunk in chunks:
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/download.py", line 607, in written_chunks
    for chunk in chunks:
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/utils/ui.py", line 159, in iter
    for x in it:
  File "/tmp/tmpOuRrpM/pip.zip/pip/_internal/download.py", line 596, in resp_read
    decode_content=False):
  File "/tmp/tmpOuRrpM/pip.zip/pip/_vendor/urllib3/response.py", line 494, in stream
    data = self.read(amt=amt, decode_content=decode_content)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_vendor/urllib3/response.py", line 459, in read
    raise IncompleteRead(self._fp_bytes_read, self.length_remaining)
  File "/usr/lib/python2.7/contextlib.py", line 35, in __exit__
    self.gen.throw(type, value, traceback)
  File "/tmp/tmpOuRrpM/pip.zip/pip/_vendor/urllib3/response.py", line 365, in _error_catcher
    raise ReadTimeoutError(self._pool, None, 'Read timed out.')
ReadTimeoutError: HTTPSConnectionPool(host='files.pythonhosted.org', port=443): Read timed out.
pi@raspberrypi:~/wukong-robot $ python get-pip.py
DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 won't be maintained after that date. A future version of pip will drop support for Python 2.7.
Looking in indexes: https://pypi.org/simple, https://www.piwheels.org/simple
Collecting pip
  Retrying (Retry(total=4, connect=None, read=None, redirect=None, status=None)) after connection broken by 'NewConnectionError('<pip._vendor.urllib3.connection.VerifiedHTTPSConnection object at 0x759b22f0>: Failed to establish a new connection: [Errno 101] \xe7\xbd\x91\xe7\xbb\x9c\xe4\xb8\x8d\xe5\x8f\xaf\xe8\xbe\xbe',)': /simple/pip/
  Retrying (Retry(total=3, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLError("bad handshake: SysCallError(-1, 'Unexpected EOF')",),)': /simple/pip/
  Downloading https://files.pythonhosted.org/packages/d8/f3/413bab4ff08e1fc4828dfc59996d721917df8e8583ea85385d51125dceff/pip-19.0.3-py2.py3-none-any.whl (1.4MB)
    100% |████████████████████████████████| 1.4MB 14kB/s 
Installing collected packages: pip
  Found existing installation: pip 9.0.1
    Uninstalling pip-9.0.1:
Could not install packages due to an EnvironmentError: [Errno 13] 权限不够: '/usr/bin/pip'
Consider using the `--user` option or check the permissions.

pi@raspberrypi:~/wukong-robot $ sudo python get-pip.py
DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 won't be maintained after that date. A future version of pip will drop support for Python 2.7.
Looking in indexes: https://pypi.org/simple, https://www.piwheels.org/simple
Collecting pip
  Downloading https://files.pythonhosted.org/packages/d8/f3/413bab4ff08e1fc4828dfc59996d721917df8e8583ea85385d51125dceff/pip-19.0.3-py2.py3-none-any.whl (1.4MB)
    28% |█████████▏                      | 389kB 2.1kB/s eta 0:07:49Exception:
Traceback (most recent call last):
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/cli/base_command.py", line 179, in main
    status = self.run(options, args)
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/commands/install.py", line 315, in run
    resolver.resolve(requirement_set)
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/resolve.py", line 131, in resolve
    self._resolve_one(requirement_set, req)
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/resolve.py", line 294, in _resolve_one
    abstract_dist = self._get_abstract_dist_for(req_to_install)
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/resolve.py", line 242, in _get_abstract_dist_for
    self.require_hashes
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/operations/prepare.py", line 334, in prepare_linked_requirement
    progress_bar=self.progress_bar
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/download.py", line 878, in unpack_url
    progress_bar=progress_bar
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/download.py", line 702, in unpack_http_url
    progress_bar)
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/download.py", line 946, in _download_http_url
    _download_url(resp, link, content_file, hashes, progress_bar)
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/download.py", line 639, in _download_url
    hashes.check_against_chunks(downloaded_chunks)
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/utils/hashes.py", line 62, in check_against_chunks
    for chunk in chunks:
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/download.py", line 607, in written_chunks
    for chunk in chunks:
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/utils/ui.py", line 159, in iter
    for x in it:
  File "/tmp/tmpBjep68/pip.zip/pip/_internal/download.py", line 596, in resp_read
    decode_content=False):
  File "/tmp/tmpBjep68/pip.zip/pip/_vendor/urllib3/response.py", line 494, in stream
    data = self.read(amt=amt, decode_content=decode_content)
  File "/tmp/tmpBjep68/pip.zip/pip/_vendor/urllib3/response.py", line 459, in read
    raise IncompleteRead(self._fp_bytes_read, self.length_remaining)
  File "/usr/lib/python2.7/contextlib.py", line 35, in __exit__
    self.gen.throw(type, value, traceback)
  File "/tmp/tmpBjep68/pip.zip/pip/_vendor/urllib3/response.py", line 365, in _error_catcher
    raise ReadTimeoutError(self._pool, None, 'Read timed out.')
ReadTimeoutError: HTTPSConnectionPool(host='files.pythonhosted.org', port=443): Read timed out.


```
