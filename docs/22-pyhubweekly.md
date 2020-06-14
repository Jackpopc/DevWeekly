## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[PyHubWeekly](https://github.com/Jackpopc/PyHubWeekly "**PyHubWeekly**")，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **textshot**
- **whoogle-search** 
- **sphinx**
- **snakeware**
- **video2x**

下面分别来介绍一下上述5个GitHub项目。

## textshot

**Star：745**

![](https://imgkr.cn-bj.ufileos.com/51526378-ff29-4a6c-b34e-c4dc47e3b64e.gif)


[textshot](https://github.com/ianzhao05/textshot "**textshot**")是一款截图识别文字的Python小工具。

关于这款工具，我已经在另外一篇文章：[100行Python代码实现一款高精度免费OCR工具](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485506&idx=1&sn=fbc96c178db365929a68f04a8314bfd3&chksm=e94e974ade391e5c63b9f6bb7300f8b6eba288a7dc088253b68dd139f2dd2b1b3d76b024591c&token=664463365&lang=zh_CN#rd)中进行过详细介绍。

或许textshot在识别精度并不如哪些付费的API，在包装方面不如那些商业化成都较高的OCR工具，但是，我还是很推荐学习一下这个项目。

它通过简洁、少量的代码实现了从前端到后端调用整个完整系统的开发，通过这个项目可以了解一个完成的应用涉及哪些环节，而且能够从细节学习到如何通过Python实现UI开发、实现一款截图工具、调用后端引擎。

## whoogle-search

**Star：870**


![](https://imgkr.cn-bj.ufileos.com/7ac08fa9-4c13-42fd-8925-d73d74ee47e5.png)


[whoogle-search](https://github.com/benbusby/whoogle-search "**whoogle-search**")是一款可以自己架设，能够爬取谷歌搜索结果、无广告、不追踪、保护隐私的搜索引擎工具。

**whoogle-search**的安装部署方式非常丰富而且简单，可以通过Docker、Heroku、pip、手动等方式进行安装配置。

安装之后配置相应的ip和端口就可以启动whoogle-search服务。

以**pip**安装配置为例。

**安装**

```python
pip install whoogle-search
```

**启动服务**

```shell
whoogle-search --host <your ip> --port <your port>
```

## sphinx

**Star：3.3k**

[sphinx](https://github.com/sphinx-doc/sphinx "**sphinx**")是一款可以快速创建漂亮文档的Python工具。

之前我曾介绍过另外一款文档生成工具mkdoc，而sphinx是一款更加全面、智能、强大的文档生成工具。

它具有如下特点：

- 输出格式全面：HTML、LaTeX、ePub、纯文本等；

- 广泛的交叉引用：函数、类、引文、词汇表术语等；

- 层次结构：简单定义文档树，自动链接到同级、父级和子级；

- 代码处理：使用Pygments highlighter自动突出代码显示；

- 扩展：自动测试代码片段，包含来自Python模块（API文档）的docstring；

## snakeware

**Star：1.3k**


![](https://imgkr.cn-bj.ufileos.com/ae91b714-4220-4b51-96a4-7137a8bf0bb1.png)


[snakeware](https://github.com/joshiemoore/snakeware "**snakeware**")是一款基于Python开发的Linux发行版操作系统。

snakeware的窗口管理器snakewm是基于pygame/pygame_gui。而且，snakeware不使用任何其他大型且不透明的软件，如systemd等。它的目标是最终拥有一组完全用Python编写的可用的用户空间应用程序和实用程序，用户将直接被引导到一个Python解释器中，可以使用该解释器对计算机执行任何想要的操作。

## video2x

**Star：1.3k**

![](https://imgkr.cn-bj.ufileos.com/6cb591a2-bfe1-4f19-86b5-5056c6baadba.png)

[video2x](https://github.com/k4yt3x/video2x "**video2x**")是一款**视频/图片/GIF**无损方法工具。

之前曾介绍过几款图片无损放大工具，例如，bigjpg、waifu2x。

而video2x就是基于waifu2x、Anime4K、SRMD和RealSR等实现的一款视频、图片、GIF无损放大工具。

**示例**

原GIF图像（160x120）：

![](https://imgkr.cn-bj.ufileos.com/f7b4b9f4-4939-4b7c-9a55-a5299dc4c090.gif)

经过放大4倍（640x480 ）之后的结果：

![](https://imgkr.cn-bj.ufileos.com/b1df0337-3649-46ad-990f-c8b656a68469.gif)

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN&scene=21#wechat_redirect)

---

**个人微信**

欢迎各位同学添加我的个人微信，互相交流、互相学习，第一时间获得更多冷门好用的小工具！


![](https://imgkr.cn-bj.ufileos.com/7310b2b1-3b60-4c62-bdd2-2d3b6414e3c8.png)

我整理了10T+资源进行共享，其中包括**实用工具、Python电子书、Spring视频教程、机器学习资源**，扫码关注我的公众号“**平凡而诗意**”，后台回复相应关键字即可获得。除此之外，原创技术文章会第一时间推送，如果喜欢，麻烦点一下“**在看**”~


![](https://imgkr.cn-bj.ufileos.com/32d5c0b0-7012-4353-825e-ffb216b12d3b.png)



