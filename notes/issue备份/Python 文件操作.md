> 本文针对近期的文件操作进行小结，包括文件是否存在、创建文件、获取文件路径

## 1. 文件是否存在

通常，在创建文件之间会查看文件是否存在，如果不存在则创建，Python中代码如下：

```python
import os
if not os.path.exists('foldername'):
    os.mkdirs('foldername')
```

