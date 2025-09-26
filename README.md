# Using git and termux to synchronize Android and computer
1. **部署git**
    1. 安装 Git 和 OpenSSH
   ```
   pkg update && pkg upgrade
      pkg install git openssh
   ```
    2. 设置你的 Git 用户名和邮箱
   ```git config --global user.name "你的用户名"
	    git config --global user.email "你的邮箱"
   ```
	3. SSH认证
	```ssh-keygen -t ed25519 -C "你的邮箱"`(一路回车使用默认设置,密钥文件路径在 `~/.ssh/id_ed25519`)
	cat ~/.ssh/id_ed25519.pub复制输出的内容
	4. 登录GitHub/GitLab>**Settings**（设置）> **SSH and GPG keys**>将刚才复制的公钥粘贴进去并保存
2. **上传至仓库**
3. **拉取**
    `cd 你的仓库名
    `git pull origin 你的分支名
4. 推送
    `cd 你的仓库名
    `git add .
    `git commit -m "你的提交信息"
    `git push origin 你的分支名
    
