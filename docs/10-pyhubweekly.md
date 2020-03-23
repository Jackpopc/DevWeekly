## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **igcommit**
- **pyxelate**
- **automl**
- **salt**
- **public-apis**

下面分别来介绍一下上述5个GitHub项目。

## igcommit

**Star：105**

git是一个非常强大，但是管理起来又相对麻烦的一款版本控制工具，为了保证代码的整洁性、一致性、安全性，我们需要人工进行非常多的检视工作。

如果是Python、php这类脚本语言还好，毕竟代码量相对较少，但是，如果是C++、Java，需要耗费很大功夫在代码的检视方面。

[**igcommit**](https://github.com/innogames/igcommit)提供一种pre-receive钩子，使得当提交代码时能够提前与服务器端代码进行校验和规范检查，如果不符合要求则会直接拒绝，能够很大程度上减少代码检视工作量。它主要有如下特性：

- 支持`BUGFIX`、`FEATURE`、`WIP`等标签验证
- 支持CSS、Go、Python、php、html等语法检查
- 能够验证json、yaml、xml等数据格式
- 坚持提交摘要的格式
- 校验提交者信息和邮件地址

**安装配置**

```shell
pip install igcommit
ln -s igcommit-receive /home/git/repositories/myproject.git/hooks/pre-receive
```

**示例**

```shell
=== CheckDuplicateCommitSummaries on CommitList ===
ERROR: summary "Add nagios check for early expiration of licenses" duplicated 2 times

=== CheckCommitSummary on 31d0f6b ===
WARNING: summary longer than 72 characters

=== CheckCommitSummary on 6bded65 ===
WARNING: past tense used on summary

=== CheckCommand "flake8" on src/check_multiple.py at 6bded65 ===
INFO: line 10 col 5: E225 missing whitespace around operator
INFO: line 17 col 80: E501 line too long (122 > 79 characters)
INFO: line 17 col 85: E203 whitespace before ','

=== CheckCommitMessage on 6fdbc00 ===
WARNING: line 7 is longer than 80
WARNING: line 9 is longer than 80
```

## pyxelate

**Star：319**

[**pyxelate**](https://github.com/sedthh/pyxelate)是一款生成图像像素艺术照的工具，它通过对图像进行下采样，然后结合无监督学习生成调色板合成衣服像素图片。

**安装**

```shell
pip3 install git+https://github.com/sedthh/pyxelate.git
```

**示例**

```python
from pyxelate import Pyxelate
from skimage import io
import matplotlib.pyplot as plt

img = io.imread("kobe.jpg")
# generate pixel art that is 1/14 the size
height, width, _ = img.shape 
factor = 3
colors = 16
dither = True

p = Pyxelate(height // factor, width // factor, colors, dither)
img_small = p.convert(img)  # convert an image with these settings

_, axes = plt.subplots(1, 2, figsize=(16, 16))
axes[0].imshow(img)
axes[1].imshow(img_small)
plt.show()
```

**输出结果**

![img](https://pic4.zhimg.com/80/v2-49da0155e90f1b6fdd333df349fedfdb_1440w.png)

## automl

**Star：557**

[**automl**](https://github.com/google/automl)是有Google Brain刚开源不到一周的一款自动机器学习项目，此项目包含了与AutoML相关的模型和库的列表。

由于项目刚开源，所以列表中只包含了谷歌最新目标检测模型EfficientDet，该模型在模型大小、计算量方面都对比于当前最优秀的模型有了很大的提升。

![img](https://pic1.zhimg.com/80/v2-5c9a1c12265e03376f9d8b880139b1b4_1440w.png)

## salt

**Star：10.7k**

[**salt**](https://github.com/saltstack/salt)是一款由Python开发的应用集中管理平台，设计最初的目的是用于远程执行系统，但是经过多年的丰富和晚上，现在具备如下几项主要功能，

- 远程执行
- 监控
- 配置管理

这款工具比较适合于运维人员使用，它能够批量在大量的服务器上执行命令，对多种任务进行综合管理、文件分发。

## public-apis

**Star：72.5k**

我们总是在网上看到很多好用的工具或者网站，你是否想过自己实现一款解决某项痛点的工具？

[**public-apis**](https://github.com/public-apis/public-apis)是一个软件和web开发的免费api的集合，它涵盖内容包括但不限于，

- 动漫
- 艺术设计
- 日历
- 数据验证
- 金融
- 事件
- 音乐
- 机器学习
- 购物
- 社交
- ...

我们可以找到自己需要的api，然后给它封装一层外壳，形成一款完整易用的产品。例如，可以使用Python的一些web开发框架或者javascript库React、Vue写一个前端，这些api作为后端，这样就成了一款web应用。当然，也可以使用PyQt、tkinter、PySimpleGUI开发一款分发工具。

------

#### 推荐阅读

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)

