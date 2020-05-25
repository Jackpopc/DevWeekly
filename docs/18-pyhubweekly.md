## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目PyHubWeekly**[1]，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **FlashText**
- **PyFlux**
- **bamboolib**
- **MrDoc**
- **AutoViz**

下面分别来介绍一下上述5个GitHub项目。

## FlashText

**Start：4.3k**

**FlashText**[2]是一款用于**提取**或者**替换**句子中关键字的工具。

FlashText具有诸多适合于网页爬虫或者文本处理的功能，例如，

- 提取
- 替换
- 删除
- 多关键字
- ...

有同学会有疑问，它和**正则表达式**功能大同小异，为什么要选择FlashText呢？

下面来通过一幅图对比一下两款工具在速度方面的表现，

![null](https://mmbiz.qpic.cn/mmbiz_png/sbzaBxCErLglQGybT2qc69ewNVyJVJuXS9gEOJXZyR4DSVaM6waXLgZrwSRgicVhcVQSGqQKy6BEgKMAic85s5LA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**安装使用**

可以直接使用pip命令进行安装，

```
pip install flashtext
```

可以通过一个简单的示例看一下FlashText的使用，

```
>>> from flashtext import KeywordProcessor>>> keyword_processor = KeywordProcessor()>>> # keyword_processor.add_keyword(<unclean name>, <standardised name>)>>> keyword_processor.add_keyword('Big Apple', 'New York')>>> keyword_processor.add_keyword('Bay Area')>>> keywords_found = keyword_processor.extract_keywords('I love Big Apple and Bay Area.')>>> keywords_found>>> # ['New York', 'Bay Area']
```

## PyFlux

**Start：1.7k**

**PyFlux**[3]是一款开源的时间序列分析库。

时序分析是统计学中非常重要的一个分支，在具有时序特征的数据中，往往蕴含着很多令人感兴趣的特征信息，可以根据这些信息对未来进行准确的预测。

PyFlux将推理模型（frequentist和Bayesian）和参数设置应用于时序分析中，使得时序分析变得更加容易。PyFlux具备如下特性，

•为时间序列数据建立模型•对模型进行推理•模型的检查和评估•模型修改•用模型进行回顾和预测

具体的示例，可以查看**官方文档**[4]。

## bamboolib

**Start：550**

**bamboolib**[5]是使得pandas DataFrames数据分析变得更加容易的一款Python库。

做数据相关工作的同学，对pandas肯定不会陌生。它很强大，甚至对于很多Python开发者具备着不可替代的位置，但是对于初学者却有时候让人难以理解。

bamboolib使得pandas DataFrames数据分析变得更加简单容易，在以往需要上百行完成的工作，在bamboolib中只需要简短的一行即可。

通过bamboolib的使用，它可以提升你的工作效率，减少在无价值的事情上浪费过多精力。

![null](https://mmbiz.qpic.cn/mmbiz_png/sbzaBxCErLglQGybT2qc69ewNVyJVJuXtKgXVRgV1Te3xWqupoYp5R2xPoxT0nXqt06mPMAEicNKS523Ehb1icyA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

另外，bamboolib不仅支持本地使用，还可以在jupyter notebook和jupyterLab中使用。

**安装**

下面分别是本地、jupyter notebook、jupyterLab中安装的方法，

```python
pip install bamboolib
# Jupyter Notebook extensions
python -m bamboolib install_nbextensions
# JupyterLab extensions
python -m bamboolib install_labextensions
```

## MrDoc

**Start：167**

**MrDoc**[6]基于Python开发的在线文档系统，适合作为个人和小型团队的文档、笔记、知识管理工具。

![null](https://mmbiz.qpic.cn/mmbiz_png/sbzaBxCErLglQGybT2qc69ewNVyJVJuXeYB4icfjmFBt1KOsbZeG1KkjSbbTXjG7nW4XB9ykatuGj2ZryuNpq6g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

MrDoc可以支持markdown、表格、图片上传等文档常用的功能，另外，它还具备一个完善系统应当具备的用户注册、管理等功能。可以用于团队内部的知识共享，文档管理。

另外，MrDoc已经开源，作为一个完善的应用系统，对于Python感兴趣的同学也可以拿这个项目用于学习和提升，了解一个完善系统的开发需要哪些环节，包含哪些模块，整个链路又是如何衔接的。

## AutoViz

**Start：140**

**AutoViz**[7]是一款数据集可视化工具。

通过AutoViz，一行代码就可以轻松实现数据集的可视化工作。

![null](https://mmbiz.qpic.cn/mmbiz_png/sbzaBxCErLglQGybT2qc69ewNVyJVJuXXhdPmic3cc7nVpibUZjrJzsUqfST1ZDTqAXncUfFJaVEA3SDee5qanvw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

AutoViz除了在数据可视化方面做了很多优化之外，还在数据源接口方面提供了很大的便利。它可以同时兼容txt、json、csv等离线数据格式。

**安装使用**

通过pip安装AutoViz，

```
pip install autoviz
```

使用AutoViz过程中，首先需要对AutoViz进行实例化，

```
from autoviz.AutoViz_Class 
import AutoViz_ClassAV = AutoViz_Class()
```

然后加载数据，在家在数据过程中，可以把数据加载进pandas DataFrame，也可以简单的提供一个数据路径。剩余的工作，交给AutoViz即可，

```python
filename = ""
sep = ","
dft = AV.AutoViz(filename,sep,target,df,header=0,    verbose=0,lowess=False,chart_format="svg",    max_rows_analyzed=150000,max_cols_analyzed=30,)
```

------

#### 推荐阅读

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN&scene=21#wechat_redirect)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN&scene=21#wechat_redirect)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN&scene=21#wechat_redirect)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)

------

欢迎关注我的公众号“**平凡而诗意**”，原创技术文章第一时间推送，如果喜欢，麻烦点一下“**在看**”~

![img](https://mmbiz.qpic.cn/mmbiz_png/sbzaBxCErLglQGybT2qc69ewNVyJVJuXSxwbUdHg7Lhrhic2xIvek48Dj6bRNQNatTibTJElnqBkFsRNTnIHUbBw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

#### 引用链接

`[1]` **PyHubWeekly**: *https://github.com/Jackpopc/PyHubWeekly*
`[2]` **FlashText**: *https://github.com/vi3k6i5/flashtext*
`[3]` **PyFlux**: *https://github.com/RJT1990/pyflux*
`[4]` **官方文档**: *https://pyflux.readthedocs.io/en/latest/getting_started.html*
`[5]` **bamboolib**: *https://github.com/tkrabel/bamboolib*
`[6]` **MrDoc**: *https://github.com/zmister2016/MrDoc*
`[7]` **AutoViz**: *https://github.com/AutoViML/AutoViz*