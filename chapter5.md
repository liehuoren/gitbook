# 个性化配置

除了编辑文章之外，我们还可以通过配置`book.json`文件来修改gitbook在编译书籍时的一些个性化配置。

gitbook 在编译书籍的时候会读取书籍源码顶层目录中的 `book.js` 或者 `book.json`，这里以 book.json 为例，参考 gitbook 文档 可以知道，book.json 支持如下配置：

```json
{
    // Folders to use for output
    // Caution: it overrides the value from the command line
    // It's not advised this option in the book.json
    "output": null,

    // Generator to use for building
    // Caution: it overrides the value from the command line
    // It's not advised this option in the book.json
    "generator": "site",

    // Book metadats (somes are extracted from the README by default)
    "title": null,
    "description": null,
    "isbn": null,
    "language": "en",
    // For ebook format, the extension to use for generation (default is detected from output extension)
    // "epub", "pdf", "mobi"
    // Caution: it overrides the value from the command line
    // It's not advised this option in the book.json
    "extension": null,

    // Plugins list, can contain "-name" for removing default plugins
    "plugins": [],

    // Global configuration for plugins
    "pluginsConfig": {
        "fontSettings": {
            "theme": "sepia", "night" or "white",
            "family": "serif" or "sans",
            "size": 1 to 4
        }
    },

    // Variables for templating
    "variables": {},

    // Links in template (null: default, false: remove, string: new value)
    "links": {
        // Custom links at top of sidebar
        "sidebar": {
            "Custom link name": "https://customlink.com"
        },

        // Sharing links
        "sharing": {
            "google": null,
            "facebook": null,
            "twitter": null,
            "weibo": null,
            "all": null
        }
    },


    // Options for PDF generation
    "pdf": {
        // Add page numbers to the bottom of every page
        "pageNumbers": false,

        // Font size for the fiel content
        "fontSize": 12,

        // Paper size for the pdf
        // Choices are [u’a0’, u’a1’, u’a2’, u’a3’, u’a4’, u’a5’, u’a6’, u’b0’, u’b1’, u’b2’, u’b3’, u’b4’, u’b5’, u’b6’, u’legal’, u’letter’]
        "paperSize": "a4",

        // Margin (in pts)
        // Note: 72 pts equals 1 inch
        "margin": {
            "right": 62,
            "left": 62,
            "top": 36,
            "bottom": 36
        },

        //Header HTML template. Available variables: _PAGENUM_, _TITLE_, _AUTHOR_ and _SECTION_.
        "headerTemplate": null,

        //Footer HTML template. Available variables: _PAGENUM_, _TITLE_, _AUTHOR_ and _SECTION_.
        "footerTemplate": null
    }
}
```

首先，在根目录下新建一个`book.json`文件，然后自定义你需要的配置，记得去除注释跟空行，来保证book.json是合法的配置项，否则将会无效。

现在，修改一些配置，将其修改为你的内容，例如：
```json
{
  "title": "GitBook", // 书籍名
  "description": "This is a sample book created by gitbook", // 书籍描述
  "generator": "site",
  "language": "zh-hans", // 语言
  "links": {
    "sidebar": {
       "zhl的博客": "https://blog.zhlzzz.com" // 侧边栏自定义地址
    }
  },
  "plugins": [
     "fontsettings",
    "sharing",
    "lunr",
    "search",
    "-highlight",
    "prism",
    "livereload",
    "baidu",
    "multipart"
  ], // 插件
  "pluginsConfig": {
    "fontSettings": {
        "theme": "sepia", "night" or "white",
        "family": "serif" or "sans",
        "size": 1 to 4
    }
  }, // 插件配置
}
```
你可以粘贴你的 book.json 去 [jsonlint.com](jsonlint.com) 验证JSON语法。

现在重新编译下，看看发生了哪些变化，如果你添加了插件，那么请继续看下一部分的详解。