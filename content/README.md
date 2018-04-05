# 图书项目结构

```README.md```和```SUMMARY.md```
是Gitbook项目必备的两个文件，也就是一本最简单的gitbook也必须含有这两个文件，它们在一本Gitbook中具有不同的用处。

## 目录结构
Gitbook 使用简单的目录结构

```markdown
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

简单的介绍下每个文件的作用

File                   | 作用描述
-----------------------|--------------------------
book.json    | 记录电子书的[配置](https://toolchain.gitbook.com/config.html) (可选)
README.md	 | 前言 或者 电子书的介绍 必须
SUMMARY.md	 | 电子书的目录 可选，参考[Pages](https://toolchain.gitbook.com/pages.html)
GLOSSARY.md  | 术语表 ，可选，参考 [Glossary](https://toolchain.gitbook.com/lexicon.html)


## 多语言

当使用多语言时，为每一种语言建立一个子目录，然后需要额外根目录建立一个文件 `LANGS.md` 

```markdown
# Languages

* [English](en/)
* [French](fr/)
* [Español](es/)
```

