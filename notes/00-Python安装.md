# Python入门

## Python安装   ubuntu自带python版本

首先是安装Python（[参考](https://www.runoob.com/python3/python3-install.html)），可以在https://www.python.org/downloads/source/选择一款安装，如果是ubuntu则安装如下，安装采用的工具是[Cloud Studio](https://cloudstudio.net/)，这是一款和VScode长得一摸一样的在线工具。

```
wget https://www.python.org/ftp/python/3.7.1/Python-3.7.1.tgz
```

下载好之后进行解压

```bash
tar -zxvf Python-3.7.1.tgz
cd Python-3.7.1
./configure
make && make install
```

然后检查Python3是否正常

```bash
python3 -V
```

进入Python的交互式编程模式

```
python3 
```

