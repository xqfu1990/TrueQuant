# 介绍

券商接口。

RQAlpha将产生的订单提交给此对象，此对象负责对订单进行撮合（不论是自行撮合还是委托给外部的真实交易所），并通过\`\`EVENT.ORDER\_\*\`\`及\`\`EVENT.TRADE\`\`事件将撮合结果反馈进入RQAlpha。

在mod中，可以通过调用\`\`env.set\_broker\`\`来替换默认的Broker。

**抽象方法**

* get\_portfolio\(self\): 获取投资组合。

系统初始化时，会调用此接口，获取包含账户信息、净值、份额等内容的投资组合

* submit\_order\(self, order\): 提交订单。

在当前版本，RQAlpha会生成:class:\`~Order\`对象，再通过此接口提交到Broker。

TBD: 由Broker对象生成 Order 并返回？

* cancel\_order\(self, order\): 撤单。

order: 订单



