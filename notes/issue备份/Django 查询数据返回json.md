> 实际开发中，后端django常用json格式返回，本文主要介绍如何将数据库查询到的数据以json格式返回前端

## 约束json数据给前端

通常，前后端由不同的人进行开发，为了不在接口对接时产生额外的时间成本开销，最好在事先就约束好返回数据格式。在本次开发中，我们按照这样的格式进行返回：

```json
 {"res_code": 0, "message": "success","data": []}
```

由此，我们可以看出，查询结果放在data中，我们可以将查询结果返回给前端

```python
from django.http.response import JsonResponse

def test(request):
    result =  {"resCode": '0', "message": 'success',"data": []}
    user_file_set = ServerInfo.objects.all() # 查询服务器信息
    
    for user_file in user_file_set:
        user_file = UserFile.objects.get(file_id=file_info.file_id)
            data = {
                "file_id": file_info.file_id,
                "file_name": file_info.file_name,
                "user_id": user_file.user_id,
            }
            res["data"].append(data)
        return JsonResponse(res)
```



参考文章：[Django 2.1.7 查询数据返回json格式](https://juejin.im/post/6844903970385690637)

