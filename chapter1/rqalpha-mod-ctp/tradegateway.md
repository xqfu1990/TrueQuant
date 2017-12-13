# TradeGateway对象

交易服务器对象

**属性**

_\_env:  环境，需要构造对象是赋值，是个对象，里面包含了rqalpha所有的配置信息_

_\_retry\_times: 尝试连接的次数，默认5次_

\__retry\_interval:每次间隔的时间，默认1秒_

_\_cache: 缓存，DataCache\(\)对象_

\__query\_returns: 查询结果，默认是空字典{}_

_\_data\_update\_date: 数据更新时间，默认是date.min，即0001-01-01_

_td\_api:交易服务器的api，默认是None_

**注意：构造方法中**

将 _get\_ins\_dict_\(\) 方法添加为Environment类 \(rqalpha.environment\) 的方法

```
Environment.get_ins_dict = self.get_ins_dict
```

**方法**

_connect\(user\_id, password, broker\_id, td\_address\): _

user\_id: str. 用户Id代码

password: str. 用户密码

broker\_id: str. 经纪公司代码

td\_address: str. 交易服务器地址

return: 

