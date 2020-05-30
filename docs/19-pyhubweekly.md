## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目PyHubWeekly**，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **vardbg**
- **yfinance** 
- **Keylogger**
- **numerizer**
- **sentry-python**

下面分别来介绍一下上述5个GitHub项目。

## vardbg

**Star：508**

**vardbg**[2]是一款可以把Python代码调试生成可视化图像的工具。

代码调试是开发过程中占比很重的一个环节，也是非常繁琐、复杂的一个阶段。开发者一直在考虑，如果实现更加高效、准确的代码调试。

记得前不久看到Microsoft也在测试vs code的代码调试可视化工具，这让我颇为期待，我想，和我有同样心理的开发者应该不在少数。

其实，不需要等待vs code正式发布，我们就可以尝鲜这项功能。

vardbg可以把代码程序执行流程生成可视化图像，这样不仅可以有助于调试代码，还可以帮助可视化算法流程，有助于算法的学习。

![null](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)

**安装使用**

可以直接使用pip命令安装，

```
pip install vardbg
```

也可以通过源码安装，

```
git clone https://github.com/CCExtractor/vardbgcd vardbg
python3 -m venv venvsource venv/bin/activatepip install poetry
poetry install ../debug.py
pip install .
```

下面是执行一个快速排序代码的示例，

```
vardbg run sort.py quick_sort -o qsort.json -a 9 -a 3 -a 5 -a 1
```

然后，它就可以生成一个记录执行过程的可视化视频。

```
vardbg replay qsort.json -v sort_vis.mp4
```

## yfinance

**Star：1.8k**

**yfinance**[3]是一款Yahoo！金融数据下载工具。

数据对于从事数据分析、挖掘方向的同学一直都是一个巨大挑战。算法、编码都是非常成熟的。但是，如果没有数据，其余的都无从谈起。

金融，作为数据应用的一个典型的应用场景，受到很多同学的青睐，但是，从哪里获取到金融数据，却成了一个令人困扰的问题。

yfinance提供一种可靠、线程化、Python化的方式，使得能够轻松从雅虎下载金融市场数据。

**安装使用**

通过pip安装，

```
pip install yfinance --upgrade --no-cache-dir
```

通过conda安装，

```
conda install -c ranaroussi yfinance
```

下载数据，

```python
import yfinance as yf

msft = yf.Ticker("MSFT")

# get stock info
msft.info

# get historical market data
hist = msft.history(period="max")

# show actions (dividends, splits)
msft.actions

# show dividends
msft.dividends

# show splits
msft.splits

# show financials
msft.financials
msft.quarterly_financials

# show major holders
stock.major_holders

# show institutional holders
stock.institutional_holders

# show balance heet
msft.balance_sheet
msft.quarterly_balance_sheet

# show cashflow
msft.cashflow
msft.quarterly_cashflow

# show earnings
msft.earnings
msft.quarterly_earnings

# show sustainability
msft.sustainability

# show analysts recommendations
msft.recommendations

# show next event (earnings, etc)
msft.calendar

# show ISIN code - *experimental*
# ISIN = International Securities Identification Number
msft.isin

# show options expirations
msft.options

# get option chain for specific expiration
opt = msft.option_chain('YYYY-MM-DD')
# data available via: opt.calls, opt.puts
```

## Keylogger

**Star：802**

**Keylogger**[4]是一款用于记录敲击键盘记录，同时生成一份日志文件的工具。

通过这款工具，你可以应用于很多场景的监控之中，例如，

- 监控员工工作
- 记录禁用的字符
- 保护个人隐私，确保自己不在时没有人使用你的计算机
- 自我分析

Keylogger是一款跨平台的开源免费工具，它同时支持如下操作系统，

- Windows
- macOS
- Linux

## numerizer

**Star：73**

**numerizer**[5]是一款将自然语言中数字转化成`int`或者`float`型数字的Python小工具。

在文本分析或者网页爬虫时，无法避免的会遇到很多数字处理的问题，例如，`forty two`、`one million two hundred and fifty thousand and seven`。想要把这些语言表述转化为数据，往往需要写一个工具类，建立自然语言与数值之间的对应关系，同时还要处理自然语言的逻辑，这样显然会复杂很多。

