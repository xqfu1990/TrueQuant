# RedisDataSource对象

实时行情数据源对象, 继承了aqalpha里面BaseDataSource对象

**属性**

* \_env: Environment对象. 包含了rqalpha所有的配置信息

**构造方法**

* \_\_init\_\_\(self, path\)

对DirectDataSource对象属性赋值

**重写的方法**

* get\_bar\(instrument, dt, frequency\)

根据order-book-id来获取对应的实时的bar的信息

参数：instrument：合约对象， frequency：周期频率， dt：当前时间

* current\_snapshot\(instrument, dt, frequency\)

获取当前的市场快照数据， 市场快照数据记录了每日从开盘到当前的数据信息，可以理解为一个动态的day bar 数据

返回一个snapshot的对象。

