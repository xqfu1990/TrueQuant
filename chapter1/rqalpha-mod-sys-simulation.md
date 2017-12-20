# 介绍

它是RQAlpha整个回测模块。其中定义了基于Bar回测的`event_source`和`simulation_broker`，其中包含了MarketEvent和OrderEvent大部分事件源的定义和发布。

# Config

    # 是否开启信号模式。信号模式：不进行撮合，直接成交
    "signal":False,

    # 启用的回测引擎
    # 非tick级的回测只支持 `current_bar` (当前Bar收盘价撮合) 和 `next_bar` (下一个Bar开盘价撮合)
    # tick级的回测支持'last'、'best_own'、'best_counterparty'
    "matching_type":"current_bar",

    # 设置滑点
    "slippage":0,

    # 设置手续费乘数，默认为1
    "commission_multiplier":1,

    # price_limit:在处于涨跌停时，无法买进/卖出，默认开启【在Signal模式下，不再禁止买进/卖出，如果开启，则给出警告提示。】
    "price_limit":True,

    # liquidity_limit:当对手盘没有流动性的时候，无法买进/卖出，默认关闭
    "liquidity_limit":False,

    # 是否有成交量限制
    "volume_limit":True,

    # 按照当前成交量的百分比进行撮合
    "volume_percent":0.25,



