# 事件源的订阅及使用

RQAlpha大部分的组件通过**add\_listener**的方式进行注册。

\#

_env.event\_bus.add\_listener\(EVENT.POST\_SYSTEM\_INIT, self.\_init\)_

```
#注册事件,并使用_init和_tick两个函数来响应事件。表示当该事件发生时，对应的函数进行响应。
env.event_bus.add_listener(EVENT.POST_SYSTEM_INIT,self._init)
```

```
def _init(self, event):
        """
        初始化progressBar,进度条的长度作为回测的总时长
        :return:
        """
        pass
```



