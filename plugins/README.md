# 常用的插件
可以通过 Gitbook 的插件来扩展 Gitbook 的功能，现有的 Gitbook 插件能够实现数学公式，Google 统计，评论等等功能。

所有的插件都可以从 <https://plugins.gitbook.com/> 获取。

## 安装插件
Gitbook 安装插件比较简单，需要在项目下添加 `book.json` 文件，然后在其中添加


```json
{
    "plugins": ["plugins1", "plugins2"],
    "pluginsConfig": {
        "plugins1": {}
    }
}
```

注册完插件之后，可以通过下面的命令来安装插件

    gitbook install
    
## 常用的插件

### 修改页面样式

- [editlink](https://plugins.gitbook.com/plugin/editlink) 顶部显示编辑此页
- [image captions](https://plugins.gitbook.com/plugin/image-captions) 抓取图片中 `alt` 或者 `title` 属性显示在图片下
- [anchors](https://plugins.gitbook.com/plugin/styles-sass) 标题带有锚点
- [splitter](https://plugins.gitbook.com/plugin/splitter) 侧边栏可以调解宽度
- [localized-footer](https://github.com/noerw/gitbook-plugin-localized-footer#readme) 为 Gitbook 每一个页面添加页脚
- Expandable-chapters-small  使左侧的章节目录可以折叠

### 功能增强

- [disqus](https://plugins.gitbook.com/plugin/disqus) Disqus 评论插件
- Search Plus 增强搜索，支持中文
- Sharing Plus 分享增强
- KaTex 支持数学公式
- Chart 绘制图形
- rss 添加 rss 订阅功能
- Edit Link 链接到当前页源文件上
- Donate 打赏插件
- Github Buttons - 添加项目在 Github 上的 star、fork、watch 信息
- Advanced Emoji - 支持 emoji 表情
- Favicon - 更改网站的 favicon.ico
- Sitemap-general - 生成sitemap


### 统计

- ga Google统计
- 3ba 百度统计