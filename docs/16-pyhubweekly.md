## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[**PyHubWeekly**](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **riskquant**
- **pydata-book**
- **avatarify**
- **pyprotect**
- **prophet**

下面分别来介绍一下上述5个GitHub项目。

## riskquant

**Star：457**

[**riskquant**](https://github.com/Netflix-Skunkworks/riskquant)是一款Python量化风险库。

riskquant内置了多个知名的数据分析算法，例如`simpleloss`、`pertloss`，可以很简单的在Python中实现量化风险分析。

**安装**

克隆下源代码，进入根目录，执行下方命令，

```python
pip install .
```

**示例**

```python
>> from riskquant import pertloss
>> p = pertloss.PERTLoss(low_loss=10, high_loss=100, min_freq=0.1, max_freq=0.7, most_likely_freq=0.3, kurtosis=1)
>> simulate_100 = p.simulate_years(100)
>> p.summarize_loss(simulate_100)

{'minimum': 0,
 'tenth_percentile': 0,
 'mode': 0,
 'median': 1,
 'ninetieth_percentile': 2,
 'maximum': 6}
```

## pydata-book

**Star：12.1k**


![](https://imgkr.cn-bj.ufileos.com/f3dc992b-3e52-4cb8-b998-aa6447ab4d94.png)


[**pydata-book**](https://github.com/wesm/pydata-book)是Wes McKinney(pandas的创作者)和O'Reilly Media编著的《Python for Data Analysis》书籍的学习资料和IPython Notebook源代码。

这份学习资料不仅包含数据分析、机器学习里常用的工具，例如，numpy和pandas。也包含数据分析中常用的技术和手段，例如，

- 数据清洗和处理
- 时间序列
- 缺失数据处理
- ......

此外，pydata-book还包含数据分析实例，在实践中对数据分析的知识、工具使用有更加深入的认识。

## avatarify

**Star：5.6k**

[**avatarify**](https://github.com/alievk/avatarify)是一款应用来自NIPS的中心模型，能够为 Zoom、Skype 这类视频通话运用添加自己的替身Python工具。


![](https://imgkr.cn-bj.ufileos.com/fda5106c-c226-4c06-8763-288c2c96cf72.gif)

**使用教程**

- 安装miniconda和git
- 克隆代码，执行安装命令

```shell
git clone https://github.com/alievk/avatarify.git
cd avatarify
scripts\install_windows.bat
```
- 下载训练的权重，放置到目录下
- 安装媒体播放器，例如，OBS

avatarify项目提供了完整的训练、安装、配置过程，涉及的知识体系、架构较为完善。因此，通过学习该项目，可以对一款完整应用的开发有更加清晰的认识。

## pyprotect

**Star：266**

[**pyprotect**](https://github.com/ga0/pyprotect)是一个轻量级的python代码保护、加密工具。

这款工具有如下特性，

- 跨平台
- 简单易用
- 不需要额外依赖

**使用教程**

编译项目，

```python
mkdir build
cd build && cmake .. && make
```

加密项目，

```Python
python encrypt.py -s SCRIPTS_DIR -e ENTRY_POINT_LIST -o OUTPUT_DIR [--exclude EXCLUDED_SCRIPT_LIST]
```

## prophet

**Star：10.7k**

[**prophet**](https://github.com/facebook/prophet)是一个用于线性或非线性增长的多个季节性的时间序列数据提供高质量预测的工具。

Prophet是一个基于加法模型预测时间序列数据的过程，其中非线性趋势与年、周、日的季节性以及假日效应相吻合。它最适用于具有强烈季节效应和几个季节的历史数据的时间序列。Prophet对丢失的数据和趋势的变化是很健壮的，并且能很好地处理异常值。

**使用教程**

可以直接使用pip命令安装，

```python
pip install fbprophet
CMDSTAN=/tmp/cmdstan-2.22.1 STAN_BACKEND=PYSTAN,CMDSTANPY pip install fbprophet
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
