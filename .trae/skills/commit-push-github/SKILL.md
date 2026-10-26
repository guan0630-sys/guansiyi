---
name: commit-push-github
description: Commit and push the whole project to the GitHub remote guan0630-sys/guansiyi via SSH. Use when the user asks to commit and push to GitHub or sync the project to GitHub. Do not use for Gitee pushes.
---

# Commit Push GitHub

提交并推送整个项目到 GitHub 仓库（SSH 方式，公钥已配置）。

- 仓库主页：https://github.com/guan0630-sys/guansiyi
- SSH 地址（443 端口，已验证可用）：ssh://git@ssh.github.com:443/guan0630-sys/guansiyi.git
- 备用 SSH 地址（22 端口，本机网络已屏蔽）：git@github.com:guan0630-sys/guansiyi.git

## 步骤

1. 检查当前 git 状态（`git status`），确认要提交的更改。
2. 暂存所有更改（`git add -A`）。
3. 创建提交（`git commit -m "更新项目文件"`）。
4. 确认当前分支（`git branch --show-current`），通常是 main 或 master。
5. 推送到远程仓库（`git push -u origin <当前分支>`）。

## 注意事项

- PowerShell 5 环境下多个命令用 `;` 连接，不要用 `&&`
- 如果远程仓库未配置，先执行 `git remote add origin git@github.com:guan0630-sys/guansiyi.git`
- 如果远程已存在但指向其他地址（如 Gitee），不要改动现有 origin；改用 `git remote add github git@github.com:guan0630-sys/guansiyi.git` 新增名为 `github` 的远程，推送时用 `git push -u github <当前分支>`
- 如果推送被拒绝（远程有更新），先 `git pull --rebase origin <当前分支>` 再推送
- 提交信息使用中文，简洁描述本次更新内容
- 公钥已设置，若提示权限错误，先运行 `ssh -T git@github.com` 验证 SSH 连接