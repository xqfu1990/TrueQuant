# CtpTdApi对象

实现了CTP交易API接口——TdApi

**属性**

* gateway:  gateway对象，如TradeGateway
* _\_req\_id:_ int. 操作请求编号，初始0
* connected: bool. 连接状态，初始False
* loginStatus: bool. 登录状态，初始False
* authenticated: bool.验证状态，初始False
* user\_id: str. 用户账号
* password: str. 密码
* broker\_id: str. 经纪商代码
* address: str. 交易服务器地址
* auth\_code: str. 客户端认证码，初始None
* user\_\_production\_info: \_str. 用户端产品信息，初始None
* front\_id: int. 前置编号，初始0
* session\_id: int. 会话编号，初始0
* require\_authentication: bool. 是否进行客户端身份认证，初始False
* pos\_cache: dict. 保存合约缓存对象，初始{}
* ins\_cache: dict. 保存合约代码和交易所的映射关系，初始{}
* order\_cache: dict. 保存合约代码和合约大小的映射关系，初始{}
* api\_\_name: \_str. api名称，初始“ctp\_td”

**构造方法**

* \_\__init\_\_\_\(gateway, user\_id, password, broker\_id, address, api\_name='ctp\_td'\)

  构造方法中的参数对CtpTdApi对象的属性进行赋值



