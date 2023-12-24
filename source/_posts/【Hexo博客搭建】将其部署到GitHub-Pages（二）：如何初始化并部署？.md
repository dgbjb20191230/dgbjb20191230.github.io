---
title: 【Hexo博客搭建】将其部署到GitHub Pages（二）：如何初始化并部署？
date: 2023-12-23 12:58:21
tags:
---

> **简介：** 本系列文章属于半笔记半教程的零基础小白入门文，教你将 [Hexo](https://so.csdn.net/so/search?q=Hexo&spm=1001.2101.3001.7020) 部署到 GitHub Pages 的前期需要做哪些准备，跟着此系列文章最终可以获得自己的静态博客网站。流程很长，分成不同的篇幅，此为本系列的第二篇。

## 前言

 本系列文章属于半笔记半教程的零基础小白入门文，教你将 Hexo 部署到了 GitHub Pages，从而获得自己的静态博客网站。流程很长，分成不同的篇幅，此为本系列的第二篇。

## 步骤

### 六、初始化 Hexo 工程

注意：接下来应该是你自己的自定义的目录，请不要完全复制粘贴我的！

比如说我是Windows用户，想把我的网站代码储存在

电脑 E 盘的 _**Hexo**_ 文件夹下

那么我要先在E盘建立相应的文件夹，然后再继续操作。

由于cmd终端最开始默认在C盘操作，我得先切换到E盘，那么我要输入 _**E:**_ 然后回车,即：

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">Microsoft Windows [版本 10.0.19042.1165]
(c) Microsoft Corporation。保留所有权利。

C:\Users\10272&gt;E:

E:\&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li></ul>
```

然后此时，我要通过 _**cd**_ 进入我本地电脑打算存储网站代码的文件夹目录。（或者右键文件夹 Git Bash Here），即 _**Hexo**_ 文件夹里

也就是说我需要输入 _**cd Hexo**_ 然后回车，我会看到：

```
E:\&gt;cd Hexo

E:\Hexo&gt;
<div class="hljs-button {2}" data-title="复制"></div>
```

好了成功进入，接下来输入下方代码，再按回车：

```
hexo init blog
<div class="hljs-button {2}" data-title="复制"></div>
```

> `hexo` ：正是因为我们之前安装了 `hexo-cli` 这一个包，所以我们可以在终端中使用 `hexo` 这一命令。
>
> `init` ：用来初始化博客的模版文件。后面跟的是你要新建的文件夹比如我的是：_**blog**_

然后我会看到

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo&gt;hexo init blog
INFO  Cloning hexo-starter https://github.com/hexojs/hexo-starter.git
[32mINFO [39m Install dependencies
added 242 packages from 207 contributors in 105.871s
15 packages are looking for funding
  run `npm fund` for details
INFO  Start blogging with Hexo!
E:\Hexo&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li></ul>
```

下面通过 _**cd**_ 进入我的博客文件夹，

即输入 _cd blog_ 后按回车，我会看到：

```
E:\Hexo&gt;cd blog
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div>
```

现在我就是处于 E:\\Hexo\\blog 文件夹下操作了，

现在在这个文件夹内默认安装所有 `package.json` 文件中提到的包，

即输入 _**npm install**_ 然后回车，我会看到：

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo\blog&gt;npm install
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@2.3.2 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.2: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})
audited 243 packages in 4.956s
15 packages are looking for funding
  run `npm fund` for details
found 0 vulnerabilities
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li></ul>
```

这时候，我的 blog 文件夹里面会多出一堆文件，

文件夹结构应该大致是这样：

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">.
├── config.yml
├── package.json
├── scaffolds
├── source
|  ├── _drafts
|  └── _posts
└── themes
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li></ul>
```

现在我们输入 _**hexo server**_ 然后回车，会看到：

```
E:\Hexo\blog&gt;hexo server
INFO  Validating config
INFO  Start processing
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
<div class="hljs-button {2}" data-title="复制"></div>
```

> `server` 代表开启本地的 Hexo 服务器，这时你就可以打开浏览器，在地址栏中输入 `localhost:4000` 就可以看到本地的网页了。

