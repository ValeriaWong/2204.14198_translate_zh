# 2204.19148_translate_zh
cvpr2022综述中文latex翻译

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

## todo: latex使用技巧
这里可以共创，记录使用心得
1.进入左上角菜单（Menu）界面
选择编译器格式（Compiler）为XeLatex

2.基础名称与格式
\title {输入标题名称}
\abstract{里面输入摘要}
\key word{里面输入关键词}
\section{里面输入一级标题}
\subsection{里面输入二级标题}
\subsubsection{里面输入三级标题}
标题与正文间需要空一行
段与段间需要空一行
图片、表格，公式与正文需要空一行

3.如何插入公式：
在latex代码界面输入：
\begin(equation)
将公式转换的代码输入在该行
\end(equation)

如何的到公式转换的代码：
将所需公式转为图片，然后再复制进图片公式转换网址中
图片转公式网址（1）：https://simpletex.cn/
图片转公式网址（2）：http://img2latex.com/

4.如何输入表格
将所需表格转换为代码
表格转代码网址：https://tablesgenerator.com/

5.如何插入图片
在latex界面，重新编译（Recompile）左边第二个键（三个点），
点击并选择当中的insert figure
然后选择Upload from computer
选择所需要插入的图片，注必须为png格式

