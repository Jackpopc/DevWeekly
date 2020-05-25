## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，<!--more-->它们分别是：

- **jukebox**
- **python-patterns**
- **dabl**
- **missingno**
- **emot**

下面分别来介绍一下上述5个GitHub项目。

## jukebox

**Star：1.8k**

[**jukebox**](https://github.com/openai/jukebox)是一款由OpenAI开源的一款自动生成音乐的神经网络。



![](https://imgkr.cn-bj.ufileos.com/678d0f52-6ab1-4131-8e06-a29501935932.png)



生成网络用于自动生成是这两年人工智能领域研究比较热门的一个方面，例如，自动生成图像、自动生成音乐。

OpenAI开源的jukebox神经网络可以生成各种流派和艺术家风格的原始音频，也包括基本的歌唱。

jukebox在生成音乐的过程中，主要包括2个过程，

- 采样
- 训练

```python
# Required: Sampling
conda create --name jukebox python=3.7.5
conda activate jukebox
conda install mpi4py=3.0.3
conda install pytorch=1.4 torchvision=0.5 cudatoolkit=10.0 -c pytorch
git clone https://github.com/openai/jukebox.git
cd jukebox
pip install -r requirements.txt
pip install -e .

# Required: Training
conda install av=7.0.01 -c conda-forge 
pip install ./tensorboardX
 
# Optional: Apex for faster training with fused_adam
conda install pytorch=1.1 torchvision=0.3 cudatoolkit=10.0 -c pytorch
pip install -v --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" ./apex
```

## python-patterns

**Star：24.6k**

[**python-patterns**](https://github.com/faif/python-patterns)是Python中设计模式/习惯用法的集合。

我曾经不止在一篇文章中提及过设计模式的重要性，而对于Python这类语法简单、效率偏低的编程语言，更加重视设计模式。

设计模式并不是一种老生常谈的固定知识，而更加偏重于一种思维方式的转变，例如，原型模式、工厂模式。也就是说，即便你不使用这种设计模式也可以实现某种功能，但是如果使用，执行效率、维护成本、可读性都会得到极大程度的优化。

例如，下面示例的原型模式，

```python
class Prototype:

    value = 'default'

    def clone(self, **attrs):
        """Clone a prototype and update inner attributes dictionary"""
        # Python in Practice, Mark Summerfield
        obj = self.__class__()
        obj.__dict__.update(attrs)
        return obj


class PrototypeDispatcher:
    def __init__(self):
        self._objects = {}

    def get_objects(self):
        """Get all objects"""
        return self._objects

    def register_object(self, name, obj):
        """Register an object"""
        self._objects[name] = obj

    def unregister_object(self, name):
        """Unregister an object"""
        del self._objects[name]


def main():
    """
    >>> dispatcher = PrototypeDispatcher()
    >>> prototype = Prototype()
    >>> d = prototype.clone()
    >>> a = prototype.clone(value='a-value', category='a')
    >>> b = prototype.clone(value='b-value', is_checked=True)
    >>> dispatcher.register_object('objecta', a)
    >>> dispatcher.register_object('objectb', b)
    >>> dispatcher.register_object('default', d)
    >>> [{n: p.value} for n, p in dispatcher.get_objects().items()]
    [{'objecta': 'a-value'}, {'objectb': 'b-value'}, {'default': 'default'}]
    """


if __name__ == '__main__':
    import doctest
    doctest.testmod()
```

## dabl

**Star：438**

[**dabl**](https://github.com/dabl/dabl)是一款数据分析基准库。

这个项目试图使监督机器学习对于初学者变的更容易，并减少见任务的复杂度。

例如，利用**dabl**进行分类的一个示例，

```python
import dabl
from sklearn.model_selection import train_test_split
from sklearn.datasets import load_digits
X, y = load_digits(return_X_y=True)
X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=1)
sc = dabl.SimpleClassifier().fit(X_train, y_train)
Running ...
print("Accuracy score", sc.score(X_test, y_test))
Accuracy score 0.9...
```
就这样简单的几行代码，几秒钟的时间内既可以获得分类结果。

其实，dabl的最大优点并不在于机器学习，而是在于为数据探索提供了简单的接口。下面是一个简单地通过调用plot(X, y)生成的可视化示例:


![](https://imgkr.cn-bj.ufileos.com/bf5f03b0-b903-49e9-8850-cbcb3e2f4e4f.png)


## missingno

**Star：2.2k**

[**missingno**](https://github.com/ResidentMario/missingno)是一款Python缺失数据的可视化工具。

数据，是我们在工作中**最为重要**的一个环节，没有之一。

无论是做人工智能，还是做业务相关，或者简单的做一些用户画像，如果没有数据，或者数据质量差，一切产品规划都无从谈起。我想，在互联网、IT行业工作过的同学应该都会有这样的体会。

而数据缺失，又是我们在数据质量验证中最为重要的一项任务。

很多刚从业的同学，刚接触到项目便开始把目光放在算法的研究和开发方面，一番努力之后，发现效果并没有达到预期，回头定位问题的时候才发现数据确实严重，而在这个过程中已经浪费掉很多时间和精力。


![](https://imgkr.cn-bj.ufileos.com/0a925a86-1b19-4ef1-a427-b085d0c32a84.png)


而，如果我们在着手研发之前，先对数据质量进行验证，可视化一下缺失情况，这样就避免不必要的人力浪费。

## emot

**Star：64**

[**emot**](https://github.com/NeelShah18/emot)是一款用于提取文本中表情的简单小工具。


```python
>>> import emot
>>> text = "I love python 👨 :-)"
>>> emot.emoji(text)
>>> [{'value': '👨', 'mean': ':man:', 'location': [14, 14], 'flag': True}]
>>> emot.emoticons(text)
>>> {'value': [':-)'], 'location': [[16, 19]], 'mean': ['Happy face smiley'], 'flag': True}
```
emot可以用于从文本(字符串)中提取emojis和emoticon等，所有的表情符号。

**安装**

通过pip安装，

```python
$ pip install emot --upgrade
```
从master分支安装，

```python
$ git clone https://github.com/NeelShah18/emot.git
$ cd emot
$ python setup.py install
```

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)

---

欢迎关注我的公众号“**平凡而诗意**”，原创技术文章第一时间推送，如果喜欢，麻烦点一下“**在看**”~

<center>
    <img src="https://imgkr.cn-bj.ufileos.com/ba67a0df-9e73-4dcd-8a83-7479f9076350.jpg" style="width: 150px;">
</center>