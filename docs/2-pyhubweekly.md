[TOC]

# 前言

上一周，我写了一篇总结GitHub上优质Python项目的文章，文章发出之后在公众号和知乎受到很多同学的喜爱和认可，这有一些出乎我的意料。

思索一下，这的确是一件很值得去做的事情。<!--more-->这一年来我养成了一个每天逛一逛GitHub的习惯，因为我个人对新鲜事物充满着好奇心，或者是有趣的项目、或者是实用的小工具，我期望能够在GitHub上能够遇到我想要的东西。

GitHub是一个鱼龙混杂的地方，上面的确有很多不错的开源项目，但是，更多的是一些灌水的项目，例如，某些教育机构的大作业，例如，那些每天刷榜的中文无聊的项目。因此，虽然我每天都会花费一部分时间去浏览GitHub，但是真正让我内心觉得这个项目“不错”的却少之又少。我想，也许这就是为什么我上一篇文章受到认可的原因吧。

既然这样，我想倒不如花费一部分精力去开辟一些专门介绍GitHub上优质Python项目的版块，名称就叫PyHubWeekly，主要宗旨有两点：

- 每周更新一次
- 精选GitHub上优质Python项目

对于这个模块，我的想法是不追求数量而追求质量，换句话说，也许有的时候能介绍10个项目，有的时候只介绍1个项目，不会为了拼凑数量而一味的去美化一个项目，把它描绘的天花乱坠。也许有一天Python被淘汰了，而且优质的项目有穷有尽，再或者各位关注者对于这类文章失去了兴趣，那样的话，PyHubWeekly这个版块也就走到了尽头。

另外，针对PyHubWeekly，我的定位是通过每篇文章去介绍一些有趣，值得去了解的GitHub项目，因此，对于每个项目不会去深入介绍，会简单的介绍一些它的功能以及它的特点。如果其中我个人认为哪个项目非常不错，或者各位同学对于哪个项目特别感兴趣，我会单独再写一篇详细介绍这个项目的文章。

当然，无论写哪方面的文章，出发点都会坚持自己的初心，坚持原创、坚持与众不同，希望自己分享能够切实的帮助到需要的同学。

下面就开始介绍本期的5个项目。

# [1. Gooey](https://github.com/chriskiehl/Gooey)

Star：8.5k

这是一个将Python 2或3控制台程序转换为GUI应用程序工具，

