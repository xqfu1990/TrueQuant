# 介绍

每一个Mod都遵循扩展事件源的细则，通过对接接口即可实现各种逻辑的组合，而Mod接口是扩展事件源的标准格式，所以我们在添加或修改rqalpha指定功能时，通过是否启用Mod来实现。

#### 自定义Mod

在源代码路径下**新建python包，**命名规则为**rqalpha\_mod\_MyModName**，包下新建python文件mod.py。该mod.py含有一个Mod类，它必须实现rqalpha.interface.AbstractMod类。

Mod类中含有两个必须重写的方法：start\_up和 tear\_down.

start\_up：RQAlpha 在系统启动时会调用此接口；在此接口中，可以通过调用 \`\`env\`\` 的相应方法来覆盖系统默认组件。

tear\_down：RQAlpha 在系统退出前会调用此接口。







