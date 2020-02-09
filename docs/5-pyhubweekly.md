## **本期内容**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具，本期为大家推荐GitHub上4个优质的Python项目，它们分别是：

- **[tushare](https://github.com/waditu/tushare)**
- **[python-cheatsheet](https://github.com/gto76/python-cheatsheet)**
- **[vaex](https://github.com/vaexio/vaex)**
- **[sh](https://github.com/amoffat/sh)**
- **[python-small-examples](https://github.com/jackzhenguo/python-small-examples)**

下面分别来介绍一下上述5个GitHub项目。

> 我建了一个QQ学习交流群，旨在“分享、讨论、学习、资源分享、就业机会、互联网内推、共同进步！”，感兴趣的可以加一下，也可以添加我的QQ~ QQ群：164660119；QQ号：498073774；公众号：【平凡而诗意】~

## [1. tushare](https://github.com/waditu/tushare)

### **Star：8.8k**

数据作为当前很多应用场景是至关重要的一环，例如，计算机视觉、数据分析，没有数据，后续的开发工作和算法准确性就无从谈起。 我们在kaggle、ImageNet能够找到很多开放的数据资源用于我们的开发和研究工具，但是，这些数据这些数据更过的是偏重于工业，更重要的它们都是**静态数据**，也就是说不能及时的对数据进行更新迭代。 金融是数据分析应用非常多的一个方向，也是和我们生活比较密切相关的一个方向，例如，股票等。 我个人是对金融数据分析非常感兴趣，有时候就在想从哪里可以获取到充足的数据支撑自己的研究？[tushare](https://github.com/waditu/tushare)就提供了很好的解决方案。 tushare是实现对股票/期货等金融数据从数据采集、清洗加工到数据存储过程的工具，满足金融量化分析师和学习数据分析的人在数据获取方面的需求，它的特点是数据覆盖范围广，接口调用简单,响应快速。

来看一个示例，

```
>>> import tushare as ts
>>> ts.get_hist_data('600848')
2020-02-07  20.76  20.93  20.88  20.56   59584.18          0.07  ...  20.738  22.474  23.577  70873.17  58742.91  60007.62
2020-02-06  20.76  20.97  20.81  20.41   67450.28          0.01  ...  21.280  22.873  23.763  70166.75  60894.69  60617.59
2020-02-05  20.04  21.37  20.80  20.04   96036.71          0.83  ...  21.944  23.270  23.950  63541.08  59984.14  61566.66
2020-02-04  19.11  20.78  19.97  19.11  117212.70         -1.26  ...  22.582  23.704  24.114  56576.79  61412.18  59378.58
2020-02-03  21.23  21.23  21.23  21.23   14082.00         -2.36  ...  23.522  24.165  24.303  40371.67  54241.10  55358.40
```

可以看到，通过一些简单的函数即可获取一直股票的最新数据。

tushare除了支持数据采集，还支持清洗加工和数据存储。

## [2. python-cheatsheet](https://github.com/gto76/python-cheatsheet)

### **Star：10.7k**

[python-cheatsheet](https://github.com/gto76/python-cheatsheet)是一个非常全面的Python手册。

在很多系列化的教程和数据中，我们千篇一律的学习运算法、条件语句、循环语句、面向对象等。但是，对于开发过程中经常会用到的**实用知识点**却很少有系统的阐述。python-cheatsheet就弥补了这项空白，它很系统全面的介绍了Python实用知识点，它主要包括如下几个部分的内容，

- **容器**：列表、字典、集合等。
- **类型**：字符串、数字、日期、格式化等。
- **语法**：装饰器、类等。
- **数据**：JSON、pickle等。
- **高级**：多线程、运算法等。
- **模块**：NumPy、Logging等。

![img](https://pic2.zhimg.com/v2-7e754066333c6c0e3daf7bf041170569_b.png)

## [3. vaex](https://github.com/vaexio/vaex)

**Star：2.8k**

[vaex](https://github.com/vaexio/vaex)是一款类似于Pandas的的表格数据集处理和可视化工具，但是它在**大量数据**方面拥有Pandas所不具备的优势：**快速**。

vaex使用内存映射、零内存复制的策略可以实现每秒在超过**十亿**个对象的N维网格数据计算平均值、和、计数、标准差等。此外，还可以使用柱状图、密度图、三维图进行可视化。

因此，它相对于其他数据处理工具具有如下几点优势，

- 性能表现优秀
- 高效的内存处理
- 可视化
- 用户友好
- 支持jupyter
- 轻量化

## [4. sh](https://github.com/amoffat/sh)

### **Star：5.2k**

多进程是我们在开发过程中经常会接触到的场景，每当希望提升项目运行效率时，多进程就是其中备选项之一。

在Python开发中，当提到多进程是都会涉及到**subprocess**，它是Python内置的模块，因此，使用频率非常高。

今天介绍的[sh](https://github.com/amoffat/sh)是Python 2.6-3.6中subprocess非常值得尝试的替代者。

**它能够让你向调用Python函数一样去调用系统命令和程序。**

```
>>> from sh import ifconfig
>>> print(ifconfig("wlan0"))
wlan0   Link encap:Ethernet  HWaddr 00:00:00:00:00:00
        inet addr:192.168.1.100  Bcast:192.168.1.255  Mask:255.255.255.0
        inet6 addr: ffff::ffff:ffff:ffff:fff/64 Scope:Link
        UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
        RX packets:0 errors:0 dropped:0 overruns:0 frame:0
        TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
        collisions:0 txqueuelen:1000
        RX bytes:0 (0 GB)  TX bytes:0 (0 GB)
```

但是，需要指出，当前sh仅支持**Linux**和**osx**，不支持Windows。

## [5. python-small-examples](https://github.com/jackzhenguo/python-small-examples)

### **Star：1.8k**

[python-small-examples](https://github.com/jackzhenguo/python-small-examples)是一个可以在**闲暇之余**抽空看看的Python学习项目。

python-small-examples收集了Python开发过程中遇到的坑点、小样例，其中包括Python字符串和正则、Python绘图、Python日期和文件、Web开发、数据科学、机器学习、深度学习、TensorFlow、Pytorch等。

对于这个项目，没必要花费太多时间系统的去学习，可以利用空闲时间看一下，它里面总结了开发过程中经常用到的操作，当我们看到这些示例时会从中学习到很多教材上无法学到的妙用，或者Python中“不为人知”的冷门知识。

![img](https://pic4.zhimg.com/v2-60adb891a9efd5f9918c53b012bf9b17_b.png)

## **推荐阅读**

- [Python参数配置库ConfigParser详解](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484889&idx=1&sn=533d1b59410f8322a0c033afb861cfe6&chksm=e94e9ad1de3913c759960ad12db322daee45d108ebac658bf374fc3dd40f6f36f2692da23e06&token=1456867850&lang=zh_CN#rd)
- [迫不及待把这款开发神器推荐给大家！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484903&idx=1&sn=59dead902c4acc16c5149e3f838aab2d&chksm=e94e9aefde3913f9dc1bd9e584f4a76543253f0bc74354cc6230f2a49a319636e010d9ebb5db&token=1456867850&lang=zh_CN#rd)
- [抛弃bash，拥抱zsh！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484911&idx=1&sn=a02cb8db9508494672f86353acf48783&chksm=e94e9ae7de3913f137dda3702c314af3655c974f31ee7df7f79d7bb982f8f8d0f35adb751176&token=1456867850&lang=zh_CN#rd)
- [PyHubWeekly | 第四期：清理无效代码，给你的项目瘦瘦身吧！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484925&idx=1&sn=3cab27e39dfd34bff4aaa9c4b197ec3f&chksm=e94e9af5de3913e3199f96fb7a4304cb865387973b7552ec4ae77f5e4cfb4131badedbd021ff&token=1456867850&lang=zh_CN#rd)
- [实用工具 | 一款丰富强大的Python绘图工具](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484941&idx=1&sn=f5723139558043be73491df76a94da08&chksm=e94e9905de3910134d3afe346678d131fa9f01633879f58880c2e2ecfa1d8b66edaf44886ba3&token=1456867850&lang=zh_CN#rd)