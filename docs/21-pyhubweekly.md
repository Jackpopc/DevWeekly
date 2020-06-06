## **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **mplfinance**
- **rich** 
- **babel**
- **imgaug**
- **xxh**

下面分别来介绍一下上述5个GitHub项目。

## **mplfinance**

**Star：371**

[**mplfinance**](https://github.com/search?q=mplfinance)是一款将matplotlib应用于金融数据可视化的工具。

**mpl**正是matplotlib的缩写。

此前我在文章[**6款Python可视化工具，总有一款适合你！**](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485416&idx=1&sn=d23a1c7cc5658f4bed12d67d76275d98&chksm=e94e98e0de3911f6268346f5a8ecdad565a7a93e0cd40d1a6e96b0ad0517d53d2efeccf70c45&token=1074758556&lang=zh_CN#rd)介绍了6款Python可视化工具。但是，Python的应用场景远不于此，需要用到可视化的场景也是数不胜数。

而金融作为一个较为热门又比较特别的方向，对数据可视化需求也非常大。

mplfinance就是一款由著名的matplotlib开发团队开发的一款专门针对金融数据可视化的工具。

**安装与使用**

通过pip命令安装，

```
pip install --upgrade mplfinance
```

下面看一下mplfinance的使用示例，

```
import mplfinance as mpf
daily = pd.read_csv('examples/data/SP500_NOV2019_Hist.csv',index_col=0,parse_dates=True)
daily.index.name = 'Date'
mpf.plot(daily,type='candle',mav=(3,6,9),volume=True,show_nontrading=True)
```

![img](https://pic4.zhimg.com/v2-6b54a44d6a54c627b3cc3bb6968896bb_b.png)

## **rich**

**Star：7k**

[**rich**](https://github.com/willmcgugan/rich)是一款美化终端富文本内容的命令行工具。

在终端下使用Python过程中，内容会以同样的颜色进行展示，不能像IDE中那样根据语法进行高亮显示。这样，文本的辨识度、阅读效率就会降低很多。

rich可以让终端下富文本以彩色形式进行显示，辨识度更高，像很多成熟的IDE一样。

```
from rich import print

print("Hello, [bold magenta]World[/bold magenta]!", ":vampire:", locals())
```

![img](https://pic2.zhimg.com/v2-f3b4f3ca58c850d871282731e74d0d11_b.png)

## **babel**

**Star：892**

[**babel**](https://github.com/python-babel/babel)是一个实用程序的集合，它帮助实现Python应用程序国际化和本地化。

不同国家、地区对同样的内容表示方式是截然不同的，例如，数字、日期等。

babel就是这样一款工具，帮助你实现Python程序适用于不同国家和地区，你不需要再去写复杂的逻辑来获取所在国家信息，然后修改相应的日期、数字格式，babel一行代码就可以搞定。

**时间**

```
>>> from datetime import date, datetime, time
>>> from babel.dates import format_date, format_datetime, format_time

>>> d = date(2007, 4, 1)
>>> format_date(d, locale='en')
u'Apr 1, 2007'
>>> format_date(d, locale='de_DE')
u'01.04.2007'
```

**数字**

```
>>> format_decimal(1.2345, locale='en_US')
u'1.234'
>>> format_decimal(1.2345, locale='sv_SE')
u'1,234'
>>> format_decimal(12345, locale='de_DE')
u'12.345'
```

## **imgaug**

**Star：9.2k**

[**imgaug**](https://github.com/aleju/imgaug)是一款快速、高效的图像增广库。

数据集在人工智能领域占据着至关重要的地位，无论是算法描绘的多么天花乱坠，如果没有数据集，它的价值也无从谈起。

而且，对于很多从事计算机视觉、自然语言等领域相关同学而言，都非常清楚日常工作绝大多数时间都是在与数据在打交道。

这里面比较重要的一点就是图像增广，我曾在《动手学计算机视觉》系列课程中一节专门介绍过这项工作，能够用于扩充数据集，弥补计算机视觉中图像不足的问题。

但是，以往需要自己手动开发一定工作量。

imgaug就解决了这个问题，它具有高斯噪声、对比度、仿射变换、旋转等常用的图像增广功能，只需要少量的代码就可以生成图像增广序列。

![img](https://pic1.zhimg.com/v2-ec98c660cae979ae9b08edc0a5a96004_b.png)

## **xxh**

**Star：915**

[**xxh**](https://github.com/xxh/xxh)是一款让你随时随地可以使用自己喜欢shell的工具。

使用Linux、Mac过程中，默认的shell样式、功能都差强人意，因此，一些出色的开发者就开发出了很多不错的shell工具，例如，

- zsh
- fish
- xonsh
- osquery

但是，这也有一些地方让人使用起来很不舒服，比如，每次登录ssh后需要重复执行环境变量配置文件，而且在不同用户权限下是无法使用的。

xxh就解决了这一个问题，它让你在不进行root访问和系统安装的情况下，将你最喜欢的shell带到登录ssh的任何地方。

![img](https://pic4.zhimg.com/v2-b2205f5a33aa1c9642116f15067ed2a3_b.gif)

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN&scene=21#wechat_redirect)