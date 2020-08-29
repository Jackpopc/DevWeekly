## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[PyHubWeekly](Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **aiosql**
- **libra**
- **PyOxidizer**
- **latexify_py**
- **Ciphey**

下面分别来介绍一下上述5个GitHub项目。

### aiosql

**Star：709**

[aiosql](https://github.com/nackjicholson/aiosql)是一款让Python中执行SQL语句更加简单的一种工具包。

后端开发，避免不了和数据库的增删改查打交道。因此，在编程语言与SQL混合使用是一种非常常见的现象。无论是Java，还是Python。

在以往的方式中，都是把SQL语句作为字符串写死在核心逻辑代码中。这样虽然省事，但是，杂乱的SQL语句会大大增加代码的阅读和理解难度。

而aiosql大大简化这个问题，使得上述这个问题得到很好的解决。

**安装**

```shell
$ pip install aiosql
```

**使用**

首先，创建一个名为`users.sql`的SQL文件：

```sql
-- name: get-all-users
-- Get all user records
select userid,
       username,
       firstname,
       lastname
  from users;


-- name: get-user-by-username^
-- Get user with the given username field.
select userid,
       username,
       firstname,
       lastname
  from users
 where username = :username;
```

然后，在Python代码中引入aiosql工具包，它能够很容易解析写好的SQL代码文件，能够想执行Python函数一样去执行SQL的一些常用操作。

```python
import aiosql
import sqlite3

conn = sqlite3.connect("myapp.db")
queries = aiosql.from_path("users.sql", "sqlite3")

users = queries.get_all_users(conn)
# >>> [(1, "nackjicholson", "William", "Vaughn"), (2, "johndoe", "John", "Doe"), ...]

users = queries.get_user_by_username(conn, username="nackjicholson")
```

这种把SQL拆离出来写到文件里，通过执行Python函数去执行Python的增删改查不仅能够提升代码的可阅读性，还能够减少编码过程中的工作量。

### libra

**Star：1.7k**

[libra](https://github.com/Palashio/libra)是一款高阶的机器学习工具包，它能够让机器学习使用更加便捷、简单。

机器学习逐渐变成了”傻瓜式“，以往，网络上总是调侃机器学习、计算机视觉方面的工作人员为调参工程师。的确，反观大多数AI领域的工作人员每天的工作内容主要都是集中在准备数据、模型调优。

可是，我认为即便是这种技术程度的工作也将很快被替代。现在，很多大公司都在开发统一、易于使用的机器学习平台。使用者只需要配置数据集，就可以获得训练好的模型。

这已经够简单了，但是**libra**提供了一种更加简单的解决方案，甚至对于从来没有接触过机器学习，不理解机器学习的外行都能够很容易使用。

libra可以让你像使用搜索引擎一样去使用机器学习，你只需要输入一段自然语言，描述你想要的完成的任务，它就可以按照你的描述去选择数据集 、训练模型。

**示例**

```python
from libra import client

newClient = client('path/to/dataset') 
newClient.neural_network_query('please model the median number of households')
newClient.info()

dict_keys(['id', 'model', 'num_classes', 'plots', 'target', 'preprocesser', 
          'interpreter', 'test_data', 'losses', 'accuracy'])

newClient.svm_query('predict the proximity to the ocean')
newClient.model().keys()

dict_keys(['regression_ANN', svm'])
```



### PyOxidizer

**Star：2.5k**

[PyOxidizer](https://github.com/indygreg/PyOxidizer)是一款由Rust编写的一款强大的Python打包、分发工具。

当我们完成一项工程的开发，需要把它部署到某台服务器上，或者把这个工具分享给周围的朋友。如果把源代码传递过去显然是不合理的，因为它有很多开发环境的依赖，而且很不安全。

软件打包和分发是解决这个问题的一种方法，但是，目前Python方面打包工具很多，但是大多数使用起来都非常繁琐，不够友好。

而PyOxidizer让Python打包变得更加简单。

使用PyOxidizer依赖于Rust，因此，要使用它打包首先应该安装Rust，

```shell
$ rustc --version
rustc 1.38.0 (625451e37 2019-09-23)
```

然后，执行初始化命令，会在选择的文件创建一个配置文件，

```shell
$ pyoxidizer init-config-file pyapp
```

通过这个配置文件，就可以统一来管理Python工程的解释器、包管理工具等，使得打包任务更加完成、简单。

### latexify_py

**Star：1.2k**

[latexify_py](https://github.com/google/latexify_py)是一款能够快速把Python中函数转换为LaTeX公式的工具包。

在开发Python过程中，往往会涉及到一些公式计算。但是，编程语言的描述方式并不是很容易能够让人理解。我们比较熟悉的时从小到大接触的那些数学符号的描述方式。

而latexify_py能够快速把Python函数转换为我们容易理解的数学公式。

**示例**

```python
@latexify.with_latex
def solve(a, b, c):
  return (-b + math.sqrt(b**2 - 4*a*c)) / (2*a)

print(solve(1, 4, 3))
print(solve)
print()
solve
```

输出结果：

```python
-1.0
\operatorname{solve}(a, b, c)\triangleq \frac{-b + \sqrt{b^{2} - 4ac}}{2a}
```

![image-20200821230035928](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/image-20200821230035928.png)

只需要简单的使用装饰器，就可以把函数转换为公式。

### Ciphey

**Star：2.4k**

[Cipyey](https://github.com/Ciphey/Ciphey)是一款应用了自然语言处理和人工智能的自动化解密工具，你只需要输入加密后的文本，它能够返回你解密结果。

它具有如下特性：

- 支持20+种解密方式
- 多语言支持
- 支持加密
- 速度快

**安装**

```shell
$ python3 -m pip install ciphey --upgrade
```

**使用**

在命令行下很容易使用Ciphey，只需要执行如下命令即可：

```shell
$ ciphey -t "encrypted text here" -q
```

![3ways](https://gitee.com/sharetech_lee/blogimg/raw/master/imgs/3ways.gif)
