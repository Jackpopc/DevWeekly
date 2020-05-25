## **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **dlaicourse**
- **pysheeet**
- **table-ocr**
- **posthog**
- **RL-Stock**

下面分别来介绍一下上述5个GitHub项目。

## **dlaicourse**

**Star：2.8k**

如果说这两年比较火热的研究方向是什么？深度学习肯定能够占据一席之地。

由于人工智能的火热，各种行业的同学都在尝试着去学习深度学习。可是，该怎么学习却成了让很多人困扰的问题。

虽然免费学习资源数不胜数，但是，要么偏重理论而脱离实践，要么一味的重视实践却没有理论，让人看的云里雾里。

[**dlaicourse**](https://github.com/lmoroney/dlaicourse)是这些中我认为较为不错的一个学习深度学习github项目。

dlaicourse不仅包含了深度学习基础知识部分，这个项目还有练习、应用等方面的内容。



![img](https://pic4.zhimg.com/80/v2-87bebb3e009b305116cf5156d73d52f0_1440w.png)



更重要的是，这个项目使用jupyter notebook开发，理论部分与实践部分紧密相结合，在介绍理论知识的过程中让你直观的看到它是如何实现的，我想，这才是对于学习深度学习的同学比较友好的一种教学方式。

## **pysheeet**

**Star：5.9k**

[**pysheeet**](https://github.com/crazyguitar/pysheeet)即为Python Cheat Sheet，一个用于收集Python有价值片段，增强Python编码体验的项目。

我认为在学习一样知识时，会用与精通之间往往会有一个瓶颈。例如，一个学习歌唱的同学，总认为自己的发声是最为恰当的，但是，如果有一个有经验的教授给予指点，找到明确的方向，这时候会发生突飞猛进的变化。

编码也是，当我们学完Python并且在项目中用过很长一段时间之后，我们会陷入一个固定思维，认为当下编码的习惯就是理所当然的，就是恰到好处的，但是，也许在使用方式、编码风格等方面已经走错了方向。

pysheeet这个项目就收集了很多有有价值的Python片段，其他包括但不限于，

- 代码样式
- 列表
- 字典
- 正则表达式
- 异步
- 测试
- ...

这个项目在每个方向均给出了正反例，告诉你什么样才是一个规范的编码方式。



![img](https://pic4.zhimg.com/80/v2-03279894fd43dce8b5fa967a79131f28_1440w.png)



## **table-ocr**

**Star：119**

[**table-ocr**](https://github.com/chineseocr/table-ocr)是一个运用unet实现对文档表格的自动检测，表格重建的OCR项目。

OCR工具是目前比较受欢迎，且提高很多工作效率的一类工具。

它背后到底是如何实现的？

table-ocr这个项目可以帮你揭开它神秘的面纱。



![img](https://pic3.zhimg.com/80/v2-89f59d02a9edee42e003bb3d0771618f_1440w.jpeg)



另外，使用过OCR工具的同学应该都清楚，OCR在印刷体文字识别过程中效果越来越好，但是在表格方面一直捉襟见肘。table-ocr就针对表格检测进行设计和优化，在表格识别、重建效果方面非常突出。

## **posthog**

**Star：1.9k**

[**posthog**](https://github.com/PostHog/posthog)是一款开源的网站统计工具。

PostHog是为开发人员构建的开源产品分析工具，它能够自动收集网站或应用程序上的每个事件，无需向第三方发送数据。只需单击一下就可以部署到自己的基础设施上，并且可以对底层数据进行完整的API/SQL访问。



![img](https://pic4.zhimg.com/80/v2-8997aa0562b3bf6045666b22e77ff5f4_1440w.gif)



它具有如下特性，

- 基于事件的用户级分析-查看哪些用户正在你的应用程序中执行什么操作
- 自动捕获点击和页面浏览量，以分析用户的追溯操作
- 支持JS、Python、Ruby、Node、Go+API的库
- 简单的部署方式



## **RL-Stock**

**Star：1.2k**

[**RL-Stock**](https://github.com/wangshub/RL-Stock)是一款利用强化学习自动炒股的Python项目。

提到机器学习、人工智能在金融、炒股等方面的应用，更多的人会想到预测，例如，传统机器学习、LSTM等。

而强化学习作为机器学习的一个分支，它的模型更符合一个人做决策的过程，也更加贴近现实世界的场景。与监督学习预测未来的数值不同，强化学习根据输入的状态（如当日开盘价、收盘价等），输出系列动作（例如：买进、持有、卖出），使得最后的收益最大化，实现自动交易。



![img](https://pic1.zhimg.com/80/v2-12773f401686d2504767c0199ac65db9_1440w.png)



作者利用强化学习对炒股过程进行了建模，实现了自动炒股。

话说回来，炒股需谨慎，这个项目可以作为一个学习强化学习同时了解股票知识的一个小工具。我想，利用将强化学习应用于股市，应该早已经有很多公司考虑到这一点，但是，它所带来的收益和风险是并重的，我想这也是为什么很少有公司大规模将人工智能，尤其深度学习应用于金融领域的原因。

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)