## **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **git-imerge**
- **homu**
- **ProxyPool**
- **PythonDataScienceHandbook**
- **selenium**

下面分别来介绍一下上述5个GitHub项目。

## **git-imerge**

**Star：2k**

[**git-imerge**](https://github.com/mhagger/git-imerge)是一款用于增量合并分支、减少冲突的Python小工具。

在使用git进行版本控制的过程中，最令人痛苦的事情之一就是合并时产生的冲突，在解决冲突的过程中，不仅面临很大的误操作风险，还需要很多让人苦不堪言的手动操作。

当然，在这些冲突中，有一些是无法避免的，但是也有很多事可以避免的，使得冲突最小化。

当使用git-imerge进行增量合并时，它会给出如下提示，

```
while not done:
    <fix the conflict that is presented to you>
    <"git add" the files that you changed>
    git-imerge continue
```

解决完冲突之后，使用如下命令完成修改，

```
git-imerge finish
```

## **homu**

**Star：638**

[**homu**](https://github.com/barosl/homu)是一款与Github继承的机器人小工具，一款增强Github的自动化工具。

![img](https://pic2.zhimg.com/80/v2-108209118fad6ab97c2a155833fcd663_1440w.png)

以Travis CI为例，如果将pull请求发送到存储库，Travis CI会立即显示测试结果，这样虽然看似很好。但是，在几个其他的pull请求被合并到主分支之后，pull请求在被合并到主分支之后可能会破坏一些东西。

要解决这个问题，应该在合并之前执行测试过程，而不是在接收到pull请求之后。你可以在每次合并pull请求之前手动单击“restart build”按钮。

显然，每次手动执行这个过程是很麻烦的，homu可以自动执行此过程。它监听pull 请求，然后通过集成服务对它进行测试，只有当它通过所有测试时，它才会被合并到master中。

## **ProxyPool**

**Star：1.2k**

[**ProxyPool**](https://github.com/Python3WebSpider/ProxyPool)是一款高效的代理池工具。

我们在很多工作场景下会用到**代理**，例如，一个比较典型的场景：爬虫。通过这些代理，我们可以解决针对不同网站的请求问题，但是，有些代理是收费的，有些是免费的，当需要到用到免费代理时却无从下手。

ProxyPool提供了免费高效的代理池，它具有如下特点，

- 定时抓取免费代理网站，简易可扩展。
- 使用 Redis 对代理进行存储并对代理可用性进行排序。
- 定时测试和筛选，剔除不可用代理，留下可用代理。
- 提供代理 API，随机取用测试通过的可用代理。

**安装依赖包**

使用ProxyPool之前首先需要安装依赖包，

```
pip3 install -r requirements.txt
```

**运行代理池**

ProxyPool提供Tester、Getter、Server三种方法，可以单独运行，也可以全部运行。

全部运行，命令如下，

```
python3 run.py
```

单独运行，命令如下，

```
python3 run.py --processor getter
python3 run.py --processor tester
python3 run.py --processor server
```

## **PythonDataScienceHandbook**

**Star：22.7k**

[**PythonDataScienceHandbook**](https://github.com/jakevdp/PythonDataScienceHandbook)是一个使用Jupyter Notebook编写的一个数据科学手册。

数据分析、挖掘是Python比较热门的一个应用领域，也是现在在企业中应用和岗位较多的方向。所以，我认为，如果学习Python，数据科学是很多同学都无法绕开的，因此，掌握数据科学的技能是非常有必要的。

在数据科学中，经常用到的第三方库主要有如下几个，

- numpy
- pandas
- matplotlib
- scikit-learn

![img](https://pic1.zhimg.com/80/v2-1bede066c3ef3f57dc2bd87b91160dd0_1440w.png)

通过PythonDataScienceHandbook，你不仅可以能够学到数据分析、挖掘、机器学习的理论知识，还可以在这些知识的过程中掌握上述这些常用Python第三方库的使用。

## **selenium**

**Star：17.3k**

[**selenium**](https://github.com/SeleniumHQ/selenium)是一款热门、强大的web自动化工具。

我们每天大多数时间都花费在浏览器上，例如，知识和数据的获取。我们需要频繁、重复的访问web浏览器。虽然，我们已经对手动访问习以为常，但是，其中有很多工作是可以用自动化工具替代，可以解放一下双手。

此前，我曾介绍过一款web自动化工具helium，它就是基于selenium开发的一款工具。

但是，这些被封装好的工具难免定制性太强，灵活度不够，我们可以发散思维，基于selenium开发出一款个性化的自动化工具集，来满足个人的需求。此外，selenium还支持如下多种编程语言的API接口，

- C#
- JavaScript
- Java
- Python
- Ruby

以Python为例简单的介绍一下selenium的使用。

**安装**

```
pip install -U selenium
```

selenium的运行，需要依赖不同浏览器的驱动，例如，Firefox、Google、Edge，下面以Firefox给出一段示例代码，

```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

browser = webdriver.Firefox()

browser.get('http://www.yahoo.com')
assert 'Yahoo' in browser.title

elem = browser.find_element_by_name('p')  # Find the search box
elem.send_keys('seleniumhq' + Keys.RETURN)

browser.quit()
```

这样就可以在浏览器中完成一系列的动作。

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)

