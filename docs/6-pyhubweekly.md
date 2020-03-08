# 本期内容

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

如果喜欢，麻烦给个**Star**支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **music-dl**
- **causalnex**
- **lianjia-beike-spider**
- **yapf**
- **sherlock**

下面分别来介绍一下上述5个GitHub项目。

## music-dl

**Star：1.9k**

我在此前一篇文章 [实用工具 | 2款播放器让你免费听遍全网无损音乐](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484869&idx=1&sn=9a0208776292d69fa4657819f3662a2a&chksm=e94e9acdde3913db34f753cde062f7ebd68ba9d0622c09d525953a6d95a424c758d199916b68&token=2025215714&lang=zh_CN#rd)中介绍了一款能够**免费下载无损音乐**的工具**鱼声音乐**，后来发现受到很多同学的欢迎，这里再介绍一款**能够下载全网音乐的Python命令行工具**。

[**music-dl**](https://github.com/0xHJK/music-dl)是一个基于Python3的命令行工具，可以下载来自QQ音乐、酷狗音乐、网易云、咪咕等平台的音乐，同时还能够用于查询音乐，解决不知道版权来自于哪个平台的问题。


![](https://imgkr.cn-bj.ufileos.com/6789816e-a3c9-4b47-bdeb-b22af7eb1fb8.png)

使用方法非常简单，只需在命令行下执行**music-dl**加上歌手、歌曲名称即可，例如，

```shell
> music-dl --help
> music-dl -k "周杰伦"
```

除了指定歌手名称，还可以指定音乐链接、歌单链接等方式进行下载。

music-dl对于音乐音质默认搜索顺序为**无损 -> 320K -> 128K**，部分平台支持无损音乐也可以下载，需要指出的是，本项目采用的公开API，所以，不支持付费音乐。


## causalnex

**Star：446**

在数据分析中，只有明确因果关系，才能提出更加明确的干预措施。

[**causalnex**](https://github.com/quantumblacklabs/causalnex)基于贝叶斯网络开发的因果推理工具包，通过使用causalnex，可以完成以下工作，

- 使用最先进的结构学习方法来理解变量之间的条件依赖关系
- 基于结构关系建立预测模型
- 贝叶斯网络的拟合概率分布
- 用标准统计检验评价模型质量

安装方式，

```shell
> pip install causalnex
```


## lianjia-beike-spider

**Star：1.5k**

还在为租房买房时了解、对比不同平台、不同区域价格而苦恼吗？

[**lianjia-beike-spider**](https://github.com/jumper2014/lianjia-beike-spider)爬虫链家网和贝壳网房价，采集北京上海广州深圳等21个中国主要城市的房价数据（小区，二手房，出租房，新房）。


![](https://imgkr.cn-bj.ufileos.com/f80bdec7-367d-4831-8cf4-8613c86c12cc.png)


**使用方法：**

首先，下载项目，解压后进去项目安装依赖，

```shell
> pip install -r requirements.txt
```

然后，把解压的目录加入到环境变量，如果需要更改爬虫网站（链家或贝壳），可以修改`lib/spider/base_spider.py`中的`SPIDER_NAME`变量名。

最后，执行爬虫脚本，

```shell
> python xiaoqu.py city
```

其中，`city`是城市代码，对照关系如下，

```
hz: 杭州, sz: 深圳, dl: 大连, fs: 佛山
xm: 厦门, dg: 东莞, gz: 广州, bj: 北京
cd: 成都, sy: 沈阳, jn: 济南, sh: 上海
tj: 天津, qd: 青岛, cs: 长沙, su: 苏州
cq: 重庆, wh: 武汉, hf: 合肥, yt: 烟台
nj: 南京
```


## yapf

**Star：10.3k**

代码规范化石项目开发中至关重要的一个环节，它不仅可以提高代码的可读性，还可以减少项目维护成本，因此，很多大公司都会有一套严格的编码规范。

提到Python，首先想到的规范就是**pep8**，而比较耳熟能详的**自动格式化**工具就是**autopep8**或者**pep8ify**。但是，它们有着明显的缺陷，例如，不能重新格式化那些不违反**PEP8指南**的代码。但是，这并不意味着代码看起来很好，例如，很多格式虽然不违反指南，但是也不符合指南，介于二者之间。换句话说，目前的自动格式化工具更像是依照范本的**纠错工具**。

而来自[**谷歌**]的[**yapf**](https://github.com/google/yapf)则不同，它的算法对于那些即使原始代码没有违反样式指南也会样式指南进行重新格式化。


![](https://imgkr.cn-bj.ufileos.com/2156d20a-4c26-4fd2-b2d2-3e9dca20466a.png)


yapf预定义支持的四种样式规范分别是`pep8`、`facebook`、`Google`、`chromium`。

## sherlock

**Star：10.5k**

[**Sherlock**](https://github.com/sherlock-project/sherlock)是一个Python开发的强大命令行工具，可用于在多大306个社交网络中查找用户名，当然，包括Facebook、twitter等知名网站。
另外，它可以在MacOS、Linux和Windows上运行。


![](https://imgkr.cn-bj.ufileos.com/d3338a56-f549-460a-b96d-c4563c5ddcb9.gif)



#### 推荐阅读
- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
-[实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)
- [该如何运营一个微信公众号？](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484991&idx=1&sn=ea2039518dfeacb42639877ea226cbf1&chksm=e94e9937de3910219e52d2ae0d09e8d2754722559927083789d29554b82091133cc421d5418d&token=2025215714&lang=zh_CN#rd)

---

欢迎关注我的公众号“**平凡而诗意**”，原创技术文章第一时间推送，如果喜欢，麻烦点一下“**在看**”~

<center>
    <img src="https://imgkr.cn-bj.ufileos.com/ba67a0df-9e73-4dcd-8a83-7479f9076350.jpg" style="width: 150px;">
</center>

