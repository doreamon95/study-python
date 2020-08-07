> 在Django中可以利用ORM来根据models.py来自动创建数据库表，那如果向要直接利用数据库表该如何操作呢？本文针对该需求，进行一步步说明。

## 开始

如果您是开始一个新的项目，那么建议您创建项目和创建app，再执行下列操作。下面默认您已经拥有一个项目和一个app。

**第一步**，您需要配置连接数据库，命令如下：<注意：该修改在**项目同名文件夹**下的settings.py中修改>

```python
# setting.py 
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': '<你的mysql数据库名>',
        'USER': '<mysql用户名>',
        'PASSWORD': '<mysql密码>',
        'HOST': '127.0.0.1',
        'PORT': 3306
    }
}
```

然后，您需要在项目同名文件夹下的`_init_.py`中添加mysql，命令如下：

```python
import pymysql
pymysql.install_as_MySQLdb()
```

**第二步**，确认您已经有数据库，注意，数据库中一张表对应model中一个类。

**第三步**，反向生成models.py，在这里您需要先执行以下命令，告诉django通过setting中的databases配置来找到您的数据库表，并输出对应的models.py。

```bash
# 该命令在项目根目录下执行，执行结果是直接输出到终端窗口
python .\manage.py inspectdb
```

如果您检查终端窗口输出的结果无误，那么您可以将其输出到文件夹中，比如输出到 testapp/models.py 中。

```
python manage.py inspectdb > testapp/models.py
```

**第四步**，由于inspectdb创建的表中`managed=False`，其代表Django不能对该表进行增、删、改操作。因此，我们需要修改它，确保能够将改动应用到数据库表。

```python
# 修改models.py中的每一张表，为True
managed=True
```

---



