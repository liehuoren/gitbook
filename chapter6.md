# 插件扩展

Gitbook 本身功能丰富，但同时可以使用插件来进行个性化定制。[Gitbook 插件](https://plugins.gitbook.com/browse) 里已经有100多个插件，可以在 book.json 文件的 plugins 和 pluginsConfig 字段添加插件及相关配置，添加后别忘了进行安装。

例如：
```json
{
  "title": "GitBook教程",
  "author": "zhl",
  "description": "使用gitbook生成的电子书，主要关于gitbook使用教程介绍",
  "generator": "site",
  "language": "zh-hans",
  "links": {
    "sidebar": {
      "zhl的博客": "https://blog.zhlzzz.com"
    }
  },
  "plugins": [
    "disqus",
    "baidu"
  ],
  "pluginsConfig": {
    "disqus": {
      "shortName": "gitbook"
    },
    "baidu": {
      "token": "f2aa21e56274fea731f801e573a3f23a"
    }
  }
}
```
然后安装：
```bash
$ gitbook install ./
```

## 常用插件

- [editlink](https://plugins.gitbook.com/plugin/editlink)
内容顶部显示 编辑本页 链接。

- [ad](https://plugins.gitbook.com/plugin/ad)
在每个页面顶部和底部添加广告或任何自定义内容。

- [splitter](https://plugins.gitbook.com/plugin/splitter)
在左侧目录和右侧内容之间添加一个可以拖拽的栏，用来调整两边的宽度。

- [image-captions](https://plugins.gitbook.com/plugin/image-captions)
抓取内容中图片的 alt 或 title 属性，在图片下面显示标题。

- [github](https://plugins.gitbook.com/plugin/github)
在右上角显示 github 仓库的图标链接。

- [anchors](https://plugins.gitbook.com/plugin/anchors)
标题带有 github 样式的锚点。

- chart(https://plugins.gitbook.com/plugin/chart)
使用 C3.js 图表。

- [styles-sass](https://plugins.gitbook.com/plugin/styles-sass)
使用 SASS 替换 CSS。

- [styles-less](https://plugins.gitbook.com/plugin/styles-less)
使用 LESS 替换 CSS。

- [ga](https://plugins.gitbook.com/plugin/ga)
添加 Google 统计代码。

- [disqus](https://plugins.gitbook.com/plugin/disqus)
添加 disqus 评论插件。

- [sitemap](https://plugins.gitbook.com/plugin/sitemap)
生成站点地图。

- [latex-codecogs](https://plugins.gitbook.com/plugin/latex-codecogs)
使用数学方程式。

- [mermaid](https://plugins.gitbook.com/plugin/mermaid)
使用流程图。

- [book-summary-scroll-position-saver](https://plugins.gitbook.com/plugin/book-summary-scroll-position-saver)
自动保存左侧目录区域导航条的位置。

- [sharing](https://plugins.gitbook.com/plugin/sharing)
默认的分享插件。

- [fontsettings](https://plugins.gitbook.com/plugin/fontsettings)
默认的字体、字号、颜色设置插件。

- [search](https://plugins.gitbook.com/plugin/search)
默认搜索插件。

- [tbfed-pagefooter](https://plugins.gitbook.com/plugin/tbfed-pagefooter)
自定义页脚，显示版权和最后修订时间。

- [prism](https://plugins.gitbook.com/plugin/prism)
基于 Prism 的代码高亮。

- [atoc](https://plugins.gitbook.com/plugin/atoc)
插入 TOC 目录。

- [ace](https://plugins.gitbook.com/plugin/ace)
插入代码高亮编辑器。

- [highlight](https://plugins.gitbook.com/plugin/highlight)
默认的代码高亮插件，通常会使用 prism 来替换。

- [github-buttons](https://plugins.gitbook.com/plugin/github-buttons)
显示 github 仓库的 star 和 fork 按钮。

- [sectionx](https://plugins.gitbook.com/plugin/sectionx)
分离各个段落，并提供一个展开收起的按钮。

- [mcqx](https://plugins.gitbook.com/plugin/mcqx)
使用选择题。

- [include-codeblock](https://plugins.gitbook.com/plugin/include-codeblock)
通过引用文件插入代码。

- [fbqx](https://plugins.gitbook.com/plugin/fbqx)
使用填空题。

- [spoiler](https://plugins.gitbook.com/plugin/spoiler)
隐藏答案，当鼠标划过时才显示。

- [anchor-navigation](https://plugins.gitbook.com/plugin/anchor-navigation)
锚点导航。

- [youtubex](https://plugins.gitbook.com/plugin/youtubex)
插入 YouTube 视频。

- [redirect](https://plugins.gitbook.com/plugin/redirect)
页面跳转。

- [expandable-chapters](https://plugins.gitbook.com/plugin/expandable-chapters)
收起或展开章节目录中的父节点。

- [baidu](https://plugins.gitbook.com/plugin/baidu)
使用百度统计。

- [jsfiddle](https://plugins.gitbook.com/plugin/jsfiddle)
插入 JSFiddle 组件。

- [jsbin](https://plugins.gitbook.com/plugin/jsbin)
插入 JSBin 组件。