# 事件源的订阅及使用

RQAlpha大部分的组件通过**add\_listener**的方式进行注册。

```
#注册事件,并使用_init函数来响应事件。表示当该事件发生时，对应的函数进行响应。
env.event_bus.add_listener(EVENT.POST_SYSTEM_INIT,self._init)
```

```
def _init(self, event):
       print("系统初始化了")
       
```



