## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

如果喜欢，麻烦给个**Star**支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **pre-commit**
- **beets**
- **Picard**
- **pydantic**
- **airflow**

下面分别来介绍一下上述5个GitHub项目。

## pre-commit

**Star：4k**

代码规范检查是项目上线过程中必不可少的一环，在大多数情况下，我们都是把代码提交到代码库再进行静态检查。但是，为什么不从最**源头**把这个问题解决呢？

[**pre-commit**](https://github.com/pre-commit/pre-commit)是一款由Python开发的`git hooks`工具，它能够在合入代码，提交`commit`时对代码进行规范检查和格式化，这样就能够从根源上解决代码规范的问题，而不是把代码合入到代码库中再统一解决，这样不仅耗时，而且繁琐。

我们下面以Python项目中使用为例进行介绍，但是，它不仅适用于Python，它能够适用于**所有编程语言**。

#### 安装

```shell
pip install pre-commit
```

#### 配置文件

安装之后需要修改一下配置文件，`.pre-commit-config.yaml`，

```yaml
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.3.0
    hooks:
    -   id: check-yaml
    -   id: end-of-file-fixer
    -   id: trailing-whitespace
-   repo: https://github.com/psf/black
    rev: 19.3b0
    hooks:
    -   id: black
```

#### 使用

```shell
pre-commit install
git commit -m "Add super awesome feature"
```

提交`commit`之后就可以看到，它会用到两个工具**black**和**flake8**。black我在第七期介绍过这款工具，它是一款高效的代码格式化工具，用于修改代码格式。flake8是一款格式检查工具。

![](https://imgkr.cn-bj.ufileos.com/7e8275bb-2502-47fa-8722-a270bdc96df3.png)

## beets

**Star：9.2k**

[**beets**](https://github.com/beetbox/beets)是一款音乐收藏辅助工具，它能够让音乐收藏一劳永逸。它会对你的集合进行分类，并在此过程中自动增强其元数据。然后，它通过提供的一组工具来操作和访问你的音乐。

#### 安装

```shell
pip install beets
```

具体使用教程可以查看[**文档**](https://beets.readthedocs.io/en/stable/guides/main.html)。

## Picard

**Star：2k**

[**Picard**](https://github.com/metabrainz/picard)是一款由Python开发的跨平台音乐标记工具，它能够在Linux/Mac OS X/Windows多个平台上进行使用。

Picard支持大多数音频文件格式，能够使用音频AcoustIDs，执行CD查找和磁盘ID提交，并且具有出色的Unicode支持。

![](https://imgkr.cn-bj.ufileos.com/58f659d1-ac4c-4a48-915e-aa3df7480a82.gif)

## pydantic

**Star：2.5k**

使用过Python的应该都很清楚，Python是一种对**数据类型**非常弱化的一种编程语言。在编写Python程序时，你不需要去关心数据的类型。但是，这对于阅读代码和调试代码却带来了很多麻烦，因此，我们还是需要养成C++/Java那样的好习惯，应该关注数据类型。

[**pydantic**](https://github.com/samuelcolvin/pydantic)是一款使用Python类型提示对Python项目进行数据验证和设置管理的工具。

#### 安装

```shell
pip install -U pydantic
```

#### 示例

```Python
from datetime import datetime
from typing import List, Optional
from pydantic import BaseModel

class User(BaseModel):
    id: int
    name = 'John Doe'
    signup_ts: Optional[datetime] = None
    friends: List[int] = []

external_data = {'id': '123', 'signup_ts': '2017-06-01 12:22', 'friends': [1, '2', b'3']}
user = User(**external_data)
print(user)
#> User id=123 name='John Doe' signup_ts=datetime.datetime(2017, 6, 1, 12, 22) friends=[1, 2, 3]
print(user.id)
#> 123
```

通过上述示例我们可以看出，通过继承pydantic中的BaseModel，能够对传入的参数进行数据类型的校验和修正，这样能够避免开发过程中难以定位的问题。

## airflow

**Star：16k**

[**airflow**](https://github.com/apache/airflow)一个通过**编程方式**编写、调度和监视**工作流**的平台。

为什么调度、监视工作流的方式有很多，却偏偏选择airflow呢？

因为，当工作流被定义为代码时，它们变得更加可维护、版本化、可测试性和协作性，通过定义airflow有向无环图工作流可以实现如下优点，

- 动态
- 可扩展
- 简洁清晰

![](https://imgkr.cn-bj.ufileos.com/411ae4a0-c106-44ca-af41-0adc1b729068.png)

------

#### 推荐阅读

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)

------

欢迎关注我的公众号“**平凡而诗意**”，原创技术文章第一时间推送，如果喜欢，麻烦点一下“**在看**”~
