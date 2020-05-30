## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **AnimeGAN**
- **faker** 
- **Background-Matting**
- **PyBoy**
- **Learning-to-See-in-the-Dark**

下面分别来介绍一下上述5个GitHub项目。

### AnimeGAN

**Star：1.8**

[**AnimeGAN**](https://github.com/TachibanaYoshino/AnimeGAN)是是一款可以把真实图片转化为动漫风图像的工具。


![](https://imgkr.cn-bj.ufileos.com/e997d056-96a4-4a3b-b086-a7f3214e104b.png)


AnimeGAN是论文《AnimeGAN: a novel lightweight GAN for photo animation》的实现，利用近几年人工智能领域比较热门的GAN实现把真实图片转化为动漫风图像。

### faker

**Star：9.8k**

[**faker**](https://github.com/joke2k/faker)是一款用于生成伪造数据的Python小工具。

造数据，在开发过程中至关重要，尤其是在企业项目中，很多数据会涉及到敏感信息，很难获取到客户数据。这时候，如果要进行功能的开发和测试，就需要自己想办法造数据。

造数据是一件非常令人头疼的事情，如果让你造一条**地址信息**，可能会脱口而出。那如果让早10000条数据呢？这就是一个即耗脑力，又耗体力的活。

faker就可以一行代码实现数据的生成。

faker可以根据不同的参数生成不同语言、不同类型的数据。

**安装使用**

可以直接使用`pip`命令进行安装，

```python
pip install Faker
```

生成数据，

```python
from faker import Faker
fake = Faker(['it_IT', 'en_US', 'ja_JP'])
for _ in range(10):
    print(fake.name())

# 鈴木 陽一
# Leslie Moreno
# Emma Williams
# 渡辺 裕美子
# Marcantonio Galuppi
# Martha Davis
# Kristen Turner
# 中津川 春香
# Ashley Castillo
# 山田 桃子
```

### Background-Matting

**Star：3.1k**


![](https://imgkr.cn-bj.ufileos.com/0c53962d-2c82-485b-a9df-8e45aa107c6f.png)


[**Background-Matting**](https://github.com/senguptaumd/Background-Matting)是CVPR 2020上一篇名为《Background Matting: The World is Your Green Screen》文章的实现项目，通过这个算法，可以轻松实现图像背景的替换。

自动抠图或者替换背景早已经不是什么新鲜事，但是，大多数工具的修建图像的效果差强人意。

《Background Matting: The World is Your Green Screen》基于对抗网络提出一种新型、基于深度学习的背景消除、替换算法，在大量图像、视频数据的验证结果中显示，能够达到比以往算法更好的效果。



### PyBoy

**Star：2.7k**

[**PyBoy**](https://github.com/Baekalfen/PyBoy)是一款用Python编写的Game Boy模拟器。


![](https://imgkr.cn-bj.ufileos.com/7b6de29e-bdbb-47c1-ab3e-1b50d53a53b7.gif)

Game Boy是任天堂发售的掌上游戏机系列，而PyBoy实现了可以通过API接口的方式，模拟并控制GameBoy游戏。


### Learning-to-See-in-the-Dark

**Star：4.7**

[**Learning-to-See-in-the-Dark**](https://github.com/cchen156/Learning-to-See-in-the-Dark)是一款暗光图像处理项目。

看过华为P30、P40系列发布会的应该都被它强大的暗光处理惊艳到了。


![](https://imgkr.cn-bj.ufileos.com/aa899363-4c96-4f70-8fb6-fd73ae058855.png)


的确，在暗光条件下，受到低信噪比和低亮度的影响，图片的质量会受到很大的影响，低曝光率的照片会出现很多噪声，而长曝光时间会让照片变得模糊、不真实。

Learning-to-See-in-the-Dark通过FCN方法将在黑暗环境中进行的拍摄还原的方法，能够清晰还原暗光图像。

---

#### 推荐阅读

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN&scene=21#wechat_redirect)

---


我整理了10T+资源进行共享，其中包括**实用工具、Python电子书、Spring视频教程、机器学习资源**，扫码关注我的公众号“**平凡而诗意**”，后台回复相应关键字即可获得。除此之外，原创技术文章会第一时间推送，如果喜欢，麻烦点一下“在看”~


![](https://imgkr.cn-bj.ufileos.com/7b4f990b-6fd4-4499-8801-0e99584193af.png)