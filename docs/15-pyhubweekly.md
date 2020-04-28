## **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **photo2cartoon**
- **jumpcutter**
- **mkdocs**
- **chineseocr**
- **streamlit**

下面分别来介绍一下上述5个GitHub项目。

## **photo2cartoon**

**Star：652**

![img](https://pic1.zhimg.com/80/v2-ae1bce0699f59b17aafba65caf0f7a58_1440w.png)

[**photo2cartoon**](https://github.com/minivision-ai/photo2cartoon)是一款图像转卡通的Python项目。

这类工具、项目其实有很多，大多数效果都是差强人意。当看到这个工具的时候，我本身觉得“噱头”，但是，当使用之后顿时大感惊艳。

有很多图片转卡通工具，要么过度偏于卡通，而丢失了原图像中人物特别的信息。有很多工具过度真实，有没有卡通的感觉。

而photo2cartoon，在保持原图像ID信息和纹理细节的同时，将真实照片转换为卡通风格的非真实感图像。这款工具既有卡通图像的可爱风格，又对原始图像保留真实信息。

**使用教程**

```
git clone https://github.com/minivision-ai/photo2cartoon.git
cd ./photo2cartoon
python test.py --photo_path ./images/photo_test.jpg --save_path ./images/cartoon_result.png
```

另外，photo2cartoon有对应的微信小程序。如果你对源码很感兴趣，或者希望定制化，也可以克隆源码，进行修改，对模型重新训练。

## **jumpcutter**

**Star：2.2k**

[**jumpcutter**](https://github.com/carykh/jumpcutter)是一款智能的视频自动编辑工具。

当我们拍摄一段视频出现失误时，会怎么办？重新录制？手动编辑？

jumpcutter让这件事情变得非常简单，在拍摄视频时，当有些部分想要删除，只需要一个大拇指朝下的手势，如果希望保留，那么就竖起大拇指。这样，它在后期处理的过程中会根据视频中的手势对每一段视频选择是保留还是删除。

## **mkdocs**

**Star：9.8k**

![img](https://pic3.zhimg.com/80/v2-eff7892fa6db74956cfa76ca8533fe05_1440w.png)

[**mkdocs**](https://github.com/mkdocs/mkdocs)是一个快速、简单、漂亮的静态网站生成器，专门用于构建项目文档。

应该有很多同学都有过搭建网站的想法，它可以很复杂，也可以很简单。

如果单纯为了写作，我认为静态网站就足够了。mkdocs就是一款可以快速搭建静态网站的工具，我们在网络上找一些在线电子文档时会发现很多都非常想起，它们大多数都是基于mkdocs搭建的。

## **chineseocr**

**Star：2.8k**

[**chineseocr**](https://github.com/chineseocr/chineseocr)是一款基于yolov3的OCR工具。

- 支持0、90、180、270不同角度文字识别
- 支持(darknet/opencv dnn /keras)文字检测,支持darknet/keras训练
- 支持darknet 转keras, keras转darknet, pytorch 转keras模型
- 支持身份证/火车票结构化数据识别
- 单行图像平均时间为0.02秒以下

## **streamlit**

**Star：7.8k**

[**streamlit**](https://github.com/streamlit/streamlit)是一款用于快速创建机器学习应用的一款Python工具。

从最初C++逐行编写成千上万行代码实现一个目标识别系统，到现在利用高度集成gluon、keras深度学习库几行代码即可完成，再到这两年很多大公司都在争相竞争的AutoML平台。使得这个看似高深的机器学习领域，变得越来越简单、平民化。

![img](https://pic3.zhimg.com/80/v2-3264f6c54d9b044293a137e473d3be9a_1440w.gif)

streamlit允许您使用简单的Python脚本，创建一个机器学习应用程序。它支持热加载，所以你的应用程序能够根据你文本编辑和保存情况实时更新。

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)