## 前言

PyHubWeekly每周定期更新，精选GitHub上优质的Python项目/小工具。

我把PyHubWeekly托管到了Github，感兴趣的可以**搜索Github项目**[PyHubWeekly](Jackpopc/PyHubWeekly)，如果喜欢，麻烦给个Star支持一下吧。此外，**欢迎大家通过提交issue来投稿和推荐自己的项目**~

本期为大家推荐GitHub上5个优质的Python项目，它们分别是：

- **pyinspect**
- **jazzit**
- **mach-nix**
- **Papis**

下面分别来介绍一下上述5个GitHub项目。

### pyinspect

![img](https://mmbiz.qpic.cn/mmbiz_gif/DGwXCh99GDDlDQOyvDHzSObrS4BeIeqIiaT1gMAhSjzIp41DpyfY6EATYGw3BYBPkKwMW1ZBFs3NUiaNJQqGyIjw/640?wx_fmt=gif)

在大一些的项目开发过程中，会写很多实现不同功能的函数，久而久之，很多函数的名称都记不太清。

pyinspect[1]可以给你提供强有力的帮助！

你不仅可以在Python代码中像调用函数一样使用它，也可以在命令行下像命令行工具那样使用pyinspect。

pyinspect允许根据函数和类方法的名称搜索它们，并打印出一个清晰的列表，其中包含满足搜索条件的所有函数。你还可以使用pyinspect在终端中直接打印函数的代码，这样就可以在不打开任何文件的情况下提示它所做的工作。

### jazzit

如果你的代码在支撑过程中报错了，你该怎么能够感知到这个错误？

当我们执行一个运行时间较长的工程时，不可能一直盯着屏幕，直到它运行完成。

但是，如果这期间它出现了错误，我们却没有感知，这样势必会浪费掉大量时间。

jazzit[2]可以你的代码再运行/出错时播放对应的声音，以此来给你对应的提醒。

**安装**

```
$ pip install jazzit
```

**示例**

```Python
from jazzit import error_track

@error_track("curb_your_enthusiasm.mp3", wait=7)
def run():
    for num in reversed(range(10)):
        print(10/num)

if __name__ == "__main__":
    run()
```

这样，你就可以对你的代码运行情况有更加直观的感知！

### mach-nix

![img](https://mmbiz.qpic.cn/mmbiz_jpg/DGwXCh99GDDlDQOyvDHzSObrS4BeIeqI8Vm5KIeGiaNcq1KjsTcAxPE52Jv8GSEZwNMUq84G8vZ6ss7QqOd8GJA/640?wx_fmt=jpeg)

目前Python包/环境管理工具可以说是有非常多的选择，`pip`、`pipenv`、`conda`等。

但是，现有的Python软件包管理工具都无法实现可复用性，而且需要额外的虚拟化层。

而mach-nix旨在通过提供一种简单的使用Nix的方式来解决这些问题。

Nix是一款操作系统包管理工具，和RPM、APT一样。

通过与Nix的结合，mach-nix使得创建和共享Python环境变得更加容易，大大提升了它的可复用性和可移植性。

**安装**

可以通过pip进行安装：

```
$ pip install git+git://github.com/DavHau/mach-nix@3.0.1
```

也可以通过nix进行安装：

```
$ nix-env -if https://github.com/DavHau/mach-nix/tarball/3.0.1 -A mach-nix
```

下面，来看一下用mach-nix通过requirements.txt创建Python环境的示例：

```
$ mach-nix env ./env -r requirements.txt
```

### Papis

![img](https://mmbiz.qpic.cn/mmbiz_png/DGwXCh99GDDlDQOyvDHzSObrS4BeIeqIV2Aq5bibOo7hOQhH8XobTyFAYeAYTicRHz4nD6sz9SAX9qweR5obAvIg/640?wx_fmt=png)

Papis是一个功能强大且高度可扩展的基于命令行的文档和书目管理工具。

它可以从Dropbox、rsync、OwnCloud、GoogleDrive等主流网盘进行文档同步。也支持与其他同事进行共享文档，便于团队协作。

Papis还支持文档导出，可以导出bibtex、yaml等格式。

在兼容方面，Papis做的也很好。它可以使用`papis-zotero`和Zotero这款强大且开源的文献管理工具进行结合使用。

**示例**

首先，安装papis：

```shell
$ pip install papis
```

其次，下载2份示例PDF文档：

```
$ wget http://www.gnu.org/s/libc/manual/pdf/libc.pdf
$ wget http://www.ams.org/notices/201304/rnoti-p434.pdf
```

然后，把这2份文档加入到库中，方便管理：

```shell
$ papis add libc.pdf --set author "Sandra Loosemore" --set title "GNU C reference manual" --set year 2018 --set tags programming --confirm
# Get paper information automatically via de DOI
$ papis add --from doi 10.1090/noti963 --set tags programming rnoti-p434.pdf
```

最后，可以通过papis进行编辑和导出：

```shell
$ papis open
$ papis edit
$ apis export --all --bibtex > mylib.bib
```