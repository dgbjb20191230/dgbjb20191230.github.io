---
title: 【Hexo博客搭建】将其部署到GitHub Pages（三）：怎么写作以及更新？
date: 2023-12-23 12:59:46
tags:
---

> **简介：** 本系列文章属于半笔记半教程的零基础小白入门文，教你将 [Hexo](https://so.csdn.net/so/search?q=Hexo&spm=1001.2101.3001.7020) 部署到 GitHub Pages 应该怎么做，跟着此系列文章最终可以获得自己的静态博客网站。流程很长，分成不同的篇幅，此为本系列的第三篇。

## 前言

 本系列文章属于半笔记半教程的零基础小白入门文，教你将 Hexo 部署到了 GitHub Pages，从而获得自己的静态博客网站。流程很长，分成不同的篇幅，此为本系列的第三篇。

## 步骤

### 十一、开始写作

在上一篇文章中提到，初始化hexo博客后我们获得了它自动为我们生成的博客页面，同时还给我们生成了一个标题为“Hello World”的帖子。那么我们以后如何写新帖子发布到我们的博客网站呢？

打开“[命令提示符](https://so.csdn.net/so/search?q=%E5%91%BD%E4%BB%A4%E6%8F%90%E7%A4%BA%E7%AC%A6&spm=1001.2101.3001.7020)窗口”进行操作，即之前用到的cmd窗口。

> Windows用户打开方式是按住Win+R，再输入cmd然后回车即可。

打开后我的电脑是显示如下的：

```
Microsoft Windows [版本 10.0.19042.1165]
(c) Microsoft Corporation。保留所有权利。
C:\Users\86166&gt;
<div class="hljs-button {2}" data-title="复制"></div>
```

和第二篇文章第六步的操作相同，

由于窗口默认是在C盘操作，我们需要进入到本地电脑之前存储网站代码的“文件夹目录”，对于我来说，由于我存储网站代码的`blog`文件夹是放在 E盘 的 `Hexo` 文件夹里的，所以我需要先进入 E盘 ，然后回车，显示如下：

```
Microsoft Windows [版本 10.0.19042.1165]
(c) Microsoft Corporation。保留所有权利。
C:\Users\86166&gt;e:
E:\&gt;
<div class="hljs-button {2}" data-title="复制"></div>
```

再通过cd命令进入 Hexo\\blog” 文件夹：

（这一步请根据你自己之前存放的地址，不要照抄我的哈）

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">Microsoft Windows [版本 10.0.19042.1165]
(c) Microsoft Corporation。保留所有权利。
C:\Users\86166&gt;e:
E:\&gt;cd Hexo\blog
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li></ul>
```

（题外话：我通过上面这行命令亲自实践发现，虽然我的文件夹的命名同时包含大小写，但我全输入小写也是可以进入的）

好了，现在可以开始通过命令开始第一次写作了。

#### 1.创建新帖子

输入以下命令，并回车：

（注意双引号是英文输入法下的！双引号内文字即为你要新建的文章帖子的标题）

```
hexo new "我的第一篇博客文章"
<div class="hljs-button {2}" data-title="复制"></div>
```

（或缩写成：hexo n “我的第一篇博客文章”）

回车后不一会儿，它提示我 blog\\source\_posts\\我的第一篇博客文章.md 文件已经建好了。你会发现该文件后缀名是“.md”，没错，hexo默认我们用Markdown 格式书写文章。

> Hexo 支持以任何格式书写文章，只要安装了相应的渲染插件。
>
> 例如，Hexo 默认安装了 hexo-renderer-marked 和 hexo-renderer-ejs，因此你不仅可以用 Markdown 写作，你还可以用 EJS 写作。如果你安装了 hexo-renderer-pug，你甚至可以用 Pug 模板语言书写文章。
>
> 只需要将文章的扩展名从 md 改成 ejs，Hexo 就会使用 hexo-renderer-ejs 渲染这个文件，其他格式同理。

现在，我之前让大家下载的VSCode编辑器这时候就派上用场了，当然，如果你对Markdown非常熟悉也有自己用的顺手的编辑器的话，当然可以根据你自己的习惯使用别的编辑器进行写作，但本文章仅使用VSCode进行演示。

#### 2.编写文章内容

双击打开VSCode，

点击左上角“文件”，点击“选择文件”，

找到刚刚新建的“我的第一篇博客文章.md ” 并打开，

现在可以开始你的创作之旅了。

> 如果不会用Markdown语法书写文章的话可以在其他地方学习一下，
>
> 或进入官网进行学习：
>
> [Markdown 官方中文文档](https://markdown.com.cn/)

这里插个话：理论上，vscode 在没有安装任何插件的情况下是可以直接编写markdown文档的，书写过程中点击vscode右上角的其中一个小按钮可以在右侧实时预览效果。

但是为了能够得到一些更加丰富的功能和有好多体验，可以通过增添新的插件对其功能进行完善。

> 比如 Markdown Preview Enhanced 就是一个很好用的完善预览功能的插件，可以更加形象的展示所编写的pdf格式的文档样式。在插件库中搜索markdown即可找到该插件，然后点击安装后重新加载。

写完后Ctrl+S保存你的文章（或点击vscode左上角“文件”，然后“保存”），关闭vscode。

### 十二、更新main分支

#### 1.清除缓存（可跳过）

```
hexo clean
<div class="hljs-button {2}" data-title="复制"></div>
```

此命令用于清除缓存文件 (db.json) 和已生成的静态文件 (public)。

在某些情况（尤其是更换主题后），如果发现你对站点的更改无论如何也不生效，可能需要运行该命令。如果进行了多次生成，为了避免受错误缓存影响，最好使用 hexo clean 先清除一遍。也就是说，网站显示异常时可以执行这条命令试试。

#### 2.生成静态文件

输入以下命令，并回车：

```
hexo generate
<div class="hljs-button {2}" data-title="复制"></div>
```

（或缩写成：`hexo g` ）

此命令使刚刚完成写作的文章生成网站静态文件到默认设置的 public 文件夹。

#### 3.启动本地服务器（可跳过）

此步骤用于发布前的本地预览

```
hexo server
<div class="hljs-button {2}" data-title="复制"></div>
```

（或缩写成：`hexo s` ）

默认情况下，访问网址为： http://localhost:4000/

浏览器输入该网址就能看本地生成的博客了，但也仅仅在本地，GitHub上没有。

在cmd窗口按 Ctrl+C 中断服务器的运行，

系统提示 终止批处理操作吗(Y/N)? 输入 Y 然后回车。

#### 4.一键部署

输入以下命令，并回车：

```
hexo deploy
<div class="hljs-button {2}" data-title="复制"></div>
```

（或缩写成：`hexo d` ）

此命令使刚刚完成写作的文章自动生成网站静态文件，并部署到设定的仓库。

Hexo 提供了快速方便的一键部署功能，只需一条命令就能将网站部署到服务器上。在开始之前，必须先在 \_config.yml 中修改参数，一个正确的部署配置中至少要有 type 参数。在我这个系列文章的第二篇第九步，我已经带大家修改过了，跟我一路走下来的朋友们不用管了，还没设置过 \_config.yml 参数的新来的朋友麻烦去看一下本系列我的上篇文章哈。

只需等待一会，就可以打开你的博客地址看到新文章发布成功啦，

比如我的博客地址为：[XiaoYang の Blog](https://aizhiqian.github.io)

> 这一切是如何发生的？
>
> 当执行 hexo deploy 时，Hexo 会将 public 目录中的文件和目录推送至 \_config.yml 中指定的远端仓库和分支中，并且完全覆盖该分支下的已有内容。

### 十三、更新备份hexo分支

根据我上一篇文章中对 \_config.yml 文件参数的修改，上边这个部署的命令默认是对我GitHub上的主分支（也可以叫main或者master分支）进行部署更新，上篇文章说过了，我同时管理了两个分支，分别存放不同内容：

> main -负责展示静态网页
>
> hexo -备份本地hexo文件

分别运行下面三行命令，进行hexo分支更新（后面括号内为注释，无需输入）

```
git add . （此命令用来添加所有文件到暂存区）
git commit -m "新增博客文章"  （此命令用来提交，双引号内可自定义内容，双引号前有空格）
git push origin hexo （此命令用来推送hexo分支到Github）
<div class="hljs-button {2}" data-title="复制"></div>
```

第一行命令其实有三种写法：（注意第三种写法后面有个点）

> git add -A
>
> 提交所有变化（就是git add --all的缩写）
>
> git add -u
>
> 提交被修改 (modified) 和被删除 (deleted) 的文件，不包括新文件 (new)
>
> git add .
>
> 提交新文件 (new) 和被修改 (modified) 文件，不包括被删除 (deleted) 文件

> git add . ：他会监控工作区的状态树，使用它会把工作时的所有变化提交到暂存区，包括文件内容修改(modified)以及新文件(new)，但不包括被删除的文件。
>
> git add -u ：他仅监控已经被add的文件（即tracked file），他会将被修改的文件提交到暂存区。add -u 不会提交新文件（untracked file）。（git add --update的缩写）
>
> git add -A ：是上面两个功能的合集（git add --all的缩写）

第二行的“-m”应该是“message”的缩写，双引号内是自定义提交信息

> 在上一篇文章中我们对 \_config.yml 的message参数设置的就是这个，你可以自定义此次部署更新的说明，比如：“x年x月x日的备份”、“第x次备份”等等都可以

从而推送到 GitHub 仓库进行了备份。

## 总结

每次更新博客时都可以走以下三个大步

#### 一、写作部分

1、打开cmd进入存放博客代码文件夹

2、创建文章：

```
hexo n "文章标题"
<div class="hljs-button {2}" data-title="复制"></div>
```

3、使用vscode打开新建的.md文件编写内容

#### 二、对main分支进行部署更新：

```
hexo clean （清理缓存，可选用）
hexo g （生成资源文件）
hexo d （部署到服务器）
<div class="hljs-button {2}" data-title="复制"></div>
```

#### 三、对hexo分支进行部署更新：

```
git add . （添加所有文件到暂存区）
git commit -m "自定义信息" （提交此次更新的信息）
git push origin hexo （推送hexo分支到Github）
<div class="hljs-button {2}" data-title="复制"></div>
```

#### 四、打开你的博客网址查看显示效果

___

好了，这就是本篇文章：

> [【Hexo博客搭建】将其部署到 GitHub Pages（三）：怎么写作以及更新？](https://blog.csdn.net/y3332664073/article/details/130846008)

的全部内容了，更多内容会很快写出来，尽情期待。
