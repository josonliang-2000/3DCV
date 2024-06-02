## 3DCV
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
## 用ssh连接代替https
```
# 1 生成SSH密钥：
ssh-keygen -t ed25519 -C "your_email@example.com"

# 2 添加SSH密钥到SSH代理：
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# 3 添加SSH公钥到GitHub：
# 打开SSH公钥文件并复制其内容：
cat ~/.ssh/id_ed25519.pub
# 登录GitHub，进入 Settings > SSH and GPG keys。
# 点击 New SSH key，将公钥粘贴到文本框中，并保存。

# 4 配置SSH（可选，但推荐）：
# 编辑或创建你的~/.ssh/config文件，添加以下内容：
# Host github.com
#     HostName ssh.github.com
#     User git
#     Port 443
#     IdentityFile ~/.ssh/id_ed25519

# 5 检查权限：
chmod 600 ~/.ssh/id_ed25519
chmod 644 ~/.ssh/id_ed25519.pub

# 6 测试连接：
ssh -T git@github.com

# 如果问题仍然存在：
# - 检查SSH公钥是否正确添加到GitHub。
# - 尝试重新生成密钥。

```
