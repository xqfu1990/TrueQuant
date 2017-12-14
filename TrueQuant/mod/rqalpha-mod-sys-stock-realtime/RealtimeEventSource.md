# RealtimeEventSource对象

实时事件源，RQalpha从此对象中获取事件，驱动整个事件循环

**属性**

* \_env: Environment对象. 包含了rqalpha所有的配置信息
* mod\_config：这个mod的配置文件
* fps：停留时间，设定程序加入新的事件的间隔时间
* event\_queue：事件队列
* before-trading-fire-date:  上一次触发before\_trading事件的日期
* after-trading-fire-date: 上一次触发after\_trading事件的日期
* settlement-fire-date: 上一次触发settlement事件的日期

**构造方法**

* \_\_init\_\_\(self, path\)

对RealtimeEventSource对象属性初始化

**方法：**

* set\_state\( state\)

根据order-book-id来获取对应的实时的bar的信息

参数：instrument：合约对象， frequency：周期频率， dt：当前时间

* quotation\_worker\(\)

实时从tushare中获取行情数据

* clock\_worker\(\)

实时运行：判断before-trading事件, after-trading事件, settlement事件, 接收到新k线产生的事件触发时间，并且推送这些事件

**扩展方法：**

* event \(\)

事件发生器，提取事件队列里面最先推送的事件，并逐个返回事件

