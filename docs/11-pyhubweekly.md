## **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **Komodoedit**
- **git-sweep**
- **plotly.py**
- **DecryptLogin**
- **hubcommander**

下面分别来介绍一下上述5个GitHub项目。

## **Komodoedit**

**Star：1.4k**

[**KomodoEdit**](https://github.com/Komodo/KomodoEdit)是一个基于Mozilla平台由Python、JS、C++开发的一款**快速**、**免费**、**多语言**的代码编辑器。

常见的IDE上拥有的主要功能，Komodo都有用，例如，

- 多语言支持
- 自动补全
- 小地图
- 工具箱
- 项目管理
- 单元测试
- 交互式命令行
- ...

![img](https://pic2.zhimg.com/80/v2-bbcd37be896579b111dffcfad864d255_1440w.jpg)

## **git-sweep**

**Star：2k**

[**git-sweep**](https://github.com/arc90/git-sweep)是一款由Python开发，用于清理合并到master中的Git分支的命令行工具。

master分支是我们开发过程中最终代码的聚合地，在团队开发过程中会创建各种不同的分支，然后将代码合入到master中。其中不乏一些临时分支，久而久之就会创建很多无用的分支，git-sweep就是用于清理这些无用分支的一款命令行工具。

**安装**

```
pip install git-sweep || easy_install git-sweep
```

**使用**

安装git-sweep之后，我们就可以进入工程路径下，使用命令进行清理无用分支，

```
git-sweep cleanup
Fetching from the remote
These branches have been merged into master:

  branch1
  branch2
  branch3
  branch4
  branch5

Delete these branches? (y/n) y
  deleting branch1 (done)
  deleting branch2 (done)
  deleting branch3 (done)
  deleting branch4 (done)
  deleting branch5 (done)

All done!

Tell everyone to run `git fetch --prune` to sync with this remote.
(you don't have to, yours is synced)
```

当然，除此之外还可以指定远程master分支名称等高级用法。

## **plotly.py**

**Star：6.3k**

[**plotly.py**](https://github.com/plotly/plotly.py)是一款开源、交互式的Python绘图库。

使用plotly.py，可以在浏览器中生成交互式的图像便于发布，不仅如此，它支持的图形类别也非常丰富，例如，线图、散点图、面积图、柱状图、误差条、箱形图、直方图、热力图、副图、多轴、极坐标图和气泡图。

**安装**

```
pip install plotly==4.5.4
```

**示例**

```
import plotly.graph_objects as go
fig = go.Figure()
fig.add_trace(go.Scatter(y=[2, 1, 4, 3]))
fig.add_trace(go.Bar(y=[1, 4, 3, 2]))
fig.update_layout(title = 'Hello Figure')
fig.show()
```

除了Python之外，plotly还支持js, python, R等语言。

## **DecryptLogin**

**Star：270**

[**DecryptLogin**](https://github.com/CharlesPikachu/DecryptLogin)是一款实用requests方式登录一些网站的工具。

我们在爬虫或者使用网页自动化工具的过程中，会遇到各种各样的问题，其中登录拦截就是其中一项较为常见的难题，而DecryptLogin就是用于解决这种问题的款工具。

![img](https://pic1.zhimg.com/80/v2-7942f08cbc9de0bad29ba32eb644f0b7_1440w.jpg)

它目前支持的网站覆盖比较全面，例如，淘宝、百度网盘、京东、github、网易云音乐、知乎、B站、推特、拉勾网等。

## **hubcommander**

**Star：1.1k**

[**hubcommander**](https://github.com/Netflix/hubcommander)一款由Netflix开源，用于 GitHub 组织管理的 Slack 机器人。

HubCommander 使用聊天操作或对话驱动的开发来帮助管理 GitHub 项目，它具有如下功能，

- 存储库创建
- 删除库
- 存储库描述和网站修改
- 向存储库授予外部协作者特定的权限
- 存储库默认分支修改
- 创建/删除库主题
- 启用/禁用存储库分支保护
- ......

HubCommander使用Python基于slackhq/python-rtmbot，所以使用之前最基本的需求需要Python 3.5+、Github账户、Slack凭证。

目前HubCommander支持Docker、Linux、macOS安装。

也许对于个人开发者来说，这样相对繁琐、复杂，但是对于多人开发的大型项目而言，这款工具显然能够节省很多精力。

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)