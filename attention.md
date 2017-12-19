# 目前仍需改进的地方

**回测问题**

1. 股票类每笔交易时的手续费（买入时佣金万分之三，卖出时佣金万分之三加千分之一印花税, 每笔交易佣金最低扣5块钱）
2. 日线回测，每天15:00发出交易信号——&gt;修改成每天9:30发出交易信号

rqalpha\_mod\_sys\_accounts\account\_model\benchmark\_account.py  修改

```
# 以收盘价进行购买
price=event.bar_dict[self.benchmark].open
```

D:\Program Files \(x86\)\Anaconda3\Lib\site-packages\rqalpha\mod\rqalpha\_mod\_sys\_simulation\simulation\_event\_source.py



**数据问题**

1. 动态复权模式——数据问题

# 



