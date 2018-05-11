# Gitbook命令行使用

Gitbook是一个命令行工具，使用方法：

## 初始化
初始化一本书

    gitbook init

在使用 `gitbook init` 之后本地会生成两个文件 `README.md` 和 `SUMMARY.md` ，这两个文件都是必须的，一个为介绍，一个为目录结构。

## 编辑电子书
首先，GitBook使用SUMMARY.md文件组织整个内容的目录，比如可以新建 `Faq.md` 文件，来记录常见问题，并在 SUMMARY.md 文件中添加目录。

```markdown
# Summary

* [简介](README.md)
* [常见问题](Faq.md)
```

## 本地预览
当内容书写完毕后，可以在终端中输入如下命令，实现实时预览

```bash
gitbook serve
gitbook serve ./{book_name}
```

`gitbook serve` 命令实际会先调用 `gitbook build` 编译书籍，完成后打开 web 服务器，默认监听本地 4000 端口，在浏览器打开 <http://localhost:4000> 即可浏览电子书。

## 发布电子书

```bash
gitbook build
gitbook build ./{book_name} --output=./{outputFolde}
gitbook build ./ --log=debug --debug
```

当电子书内容制作好之后，可以使用如下命令来生成 HTML 静态网页版电子书。该命令会在当前文件夹中生成 `_book` 文件夹，这个文件夹中的内容就是静态网页版电子书。

使用 `--log=debug --debug` 可以用来调试，会打印出 stack trace。

## 查看帮助

```bash
$ gitbook -h

  Usage: gitbook [options] [command]

  Commands:

    build [options] [source_dir] Build a gitbook from a directory
    serve [options] [source_dir] Build then serve a gitbook from a directory
    install [options] [source_dir] Install plugins for a book
    pdf [options] [source_dir] Build a gitbook as a PDF
    epub [options] [source_dir] Build a gitbook as a ePub book
    mobi [options] [source_dir] Build a gitbook as a Mobi book
    init [source_dir]      Create files and folders based on contents of SUMMARY.md
    publish [source_dir]   Publish content to the associated gitbook.io book
    git:remote [source_dir] [book_id] Adds a git remote to a book repository

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```
