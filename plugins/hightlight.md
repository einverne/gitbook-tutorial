# 代码高亮

使用 Prism.js 为语法添加高亮显示，需要将 highlight 插件去掉。

地址： <https://plugins.gitbook.com/plugin/prism> <https://plugins.gitbook.com/plugin/prism-themes>

```json
{
    "plugins": [
        "prism",
        "-highlight"
    ],
    "pluginsConfig": {
        "prism": {
            "css": [
                "prism-themes/themes/prism-base16-ateliersulphurpool.light.css"
            ]
        }
    }
}
```

如果需要修改背景色、字体大小等，可以在 website.css 定义 pre[class*="language-"] 类来修改，下面是一个示例：

```css
pre[class*="language-"] {
    border: none;
    background-color: #f7f7f7;
    font-size: 1em;
    line-height: 1.2em;
}
```