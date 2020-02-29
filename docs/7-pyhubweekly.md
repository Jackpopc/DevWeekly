### **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具，本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **black**
- **musicbox**
- **nba_api**
- **akshare**
- **helium**

下面分别来介绍一下上述5个GitHub项目。

## **black**

**Start：14.9k**

[**black**](https://github.com/psf/black)是一款强大的Python**代码格式化工具**，通过使用black，可以解放双手，再也不用手动调整代码格式了。

black参照**PEP**格式规范，它能够格式化字符串、消除空行、修改代码长度等。另外，相对于大多数代码格式化工具，它具有**更加快速**、**更见简便**的优点，它能够让你在代码格式化方面节省更多时间和精力。

black的安装和使用也非常简单，下面来简单的介绍一下。

**安装**

```
pip install black
```

**使用**

```
black {source_file_or_directory}
```

下面来举一个例子，来看一下它的效果。

**示例代码**

```
# test.py
j = [1,
     2,
     3
]



def hello():
    print("hello world")



class One:
    pass
```

在命令行下运行下面命令，

```
black test.py
```

然后，来看一下格式化后的效果，

```
j = [1, 2, 3]


def hello():
    print("hello world")


class One:
    pass
```

## **musicbox**

**Start：8.1k**

[**musicbox**](https://github.com/darknessomi/musicbox)是Python实现的网易云音乐**命令行版本**，支持320kbps的**高品质音乐**，当然，每日推荐、歌曲评论......这些功能也都支持，经常使用***nix系统**系统的同学可以尝试一下。

**安装**

```
pip(3) install NetEase-MusicBox
```

**使用**

```
musicbox
```

![img](https://pic1.zhimg.com/80/v2-ee6a152be7a65a32481fa38482964995_1440w.gif)

目前已经通过测试支持的系统包括，macOS、Ubuntu、Kali、CentOS、openSUSE、Fedora、Arch，暂时不支持Windows。

## **nba_api**

**Start：604**

[**nba_api**](https://github.com/swar/nba_api)是一个访问**NBA.com**的API工具包。

通过使用nba_api可以轻松获取**球员**、**球队**、**比赛**信息，如果你对想做**数据分析**，恰好又对NBA感兴趣，那么可以尝试一下这款Python小工具。

**安装**

```
pip install nba_api
```

**示例**

```
from nba_api.stats.static import players
players.find_players_by_first_name('lebron')
# 输出
[{'id': 2544, 'full_name': 'LeBron James', 'first_name': 'LeBron', 'last_name': 'James', 'is_active': True}]
```

## **akshare**

**Start：251**

[**akshare**](https://github.com/jindaxiang/akshare)是一个简单易用的**金融数据接口库**，实现了对股票、期货、期权、基金、外汇、债券、指数、数字货币等金融产品数据实时和历史数据、衍生数据采集、清洗、落地全流程的开源工具。

能够满足对数据分析师或者对金融感兴趣同学的需求，能够提供丰富的业务数据供开发、研究使用。

**安装**

```
pip install akshare  --upgrade
```

**示例**

```
import akshare as ak
ak.get_roll_yield_bar(type_method="date", var="RB", start_day="20180618", end_day="20180718", plot=True)
```

输出结果，

```
            roll_yield near_by deferred
2018-06-19    0.191289  RB1810   RB1901
2018-06-20    0.192123  RB1810   RB1901
2018-06-21    0.183304  RB1810   RB1901
2018-06-22    0.190642  RB1810   RB1901
2018-06-25    0.194838  RB1810   RB1901
2018-06-26    0.204314  RB1810   RB1901
2018-06-27    0.213667  RB1810   RB1901
2018-06-28    0.211701  RB1810   RB1901
2018-06-29    0.205892  RB1810   RB1901
2018-07-02    0.224809  RB1810   RB1901
2018-07-03    0.229198  RB1810   RB1901
2018-07-04    0.222853  RB1810   RB1901
2018-07-05    0.247187  RB1810   RB1901
2018-07-06    0.261259  RB1810   RB1901
2018-07-09    0.253283  RB1810   RB1901
2018-07-10    0.225832  RB1810   RB1901
2018-07-11    0.210659  RB1810   RB1901
2018-07-12    0.212805  RB1810   RB1901
2018-07-13    0.170282  RB1810   RB1901
2018-07-16    0.218066  RB1810   RB1901
2018-07-17    0.229768  RB1810   RB1901
2018-07-18    0.225529  RB1810   RB1901
```

## **helium**

**Start：1k**

终于到本文的重头戏了，下面就来介绍一下Helium这款神器。

[**Helium**](https://github.com/JadenGeller/Helium)是一款基于 [**Selenium**](https://www.selenium.dev/)实现的**网页自动化工具**，它能够解放你的双手，让你实现日常各种网页的使用。

废话不多说，来先看一个**示例**，应该就明白它到底是干什么用的。

```
from helium import *
start_chrome('google.com')
write('helium selenium github')
press(ENTER)
click('mherrmann/helium')
go_to('github.com/login')
write('username', into='Username')
write('password', into='Password')
click('Sign in')
kill_browser()
```

看一下具体的演示，

![img](https://pic3.zhimg.com/80/v2-90b7819f4a0d8a72f542114ab4678f9b_1440w.gif)

看了演示应该大概明白helium是干什么用的了，它能够实现网页端的各种自动化操作，例如，

- 启动浏览器
- 与浏览器交互
- 查找相关元素
- 等待元素出现
- ......

其中，较为常用的就是**启动浏览器**和**浏览器交互**，启动浏览器应该都明白，不需要多说，这里就来介绍一下与浏览器交互。

helium能够输入**内容、敲击键盘、点击按钮、跳转、关闭**等各种我们日常访问网页时常用的操作。

回想一下，我们平时浏览网页不也就是这些操作吗？只是，helium自动化实现了我们日常的操作。

也许看到这里很多同学还是认为，这有什么用啊？

我觉得这个可以发散一下思维，自己寻找一下应用场景，例如，

- 批量下载音乐
- 批量下载电影、电视剧
- 下载图片
- 快速填单
- 便捷访问日常网址

举个例子，假如你日常的工作就是在网站填写表格或者处理订单等重复性的工作，那么就可以写一个脚本，然后循环同样一个动作，自己就不用动手操作了。

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)

- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)
- [该如何运营一个微信公众号？](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484991&idx=1&sn=ea2039518dfeacb42639877ea226cbf1&chksm=e94e9937de3910219e52d2ae0d09e8d2754722559927083789d29554b82091133cc421d5418d&token=2025215714&lang=zh_CN#rd)