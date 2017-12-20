# 介绍

券商接口。

RQAlpha将产生的订单提交给此对象，此对象负责对订单进行撮合（不论是自行撮合还是委托给外部的真实交易所），并通过\`\`EVENT.ORDER\_\*\`\`及\`\`EVENT.TRADE\`\`事件将撮合结果反馈进入RQAlpha。

在mod中，可以通过调用\`\`env.set\_broker\`\`来替换默认的Broker。



