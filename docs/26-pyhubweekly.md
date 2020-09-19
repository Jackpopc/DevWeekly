## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[PyHubWeekly](Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **SciencePlots**
- **hickory**
- **PyPaperBot**
- **sweetviz**
- **toolz**

下面分别来介绍一下上述5个GitHub项目。

### SciencePlots

**Star：1.4k**

[SciencePlots](garrettj403/SciencePlots)是一款用于科学绘图的Python工具包。

当我们看学术期刊、论文时会看到各种各样高大上的图形。会好奇，这么好看的图到底怎么画的？是不是很困难？

的确，现在很多Python绘图工具只是关注图形所表达的数据信息，而忽略了样式。

SciencePlots则弥补了这片空白，它是一款专门针对各种学术论文的科学绘图工具，例如，science、ieee等。

**安装**

```shell
# for latest commit
pip install git+https://github.com/garrettj403/SciencePlots.git

# for lastest release
pip install SciencePlots
```

**使用**

SciencePlots的使用非常简单，你只需要指定使用的样式、是否需要网格、背景，它就可以很容易的绘制出你想要的图形。

```python
import matplotlib.pyplot as plt
plt.style.use('science')
```

![fig1 (1)](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/fig1%20(1).jpg)

### hickory

**Star：11**

[hickory](maxhumber/hickory)是一款调度Python脚本的命令行工具。

当我们开发一个程序，需要它定时被调度、定时执行时，每天定好闹钟，到点手动执行代码显然是不现实的。

你可以选择Docker、k8s这些工具去部署你的定时作业，但是，显然这种方案太**重**了。

hickory就是一种能够轻松实现定时调度Python脚本的工具，很轻量、很简单。

**示例**

首先，编写一个名为`foo.py`的Python脚本：

```python
import datetime
import time

stamp = datetime.datetime.now().strftime("%H:%M:%S")
time.sleep(5)

print(f"Foo - {stamp} + 5 seconds")
```

然后，在命令行下调度它，使它每10分钟执行一次：

```shell
hickory schedule foo.py --every=10minutes
```

这样，它就可以在后台执行，并按时调度。此外，你还可以使用`hickory status`命令来查看它的状态。

### PyPaperBot

**Star：12**

[PyPaperBot](ferru97/PyPaperBot)是一款可以从谷歌Scholar、Crossref和SciHub下载学术论文的Python工具。

PyPaperBot会尝试从谷歌学术、SciHub、作者相关的链接等不同来源去下载你想要的PDF学术论文，避免你再去逐个网站寻找你想要的论文的困境。

**安装**

```shell
pip install PyPaperBot
```

**使用**

你可以通过提供索引关键字、DOI等方式搜索你需要的论文，

```shell
python -m PyPaperBot --query="Machine learning" --scholar-pages=3  --min-year=2018 --dwn-dir="C:\User\example\papers"
```

### sweetiviz

**Star：943**

[sweetiviz](fbdesignpro/sweetviz)是一款简单、易用的数据对比、可视化工具。

我们在做大数据相关的项目，例如，计算机视觉、机器学习、数据分析等过程中，经常会用到数据对比，训练集与测试集对比、各个子集之间的对比...

通过人肉逐个去对比显然是不现实的，而且很浅显。

sweetiviz围绕数据对比进行构建，能够深度探索不同数据之间的关系，并输出HTML程序，便于我们对数据有一个全局的把握。

**安装**

```shell
pip install sweetviz
```

**使用**

生成对比分析报告，主要会用到3个函数：

- analyze(...)
- compare(...)
- compare_intra(...)

下面通过一段代码来看一下它的使用：

```python
import sweetviz as sv

my_report = sv.analyze(my_dataframe)
my_report.show_html() # Default arguments will generate to "SWEETVIZ_REPORT.html"
```

然后，它就会生成一个1080p的宽屏HTML报告，可以在浏览器中打开并查看，

![a](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/a.png)

### toolz

**Star：2.9k**

[toolz](pytoolz/toolz)是一款包含迭代、字典、函数的工具集合。

迭代、字典、函数，这里面每一类在Python中的使用频率都非常频繁。

我们经常会用到迭代器、字典、函数中的各种各样的功能，但是默认的数组、字典中却没有这些功能，这样我们就不可不再去实现一遍。例如，分组、去重、合并等待。

toolz就提供了这一组方便的工具集合，你不需要去重复实现一些功能就可以使用你意想不到的便利。

**安装**

```shell
pip install toolz
```

**使用**

下面就来看一下字计数的示例：

```python
>>> def stem(word):
...     """ Stem word to primitive form """
...     return word.lower().rstrip(",.!:;'-\"").lstrip("'\"")

>>> from toolz import compose, frequencies, partial
>>> from toolz.curried import map
>>> wordcount = compose(frequencies, map(stem), str.split)

>>> sentence = "This cat jumped over this other cat!"
>>> wordcount(sentence)
{'this': 2, 'cat': 2, 'jumped': 1, 'over': 1, 'other': 1}
```

这里就用到了组合`compose`和频率`frequencies`的功能。

---

给大家推荐1个宝藏公众号【**七步编程**】，专注于Python、AI、大数据领域内容分享。创作内容坚持原创与高质量，发表内容已经被诸多公众号大V转发，备受欢迎。现在关注，后台回复关键**567**就可以获得我精心整理的机器学习、深度学习、Python、推荐系统等技术方向的干货！

![image-20200829151145405](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/image-20200829151145405.png)