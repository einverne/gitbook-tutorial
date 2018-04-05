# 发布到Github Pages

## 将静态网站直接发布到Github Pages

可以将编写好的.md文件通过Gitbook处理成静态网站，然后发布到[Github Pages](https://pages.github.com/)上。

将md文件与Github Pages静态文件存放在一个仓库中。md文件为master分支，而html文件为 `gh-pages`分支。

下面将介绍使用一个仓库托管源码，而使用 Travis 自动将静态网站发布到 `gh-pages` 分支中。这样就可以避免提交源码的同时，还需要同步一遍 `gh-pages` 分支。

[domenic](https://gist.github.com/domenic/ec8b0fc8ab45f39403dd) 制作了一个脚本，当 master 分支更新时，自动使用 CI Travis 拉取更新，然后和 `gh-pages` 分支做比较，如果有差异了，自动将 master 分支的修改提交到 `gh-pages` 分支。

## 使用项目的Pages服务

除了上面的直接发布静态文件到Github Pages的方法以外，还可以使用一个单独的项目的Github Pages功能。

### 创建仓库与分支

1. 登陆到Github，创建一个新的仓库，名称我们就命名为`gitbook-tutorial`，这样我就得到一个`gitbook-tutorial`仓库。
2. 克隆仓库到本地： `git clone git@github.com:/USER_NAME/gitbook-tutorial.git`
3. 创建一个新分支： `git checkout -b gh-pages`，注意，分支名必须为`gh-pages`。
4. 将分支push到仓库： `git push -u origin gh-pages`。
5. 切换到主分支：`git checkout master`。

经过这一步处理，我们已经创建了`gh-pages`分支了，有了这个分支，Github会自动为你分配一个网址。

> http://USERNAME.github.io/gitbook-tutorial

你可以在项目页面右下角```setting```中看到：

![Github Pages](../imgs/gh-pages-setting.png)

