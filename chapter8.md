# 常见问题

在运行`gitbook build`跟`gitbook serve`时经常会遇到缺失文件的错误信息，例如：

```shell
Error: ENOENT: no such file or directory, stat 'C:\Projects\myproject_book\gitbook\gitbook-plugin-fontsettings\buttons.js'

Error: ENOENT: no such file or directory, stat 'C:\Projects\myproject_book\gitbook\gitbook-plugin-lunr\lunr.min.js'

Error: ENOENT: no such file or directory, stat 'C:\Projects\myproject_book\gitbook\gitbook-plugin-livereload\plugin.js'
```

## 解决方案

在book目录下，如下代码修改book.json：

```json
{
    "plugins": [
            "fontsettings",
            "sharing",
            "lunr",
            "search",
            "highlight",
            "livereload"
    ]
}
```
保存文件后，运行`gitbook install`安装插件依赖

重新执行`gitbook build`或`gitbook serve`