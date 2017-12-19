# TradeGateway对象

交易服务器对象

**属性**

* \_env: Environment对象. 包含了rqalpha所有的配置信息
* \_retry\_times: int. 尝试连接的次数，初始为5
* \_retry\_interval: int. 每次间隔的时间，初始为1
* \_cache: DataCache对象. 数据缓存，初始为空DataCache对象
* \_query\_returns: dict. 查询结果，初始为是空字典{}
* \_data\_update\_date: date. 数据更新时间，初始是date.min，即0001-01-01
* td\_api: CtpTdApi对象. 交易服务器的api，初始为None

**构造方法**

* \_\_init\_\_\(self, env, retry\_times=5, retry\_interval=1\)

对TradeGateway对象属性赋值

注意：将 _get\_ins\_dict_\(\) 方法添加为Environment类 \(rqalpha.environment\) 的方法

```
Environment.get_ins_dict = self.get_ins_dict
```

**方法**

* _connect\(user\_id, password, broker\_id, td\_address\): _

user\_id: str. 用户Id代码

password: str. 用户密码

broker\_id: str. 经纪公司代码

td\_address: str. 交易服务器地址

return:

