# 介绍

**属性**

* \_env: Environment类
* \_config: dict. 配置文档
* \__universe_\_changed: bool. 策略证券池是否发生了变化



**方法**

events\(start\__date, end_\_dtae, frequnency\)

events函数是一个generator, 在rqalpha\_mod\_sys\_simulation 中主要返回`BEFORE_TRADING`,`BAR`,`AFTER_TRADING`和`SETTLEMENT`事件。RQAlpha 在接受到对应的事件后，会自动的进行相应的publish\_event操作，并且会自动 publish 相关的PRE\_和POST\_事件。

