# Git教程

- 前提设置
    
    ```bash
    # 设置姓名和邮箱地址
    git config --global user.name "名字"
    git config --global user.email "邮箱"
    # 创建SSH Key
    ssh-keygen -t rsa -C "邮箱"
    # 查看公开密钥
    cat ~/.ssh/id_rsa.pub
    # 测试SSH匹配
    ssh -T git@github.com  
    ```
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/567fcc57-9d8d-422b-8374-810645e7258e/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/68bf8a80-6e41-4bd0-8ff2-9b9a037dae66/Untitled.png)
    
    - 基本操作
    
    ```bash
    # 初始化仓库
    git init
    # 查看仓库流程
    git status
    # 暂存区添加文件
    git add 文件名
    # 保存仓库历史记录
    git commit -m "详细提交信息"
    # 查看提交日志
    git log
    # 查看提交日志第一行
    git log --pretty=short
    # 查看指定提交日志
    git log 文件名
    # 查看指定日志的文件改动
    git log -p 文件名
    # 查看工作树和暂存区的差别
    git diff
    # 查看工作树和最新提交的差别(提交前检查)
    git diff HEAD
    
    ```
    
    - 分支操作
    
    ```bash
    # 显示分支一览表
    git branch
    # 创建切换分支
    git checkout -b 分支名
    # 切换分支
    git checkout 分支名
    # 切换回上一个分支
    git checkout -
    # 合并分支
    git merge --no-ff 分支名
    # 以图表形式查看分支
    git log --graph
    ```
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/af7e97cd-da87-4ee5-9ccd-48fb419b097f/Untitled.png)
    
    - 更改提交
    
    ```bash
    # 查看当前仓库操作日志
    git reflog
    # 回溯历史
    git reset --hard 哈希值
    # 修改提交信息
    git commmit --amend
    # 添加提交
    git commit -am "提交分支树"
    # 压缩历史
    git rebase -i
    ```
    
    - 推送远程仓库
    
    ```bash
    # 删除远程仓库
    git remote rm origin
    # 添加远程仓库
    git remote add origin git@github.com:用户名/仓库名.git
    # 推送远程仓库
    git push -u origin master
    # 推送不同分支
    git push -u origin 分支名
    ```
    - 远程仓库获取
    
    ```bash
    # 下载远程仓库(默认master)
    git clone
    # 查看远程提交日志
    git branch -a
    # 获取远程分支到本地仓库
    git checkout -b 本地分支 origin/远程分支
    # 获取最新远程仓库分支
    git pull origin 远程分支
    ```
    - Pull Request
    
    ```bash
    # 测试网站 http://ituring.github.io/first-pr/
    git clone -> git branch -a -> git checkout -b 新分支 -> 修改
    git diff -> git add -> git commit -m "" -> git push origin 分支
    
    ```
    
    
