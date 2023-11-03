# 2204.19148_translate_zh
cvpr2022综述中文latex翻译

## 论文文件名命名规范
日期-文件标题-版本号-作者
如`20231130-商标驳回复审预测结果模型with_tfidf_and_xgboost-v1.0-valeria`
请注意，文件名不能有空格，空格请用下划线 `_`代替。

## 本仓库用于零基础人员实践学习latex项目结构及git基本操作

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
  3. 当不小心覆盖了main的commit 如在main 分支下pull dev分支时 ，请使用回退，撤销commit、暂存区 回退前一版本代码：`git reset HEAD~1`
2. Git commit 遵循 angular 规范
type: (scope)subject #issueNum请注意type:后面有一个空格
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

## 保姆级流程

### git clone 
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/2fb3ee12-b42b-4aaf-9904-37f1b91578c1)
1. 点击code
2. 在https/ssh中选一个，新手建议https 点击复制 
3. windows 使用cmd+r开启命令行 ， mac 开启终端terminal
4. 在cmd / 终端 填入 `git clone + 「你复制的地址」`
- 注意，如果没有git ,请参照安装git一节

### 进入目录切换分支
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

### 进行开发中...

main.tex文件是很多latex仓库的入口文件

有一些latex排版，会在main.tex文件中使用`\input{}`或者`\section*{}`引入外部tex文件，括号中是其他tex文件的文件名。

我们现在翻译到了content.tex文件
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/a84b6d58-290d-4080-9ec7-a87451046f0a)
请注意在翻译的时候将命令保留，命令就是那些高亮的比如`\textbf{}`等等

### 开发完成提交
1. 添加到工作区 `git add .` 请不要忘记那个 `.` 这是所有的意思。如果不是所有，这里可以写你要添加的文件名（要有文件类型的后缀才可以）
2. 填写提交信息 `git commit -m "你要填写的提交信息，请遵循上文的开发规范填写此处"`
3. 从远程仓库拉取最新代码 `git pull `
4. 如果有冲突需要手动解决冲突，我们这个场景一般很少出现冲突。
5. 上传到远程存储库 `git push + 「你的仓库简称，一般是origin」`




### 安装Git

Git开源书籍描述了[如何安装git](https://git-scm.com/book/en/v2)。
这通常通过Ubuntu Linux上的`apt install git`，
在MacOS上安装Xcode开发人员工具或使用gihub的
[桌面客户端](https://desktop.github.com)来实现。
如果你没有GitHub帐户，则需要注册一个帐户。

### fork仓库
你可以在任意github代码存储库点击fork，复制一份（分叉）到你的用户名。
单击 右上角红色框中的`Fork`按钮，以复制本书的存储库。
这将是你的副本，你可以随心所欲地更改它。

## 其他未尽事项可参照[地址](https://github.com/d2l-ai/d2l-zh/blob/master/chapter_appendix-tools-for-deep-learning/contributing.md)


## overleaf  latex使用技巧

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

## latex 本地环境搭建及使用
请自行下载latex环境
以vscode 为例
![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/75c232f8-2ea5-404c-a4c2-6f86643b5678)
1. 点击红色框，扩展，下载latex workshop
<img width="840" alt="image" src="https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/cd044916-32a5-489d-8256-5aa7189f1479">
2. 成功安装后，可以看到蓝色框TeX，点击后可以看到

![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/a2ce5f6f-dd64-4a2b-a066-2e3998f2302c)

4. 上图中绿色框是编译latex，蓝色框点击后可以选择view in vscode从而可以内嵌观看pdf

![image](https://github.com/ValeriaWong/2204.19148_translate_zh/assets/63283616/203b2a09-c9f4-4bc6-b32d-f867d3ea0721)

   
## markdown

