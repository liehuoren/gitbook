# 发布到自己的网站

gitbook生成的是完全的静态文件，可以上传到任何的web服务器站点上。

首先，编辑完你的书籍后，编译你的书籍

```bash
$ gitbook build
```
 此命令会在你的根目录下生成`_book`文件夹，然后将次目录下的所有文件（不包括`_book`）上传到你站点指定的目录下，例如`http://book.abc.com/gitbook`目录下，这样你就可以跟你对应的url去访问你的书籍了。