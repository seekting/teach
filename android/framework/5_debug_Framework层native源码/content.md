# debug Framework层native源码

> 作者:seekting

在有源码的情况下，采用lldb的方式

1. 进EditConfig

2. 在debug里选native

3. 通过debug方式启动app  会看到加载很多so的画面


4. 在debug那一栏 点击pause按钮


5. 添加一个要debug的方法

```shell
br s -n nativeScheduleVsync
```

7. 添加文件关联:

```shell
Lines found in module `libandroid_runtime.so
```
8. 映射代码
```c {.line-numbers}
settings set target.source-map frameworks/base/ /home/seekting/work/sources/android6.0_r77/frameworks/base
```

lldb的一些命令

```shell
#查看断点数
breakpoint list
#删除断点
breakpoint delete 1
```

