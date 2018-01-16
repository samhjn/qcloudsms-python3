# qcloudsms-python3

## 中文

腾讯云短信SDK for Python 3（官方Python SDK只兼容Python 2），修改自官方SDK。

### 用法

在本repo根目录创建下面的Python文件

```python
import json
from Sms.sms import SmsSingleSender

appid = 1000000
appkey = "ffffffffffffffffffffffffff"  
single_sender = SmsSingleSender(appid, appkey)

templ_id = 20000
phone_number = "132xxxxxxxx"
params = ["赋影", "100.00"]
result = single_sender.send_with_param("86", phone_number, templ_id, params, "", "", "")
rsp = json.loads(result)
print(rsp)
```

其余功能的具体使用与官方SDK类似，可以参考[官方SDK使用样例](https://github.com/qcloudsms/qcloudsms/blob/master/demo/python/main.py)。

**注意:** 这个例子引入SDK的方式和官方文档有所不同，目录结构较官方文档也少一层，使用的时候需自行注意这些问题。

## English

Tencent Cloud SMS SDK for Python 3 (Official Python SDK only supports Python 2), adapted from official SDK。

### Usage

Create a python file under the directory of this repo

```python
import json
from Sms.sms import SmsSingleSender

appid = 1000000
appkey = "ffffffffffffffffffffffffff"  
single_sender = SmsSingleSender(appid, appkey)

templ_id = 20000
phone_number = "132xxxxxxxx"
params = ["ShadowMov", "100.00"]
result = single_sender.send_with_param("86", phone_number, templ_id, params, "", "", "")
rsp = json.loads(result)
print(rsp)
```

The rest usage are similar to the official SDK. You can see [the official repo example](https://github.com/qcloudsms/qcloudsms/blob/master/demo/python/main.py) for help.

**Caution:** This example is slightly different from official document while importing the SDK and the directory structure is not the same. 
You should notice these problems.
