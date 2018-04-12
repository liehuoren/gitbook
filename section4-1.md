# 发布到GitHub

`GitHub Pages`就是一个可以免费托管静态网站的git项目，详细可以参考 [GitHub Pages 主页](https://pages.github.com/)。

## 创建GitHub远程仓库

首先，在GitHub上创建一个远程仓库，然后将你的书籍目录下创建一个git仓库并与之关联，然后将你的文件上传到GitHub上去，这里不作细讲，如果不熟悉git的伙伴可以先去网上了解下git的基本使用。

## 编译构建书籍

首先，用`gitbook build`来编译构建你的书籍，书籍内容会生成输出到此目录下的*_book*目录下。
```bash
$ gitbook build
...
info: >> generation finished with success in 1.4s !
```

## 创建gh-pages分支

执行如下命令来创建分支，并且删除不需要的文件：

```bash
$ git checkout --orphan gh-pages
$ git rm --cached -r .
$ git clean -df
$ rm -rf *~
```

现在，目录下应该只剩下 _book 目录了，首先，忽略一些文件：
```bash
$ echo "*~" > .gitignore
$ echo "_book" >> .gitignore
$ git add .gitignore
$ git commit -m "Ignore some files"
```
然后，加入 _book 下的内容到分支中：
```bash
$ cp -r _book/* .
$ git add .
$ git commit -m "Publish book"
```

## 上传书籍到GitHub

现在，可以将编译好的书籍内容上传到 GitHub 中 gitbook项目（此处为你自己创建项目的名称）的 gh-pages 分支了

```bash
$ git push -u origin gh-pages
```
> 第一次上传需要你输入你github的账户跟密码

现在，书籍的内容已经上传到 GitHub 上，所以通过访问 https://liehuoren.github.io/gitbook/ 就可以阅读 gitbook 这本书了！

关于GitHub Pages的一些使用及配置，我会抽时间单独去讲解这些。