![在这里插入图片描述](https://img-blog.csdnimg.cn/e6d62ce9c4b74ead873d3a95dbbe05bb.png#pic_center)

这个网页就是Hexo为你自动生成的博客页面。

按 _Ctrl+C_ 中断服务器的运行，

系统提示 _**终止批处理操作吗(Y/N)?**_ 输入 _**Y**_ 然后回车。

至此，基础的模版页面便已经搭建好了。

### 七、生成静态文件

到现在，我们的工作都是在本地进行，想必你也很想放到线上与小伙伴们分享。这便轮到了 GitHub Pages 的出场，不过 GitHub Pages 只支持纯静态文件。

所以我们需要使用下面一行命令先来生成站点的静态文件。

```
（如果进行多次生成，为了避免受错误缓存影响，最好使用 hexo clean 先清除一遍。）
hexo generate
（上方命令也可以缩写为 hexo g）
<div class="hljs-button {2}" data-title="复制"></div>
```

输入后回车，我会看到：

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo\blog&gt;hexo g
INFO  Validating config
INFO  Start processing
INFO  Files loaded in 209 ms
INFO  Generated: archives/index.html
INFO  Generated: archives/2021/index.html
INFO  Generated: archives/2021/08/index.html
(node:20772) Warning: Accessing non-existent property 'lineno' of module exports inside circular dependency
(Use `node --trace-warnings ...` to show where the warning was created)
(node:20772) Warning: Accessing non-existent property 'column' of module exports inside circular dependency
(node:20772) Warning: Accessing non-existent property 'filename' of module exports inside circular dependency
(node:20772) Warning: Accessing non-existent property 'lineno' of module exports inside circular dependency
(node:20772) Warning: Accessing non-existent property 'column' of module exports inside circular dependency
(node:20772) Warning: Accessing non-existent property 'filename' of module exports inside circular dependency
INFO  Generated: index.html
INFO  Generated: fancybox/jquery.fancybox.min.css
INFO  Generated: js/script.js
INFO  Generated: 2021/08/25/hello-world/index.html
INFO  Generated: css/style.css
INFO  Generated: css/fonts/fontawesome-webfont.woff2
INFO  Generated: css/fonts/fontawesome-webfont.woff
INFO  Generated: fancybox/jquery.fancybox.min.js
INFO  Generated: css/fonts/fontawesome-webfont.ttf
INFO  Generated: css/fonts/FontAwesome.otf
INFO  Generated: css/fonts/fontawesome-webfont.eot
INFO  Generated: js/jquery-3.4.1.min.js
INFO  Generated: css/images/banner.jpg
INFO  Generated: css/fonts/fontawesome-webfont.svg
INFO  17 files generated in 1.98 s
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><div class="hide-preCode-box"><span class="hide-preCode-bt" data-report-view="{&quot;spm&quot;:&quot;1001.2101.3001.7365&quot;}"><img class="look-more-preCode contentImg-no-view" src="https://csdnimg.cn/release/blogv2/dist/pc/img/newCodeMoreWhite.png" alt="" title=""></span></div><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li><li style="color: rgb(153, 153, 153);">12</li><li style="color: rgb(153, 153, 153);">13</li><li style="color: rgb(153, 153, 153);">14</li><li style="color: rgb(153, 153, 153);">15</li><li style="color: rgb(153, 153, 153);">16</li><li style="color: rgb(153, 153, 153);">17</li><li style="color: rgb(153, 153, 153);">18</li><li style="color: rgb(153, 153, 153);">19</li><li style="color: rgb(153, 153, 153);">20</li><li style="color: rgb(153, 153, 153);">21</li><li style="color: rgb(153, 153, 153);">22</li><li style="color: rgb(153, 153, 153);">23</li><li style="color: rgb(153, 153, 153);">24</li><li style="color: rgb(153, 153, 153);">25</li><li style="color: rgb(153, 153, 153);">26</li><li style="color: rgb(153, 153, 153);">27</li><li style="color: rgb(153, 153, 153);">28</li><li style="color: rgb(153, 153, 153);">29</li><li style="color: rgb(153, 153, 153);">30</li></ul>
```

此时我的文件夹目录下会出现 _**public**_ 这个文件夹，里面存放的就是我的站点的静态文件。

### 八、与远程仓库建立关联

接下来我们将本地的仓库与此前在 GitHub 上建立的仓库建立关联。

输入 _**git init**_ 初始化 Git 仓库，只需要执行一次即可，看到：

```
E:\Hexo\blog&gt;git init
Initialized empty Git repository in E:/Hexo/blog/.git/
<div class="hljs-button {2}" data-title="复制"></div>
```

在将其部署到 GitHub Pages 上之前，我们最好先建立一个分支。

> 什么是分支？
>
> Git 提供了版本管理功能，其中还有一个分支功能，你现在可以简单地将其理解为平行世界。

_**用户名.github.io**_ 部署后，GitHub Pages 将默认使用你的 main分支（以前叫 master分支，一个意思，主要分支的意思）作为静态文件部署。所以我们最好新建一个 hexo 分支（命名无所谓）用来存储 Hexo 地源代码，main 分支则用来存储部署后的静态文件。为了方便，不想其他名字了，这个分支我就起名叫 hexo 吧。

新建该分支的命令语句是 _**git checkout -b hexo**_ ，然后回车，可以看到：

```
E:\Hexo\blog&gt;git checkout -b hexo
Switched to a new branch 'hexo'
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div>
```

这时便成功建立了一个 hexo 分支。（此后的工作都将在 hexo 分支下进行）

你可以通过 **`git branch -v`** 来查看当前有哪些分支，使用 **`git checkout 分支名`** 来切换到对应的分支。

> [Git 学习笔记](https://www.yunyoujun.cn/note/git-learn-note/)

### 九、部署到 GitHub Pages

为了更方便的部署到 GitHub Pages，Hexo 提供了 `hexo-deployer-git` 插件。

老规矩，安装该插件，要输入下面命令，

```
npm install hexo-deployer-git --save
<div class="hljs-button {2}" data-title="复制"></div>
```

回车后可以看到

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo\blog&gt;npm install hexo-deployer-git --save
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@2.3.2 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.2: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})
+ hexo-deployer-git@3.0.0
added 1 package from 1 contributor and audited 244 packages in 8.166s
15 packages are looking for funding
  run `npm fund` for details
found 0 vulnerabilities
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li></ul>
```

下面对 _**blog**_ 文件夹下的 _**\_config.yml**_ 文件进行配置。

右键 _**\_config.yml**_ ，打开方式选VS Code（或者直接用VS Code打开该文件），

滑到最下面，把关于

```
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:' '
<div class="hljs-button {2}" data-title="复制"></div>
```

的这段代码补充为

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"># Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: git
  repo: https://github.com/aizhiqian/aizhiqian.github.io.git   #仓库地址
  branch: main  # 默认使用 master 分支(Github现在改名为main分支)
  message: Update Hexo Static Content # 你可以自定义此次部署更新的说明说明
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li></ul>
```

Ctrl+S保存，退出VS Code，部署！

终端里输入命令 _**hexo deploy**_ 后（或者缩写为 _**hexo d**_ ）回车，我的电脑显示：

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo\blog&gt;hexo deploy
INFO  Validating config
INFO  Deploying: git
INFO  Setting up Git deployment...
Initialized empty Git repository in E:/Hexo/blog/.deploy_git/.git/
Author identity unknown
*** Please tell me who you are.
Run
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
to set your account's default identity.
Omit --global to set the identity only in this repository.
fatal: unable to auto-detect email address (got '10272@DESKTOP-N3PNS7C.(none)')
FATAL {
  err: Error: Spawn failed
      at ChildProcess.&lt;anonymous&gt; (E:\Hexo\blog\node_modules\hexo-util\lib\spawn.js:51:21)      at ChildProcess.emit (events.js:400:28)
      at ChildProcess.cp.emit (E:\Hexo\blog\node_modules\cross-spawn\lib\enoent.js:34:29)
      at Process.ChildProcess._handle.onexit (internal/child_process.js:277:12) {
    code: 128
  }
} Something's wrong. Maybe you can find the solution here: %s https://hexo.io/docs/troubleshooting.html
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><div class="hide-preCode-box"><span class="hide-preCode-bt" data-report-view="{&quot;spm&quot;:&quot;1001.2101.3001.7365&quot;}"><img class="look-more-preCode contentImg-no-view" src="https://csdnimg.cn/release/blogv2/dist/pc/img/newCodeMoreWhite.png" alt="" title=""></span></div><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li><li style="color: rgb(153, 153, 153);">12</li><li style="color: rgb(153, 153, 153);">13</li><li style="color: rgb(153, 153, 153);">14</li><li style="color: rgb(153, 153, 153);">15</li><li style="color: rgb(153, 153, 153);">16</li><li style="color: rgb(153, 153, 153);">17</li><li style="color: rgb(153, 153, 153);">18</li><li style="color: rgb(153, 153, 153);">19</li><li style="color: rgb(153, 153, 153);">20</li><li style="color: rgb(153, 153, 153);">21</li><li style="color: rgb(153, 153, 153);">22</li></ul>
```

是的，部署出错（FATAL）了,“ Please tell me who you are.”

原来是创建git文件夹的时候信息不完善导致的，

它提示我需要运行（Run）下面两行程序，来设置我帐户的默认标识。

git config --global user.email “you@example.com”

git config --global user.name “Your Name”

> 注意双引号前有空格，邮箱随便填也可以，比如QQ邮箱啥的，
>
> 我用的这个邮箱查找路径是：点击Github主页右上角头像，点击settings，点击Emails，然后就能找到Github的这个邮箱了

那么我分别输入这两个命令按回车，可见下方代码：

```
E:\Hexo\blog&gt;git config --global user.email "你的邮箱"
E:\Hexo\blog&gt;git config --global user.name "用户名"
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div>
```

再用命令 \***git config -l\*** 查看所有的配置信息

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo\blog&gt;git config -l
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=E:/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=你的邮箱
user.name=用户名
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><div class="hide-preCode-box"><span class="hide-preCode-bt" data-report-view="{&quot;spm&quot;:&quot;1001.2101.3001.7365&quot;}"><img class="look-more-preCode contentImg-no-view" src="https://csdnimg.cn/release/blogv2/dist/pc/img/newCodeMoreWhite.png" alt="" title=""></span></div><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li><li style="color: rgb(153, 153, 153);">12</li><li style="color: rgb(153, 153, 153);">13</li><li style="color: rgb(153, 153, 153);">14</li><li style="color: rgb(153, 153, 153);">15</li><li style="color: rgb(153, 153, 153);">16</li><li style="color: rgb(153, 153, 153);">17</li><li style="color: rgb(153, 153, 153);">18</li><li style="color: rgb(153, 153, 153);">19</li><li style="color: rgb(153, 153, 153);">20</li><li style="color: rgb(153, 153, 153);">21</li><li style="color: rgb(153, 153, 153);">22</li><li style="color: rgb(153, 153, 153);">23</li><li style="color: rgb(153, 153, 153);">24</li></ul>
```

可以看见下面这两条信息，代表信息以及完善上去了

> user.email=你的邮箱
>
> user.name=用户名

那我们接着部署吧！

终端里输入命令 _**hexo deploy**_ 后（或者缩写为 _**hexo d**_ ）回车，我的电脑再次报错：

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo\blog&gt;hexo deploy
INFO  Validating config
INFO  Deploying: git
INFO  Clearing .deploy_git folder...
INFO  Copying files from public folder...
INFO  Copying files from extend dirs...
warning: LF will be replaced by CRLF in 2021/08/25/hello-world/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in archives/2021/08/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in archives/2021/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in archives/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in css/fonts/fontawesome-webfont.svg.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in css/style.css.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in fancybox/jquery.fancybox.min.js.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in js/jquery-3.4.1.min.js.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in js/script.js.
The file will have its original line endings in your working directory
[master (root-commit) a9fc5f8] Update Hexo Static Content
 17 files changed, 5174 insertions(+)
 create mode 100644 2021/08/25/hello-world/index.html
 create mode 100644 archives/2021/08/index.html
 create mode 100644 archives/2021/index.html
 create mode 100644 archives/index.html
 create mode 100644 css/fonts/FontAwesome.otf
 create mode 100644 css/fonts/fontawesome-webfont.eot
 create mode 100644 css/fonts/fontawesome-webfont.svg
 create mode 100644 css/fonts/fontawesome-webfont.ttf
 create mode 100644 css/fonts/fontawesome-webfont.woff
 create mode 100644 css/fonts/fontawesome-webfont.woff2
 create mode 100644 css/images/banner.jpg
 create mode 100644 css/style.css
 create mode 100644 fancybox/jquery.fancybox.min.css
 create mode 100644 fancybox/jquery.fancybox.min.js
 create mode 100644 index.html
 create mode 100644 js/jquery-3.4.1.min.js
 create mode 100644 js/script.js
fatal: unable to access 'https://github.com/Barry-Flynn/blog/': OpenSSL SSL_read: Connection was reset, errno 10054
FATAL {
  err: Error: Spawn failed
      at ChildProcess.&lt;anonymous&gt; (E:\Hexo\blog\node_modules\hexo-util\lib\spawn.js:51:21)      at ChildProcess.emit (events.js:400:28)
      at ChildProcess.cp.emit (E:\Hexo\blog\node_modules\cross-spawn\lib\enoent.js:34:29)
      at Process.ChildProcess._handle.onexit (internal/child_process.js:277:12) {
    code: 128
  }
} Something's wrong. Maybe you can find the solution here: %s https://hexo.io/docs/troubleshooting.html
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><div class="hide-preCode-box"><span class="hide-preCode-bt" data-report-view="{&quot;spm&quot;:&quot;1001.2101.3001.7365&quot;}"><img class="look-more-preCode contentImg-no-view" src="https://csdnimg.cn/release/blogv2/dist/pc/img/newCodeMoreWhite.png" alt="" title=""></span></div><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li><li style="color: rgb(153, 153, 153);">12</li><li style="color: rgb(153, 153, 153);">13</li><li style="color: rgb(153, 153, 153);">14</li><li style="color: rgb(153, 153, 153);">15</li><li style="color: rgb(153, 153, 153);">16</li><li style="color: rgb(153, 153, 153);">17</li><li style="color: rgb(153, 153, 153);">18</li><li style="color: rgb(153, 153, 153);">19</li><li style="color: rgb(153, 153, 153);">20</li><li style="color: rgb(153, 153, 153);">21</li><li style="color: rgb(153, 153, 153);">22</li><li style="color: rgb(153, 153, 153);">23</li><li style="color: rgb(153, 153, 153);">24</li><li style="color: rgb(153, 153, 153);">25</li><li style="color: rgb(153, 153, 153);">26</li><li style="color: rgb(153, 153, 153);">27</li><li style="color: rgb(153, 153, 153);">28</li><li style="color: rgb(153, 153, 153);">29</li><li style="color: rgb(153, 153, 153);">30</li><li style="color: rgb(153, 153, 153);">31</li><li style="color: rgb(153, 153, 153);">32</li><li style="color: rgb(153, 153, 153);">33</li><li style="color: rgb(153, 153, 153);">34</li><li style="color: rgb(153, 153, 153);">35</li><li style="color: rgb(153, 153, 153);">36</li><li style="color: rgb(153, 153, 153);">37</li><li style="color: rgb(153, 153, 153);">38</li><li style="color: rgb(153, 153, 153);">39</li><li style="color: rgb(153, 153, 153);">40</li><li style="color: rgb(153, 153, 153);">41</li><li style="color: rgb(153, 153, 153);">42</li><li style="color: rgb(153, 153, 153);">43</li><li style="color: rgb(153, 153, 153);">44</li><li style="color: rgb(153, 153, 153);">45</li><li style="color: rgb(153, 153, 153);">46</li><li style="color: rgb(153, 153, 153);">47</li><li style="color: rgb(153, 153, 153);">48</li><li style="color: rgb(153, 153, 153);">49</li><li style="color: rgb(153, 153, 153);">50</li><li style="color: rgb(153, 153, 153);">51</li><li style="color: rgb(153, 153, 153);">52</li><li style="color: rgb(153, 153, 153);">53</li><li style="color: rgb(153, 153, 153);">54</li><li style="color: rgb(153, 153, 153);">55</li></ul>
```

又报错了？我很晕。问了群里大佬，说可能是国内的墙导致的网络问题。好吧，免费的那个什么软件工具果然不太靠谱。解决该问题并重新连接后第三次输入命令 _**hexo deploy**_ ，回车

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">E:\Hexo\blog&gt;hexo deploy
INFO  Validating config
INFO  Deploying: git
INFO  Clearing .deploy_git folder...
INFO  Copying files from public folder...
INFO  Copying files from extend dirs...
warning: LF will be replaced by CRLF in 2021/08/25/hello-world/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in archives/2021/08/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in archives/2021/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in archives/index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in css/fonts/fontawesome-webfont.svg.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in css/style.css.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in fancybox/jquery.fancybox.min.js.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in index.html.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in js/jquery-3.4.1.min.js.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in js/script.js.
The file will have its original line endings in your working directory
On branch master
nothing to commit, working tree clean
info: please complete authentication in your browser...
Enumerating objects: 31, done.
Counting objects: 100% (31/31), done.
Delta compression using up to 4 threads
Compressing objects: 100% (25/25), done.
Writing objects: 100% (31/31), 882.21 KiB | 4.98 MiB/s, done.
Total 31 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/Barry-Flynn/blog
 + 4b62927...a9fc5f8 HEAD -&gt; main (forced update)
Branch 'master' set up to track remote branch 'main' from 'https://github.com/Barry-Flynn/blog'.
[32mINFO [39m Deploy done: [35mgit[39m
E:\Hexo\blog&gt;
<div class="hljs-button {2}" data-title="复制"></div></code><div class="hide-preCode-box"><span class="hide-preCode-bt" data-report-view="{&quot;spm&quot;:&quot;1001.2101.3001.7365&quot;}"><img class="look-more-preCode contentImg-no-view" src="https://csdnimg.cn/release/blogv2/dist/pc/img/newCodeMoreWhite.png" alt="" title=""></span></div><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li><li style="color: rgb(153, 153, 153);">12</li><li style="color: rgb(153, 153, 153);">13</li><li style="color: rgb(153, 153, 153);">14</li><li style="color: rgb(153, 153, 153);">15</li><li style="color: rgb(153, 153, 153);">16</li><li style="color: rgb(153, 153, 153);">17</li><li style="color: rgb(153, 153, 153);">18</li><li style="color: rgb(153, 153, 153);">19</li><li style="color: rgb(153, 153, 153);">20</li><li style="color: rgb(153, 153, 153);">21</li><li style="color: rgb(153, 153, 153);">22</li><li style="color: rgb(153, 153, 153);">23</li><li style="color: rgb(153, 153, 153);">24</li><li style="color: rgb(153, 153, 153);">25</li><li style="color: rgb(153, 153, 153);">26</li><li style="color: rgb(153, 153, 153);">27</li><li style="color: rgb(153, 153, 153);">28</li><li style="color: rgb(153, 153, 153);">29</li><li style="color: rgb(153, 153, 153);">30</li><li style="color: rgb(153, 153, 153);">31</li><li style="color: rgb(153, 153, 153);">32</li><li style="color: rgb(153, 153, 153);">33</li><li style="color: rgb(153, 153, 153);">34</li><li style="color: rgb(153, 153, 153);">35</li><li style="color: rgb(153, 153, 153);">36</li><li style="color: rgb(153, 153, 153);">37</li><li style="color: rgb(153, 153, 153);">38</li><li style="color: rgb(153, 153, 153);">39</li><li style="color: rgb(153, 153, 153);">40</li><li style="color: rgb(153, 153, 153);">41</li></ul>
```

成功了！Ohhhhhhhhhhh~

等待完成后，打开网址 `https://用户名.github.io` 就能看到你的线上网站了！

> 使用 https，http 可能无法正常打开。HTTPS 是多了安全加密的 HTTP，Chrome 浏览器已经默认会显示 `http` 链接为不安全。
>
> 为了安全，建议开启强制 https 跳转。`项目地址页面 -> Settings -> Options -> GitHub Pages -> Enforce HTTPS`。（翻到下面）
>
> 此时，http 网址会自动重定向到 https

### 十、备份与自动部署

我们当前只是将生成的静态文件部署到了云端。

为了以防万一，我们应该将网站的源代码文件也推送到 GitHub 仓库备份。

输入下方代码按回车，与远程 Git 仓库建立连接，只此一次即可

```
git remote add origin https://github.com/用户名/用户名.github.io
<div class="hljs-button {2}" data-title="复制"></div>
```

若输入错误，可以运行输入 _**git remote rm origin**_ 删除远程地址，

然后再输入一遍正确的命令与远程 Git 仓库建立连接，之后就行了。

接下来准备提交，这三句命令将是你以后每次备份所需要输入。

（括号内为注释，不用输入哈！）

```
<merlin-component id="merlin-code-summarizer" class="merlin-code-summarizer"></merlin-component><code class="has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">（添加到缓存区）
git add .
（这次做了什么更改，简单描述下即可）
git commit -m 'backup'
（第一次提交时，你可能需先运行下面命令设置一下默认提交分支）
（git push --set-upstream origin hexo）
（推送至远程仓库）
git push
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li></ul>
```

> 之后写文章可以在该项目下写，与之前一样，只不过这里同时管理了两个分支。
>
> main -负责展示静态网页
>
> hexo -备份本地hexo文件

> main分支更新

```
hexo d
<div class="hljs-button {2}" data-title="复制"></div>
```

> hexo分支更新

```
git add . #添加所有文件到暂存区
git commit -m "新增博客文章"  #提交
git push origin hexo #推送hexo分支到Github
<div class="hljs-button {2}" data-title="复制"></div>
```

## 
