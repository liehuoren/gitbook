# 插件扩展

Gitbook 本身功能丰富，但同时可以使用插件来进行个性化定制。[Gitbook 插件](https://plugins.gitbook.com/) 里已经有700多个插件，可以在 book.json 文件的 plugins 和 pluginsConfig 字段添加插件及相关配置。

你也可以从[NPM](https://www.npmjs.com/)上搜索gitbook插件，gitbook推荐插件的命名方式为：

- gitbook-plugin-theme-X: 主题
- gitbook-plugin-X: 插件

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
配置完插件后要记安装：
```bash
$ gitbook install ./
```
