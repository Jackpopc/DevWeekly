## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[PyHubWeekly](Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **PandasGUI**
- **Pippi**
- **pylambdarest**
- **Fixit**
- **isort**

下面分别来介绍一下上述5个GitHub项目。

### PandasGUI

![img](https://mmbiz.qpic.cn/mmbiz_png/DGwXCh99GDDlDQOyvDHzSObrS4BeIeqIyQiafTsDxPq6WxaoHfAXVPgFWStGMcWp2cQe9IuRPyP6af3N4boEReQ/640?wx_fmt=png)

学习Python数据分析，有2个工具包一定会被用到，分别是`numpy`和`pandas`。

`pandas`可以说是Python数据分析中的神器，它可以在Python语言中实现很多SQL语句的功能。而且，还具备很多数据清洗和处理的附加功能。

但是，对比于很多数据库工具，它有一点不好的地方就是，它在可视化方面做的很差。

而**PandasGUI**的出现，让我大为经验，它能够直接把pandas的DataFrames进行可视化，让我们数据分析过程中对数据有一个更加清晰的认知。

**安装**

```shell
$ pip install pandasgui
或
$ pip install git+https://github.com/adamerose/pandasgui.git
```

**用法**

首先，创建一个简单的DataFrames：

```Python
import pandas as pd
from pandasgui import show
df = pd.DataFrame(([[1, 2, 3], [4, 5, 6], [7, 8, 9]]), columns=['a', 'b', 'c'])
show(df)
```

如果你将代码作为脚本而不是在IPython或Jupyter中运行，则需要这样做：

```Python
show(df, settings={'block': True})
```

### Pippi

从事计算机视觉，能够找到很多和图像处理相关的Python库。从事自然语言处理，NLP相关的工具包也是层出不穷。

而音乐作为一种常见的多媒体形式，却鲜有相关的Python工具包。

如果你想通过代码处理一段音乐，然后对它进行控制和调整，就会不知所措、无从下手。

Pippi[3]就可以满足你的这个需求，它是一款用于Python的音乐处理库，它包含了一些方便的音乐数据结构，如SoundBuffer和Wavetable，使得处理音乐变得非常简单。除此之外，它还可以对音乐格式进行**转换**。

```Python
from pippi import dsp

sound1 = dsp.read('sound1.wav')
sound2 = dsp.read('sound2.flac')

# Mix two sounds
both = sound1 & sound2

# Apply a skewed hann Wavetable as an envelope to a sound
enveloped = sound * dsp.win('hann').skewed(0.6)

# Or just a sine envelope via a shortcut method on the `SoundBuffer`
enveloped = sound.env('sine')

# Synthesize a 10 second graincloud from the sound, 
# with grain length modulating between 20ms and 2s 
# over a triangle shaped curve.
cloudy = enveloped.cloud(10, grainlength=dsp.win('tri', dsp.MS*20, 2))
```

### pylambdarest

当让你用Python写一个REST API接口时，大概率会想到Flask。

而pylambdarest[4]是Flask之外一个非常不错的选择。

它是一款轻量级的框架，用于使用AWS Lambda + API网关构建REST API。

与大多数其他Python框架不同，它不提供任何路由功能，路由由API网关本身处理。

下面通过一个示例来对于pylambdarest与其他工具包的不同之处，

**其他工具包**

```Python
import json

def handler(event, context):
    body = json.loads(event["body"])
    query_params = event["queryStringParameters"]
    path_params = event["pathParameters"]

    return {
        "statusCode": 200,
        "body": json.dumps({
            "message": f"Hello from AWS Lambda {body['name']}!!"
        })
    }
```

**pylambdarest**

```Python
from pylambdarest import route

@route()
def handler(request):
    body = request.json
    query_params = request.query_params
    path_params = request.path_params

    return200, {"message": f"Hello from AWS Lambda {body['name']}!!"}
```

当使用API网关和python Lambdas时，最常见的模式是由代理API网关资源触发一个唯一的Lambda。Lambda然后使用类似于Flask的框架来完成所有的路由。在API Gateway + Lambda上下文中，作者认为路由应该由API Gateway本身处理，然后将请求转发给针对每个资源或endoint的特定Lambda函数。

### Fixit

Fixit[5]是一个对Flake8进行补充的lint框架。它基于LibCST，这使得提供自动修复成为可能。通过模式匹配、测试工具包和实用工具助手(例如范围分析)，可以很容易地构建Lint规则。它是优化的效率，易于定制。

**安装**

```
$ pip install fixit
```

通过配置fixit规则，可以对Python代码进行静态检查，能够有效的提升Python代码的质量。

### isort

Python是一门对语法要求相对宽松的编程语言，因此对于很多Python初学者来说这门语言非常简单。

但是，Python中有很多约定成俗的规则，通过这个规则的约束和遵从，能够提升Python代码的可读性，降低维护成本。

以Python代码中的`import`为例，就有一定的规则，内置模块、自定义模块、第三方模块的导入都是有一定顺序的。

isort[6]就是针对Python中`import`部分自动规范化的工具包，通过使用isort，可以迅速按照规则调整模块导入部分。

使用isort之前：

```Python
from my_lib import Object

import os

from my_lib import Object3

from my_lib import Object2

import sys

from third_party import lib15, lib1, lib2, lib3, lib4, lib5, lib6, lib7, lib8, lib9, lib10, lib11, lib12, lib13, lib14

import sys

from __future__ import absolute_import

from third_party import lib3

print("Hey")
print("yo")
```

使用isort之后：

```Python
from __future__ import absolute_import

import os
import sys

from third_party import (lib1, lib2, lib3, lib4, lib5, lib6, lib7, lib8,
                         lib9, lib10, lib11, lib12, lib13, lib14, lib15)

from my_lib import Object, Object2, Object3

print("Hey")
print("yo")
```