## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目PyHubWeekly**，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **shiv**
- **enaml**
- **Mimesis**
- **pyinfra**
- **pydantic**

下面分别来介绍一下上述5个GitHub项目。

### shiv

**Star：1k**

[**shiv**](https://github.com/linkedin/shiv)是一个用于构建Python工具包的命令行工具，它的宗旨是让Python打包变得更加简单。

系统要求：

- Python 3.6+
- Windows/OS X/Linux

下面，来看一下通过命令行来对Python代码进行打包。

```
$ shiv -c flake8 -o ~/bin/flake8 flake8
$ ~/bin/flake8 --version
3.7.8 (mccabe: 0.6.1, pycodestyle: 2.5.0, pyflakes: 2.1.1) CPython 3.7.4 on Darwin
```

通过一行命令就可以对Python代码进行打包。

### enaml

**Star：933**

[**enaml**](https://github.com/nucleic/enaml)是一种能够让你用最小的努力就可以实现高质量GUI界面的的Python框架，也是一种独特的编程语言

enaml将声明性语言与基于约束的布局系统结合在一起，使用户可以轻松地定义灵活布局的UI。enaml应用程序可以在任何支持Python和Qt的平台上运行。

enaml具有如下特性：

- 一种具有Python风格的声明性编程语言
- 数十个小部件都可以直接在Qt上构建
- 基于约束的布局引擎（基于Kiwi构建）
- 与数据模型工具（基于Atom构建）集成

**示例**

```python
from __future__ import print_function

import datetime

from atom.api import Atom, Str, Range, Bool, Value, Int, Tuple, observe
import enaml
from enaml.qt.qt_application import QtApplication


class Person(Atom):
    """ A simple class representing a person object.

    """
    last_name = Str()

    first_name = Str()

    age = Range(low=0)

    dob = Value(datetime.date(1970, 1, 1))

    debug = Bool(False)

    @observe('age')
    def debug_print(self, change):
        """ Prints out a debug message whenever the person's age changes.

        """
        if self.debug:
            templ = "{first} {last} is {age} years old."
            s = templ.format(
                first=self.first_name, last=self.last_name, age=self.age,
            )
            print(s)
   
....
```

完整代码可以查看**官方文档**[4]，效果如下：

![img](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/640)

### Mimesis

**Star：2.9k**

[**Mimesis**](https://github.com/search?q=Mimesis)是一款用于mock数据的Python工具。

系统开发往往是和数据不同步的，因此，在开发过程中就需要开发人员去造一批数据，但是，有一些数据并不是像生成随机数那么简单。例如，用户名、邮箱这些有规则，偏自然语言的数据。

Mimesis是一款速度快、可扩展、支持多语言的数据生成工具，你不仅可以直接使用它自带功能，还可以对它进行扩展，完成你想要的规则数据生成。

```
$ pip install mimesis
```

**使用**

Mimesis的使用非常简单，你只需要导入所需要数据的对象就行。

例如 ，你想生成的数据是和人相关的邮箱、地址、年龄，那么，你直接导入`Person`对象就行：

```
>>> from mimesis import Person
>>> person = Person('en')

>>> person.full_name()
'Brande Sears'

>>> person.email(domains=['mimesis.name'])
'roccelline1878@mimesis.name'

>>> person.email(domains=['mimesis.name'], unique=True)
'f272a05d39ec46fdac5be4ac7be45f3f@mimesis.name'

>>> person.telephone(mask='1-4##-8##-5##3')
'1-436-896-5213'
```

### pyinfra

**Star：917**

[**pyinfra**](https://github.com/Fizzadar/pyinfra)是一款可以大规模快速自动化部署、配置、管理应用的框架。

它可以用于执行临时命令、服务部署配置管理，能够轻松、快速的实现在数千台主机上进行执行你想要的操作。

**安装**

```
$ pip install pyinfra
```

现在，你就可以通过SSH去执行命令或者操作：

```
# Execute an arbitrary shell command
$ pyinfra my-server.net exec -- echo "hello world"

# Install iftop apt package if not present
$ pyinfra my-server.net apt.packages iftop sudo=true update=true
```

你也可以把它保存到部署代码文件中，

```
from pyinfra.operations import apt

apt.packages(
    name='Ensure iftop is installed',
    packages=['iftop'],
    sudo=True,
    update=True,
)
```

然后让它调用执行的Python文件：

```
$ pyinfra my-server.net deploy.py
```

### pydantic

**Star：3.9k**

[**pydantic**](https://github.com/samuelcolvin/pydantic)是一款用于数据解析和验证的Python工具。

pytantic是一款快速且可扩展，可与常用的IDE完美配合的数据解析和验证工具。

下面，通过一个示例来了解一下它的应用：

```
from datetime import datetime
from typing import List, Optional
from pydantic import BaseModel


class User(BaseModel):
    id: int
    name = 'John Doe'
    signup_ts: Optional[datetime] = None
    friends: List[int] = []


external_data = {
    'id': '123',
    'signup_ts': '2019-06-01 12:22',
    'friends': [1, 2, '3'],
}
user = User(**external_data)
print(user.id)
#> 123
print(repr(user.signup_ts))
#> datetime.datetime(2019, 6, 1, 12, 22)
print(user.friends)
#> [1, 2, 3]
print(user.dict())
"""
{
    'id': 123,
    'signup_ts': datetime.datetime(2019, 6, 1, 12, 22),
    'friends': [1, 2, 3],
    'name': 'John Doe',
}
"""
```

在这段代码中发生了什么？

- `id`在`User`类中被指定为int类型，如果传入的参数不符合要求则会报错；
- `signup_ts`被指定为datetime类型，而且`none`表名它不是必传参数，如果我们传入一个符合时间规范的字符串，它会把它转化为datetime类型；
- `friends`是一个列表，有int型和字符串型，在数据验证过程中会转化成int型；

这样做的好处是什么？

在Python中，数据类型的概念没有Java、C++这些语言中那么受人重视，这对于工程的稳定性、代码的阅读性都带来了一定的挑战。有了数据验证，它能够保证代码按照我们预先设定的那样去执行，保障工程的安全性。

---

给大家推荐1个宝藏公众号【**七步编程**】，专注于Python、AI、大数据领域内容分享。创作内容坚持原创与高质量，发表内容已经被诸多公众号大V转发，备受欢迎。现在关注，后台回复关键**567**就可以获得我精心整理的机器学习、深度学习、Python、推荐系统等技术方向的干货！

![image-20200829151145405](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/image-20200829151145405.png)