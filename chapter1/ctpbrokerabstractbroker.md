# 介绍

CTP券商接口类。实现了rqalpha中的AbstractBroker。

ctp\_broker.py文件下。

Rqalpha将产生的订单提交给此对象，此对象负责对订单进行撮合（不论是自行撮合还是委托给外部的真实交易所），并通过**EVENT.ORDER\_\*** 及 **EVENT.TRADE** 事件将撮合结果反馈进入Rqapha。

**属性**

* self.\_env
* self.\__trade_\_gateway
* self.\__open_\_orders   默认值: \[\]

**重写的方法**

* cancel\_order\(order\)

  撤单。

参数

* 


