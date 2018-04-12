# 使用

gitbook的用法非常简单，基本只需要使用三个命令：

- 1.`gitbook init`——初始化目录
- 2.`gitbook build`——编译书籍
- 3.`gitbook serve`——编译并预览书籍

下面会结合一个例子来简单介绍下gitbook的基本用法。

## gitbook init

首先，在一个空目录下面打开终端命令窗口输入：

```bash
$ gitbook init
```

你会发现目录下面会生成`README.md`和`SUMMARY.md`文件

- `README.md`是对书籍的简单介绍
- `SUMMARY.md`是书籍的目录结构

编辑SUMMARY.md文件，格式如下：

```md
# Summary

* [Introduction](README.md)
* [Chapter1](chapter1/README.md)
  * [Section1.1](chapter1/section1.1.md)
  * [Section1.2](chapter1/section1.2.md)
* [Chapter2](chapter2/README.md)
* [Chapter3](chapter3/README.md)
```

然后再执行：

```bash
$ gitbook init
```
你会发现目录下面会根据你编辑的`SUMMARY.md`里面的书籍目录生成对应的文件夹及文件

## gitbook serve

书籍目录结构创建完成后，你就可以根据目录对应的文件来编辑你的文章章节了，尝试着在每个文件中写点什么，记得要按照markdown语法规则。

写完之后，可以在本地预览一下：

```bash
$ gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...
...
Starting server ...
Serving book on http://localhost:4000
```
现在，可以用浏览器打开 [http://127.0.0.1:4000](http://127.0.0.1:4000) 查看书籍的最终效果

> gitbook serve 命令实际上会首先调用 gitbook build 编译书籍，完成以后会打开一个 web 服务器，监听在本地的 4000 端口

## gitbook build

此命令主要为编译书籍，会在你的跟目录下生成`_book`文件夹及相对应的html文件，下一章节会讲述该如何使用该目录下的文件