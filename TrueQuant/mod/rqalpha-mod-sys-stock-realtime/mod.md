# RealtimeTradeMod对象

模拟交易，实盘交易mod类。实现了RQalpha中的AbstractMod接口。

**重写的方法**

* startup\(env, mod\_config\)

参数：env： Environment对象. 包含了rqalpha所有的配置信息

            mod\_config: 

根据order-book-id来获取对应的实时的bar的信息

参数：instrument：合约对象， frequency：周期频率， dt：当前时间

* current\_snapshot\(instrument, dt, frequency\)

获取当前的市场快照数据， 市场快照数据记录了每日从开盘到当前的数据信息，可以理解为一个动态的day bar 数据

返回一个snapshot的对象。