numerizer是一款一行命令就可以实现自然语言数字到int和float的转化。

**安装使用**

可以通过pip命令安装，

```
pip install numerizer
```

也可以通过github源码安装，

```
git clone https://github.com/jaidevd/numerizer.gitcd numerizerpip install -e .
```

可以通过以下简单示例，了解numerizer的使用，

```python
>>> from numerizer import numerize
>>> numerize('forty two')'42'>>> numerize('forty-two')'42'
>>> numerize('four hundred and sixty two')'462'
>>> numerize('one fifty')'150'
>>> numerize('twelve hundred')'1200'
>>> numerize('twenty one thousand four hundred and seventy three')'21473'
>>> numerize('one million two hundred and fifty thousand and seven')'1250007'
>>> numerize('one billion and one')'1000000001'
>>> numerize('nine and three quarters')'9.75'
>>> numerize('platform nine and three quarters')'platform 9.75'
```

## sentry-python

**Star：665**

**sentry-python**[6]是Sentry的开源Python SDK。

那么问题就来到，”Sentry是什么？“

在一个完善的系统中，算法、开发只占据很小的一部分。我认为，负责过正式商业化项目的同学都应该清楚日志的重要性丝毫不亚于那些看似高大上的机器学习算法。系统出现了报警和异常，日志可以协助我们快速定位并修复问题。

Sentry就是一个代码实时事件日志记录和聚合平台，可以用于监控代码的报错及后续调试时所需的所有信息。

而通过sentry-python，我们可以很轻松的在Python中调用Sentry的SDK，

```python
from sentry_sdk import init, capture_message
init("https://mydsn@sentry.io/123")
capture_message("Hello World")  # Will create an event.
raise ValueError()  # Will also create an event.
```

------

#### 推荐阅读

- [干货 | 2019年共享免费资源整理(上)：学习资源篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484955&idx=1&sn=fa9827493c135096729fac6cd8b54fb2&chksm=e94e9913de391005dc83393528bef4530875108a2fc5fbe0e9de0da87a96a4b146621288f7f8&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [干货 | 2019年共享免费资源整理(下)：实用工具篇](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247484959&idx=1&sn=628c532c9504cbdb17bcd75fee354292&chksm=e94e9917de391001c367b78cedc19276a398c8675e9c9b5c590d02e90efdd1fc5f2e3e816db9&token=2025215714&lang=zh_CN&scene=21#wechat_redirect)
- [10款VS Code插件神器，第7款超级实用！](https://mp.weixin.qq.com/s?__biz=MzI0NTM1MzA2Mw==&mid=2247485027&idx=1&sn=be4c1275f350c9bc1ddd43b793088647&chksm=e94e996bde39107d6076a95ddcfd9c4bb5cd212363cd0138f6a8906a724da956878b012af6cc&token=1472831505&lang=zh_CN&scene=21#wechat_redirect)

---

我整理了10T+资源进行共享，其中包括**实用工具、Python电子书、Spring视频教程、机器学习资源**，扫码关注我的公众号“**平凡而诗意**”，后台回复相应关键字即可获得。除此之外，原创技术文章会第一时间推送，如果喜欢，麻烦点一下“在看”~

![null](https://mmbiz.qpic.cn/mmbiz_png/sbzaBxCErLia8veH7q6GuuWF9cpXicz2cFQkiapXU45jrESahRZFJNQbicXE3XUxlYRyNatmvLotvXb5Mgh7cEWOqw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

#### 引用链接

`[1]` **PyHubWeekly**: *https://github.com/Jackpopc/PyHubWeekly*
`[2]` **vardbg**: *https://github.com/CCExtractor/vardbg*
`[3]` **yfinance**: *https://github.com/ranaroussi/yfinance*
`[4]` **Keylogger**: *https://github.com/GiacomoLaw/Keylogger*
`[5]` **numerizer**: *https://github.com/jaidevd/numerizer*
`[6]` **sentry-python**: *https://github.com/getsentry/sentry-python*