## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[PyHubWeekly](https://github.com/Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **txtai**
- **Orchest**
- **watchdog**
- **Gitutor**
- **DearPyGui**

下面分别来介绍一下上述5个GitHub项目。

### txtai

**Star：262**

[txtai](https://github.com/neuml/txtai)是一款基于AI在文本上建立索引的工具，能够把相似的文本关联在一起，用于内容搜索。

例如，搜索**feel good story**，它能够根据索引相似性返回**Maine man wins 25 lottery ticket**。

搜索**health**，它能够返回**US tops 5 million confirmed virus cases**。

**安装**

可以通过`pip`命令轻松安装txtai：

```
$ pip install txtai
```

**示例**

首先，需要创建Embeddings实例，它是txtai的主要入口点。Embeddings实例定义了用于标记文本部分并将其转换为嵌入向量的方法。

```
from txtai.embeddings import Embeddings
```

下面，就演示如何用Embeddings搜索相似概念：

```Python
import numpy as np

sections = ["US tops 5 million confirmed virus cases",
            "Canada's last fully intact ice shelf has suddenly collapsed, forming a Manhattan-sized iceberg",
            "Beijing mobilises invasion craft along coast as Taiwan tensions escalate",
            "The National Park Service warns against sacrificing slower friends in a bear attack",
            "Maine man wins $1M from $25 lottery ticket",
            "Make huge profits without work, earn up to $100,000 a day"]

print("%-20s %s" % ("Query", "Best Match"))
print("-" * 50)

for query in ("feel good story", "climate change", "health", "war", "wildlife", "asia", "north america", "dishonest junk"):
    # Get index of best section that best matches query
    uid = np.argmax(embeddings.similarity(query, sections))

    print("%-20s %s" % (query, sections[uid]))
```

输出结果：

```
Query                Best Match
--------------------------------------------------
feel good story      Maine man wins $1M from $25 lottery ticket
climate change       Canada's last fully intact ice shelf has suddenly collapsed, forming a Manhattan-sized iceberg
health               US tops 5 million confirmed virus cases
war                  Beijing mobilises invasion craft along coast as Taiwan tensions escalate
wildlife             The National Park Service warns against sacrificing slower friends in a bear attack
asia                 Beijing mobilises invasion craft along coast as Taiwan tensions escalate
north america        US tops 5 million confirmed virus cases
dishonest junk       Make huge profits without work, earn up to $100,000 a day
```

### Orchest

**Star：222**

[Orchest](https://github.com/orchest/orchest)是一款用于创建数据科学工作量的工具。

Orchest是一款Web数据科学工具，可在文件系统上运行。使用Orchest，你可以实现如下功能：

- 通过其可视界面构建数据科学工作流
- 自动并行运行工作流
- 在你喜欢的编辑器中开发代码
- ...

orchest的使用依赖Docker，所以，如果你想要尝试，需要首先安装和配置Docker。

```
$ git clone https://github.com/orchest/orchest.git
$ cd orchest
$ ./orchest.sh start
```

![ezgif.com-optimize](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/ezgif.com-optimize.gif)

### watchdog

**Star：4.2k**

[watchdog](https://github.com/gorakhargosh/watchdog)是一款用于监控系统事件的Python工具，它在Python代码中和命令行下都可以使用。

首先，来看一下在Python中以API方式使用系统事件监控：

```
import sys
import time
import logging
from watchdog.observers import Observer
from watchdog.events import LoggingEventHandler

if __name__ == "__main__":
    logging.basicConfig(level=logging.INFO,
                        format='%(asctime)s - %(message)s',
                        datefmt='%Y-%m-%d %H:%M:%S')
    path = sys.argv[1] if len(sys.argv) > 1else'.'
    event_handler = LoggingEventHandler()
    observer = Observer()
    observer.schedule(event_handler, path, recursive=True)
    observer.start()
    try:
        whileTrue:
            time.sleep(1)
    except KeyboardInterrupt:
        observer.stop()
    observer.join()
```

再看一下命令行下使用，下面这个示例忽略无关的文件，只监控和py和txt相关的事件：

```
watchmedo log \
    --patterns="*.py;*.txt" \
    --ignore-directories \
    --recursive \
    .
```

### Gitutor

**Star：6**

[Gitutor](https://github.com/artemisa-mx/gitutor)是一款用Python开发，让git命令更加简单的工具。

git是项目开发过程中经常会用到的一种工具，它用于代码的版本控制。

但是，对于初学者它不是特别友好，代码提交、版本回退、代码比较...

而Gitutor让你通过一行命令就可以轻松实现代码版本控制，让git的门槛进一步被拉低。

**安装**

```
$ pipx install gitutor
```

然后，使用`gt --help`命令就可以查看能够使用的命令：

- `gt init`：初始化本地和远程仓库
- `gt save`：把代码变动保存到本地和远程仓库
- `gt goback`：回退到前一个commit
- `gt compare`：对比当前状态和前一个commit
- `gt ignore`：忽略选中的文件
- `gt lesson`：阅读gitutor文档

### DearPyGui

**Star：273**

[DearPyGui](https://github.com/hoffstadt/DearPyGui)是一个易于使用且功能强大的Python GUI框架，它提供了DearImGui的包装。

它与其他Python GUI框架从根本上存在不同，在后台DearPyGui使用即时模式范式，这样能够实现更加灵活的动态界面。此外，DearPyGui不使用本机窗口小部件，而是使用计算机的GPU绘制窗口小部件，它支持如下平台：

- **Windows 10**
- **macOs**
- **Linux**

DearPyGui提供与DearImGui相同的方式为游戏开发人员提供了一种创建工具的简单方法，DearPyGui提供了一种简单的方法为Python开发人员创建快速而强大的GUI。

---

给大家推荐1个宝藏公众号【**七步编程**】，专注于Python、AI、大数据领域内容分享。创作内容坚持原创与高质量，发表内容已经被诸多公众号大V转发，备受欢迎。现在关注，后台回复关键**567**就可以获得我精心整理的机器学习、深度学习、Python、推荐系统等技术方向的干货！

![image-20200829151145405](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/image-20200829151145405.png)