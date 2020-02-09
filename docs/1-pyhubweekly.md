

# 前言

Github是一个使用非常广泛且非常受欢迎的开源项目托管平台，其中有很多个人开发者，也不乏一些知名的科技公司，例如，Google、Facebook、Microsoft、腾讯、阿里。这么庞大的项目数量中有一些非常有价值，但是在整体中还是占据较小的比重，怎么从这么庞大的群体中筛选出真正有价值的就成了一件很难的事情，本文就推荐6个简单且非常优秀的Python项目。

> 我建了一个QQ学习交流群，旨在“分享、讨论、学习、资源分享、就业机会、互联网内推、共同进步！”，感兴趣的可以加一下，也可以添加我的QQ~ QQ群：1002821945；QQ号：498073774；

# [GeneralNewsExtractor](https://github.com/kingname/GeneralNewsExtractor)

根据论文[《基于文本及符号密度的网页正文提取方法》](https://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFDLAST2019&filename=GWDZ201908029&v=MDY4MTRxVHJXTTFGckNVUkxPZmJ1Wm5GQ2poVXJyQklqclBkTEc0SDlqTXA0OUhiWVI4ZVgxTHV4WVM3RGgxVDM=)实现的一款网络正文抽取工具。在今日头条、网易新闻、游民星空、观察者网、凤凰网、腾讯新闻、ReadHub、新浪新闻做了测试，发现提取效果非常出色，几乎能够达到100%的准确率。

![img](https://pic2.zhimg.com/50/v2-9b1022893ffd5fb69269e330370d715d_b.jpg)

# [you-get](https://github.com/soimort/you-get)

一款用于从Web下载媒体内容(视频、音频、图像)Python命令行工具，使用便捷，支持Youtube、Twitter、TED、网易云音乐、哔哩哔哩、腾讯视频、优酷视频、央视网、抖音、爱奇艺、虾米、酷狗......等几十个音视频平台。而且，功能非常强大，别的工具无法下载的，它都可以。

![img](https://pic4.zhimg.com/50/v2-336ed4d3e9f76065c324b6ca48238aa8_b.jpg)

# [bullet](https://github.com/Mckinsey666/bullet)

一个支持终端输入和菜单选择的 Python 库。可以让使用者在终端上用方向键移动、单选、复选、密码输入等，而且支持定制化格式和颜色。

![img](https://pic4.zhimg.com/50/v2-a3f6abd2469dbeb03820719617161498_b.jpg)

# [one-python-craftsman](https://github.com/piglei/one-python-craftsman)

学习一门编程语言很容易，但是用好一门编程语言却很难，包括Python这门被大多数人认为“简单”的编程语言。如何写出优秀的Python代码？这个项目就是详细讲解 Python 那些细节教你如何做到这一点，比如何时使用异常、怎么给变量起名、怎么编写条件分支等等，看似简单的可能也是最难的地方。

![img](https://pic2.zhimg.com/50/v2-4f50470335df498aee69f577582d45a7_b.jpg)

# [arrow](https://github.com/crsmithdev/arrow)

这是一款对我来说非常有用的Python工具，轻松解决令我十分头疼的时区、时间问题。在开发大型项目过程中，为了保持不同环境的协调一致，尤其是时区不协调会带来运维、上报告警信息等问题。以往的做法需要配置Linux软件源、安装tzdata、配置zoneinfo，但是arrow这块Python工具包能够轻松解决这些问题，能够便捷获取当前时区并设定目标时区。

```
>>> import arrow
>>> arrow.get('2013-05-11T21:23:58.970460+07:00')
<Arrow [2013-05-11T21:23:58.970460+07:00]>

>>> utc = arrow.utcnow()
>>> utc
<Arrow [2013-05-11T21:23:58.970460+00:00]>

>>> utc = utc.shift(hours=-1)
>>> utc
<Arrow [2013-05-11T20:23:58.970460+00:00]>

>>> local = utc.to('US/Pacific')
>>> local
<Arrow [2013-05-11T13:23:58.970460-07:00]>
```

# [PySimpleGUI](https://github.com/PySimpleGUI/PySimpleGUI)

Python能做很多事情，深度学习、数据分析、前后端开发等，当然，它也可以用于用户界面开发。

接触过Python用户界面开发的同学应该都知道tkinter、WxPython、Qt，其中使用较多的就是tkinter，有很多知名的图形库都是基于tkinter进行开发。但是它们各有优缺点，例如，tkinter扩展不够灵活，对用户不够友好，而WxPython、Qt在开发过程中又非常繁琐。PySimpleGUI将tkinter、Qt、Remi、WxPython转换为可移植且友好的python接口，便于开发者实现强大灵活的用户界面。

![img](https://pic3.zhimg.com/50/v2-d4d4ef0e4c56725fae9ea2819cbab82b_b.jpg)

------

> 更多精彩内容，请关注公众号【平凡而诗意】~

# 更多我的作品

[实用工具 | 2款播放器让你免费听遍全网无损音乐](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484869&idx=1&sn=9a0208776292d69fa4657819f3662a2a&chksm=e94e9acdde3913db34f753cde062f7ebd68ba9d0622c09d525953a6d95a424c758d199916b68#rd)

[大数据 | Spark机器学习工作流开发指南](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484860&idx=1&sn=a18e7e9846006668e2e3989e85e2a6b2&chksm=e94e9ab4de3913a207f69307e1386c9b4f173a9aa85f89170db2f99b6886fb692da6ce8b85c1#rd)

[实用工具 | 你距离PS大神只差这6款免费在线工具！](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484855&idx=1&sn=0ed13e66d4e2bb8b44a1c53e422ec248&chksm=e94e9abfde3913a9962d2abf156115165cbf9337ef375ea1c02ac88b9eba4e9285b12143e353#rd)

[简易教程 | 分布式消息发布订阅系统Kafka从搭建到使用](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484849&idx=1&sn=7b22b424678c9917c6327168a641a117&chksm=e94e9ab9de3913af50f1bf3412a402f3bf27b4abd50678f153d07778e61ac9a21b4a4bdce2cc&token=326900528&lang=zh_CN#rd)

[教程 | 一文搭建你的第一个免费专属博客](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484843&idx=1&sn=288496d86fa5113204c0c72b15b8b082&chksm=e94e9aa3de3913b562153b73d6214eb4a09e4ba0177ae7f0476437494c5f45408af4cf894e66#rd)

[办公效率 | 让你突飞猛进的10个Word技能](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484829&idx=1&sn=a607a218cf19bf24fb4ddac599c4196c&chksm=e94e9a95de391383cb33494a8b5dffd1565617cfd1b79c3e97c4da64517d5d16d632f1915d96#rd)

[学习工具 | 推荐10款提升自己的优质APP](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484812&idx=1&sn=70be06850fa9e001ec5f5b1aa53dff7c&chksm=e94e9a84de391392ac32e8365474317f209113bec08b3d0acedb32fc845c755b61b20d83af2b#rd)

[Google | Python编程规范指南](http://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484788&idx=1&sn=24ce3cec2d248f11eb8a82908f921ec6&chksm=e94e9a7cde39136a0eda417946a45513be5c8500f77b6ead2f7824c930ebd8e90cc21fede9fa#rd)