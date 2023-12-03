# 2204.14198_translate_zh
cvpr2022综述中文latex翻译

## 本仓库用于零基础人员实践学习latex项目结构及git基本操作

在 20 世纪，计算机教授高德纳（Donald Ervin Knuth）编写了一个排版软件，它可以处理非常复杂的数学公式，后来发展出了非常多的语言排版，它在学术界特别是数学、物理学和计算机科学界十分流行。tex 被普遍认为是一个优秀的排版工具，尤其是对于复杂数学公式的处理。利用 latex 等终端软件，tex 就能够排版出精美的文本以帮助人们辨认和查找。

latex 是一种基于 tex 的排版系统，利用这种格式系统的处理，即使用户没有排版和程序设计的知识也可以充分发挥由 tex 所提供的强大功能，不必一一亲自去设计或校对，能在几天，甚至几小时内生成很多具有书籍质量的印刷品。

目前来看，我们使用 latex 写文档，进行 git 提交，在使用的时候编译成 pdf，发送给其他人使用，其他人更新文档我们也可以非常方便进行 review。


### 使用时可采取两种协作方式：
第一种：团队内部成员 new branch后再提交

⚠️ 除非你知道自己在做什么并且确认你做的是对的，否则不要直接提交master分支！

第二种：团队外部成员 fork 后提issue，commit中使用`#`链接issue id，之后再提pr

`git commit -m "type(scope):subject #issuenum" `

## 开发规范
1. dev分支下自己切分支开发，平时merge到dev上；
  1. 使用时，
```
     git clone ->
     git checkout dev ->
     git branch "新分支名称" ->
     进行开发 ->
     开发完毕 ->
     git add . ->
     git commit -m "type(scope):subject #issuenum"
```
- 当不小心覆盖了main的commit 如在main 分支下pull dev分支时 ，请使用回退，撤销commit、暂存区
- 回退前一版本代码：`git reset HEAD~1`
  
