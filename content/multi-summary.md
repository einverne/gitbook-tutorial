# 目录初始化

当`SUMMARY.md`创建完毕之后，我们可以使用Gitbook的命令行工具将这个目目录结构生成相应地目录及文件

我们可以看到，gitbook给我们生成了与`SUMMARY.md`所对应的目录及文件。

每个目录中，都有一个`README.md`文件，用于描述这一章的说明。

## 多级目录

Gitbook 使用 `SUMMARY.md` 文件来实现目录结构，通过该文件可以实现多级目录效果，如：

```markdown
* [第一章](section1/README.md)
    * [第一节](section1/example1.md)
    * [第二节](section1/example2.md)
* [第二章](section2/README.md)
    * [第一节](section2/example1.md)
```

md 文件可以存放在子文件夹中，另外需要注意的是 Gitbook 目录结构限定为三级。

用户还可以通过标题或者**水平分割线**将 Gitbook 目录分为不同的部分，比如

```markdown
# Summary

### 第一部

* [Introduction](README.md)
* [Writing is nice](part1/writing.md)
* [GitBook is nice](part1/gitbook.md)

### 第二部

* [We love feedback](part2/feedback_please.md)
* [Better tools for authors](part2/better_tools.md)

----

* [Last part without title](part3/title.md)
```


## 锚点标记

目录结构中也可以直接指向文件中的锚点标记，让目录结构更加清晰

```markdown
# Summary

### Part I

* [Part I](part1/README.md)
    * [Writing is nice](part1/README.md#writing)
    * [GitBook is nice](part1/README.md#gitbook)
* [Part II](part2/README.md)
    * [We love feedback](part2/README.md#feedback)
    * [Better tools for authors](part2/README.md#tools)

```

