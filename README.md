# 3DCV
可以直接合并主分支，也可以自己开个分支：
1. 先获取远程仓库更新，否则不同步会报错
```
  git fetch origin
```
3. 创建并切换到自己分支
 ```
   git checkout -b [名字拼音]
 ```
3. 提交你的内容
```
  git add .
  git commit -m "描述你所做的更改"
```
4. 提交到远程仓库
```
  git push -u origin [你的分支名]
```
