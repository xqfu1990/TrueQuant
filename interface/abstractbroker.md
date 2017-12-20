# 介绍

券商接口。

券商代理模块：用户的所有下单、账户、撮合逻辑其实都来自于券商+交易所，即使是回测，也实际是一个回测模拟交易所。因此可以通过扩展该模块来自定义Broker，也可以通过该模块扩展实盘交易等。

RQAlpha将产生的订单提交给此对象，此对象负责对订单进行撮合（不论是自行撮合还是委托给外部的真实交易所），并通事件将撮合结果反馈进入RQAlpha。

在mod中，可以通过调用\`\`env.set\_broker\`\`来替换默认的Broker。

**抽象方法**

* get\_portfolio\(self\): 获取投资组合。

系统初始化时，会调用此接口，获取包含账户信息、净值、份额等内容的投资组合

* submit\_order\(self, order\): 提交订单。

在当前版本，RQAlpha会生成:class:\`~Order\`对象，再通过此接口提交到Broker。

TBD: 由Broker对象生成 Order 并返回？

* cancel\_order\(self, order\): 撤单。

order: 订单

* get\_open\_orders\(self,order\_book\_id=None\): 获得当前未完成的订单

返回：list\[:class:\`~Order\`\]

