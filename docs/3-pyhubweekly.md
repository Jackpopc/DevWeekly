[TOC]

# 本期内容

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具，本期为大家推荐GitHub上5个优质的Python项目，<!--more-->它们分别是：

[1. explainshell](https://github.com/idank/explainshell)

[2. httpie](https://github.com/jakubroztocil/httpie)

[3. glances](https://github.com/nicolargo/glances)

[4. python-fire](https://github.com/google/python-fire)

[5. aiLearnNotes](https://github.com/Jackpopc/aiLearnNotes)

下面分别来介绍一下上述5个GitHub项目。

# [1. explainshell](https://github.com/idank/explainshell)

Star：7.5k

作为IT/互联网相关的工作人员，哪怕不是开发者，也有可能会和Linux打交道，我们可以用Linux进行开发、运维等，因此，Linux就成为了一项非常重要的个人技能。

使用Linux过程中主要打交道的对象就是繁多的Linux命令和选项(options)就成了令人头疼的事情，举一个最为简单的例子，

```powershell
> ls -al
```

这个Linux命令包含两个部分，command和options，ls是查看命令，-a和-l分别代表：显示所有文件(包括以.开头的隐藏文件)、以列表形式显示。

这些常用的我们都知道，但是有很多使用频率较少的怎么办？我们可以借助explainshell。

它是一款利用Python开发的Linux命令行工具，通过解析帮助文档，逐个匹配一行Linux命令中不同字符的含义，让你对Linux命令能够一目了然，是一款非常棒的Linux学习工具。

![img](https://pic2.zhimg.com/v2-9a69e7a62db5f1d7c9a31148a4e9fc2d_b.png)

# [2. httpie](https://github.com/jakubroztocil/httpie)

Star：45.5k

不同组件之间相互访问可以通过很多方式，其中restful是比较常用的一种。这里就涉及http请求，我们需要测试数据能够正确的上传和下载。在处理http请求过程中使用较多的工具就是curl。

curl有很多明显的弊端：对用户不够友好，命令冗长；可视化效果差，没有高亮。httpie就是curl的一个非常好的替代者，它的使用更加简洁明了，而且能够高亮显示请求结果。

![img](https://pic1.zhimg.com/v2-ce825dede6a8c75e71aa5102375bb0f0_b.png)

# [3. glances](https://github.com/nicolargo/glances)

Star：14.9k

glances就如同它的汉语意思那样，“一眼”、“一瞥”，能够通过一个简单的命令对系统信息一目了然，了如指掌。

glances利用Python编写的一个跨平台的监视工具，旨在通过curses或基于Web的界面提供大量监视信息。

![img](https://pic4.zhimg.com/v2-11be2dd9bab8131f1a7db4daee6cad7b_b.png)

你不仅可以通过终端命令行使用该工具，还可以web界面、API接口等对服务器进行远程监控，可以将统计信息导出到文件或数据库。

# [4. python-fire](https://github.com/google/python-fire)

Star：16.1k

python-fire是一个款python命令行接口(CLI)，仅仅凭它的来历就值得关注一下，它是由谷歌开源的一款python工具包。

我们在开发项目时往往会需要从命令行传入参数，以往常用的有sys、argparse等，既然有一些成熟的命令行工具，为什么还要推荐python-fire呢？

因为它有如下优势：

- 实现接口更加简洁
- 创建CLI接口更加简单
- 能够将现有代码转化为接口
- 它使得bash和python之间的转换更加容易

示例，

```python
import fire

class Calculator(object):
  """A simple calculator class."""

  def double(self, number):
    return 2 * number

if __name__ == '__main__':
  fire.Fire(Calculator)
```

接下来，我们可以在命令行下调用对应的接口，也可以通过参数名称直接传参，

```powershell
> python calculator.py double 10  # 20
> python calculator.py double --number=15  # 30
```

# [5. aiLearnNotes](https://github.com/Jackpopc/aiLearnNotes)

Star：96

这是我自己在GitHub托管的项目，和上述优质的GitHub项目一起介绍有一些格格不入，也有一些自卖自夸，但是，我还是希望借此机会推荐一下这个项目。

这个项目围绕AI领域的一些方向展开，目前包含计算机视觉系列，后续会加入机器学习、强化学习、优化算法等系列内容。

该项目的核心关注点是“动手学习”，也就是说不仅仅局限于理论知识，也会去利用Python动手实现相应的算法，在实现的过程中会对算法的思想具有更加深入的理解。

以耗时近一年、已经完结的计算机时间为例，里面会有文档逐步介绍算法的思想，然后在利用Python逐步实现，再次进行巩固。此外，项目中不再千篇一律的局限于深度学习，而是从数字图像处理开始介绍，关注到像素级的知识，然后在此基础上介绍传统的图像处理、目标识别算法，然后循序渐进的引入深度学习知识，这样对计算机时间会有更深、更广泛的认识。

![img](https://pic3.zhimg.com/v2-0d0c9a25139c0109df6d2950e6751e0e_b.png)

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