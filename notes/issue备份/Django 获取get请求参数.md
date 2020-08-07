> 本文介绍Django获取get请求参数的两种方式。
>
> 写在前面：新版的path取代了之前的url，当前写路由时候不能直接利用`path`写正则表达式，而需要使用`re_path`写。

方式1：

- 当get网址类型是`127.0.0.1:8000/showupload/20/7\`时，在项目同名文件夹下的urls.py里面写

```python
from django.urls import re_path,path
from files.views import *

urlpatterns = [
	re_path('^showupload/(\d+)/(\d+)/$', showUploadFile), # 上传文件
]
```

获取参数时，需要注意对应的函数的参数个数和`upload/(\d+)/(\d+)`一致，比如下图所示，则参数取出来

```python
def showUploadFile(request,uid,fid):
```

- 当get网址类型是`127.0.0.1:8000/query/20/hello`时，在项目同名文件夹下的urls.py里面写

```python
from django.urls import re_path,path
from files.views import *

urlpatterns = [
	re_path(r'^query/(?P<uid>\d+)/(?P<filename>\w+)/$', queryFile), # 上传文件
]
```

获取参数时，需要注意对应的函数的参数必须为规则中的名称，比如下图所示，则参数取出来

```python
def queryFile(request,uid,filename):
```

方式2：

当get网址类型是`127.0.0.1:8000/fileinfo/?uid=20&fid=7`时，在项目同名文件夹下的urls.py里面写

```python
from django.urls import re_path,path
from files.views import *

urlpatterns = [
	re_path(r'^showupload/$', showUploadFile), # 查询
]
```

通过request.GET获取请求携带的参数

```python
def info(request):
    if request.method=='GET':
        uid=request.GET.get('uid',default='0')
        fid=request.GET.get('fid',default='0')
```

