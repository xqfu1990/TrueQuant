# 介绍

CTP券商接口类。实现了rqalpha中的AbstractBroker。

ctp\_broker.py文件下。

Rqalpha将产生的订单提交给此对象，此对象负责对订单进行撮合（不论是自行撮合还是委托给外部的真实交易所），并通过EVENT.ORDER\_\* 及 EVENT.TRADE 事件将撮合结果反馈进入Rqapha。

