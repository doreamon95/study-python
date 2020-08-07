# Python入门

## Python安装   ubuntu自带python版本

首先是安装Python（[参考](https://www.runoob.com/python3/python3-install.html)），可以在https://www.python.org/downloads/source/选择一款安装，如果是Ubuntu，则自带Python环境，若Ubuntu下自行安装版本，比如安装3.7.1，则执行下列版本：

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

