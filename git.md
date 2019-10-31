# git

是一个开源的分布式版本控制系统

## git 使用

### 初始化设置

- 初始化(会多个.git目录)
  - git init
- 设置全局用户名
  - git config --global user.name "jincheng.zhang"
- 设置全局邮箱
  - git config --global user.email "xiaokawayixiao@qq.com"

> -global 是值全局设置

### 提交代码到本地仓库

- 添加要提交的代码
  - git add ./git.md
  - git add .[/]  (添加所有)
- 提交代码
  - git commit -m "commit git.md"  
- 强制提交所有(可以不用add)
  - git commit -a -m "bbb"

> -m 是指提示  [] 表示可省略

### 查看状态

- 查看
  - git status (绿色代表已经add了没有提交，红色代表修改了没有add)

### git 忽略文件

.gitignore中可以设置需要忽略的文件及目录

```.gitignore
 # 忽略文件
.idea
.vscode
# 忽略目录
/dist
# 匹配忽略
*.js
```

### git 查看日志

- 查看提交记录
  - git log (每次提交一次会多一条记录)
    - commit 927905fdb81c66b571294f95ee098909ae2c21e5 (代表id)
    - Author: jincheng.zhang <xiaokawayixiao@qq.com>
    - Date:   Thu Oct 31 15:22:39 2019 +0800
    - bbb (提交的备注)
- 查看精简日志
  - git log --oneline
    - 388f564 (HEAD -> master) hahaha   # 表示目前最新的
    - 927905f aaa  (aaa 备注)
    - 9cdd8e0 commit git.md
  - git log 9cdd8e0 (查看具体某一条)

### git 版本回退

- 回退到指定版本
  - git reset --hard head~0
  - git reset --hard 388f564  (直接指定id)

- 查看操作日志 (可用于版本切换)
  - git reflog
    - 388f564 (HEAD -> master) HEAD@{4}: reset: moving to head~1
    - 17279f0 HEAD@{5}: commit: zjc

> --hard 覆盖掉本地代码  head~0 表示最新 head~1次新 ...

### git 分支 branch

- 创建分支
  - git branch dev
- 查看分支
  - git branch
    - *代表目前分支
- 切换分支
  - git checkout dev
- 删除分支
  - git branch -d dev

- 将dev合并到主分支
  - 先 git checkout master
  - git merge dev

- 解决冲突
  