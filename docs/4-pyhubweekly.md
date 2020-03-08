## **本期内容**

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具.

如果喜欢，麻烦给个**Star**支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上4个优质的Python项目，它们分别是：

[1. fastapi](https://github.com/tiangolo/fastapi)

[2. system-design-primer](https://github.com/donnemartin/system-design-primer)

[3. thefuck](https://github.com/nvbn/thefuck)

[4. vulture](https://github.com/jendrikseipp/vulture)

下面分别来介绍一下上述4个GitHub项目。

> 我建了一个QQ学习交流群，旨在“分享、讨论、学习、资源分享、就业机会、互联网内推、共同进步！”，感兴趣的可以加一下，也可以添加我的QQ~ QQ群：164660119；QQ号：498073774；公众号：【平凡而诗意】~

## [1. fastapi](https://github.com/tiangolo/fastapi)

**Star：**9.2k

在项目开发中，往往会涉及多个模块，在不同模块之间如何进行数据传递和调用是一个成熟系统需要慎重考虑的。

如果是对实时性要求不高的离线系统，有很多选择，例如，最简单的通过数据库建立连接。但是，对于那些对效率要求较高的系统，往往会选择**restful**接口。

目前，Python中用于开发api接口的工具比较知名的有flask，而本文介绍的fastapi调用更加高效、鲁棒性更强、开发和调试更加便捷，而且支持可视化的文档界面可以用于手动调试接口。

![img](https://pic1.zhimg.com/v2-d83f98215760f6a96631293d9c47b8a8_b.png)

## [2. system-design-primer](https://github.com/donnemartin/system-design-primer)

**Star：**82.3k

很多互联网、IT行业的从业者都会考虑一个问题，有一天年龄大了、该何去何从？产品经理？项目经理？

我个人认为架构师也是一个很不错的选择，一个好的架构能够让开发过程中效率大大提升。我们在开发过程中处处也都在接触架构，往小了说会接触算法核心的架构，往大了会接触整个系统从数据层到前端多个环节的架构。

在开发一些项目之后我愈发的认识到一个优秀的架构师有多么难得，要同时兼顾考虑web服务、数据读写、运维安全、网络通讯、缓存机制、负载均衡等。

因此，我给自己制定的2020年计划中有一项就是在大型系统的架构方面有更加深入的学习，无意之中我看到system-design-primer这个项目，如获至宝，它从CDN到负载均衡、从反向代理到应用层、从数据库到缓存、从异步到通讯都进行了深入的阐述，非常实用且切合实际的项目需求。

![img](https://pic2.zhimg.com/v2-58076678e376c92a16f9dcf1d5b8cebd_b.png)

## [3. thefuck](https://github.com/nvbn/thefuck)

**Star：**51.9k

这是一款由Python开发的命令行**纠错**工具。

Linux命令是在开发过程中经常接触的工具，当我们输入一长串命令，按下enter键之后怎么办？

- 重新输入一遍
- 上键+移动到指定位置修改

这显然是比较低效的。thefuck提供了简单高效的解决方案，虽然它名称看上去粗俗了一些，但是的确好用，当输入命令错误之后，只需要在命令行下输入f**k即可显示更正后的命令，免得再去手动修改。

![img](https://pic3.zhimg.com/v2-fef68d0075236e805eb657180e9bdee2_b.gif)

## [4. vulture](https://github.com/jendrikseipp/vulture)

Star：791

vulture是一款无用代码查找、清理工具。

当我们开发一个项目过程中，会不断的对某些部分进行增删、修改，这个过程中会产生很多无用的引用和代码。当这个工程代码量逐渐增多时，我们用人眼挨个去寻找无用代码自然是不现实的。

vulture在Python程序中查找未使用的代码。这对于清理和查找大型代码库中的错误很有用。如果同时在库和测试套件上运行vulture，则可以找到未经测试的代码。

例如，我们新建一个code.py文件，

```
import os

class Greeter:
    def greet(self):
        print("Hi")

def hello_world():
    message = "Hello, world!"
    greeter = Greeter()
    greet_func = getattr(greeter, "greet")
    greet_func()

if __name__ == "__main__":
    hello_world()
```

调用vulture，

```
> vulture code.py
dead_code.py:1: unused import 'os' (90% confidence)
dead_code.py:4: unused function 'greet' (60% confidence)
dead_code.py:8: unused variable 'message' (60% confidence)
```

这样，就可以输出无用的引用、函数、变量，同时，会给出每一个判断的可信度。

此外，vulture还支持设置最小可信度、白名单等功能，这对于减少项目的冗余代码非常有用。

## **推荐阅读**

- [Python参数配置库ConfigParser详解](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484889&idx=1&sn=533d1b59410f8322a0c033afb861cfe6&chksm=e94e9ad1de3913c759960ad12db322daee45d108ebac658bf374fc3dd40f6f36f2692da23e06&token=1456867850&lang=zh_CN#rd)
- [迫不及待把这款开发神器推荐给大家！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484903&idx=1&sn=59dead902c4acc16c5149e3f838aab2d&chksm=e94e9aefde3913f9dc1bd9e584f4a76543253f0bc74354cc6230f2a49a319636e010d9ebb5db&token=1456867850&lang=zh_CN#rd)
- [抛弃bash，拥抱zsh！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484911&idx=1&sn=a02cb8db9508494672f86353acf48783&chksm=e94e9ae7de3913f137dda3702c314af3655c974f31ee7df7f79d7bb982f8f8d0f35adb751176&token=1456867850&lang=zh_CN#rd)
- [PyHubWeekly | 第四期：清理无效代码，给你的项目瘦瘦身吧！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484925&idx=1&sn=3cab27e39dfd34bff4aaa9c4b197ec3f&chksm=e94e9af5de3913e3199f96fb7a4304cb865387973b7552ec4ae77f5e4cfb4131badedbd021ff&token=1456867850&lang=zh_CN#rd)
- [实用工具 | 一款丰富强大的Python绘图工具](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484941&idx=1&sn=f5723139558043be73491df76a94da08&chksm=e94e9905de3910134d3afe346678d131fa9f01633879f58880c2e2ecfa1d8b66edaf44886ba3&token=1456867850&lang=zh_CN#rd)