2. Git commit 遵循 angular 规范
这里如果不清楚，可以看 [示例issue](https://github.com/ValeriaWong/2204.14198_translate_zh/issues/5)

`type(scope): subject #issueNum` 注意`:`后面有一个空格不要忘记

type见
```
[
'build', //编译相关的修改,例如发布版本、对项目构建或者依赖的改动
'feat',//新功能(feature)
'fix',//修复bug
'upd',//更新某功能
'refactor',//重构
'docs',//文档(documentation)过程成辅助工具的变动,比如增加依赖库等
]
```

# 完成任务的保姆级流程

如果你还没有git，请安装，如果有，请直接进行第二步
### 1. 安装Git

Git开源书籍描述了[如何安装git](https://git-scm.com/book/en/v2)。

这通常通过Ubuntu Linux上的`apt install git`，

在MacOS上安装Xcode开发人员工具或使用gihub的[桌面客户端](https://desktop.github.com)来实现

如果你没有GitHub帐户，则需要注册一个帐户。

### 2. fork仓库
你可以在任意github代码存储库点击fork，复制一份（分叉）到你的用户名。

单击 右上角红色框中的`Fork`按钮，以复制本书的存储库。

这将是你的副本，你可以随心所欲地更改它。

### 3. 提一个issue

请在本仓库提一个issue ，获得issue number （后续commit信息时需要用到这个issue number）
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/b0ee5df2-2442-4fd9-9cc2-9306074978ea)

issue是提前和开发者沟通你要完成的事项，问开发者是否考虑将其列入开发计划或者你开发之后他是否会考虑合并代码。

同时提前沟通也可以防止重复开发，也就是“不要重复造轮子”

如果是其他的代码仓库开源贡献，你可能要想一个新的功能点，或者发现一个bug 并fix it才可以成功合并代码。而我们这个场景其实就是翻译某一小段内容，练习一下latex和git的全部操作流程，并不要求创新性。

理解其中的数据流动是关键点，有可能你还会因此成就感满满～

这里如果不清楚，可以看 [示例issue](https://github.com/ValeriaWong/2204.14198_translate_zh/issues/5)

### 3. git clone 
如果你已经fork了仓库，请在你已经fork的仓库执行

你是本仓库的成员，新建了分支，请在本仓库执行（一般来说你不会是本仓库的成员的，因为我还没给你发邀请邮件，所以只要看上面那句就行）

![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/2fb3ee12-b42b-4aaf-9904-37f1b91578c1)
1. 点击code
2. 在https/ssh中选一个，新手建议https 点击复制 
3. windows 使用cmd+r开启命令行 ， mac 开启终端terminal
4. 在cmd / 终端 填入 `git clone + 「你复制的地址」`
- 注意，如果没有git ,请参照安装git一节

### 4. 进入目录切换分支
请在本地pc 的cmd / 终端 执行：

![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/c801a604-e3fe-46f1-89f9-d7e3b6cf46ee)
如上图所示，本地clone后进入目录
1. 你可以在命令行中使用 `ls`显示当前目录下的文件；
2. 使用`cd + 「你要进入的目录」`进入目录
比如此时我们要进入本存储库，则应使用
`cd 2204.19148_translate_zh`
3. 切换分支 `git checkout dev`
4. 新建分支  `git branch + 「新分支名称」` ，如`git branch dev` 
5. 使用本地IDE进行开发，高阶用户可使用vim等
- 注意：如果不知道怎样用IDE开发，请见后 latex 本地环境搭建及使用 一节
- 小技巧：有的windows可以在命令行输入`./code`在当前目录打开vscode/其他IDE

### 5. 进行开发中...
建议使用vscode作为开发IDE,下文的示例也是截图自vscode。

main.tex文件是很多latex仓库的入口文件

有一些latex排版，会在main.tex文件中使用`\input{}`或者`\section*{}`引入外部tex文件，括号中是其他tex文件的文件名。

我们现在翻译到了content.tex文件
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/a84b6d58-290d-4080-9ec7-a87451046f0a)
请注意在翻译的时候将命令保留，命令就是那些高亮的比如`\textbf{}`等等

随便翻译一小段就可以了，并不是全部翻译哈[捂脸]

这个任务主要是让我们知道你确实能找得到正文和需要撰写内容的位置，知道要怎么写命令（写命令的前提是你能识别命令）

不是打黑工！

不是打黑工！

不是打黑工！

这是个练习任务😂

翻译一小段然后就可以执行👇下面的步骤了

### 5. 开发完成提交
还剩这最后一步了哦！成功在望啦！冲鸭！

1. 添加到工作区 `git add .` 请不要忘记那个 `.` 这是所有的意思。
   - 如果不是添加所有文件，这里可以写你要添加的文件名（要有文件类型的后缀才可以）
3. 填写提交信息 `git commit -m "你要填写的提交信息，请遵循上文的开发规范填写此处"`

注意这里是一定要改的！commit就是你的提交信息，告诉我们你做了什么，在哪些范围做了什么事情，具体怎么改的，并且关联`#issuenum`
> Git commit 遵循 angular 规范
> `type: (scope)subject #issueNum`请注意type:后面有一个空格
> 你更改的类型：（你更改的范围）你主要做了什么事情 #关联的issuenum
> type见
```
[
'build', //编译相关的修改,例如发布版本、对项目构建或者依赖的改动
'feat',//新功能(feature)
'fix',//修复bug
'upd',//更新某功能
'refactor',//重构
'docs',//文档(documentation)过程成辅助工具的变动,比如增加依赖库等
]
```


5. 从远程仓库拉取最新代码 `git pull `
6. 如果有冲突需要手动解决冲突，我们这个场景一般很少出现冲突。
7. 上传到远程存储库 `git push + 「你的仓库简称，一般是origin」`

成功撒花🎉🎉🎉🎉🎉🎉🎉🎉🎉


### 其他未尽事项可参照[地址0](https://juejin.cn/post/7121986744316067848) 、 [地址1](https://github.com/d2l-ai/d2l-zh/blob/master/chapter_appendix-tools-for-deep-learning/contributing.md) 、[地址2](https://cloud.tencent.com/developer/article/1885681 ) 

### ⚠️如果遇到困难或bug无法解决请提issue
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/b0ee5df2-2442-4fd9-9cc2-9306074978ea)

# latex 本地环境搭建及使用
请自行下载latex环境 https://www.latex-project.org/get/

windows：
[MiKTeX](https://miktex.org/) 或[TeX Live](https://www.tug.org/texlive)
如果选择后者可以参见该链接[windows安装latex](https://blog.csdn.net/wzk4869/article/details/126043381)

mac:
安装 MacTeX 在 Mac 上，最常用的 LaTeX 发行版是 MacTeX，因此需要先安装 MacTeX。可以在官方网站 tug.org/mactex/ 下载最新版本的 MacTeX 安装包，双击运行即可。

以vscode 为例（请务必不要使用浏览器的vscode，它并不能使用本地的latex环境）
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/75c232f8-2ea5-404c-a4c2-6f86643b5678)

1. 点击红色框，扩展，下载latex workshop

<img width="840" alt="image" src="https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/cd044916-32a5-489d-8256-5aa7189f1479">

2. 成功安装后，打开任意`.tex`为后缀的文件，可以在vscode的左边边栏看到蓝色框TeX，点击后可以看到

![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/a2ce5f6f-dd64-4a2b-a066-2e3998f2302c)

4. 上图中绿色框是编译latex，蓝色框点击后可以选择view in vscode从而可以内嵌观看pdf

![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/203b2a09-c9f4-4bc6-b32d-f867d3ea0721)

# overleaf  latex使用技巧

1.进入左上角菜单（Menu）界面
选择编译器格式（Compiler）为`XeLatex`

2.基础名称与格式
```
\title {输入标题名称}
\abstract{里面输入摘要}
\key word{里面输入关键词}
\section{里面输入一级标题}
\subsection{里面输入二级标题}
\subsubsection{里面输入三级标题}
```
- 标题与正文间需要空一行
- 段与段间需要空一行
- 图片、表格，公式与正文需要空一行

2.如何插入公式：
在latex代码界面输入：
```
\begin(equation)
将公式转换的代码输入在该行
\end(equation)
```

如何的到公式转换的代码：
将所需公式转为图片，然后再复制进图片公式转换网址中
图片转公式网址（1）：https://simpletex.cn/
图片转公式网址（2）：http://img2latex.com/

3.如何输入表格
将所需表格转换为代码
表格转代码网址：https://tablesgenerator.com/

4.如何插入图片
在latex界面，重新编译（Recompile）左边第二个键（三个点），
点击并选择当中的insert figure
然后选择Upload from computer
选择所需要插入的图片，注必须为png格式


   
# markdown

### 是什么
Markdown是一种轻量级标记语言，它以纯文本形式(易读、易写、易更改)编写文档，并最终以HTML格式发布。其语法简洁易懂，替换不同的css模版即可以达到同一种内容，多种排版的效果。

### 为什么使用
- 它是易读（看起来舒服）、易写（语法简单）、易更改纯文本。处处体现着极简主义的影子。
- 兼容HTML，可以转换为HTML格式发布。
- 跨平台使用。
- 越来越多的网站支持Markdown。

知乎、endnote、幕布、飞书、掘金、百家号、甚至于做了某种代码改动后的**微信公众号编辑器**都接受markdown格式文本。

在公众号等新媒体运营、个人笔记、知识库管理等方面是当之无愧的效率工具。

本文就是使用markdown语法书写。

初学者可以参照[官方教程](https://markdown.com.cn/basic-syntax/)学习基本语法


# 参考链接
- [git流程参考](https://juejin.cn/post/7121986744316067848) 
- [windows安装latex](https://blog.csdn.net/wzk4869/article/details/126043381)
- [vscode配置latex（包含mac）](https://blog.csdn.net/weixin_50894115/article/details/122058757)
- [markdown](https://younghz.github.io/Markdown/)
 
# 如本文档有未尽事项/使用过程中有疑问，请提issue
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/b0ee5df2-2442-4fd9-9cc2-9306074978ea)

