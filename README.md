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
