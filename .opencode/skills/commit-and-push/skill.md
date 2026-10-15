# Commit and Push

提交并推送当前项目到 Gitee 仓库。

## 远程仓库

- URL: https://gitee.com/translation-by-guan-si/gaojiwangye666

## 步骤

1. 检查当前 git 状态（`git status`）
2. 暂存所有更改（`git add -A`）
3. 创建提交（`git commit -m "更新项目文件"`）
4. 推送到远程仓库（`git push origin main`，若分支为 master 则推送 master）

## 注意事项

- 如果远程仓库未配置，先执行 `git remote add origin https://gitee.com/translation-by-guan-si/gaojiwangye666`
- 如果推送被拒绝（远程有更新），先 `git pull --rebase origin main` 再推送
- 提交信息使用中文，简洁描述本次更新内容