![img](https://pic2.zhimg.com/v2-638b01130536811089db1673d2fec7cd_b.png)

Gooey通过简单的在argarse上调用装饰器的方式就可以实现程序的界面化，如果需要进行更精细的调整，则可以使用嵌入式替换GooeyParser代替ArgumentParser，

![img](https://pic2.zhimg.com/v2-fabcc09d55ae4da7ff0a522e921658b1_b.gif)

# [2. memory_profiler](https://github.com/pythonprofilers/memory_profiler)

Star：2k

Python是一门相对简单的编程语言，这里所说的简单是指入门简单。因此，很多人忽略了程序底层的内容，例如，空间复杂度、时间复杂度等。对于很多人来说写完程序能够跑通即可，但是一个好的程序要兼备考虑程序的复杂度、内存占用等。

这是一个依赖于psutil的python模块，用于**监视进程的内存消耗**，以及对python程序的内存消耗进行逐行分析。

```python
@profile
def my_func():
    a = [1] * (10 ** 6)
    b = [2] * (2 * 10 ** 7)
    del b
    return a

if __name__ == '__main__':
    my_func()
```

执行程序，

```
$ python -m memory_profiler example.py
Line #    Mem usage  Increment   Line Contents
==============================================
     3                           @profile
     4      5.97 MB    0.00 MB   def my_func():
     5     13.61 MB    7.64 MB       a = [1] * (10 ** 6)
     6    166.20 MB  152.59 MB       b = [2] * (2 * 10 ** 7)
     7     13.61 MB -152.59 MB       del b
     8     13.61 MB    0.00 MB       return a
```

# [3. pyecharts](https://github.com/pyecharts/pyecharts)

Star：7.8k

在Python开发中，提到画图应该十有八九会想到matplotlib，它是一个老牌且强大的绘图库，但是，在使用过程中有一些弊端，例如，不适合离线查看、支持的绘图接口较为单一。

Echarts 是一个由百度开源的数据可视化，凭借着良好的交互性，精巧的图表设计，得到了众多开发者的认可。而 Python 是一门富有表达力的语言，很适合用于数据处理。当数据分析遇上数据可视化时，pyecharts 诞生了。它能够把绘图结果保存为一个html文件，能够动态展示绘图结果，且随时可以打开查看。另外，它支持的绘图类型非常丰富。

![img](https://pic3.zhimg.com/v2-61b9e0cf9eaef7b9fc27fe0a436d110a_b.gif)

# [4. wtfpython](https://github.com/satwikkansal/wtfpython)

Star：18.6k

wtfpython这个Python项目两年前就有所耳闻，首先说一下它的全名，比较粗俗“What the f*ck Python!”，就如同前面所说的那样，虽然很多人认为Python非常容易，但是它也有很多不为人知的特性。

有很多点按照我们的理解应该是这样的，但是当运行之后却发现和我期望的结果有很大出入，具体问题出现在哪了，却很难找出来。wtfpython这个项目就总结了这些不为人知的特性，能够让你发现更多Python令人惊奇的地方。

例如，下面这个例子，

```python
some_dict = {}
some_dict[5.5] = "Ruby"
some_dict[5.0] = "JavaScript"
some_dict[5] = "Python"
```

输出，

```python
>>> some_dict[5.5]
"Ruby"
>>> some_dict[5.0]
"Python"
>>> some_dict[5]
"Python"
```

按照正常的结果some_dict[5.0]不是应该输出“JavaScript”吗？为什么输出了“Python”?下面就是解释，

![img](https://pic3.zhimg.com/v2-69a494a204e918d2859f58a7e9929a02_b.png)

# [5. tqdm](https://github.com/tqdm/tqdm)

Star：12.9k

tqdm是一个Python进度条工具，如果刚开始学习Python时，我会对它不屑一顾，编程语言本身还没有学明白，为什么要用这些花里胡哨的东西？简直就是鸡肋！

但是，当开发项目久了以后才发现，它有着不可替代的价值。就如同我们排号吃饭一样，我们希望实时的监控着当前事件进行到什么程度了，Python开发也是这样，我们不能一直把它挂在那里，留给我们一个空白的shell，具体是进程死掉了，还是读数据库时出现了问题，都不清楚，有着这个进度条，能够对我们的运行过程一目了然。

![img](https://pic1.zhimg.com/v2-d86fe22b4b42866e86b4c98fb31ae8c0_b.gif)

------

> 我建了一个QQ学习交流群，旨在“分享、讨论、学习、资源分享、就业机会、互联网内推、共同进步！”，感兴趣的可以加一下，也可以添加我的QQ~ QQ群：1002821945；QQ号：498073774；公众号：【平凡而诗意】~

# 更多精彩内容

[实用工具 | 2款播放器让你免费听遍全网无损音乐](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484869&idx=1&sn=9a0208776292d69fa4657819f3662a2a&chksm=e94e9acdde3913db34f753cde062f7ebd68ba9d0622c09d525953a6d95a424c758d199916b68#rd)

[大数据 | Spark机器学习工作流开发指南](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484860&idx=1&sn=a18e7e9846006668e2e3989e85e2a6b2&chksm=e94e9ab4de3913a207f69307e1386c9b4f173a9aa85f89170db2f99b6886fb692da6ce8b85c1#rd)

[实用工具 | 你距离PS大神只差这6款免费在线工具！](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484855&idx=1&sn=0ed13e66d4e2bb8b44a1c53e422ec248&chksm=e94e9abfde3913a9962d2abf156115165cbf9337ef375ea1c02ac88b9eba4e9285b12143e353#rd)

[简易教程 | 分布式消息发布订阅系统Kafka从搭建到使用](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484849&idx=1&sn=7b22b424678c9917c6327168a641a117&chksm=e94e9ab9de3913af50f1bf3412a402f3bf27b4abd50678f153d07778e61ac9a21b4a4bdce2cc&token=326900528&lang=zh_CN#rd)

[教程 | 一文搭建你的第一个免费专属博客](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484843&idx=1&sn=288496d86fa5113204c0c72b15b8b082&chksm=e94e9aa3de3913b562153b73d6214eb4a09e4ba0177ae7f0476437494c5f45408af4cf894e66#rd)

[办公效率 | 让你突飞猛进的10个Word技能](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484829&idx=1&sn=a607a218cf19bf24fb4ddac599c4196c&chksm=e94e9a95de391383cb33494a8b5dffd1565617cfd1b79c3e97c4da64517d5d16d632f1915d96#rd)

[学习工具 | 推荐10款提升自己的优质APP](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484812&idx=1&sn=70be06850fa9e001ec5f5b1aa53dff7c&chksm=e94e9a84de391392ac32e8365474317f209113bec08b3d0acedb32fc845c755b61b20d83af2b#rd)

[Google | Python编程规范指南](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484788&idx=1&sn=24ce3cec2d248f11eb8a82908f921ec6&chksm=e94e9a7cde39136a0eda417946a45513be5c8500f77b6ead2f7824c930ebd8e90cc21fede9fa#rd)