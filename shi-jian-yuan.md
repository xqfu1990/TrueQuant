# 事件源的订阅及使用

RQAlpha大部分的组件通过**add\_listener**的方式进行注册。

```
from rqalpha.events import EVENT
#注册事件,并使用_init函数来响应事件。表示当该事件发生时，对应的函数进行响应。
#系统初始化后运行_init()函数
env.event_bus.add_listener(EVENT.POST_SYSTEM_INIT,self._init)
```

```
def _init(self, event):
    print("系统初始化了")
```

当Bar数据生成，则会触发

* `EVENT.BAR`事件，那么用户的`handle_bar`相关的代码注册了该事件则会立即执行。
* 当订单成交，则会触发`EVENT.TRADE`事件，那么系统的账户模块因为注册了该事件，就可以立即计算成交以后的收益和资金变化。
* 当订单下单，则会触发`EVENT.ORDER_PENDING_NEW`事件，前端风控模块注册了该事件，则可以立即对该订单进行审核，如果不满足风控要求，则直接指定执行`order._cancel(some_reason)`来保证有问题的订单不会进入实际下单环节。

# 事件源分类

SystemEvent：系统事件源

MarketEvent：市场及数据事件源

OrderEvent：交易事件源

# 事件源的扩展

事件发布：publish\_event

