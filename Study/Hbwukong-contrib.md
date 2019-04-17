# 安装第三方库  
 
安装成功 

## 流程
```
mkdir $HOME/.wukong
cd $HOME/.wukong
git clone http://github.com/wzpan/wukong-contrib contrib
pip3 install -r contrib/requirements.txt
```


### 细节 

```
pi@raspberrypi:~ $ mkdir $HOME/.wukong
pi@raspberrypi:~ $ ls
aawukong-robot   MagPi                              swig-3.0.10
changeSource.sh  Music                              swig-3.0.10.tar.gz
Desktop          node-v10.15.3-linux-armv7l.tar.xz  Templates
Documents        Pictures                           Videos
Downloads        Public                             wukong-robot
install.sh       snowboy.tar.bz2
pi@raspberrypi:~ $ cd /home
pi@raspberrypi:/home $ cd /home
pi@raspberrypi:/home $ cd /home
pi@raspberrypi:/home $ mkdir $HOME/.wukong
mkdir: 无法创建目录"/home/pi/.wukong": 文件已存在
pi@raspberrypi:/home $ cd /home
pi@raspberrypi:/home $ cd $HOME/.wukong
pi@raspberrypi:~/.wukong $ git clone http://github.com/wzpan/wukong-contrib contrib
正克隆到 'contrib'...
remote: Enumerating objects: 15, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 1077 (delta 6), reused 10 (delta 4), pack-reused 1062
接收对象中: 100% (1077/1077), 309.79 KiB | 391.00 KiB/s, 完成.
处理 delta 中: 100% (669/669), 完成.
pi@raspberrypi:~/.wukong $ pip3 install -r contrib/requirements.txt
Looking in indexes: https://pypi.org/simple, https://www.piwheels.org/simple
Collecting paho-mqtt>=1.3.0 (from -r contrib/requirements.txt (line 1))
  Downloading https://www.piwheels.org/simple/paho-mqtt/paho_mqtt-1.4.0-py3-none-any.whl (48kB)
    100% |████████████████████████████████| 51kB 98kB/s 
Collecting eyeD3>=0.8 (from -r contrib/requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/75/66/b1d97f06499199b3b3dfcd25e3f000c4256e7f313b3a0aae2e3d24e6acb7/eyeD3-0.8.10-py2.py3-none-any.whl (147kB)
    100% |████████████████████████████████| 153kB 208kB/s 
Requirement already satisfied: six in /usr/lib/python3/dist-packages (from eyeD3>=0.8->-r contrib/requirements.txt (line 2)) (1.12.0)
Collecting python-magic (from eyeD3>=0.8->-r contrib/requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/42/a1/76d30c79992e3750dac6790ce16f056f870d368ba142f83f75f694d93001/python_magic-0.4.15-py2.py3-none-any.whl
Installing collected packages: paho-mqtt, python-magic, eyeD3
Could not install packages due to an EnvironmentError: [Errno 13] 权限不够: '/usr/local/lib/python3.5/dist-packages/paho_mqtt-1.4.0.dist-info'
Consider using the `--user` option or check the permissions.

pi@raspberrypi:~/.wukong $ sudo pip3 install -r contrib/requirements.txt
Looking in indexes: https://pypi.org/simple, https://www.piwheels.org/simple
Collecting paho-mqtt>=1.3.0 (from -r contrib/requirements.txt (line 1))
  Downloading https://www.piwheels.org/simple/paho-mqtt/paho_mqtt-1.4.0-py3-none-any.whl (48kB)
    100% |████████████████████████████████| 51kB 101kB/s 
Collecting eyeD3>=0.8 (from -r contrib/requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/75/66/b1d97f06499199b3b3dfcd25e3f000c4256e7f313b3a0aae2e3d24e6acb7/eyeD3-0.8.10-py2.py3-none-any.whl (147kB)
    100% |████████████████████████████████| 153kB 56kB/s 
Collecting python-magic (from eyeD3>=0.8->-r contrib/requirements.txt (line 2))
  Downloading https://files.pythonhosted.org/packages/42/a1/76d30c79992e3750dac6790ce16f056f870d368ba142f83f75f694d93001/python_magic-0.4.15-py2.py3-none-any.whl
Requirement already satisfied: six in /usr/lib/python3/dist-packages (from eyeD3>=0.8->-r contrib/requirements.txt (line 2)) (1.12.0)
Installing collected packages: paho-mqtt, python-magic, eyeD3
Successfully installed eyeD3-0.8.10 paho-mqtt-1.4.0 python-magic-0.4.15
```