## **前言**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **mitmproxy**
- **pygame**
- **pytudes**
- **httpx**
- **prefect**

下面分别来介绍一下上述5个GitHub项目。

## **mitmproxy**

**Star：18.4k**

[**mitmproxy**](https://github.com/mitmproxy/mitmproxy)是一款可以用来拦截、修改、保存 HTTP/HTTPS 请求中间代理工具，可以用于开发过程中的正向代理，反向代理，透明代理等。

安装mitmproxy之后会包含3个工具，mitmproxy、mitmdump、mitmweb。

mitmproxy是一个交互式的、支持SSL/TLS的拦截代理，具有HTTP/1、HTTP/2和WebSockets的控制台接口。

mitmdump是mitmproxy的命令行版本。

mitmweb是mitmproxy的一个基于web的接口。

**安装**

mitmproxy支持macos、linux、windows等多个平台的安装，也支持使用pip命令直接安装，

```
pip install mitmproxy
```

## **pygame**

**Star：1.9k**

[**pygame**](https://github.com/pygame/pygame)是一款跨平台，用于开发各种多媒体软件（例如游戏）的一个Python库。

![img](https://pic1.zhimg.com/80/v2-7cb378c8334f87bd5b5c9e3984fac1e5_1440w.png)

pygame是一个利用SDL库的写就的游戏库，它支持的功能包括但不限于，

- 访问光驱
- 访问显示设备
- 绘制形状
- 管理事件
- 使用字体
- 加载和存储图片
- 使用手柄
- 读取键盘
- ...

通过使用pygame，你可以很容易开发一款多媒体应用，当然，你可以使用它来开发一款游戏。

## **pytudes**

**Star：13.6k**

[**pytudes**](https://github.com/norvig/pytudes)是一个汇聚Python编程技巧的github项目。

目前github有很多有关Python的编程小技巧，但是大多数都是围绕着基础语法和单点的知识在展开。

![img](https://pic4.zhimg.com/80/v2-3a15717e6d0104e843750b9f94f56a7d_1440w.png)

和大多数汇集编程技巧的项目，pytudes更多的是由某个事件而发起的，为了解决一个问题而给出一个具体的实现过程，在这个过程中会展示很多Python编程技巧，我想，这样能够让学习者理解的更加深刻。

## **httpx**

**Star：4.3k**

[**httpx**](https://github.com/encode/httpx)是一款用于Python3、功能齐全的http客户端，它提供同步和异步api，并支持HTTP/1.1和HTTP/2。

它不仅拥有requests具备的功能，它还具备更多更强大的功能，例如，

- 兼容的API
- 标准同步和异步接口
- 支持HTTP/1.1和HTTP/2
- 能够直接向WSGI应用程序或ASGI应用程序发出请求
- ...

例如，

```python
>>> import httpx
>>> r = httpx.get('https://www.example.org/')
>>> r
<Response [200 OK]>
>>> r.status_code
200
>>> r.headers['content-type']
'text/html; charset=UTF-8'
>>> r.text
'<!doctype html>\n<html>\n<head>\n<title>Example Domain</title>...'
```

## **prefect**

**Star：2k**

[**prefect**](https://github.com/PrefectHQ/prefect)是一款面向数据科学的工作流自动化管理系统。

prefect是一个新的工作流管理系统，它是为现代基础设施而设计的，由开源的Prefect核心工作流引擎提供支持。用户将任务组织成流程，而prefect就可以负责其余的各种管理工作。

**示例**

```python
from prefect import task, Flow, Parameter


@task(log_stdout=True)
def say_hello(name):
    print("Hello, {}!".format(name))


with Flow("My First Flow") as flow:
    name = Parameter('name')
    say_hello(name)


flow.run(name='world') # "Hello, world!"
flow.run(name='Marvin') # "Hello, Marvin!"
```

启动prefect的本地用户界面来协调和管理工作流：

```
prefect server start
```

然后就可以跳转到http://localhost:8080打开管理页面。

------

### **推荐阅读**

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN#rd)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN#rd)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN#rd)
- [开发者常用工具集 | 如果早一些看到这篇文章该多好](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485022&idx=1&sn=9c10067cd7a2452ffc94582c13ec160b&chksm=e94e9956de391040a4b8d55bab1708945f0c9e170a55eac18ca53a1be11724ca36a5299908da&token=886687278&lang=zh_CN#rd)
- [实用工具 | 5款超实用浏览器插件，第一款真神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485001&idx=1&sn=0664d17a6f677c9e1d433f285f096112&chksm=e94e9941de391057dea8c84c1d45925621696d5d735d2bab6e0b7ef786ac813b415c53cfb2b9&token=457191310&lang=zh_CN#rd)
- [实用工具 | 10款搜索引擎，看到第一款就会毅然放弃百度！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484976&idx=1&sn=f8ac0fd665d8918f52a5d599f636a7ad&chksm=e94e9938de39102ee33220f42bbe9a4f0832c7bf5cc8c7a47aef8548a8688bae1793facad073&token=2025215714&lang=zh_CN#rd)
- [实用工具 | 6款免费OCR工具，第一款是神器](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484951&idx=1&sn=e63f6dd0e781114515d9b27b4397c065&chksm=e94e991fde391009a1c2a77392fb89435f8fae9d266f05eadee86784ae615b89ecb7bfae4b70&token=2025215714&lang=zh_CN#rd)