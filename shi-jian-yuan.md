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

### 事件源分类

SystemEvent：系统事件源

MarketEvent：市场及数据事件源

OrderEvent：交易事件源

