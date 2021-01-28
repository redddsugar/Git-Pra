# Git常用命令

### git init
- 将本地库初始化为git库。

### git add file       （ . 则代表所有文件）
- 把文件添加到暂存区

### git commit -m "此次提交的主题"
- 提交更改，实际上就是把暂存区的所有内容提交到当前分支
### git push -u origin master
- 将当前分支推送至远程仓库(前提是远程仓库已经与本地库关联才可推送)

## 关联远程仓库
#### ssh-keygen -t rsa -C "youremail@example.com"
```text
1.创建SSH Key。位于用户主目录下的.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，id_rsa.pub是公钥
2.登录GitHub，打开“Account settings”，“SSH Keys”页面：然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容
3.登录GitHub，然后，在右上角找到“Create a new repo”按钮，创建一个新的仓库(建议与本地git库同名)
4.进入本地git库的目录下 git remote add origin https://github.com/账户名/库名.git
```

### git log
- 显示从最近到最远的提交日志

## 撤销操作
### git checkout -- file
- 丢弃工作区的修改
### git checkout -- file
- 丢弃添加至暂存区的修改

## 分支操作
### git branch dev    git branch -d dev
- 创建一个dev分支         删除dev分支
### git switch branch-name
- 切换至某分支        （此两条命令可合并为一条 git checkout -b dev）
### git merge branch-name
- 将dev分支合并至某分支



