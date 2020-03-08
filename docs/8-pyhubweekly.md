## **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

如果喜欢，麻烦给个**Star**支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **newscatcher**
- **pycodestyle**
- **pywinauto**
- **real-url**
- **docopt**

下面分别来介绍一下上述5个GitHub项目。

## **newscatcher**

**Star：719**

[**newscatcher**](https://github.com/kotartemiy/newscatcher)获取新闻资讯的工具包，它时刻监控者成千上万个新闻媒体并对其进行聚合，它包含丰富的API接口，开发者可以通过**时间**、**新闻源**、**关键字**等方式来获取新闻资讯。

也许会有同学疑惑，我们已经有这么多新闻软件，**这个工具有什么价值呢？**

**第一：**对于我们常用的新闻软件，具体怎么样，我想应该都很清楚，质量参差不齐，而且广告繁多。所以，首先，我们可以通过**newscatcher**这个工具包获取我们想要的新闻资讯。

**第二：**它提供了丰富的数据源，假如你喜欢做金融数据分析，仅凭股票等这些量化的数据是很难得到很理想的分析结果，它往往受到政策和事件的影响，所以，这时候就需要一些**非结构化的数据**区辅助分析。而新闻，在其中就是一种非常有价值的非结构化数据。

**安装：**

```
pip install newscatcher
```

**使用：**

```
from newscatcher import Newscatcher
from newscatcher import get_news
from newscatcher import get_headlines


news_source = Newscatcher('blackfaldslife.com')
news = get_news('wired.co.uk')
headlines = get_headlines('wired.co.uk')
```

## **pycodestyle**

**Star：4k**

[**pycodestyle**](https://github.com/PyCQA/pycodestyle)是根据PEP 8中的样式约定检查Python代码的工具，它具有如下特性，

- 添加新代码检查很容易
- 快速跳转到错误位置
- 轻量化
- 带有全面的测试套件

**安装：**

```
pip install pycodestyle
pip install --upgrade pycodestyle
pip uninstall pycodestyle
```

**使用：**

可以直接在命令行调用pycodestyle，通过各种选项可以实现不同的功能，例如，统计错数数量、显示PEP8相关提示，下面看一个**示例**。

```
# E40.py
import os, sys
```

然后对其进行代码检查，

```
E40.py:1:10: E401 multiple imports on one line
import os, sys
         ^
    Place imports on separate lines.

    Okay: import os\nimport sys
    E401: import sys, os

    Okay: from subprocess import Popen, PIPE
    Okay: from myclas import MyClass
    Okay: from foo.bar.yourclass import YourClass
    Okay: import myclass
    Okay: import foo.bar.yourclass
```

## **pywinauto**

**Star：2k**

在上一期我介绍了一款**网页自动化工具helium**，它能够实现网页端的很多重复性工作，的确大大提高了工作效率。

如果你的工作、学习内容不仅限于网页端、如果helium还不能满足你高效工作的需求。那么，pywinauto一定可以做到。

[**pywinauto**](https://github.com/pywinauto/pywinauto)是一款实现Windows GUI自动化的Python工具，它可以将鼠标和键盘操作发送到Windows对话框和控件。此外，它还支持更复杂的操作，例如获取文本数据。

**安装：**

```
pip install -U pywinauto
```

**使用：**

先写一段演示代码，

```
from pywinauto.application import Application
app = Application().start("notepad.exe")

app.UntitledNotepad.menu_select("帮助->关于记事本")

app.UntitledNotepad.Edit.type_keys("pywinauto Works!", with_spaces = True)
```

![img](https://pic2.zhimg.com/80/v2-8641e8236c179e0255243646d1b8ee9b_1440w.gif)

## **real-url**

**Star：256**

[**real-url**](https://github.com/wbt5/real-url)是一款**解析流媒体直播源**的Python工具包，目前支持21个直播平台：斗鱼直播、虎牙直播、哔哩哔哩直播、战旗直播、网易CC直播、火猫直播、企鹅电竞、YY直播、一直播、快手直播、花椒直播、映客直播、西瓜直播、触手直播、NOW直播、抖音直播，爱奇艺直播、酷狗直播、龙珠直播、PPS奇秀直播、六间房。

获取直播源地址之后可以在**PotPlayer**、VLC、flv.js等播放器进行播放。

**使用：**

可以直接从github下载代码zip包或者克隆代码，然后再命令行下执行对应的脚本即可。

不同的脚本对应不同的平台，例如，douyin.py对应抖音，douyu.py对应斗鱼，也就是说，我们需要哪个平台的直播源，就执行拼音对应的脚本即可。

当执行命令python [script.py]后，可以输入直播房间号或者链接即可获取直播链接，然后再PotPlayer**打开链接**即可。

下面看一下演示，

![img](https://pic3.zhimg.com/80/v2-808e879587e51d25b336652794707730_1440w.gif)

## **docopt**

**Star：7k**

[**docopt**](https://github.com/docopt/docopt)是一款Python风格的命令行参数解析工具，它通过解析Python文件开头的注释文档来解析命令行参数格式。这样的方便之处是能够实现业务代码与命令行参数模块分开，但是，对注释__doc__的格式要求也比较严格。

**示例，**

```
"""
Naval Fate.

Usage:
  naval_fate ship new <name>...
  naval_fate ship <name> move <x> <y> [--speed=<kn>]
  naval_fate ship shoot <x> <y>
  naval_fate mine (set|remove) <x> <y> [--moored|--drifting]
  naval_fate -h | --help
  naval_fate --version

Options:
  -h --help     Show this screen.
  --version     Show version.
  --speed=<kn>  Speed in knots [default: 10].
  --moored      Moored (anchored) mine.
  --drifting    Drifting mine.
"""
from docopt import docopt


if __name__ == '__main__':
    arg = docopt(__doc__, argv=None, help=True, version=None, options_first=False)
    print(arg)
```

然后在命令行执行命令就可以看到docopt通过注释文档解析的参数，

```
> test.py ship Guardian move 100 150 --speed=15
{'--drifting': False,
 '--help': False,
 '--moored': False,
 '--speed': '15',
 '--version': False,
 '<name>': ['Guardian'],
 '<x>': '100',
 '<y>': '150',
 'mine': False,
 'move': True,
 'new': False,
 'remove': False,
 'set': False,
 'ship': True,
 'shoot': False}
```

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)
- [该如何运营一个微信公众号？](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484991&idx=1&sn=ea2039518dfeacb42639877ea226cbf1&chksm=e94e9937de3910219e52d2ae0d09e8d2754722559927083789d29554b82091133cc421d5418d&token=2025215714&lang=zh_CN#rd)