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
- 提交代码
  - git commit -m "commit git.md"  

> -m 是指提示

### 查看状态

- 查看
  - git status (绿色代表已经add了没有提交，红色代表修改了没有add)
