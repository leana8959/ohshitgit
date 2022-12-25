---
tags: tip
title: 厚，我提交錯分支了！
id: accidental-commit-wrong-branch
order: 5
---

```git
# 在保留修改的同時取消上一個提交
git reset HEAD~ --soft
git stash
# 切換到正確的分支
git checkout name-of-the-correct-branch
git stash pop
git add . # 或加入指定的檔案
git commit -m "your message here";
# 現在你的修改在對的分支上了
```

很多人推薦在這個情況下使用 `cherry-pick` 指令，挑你喜歡的方法吧！

```git
git checkout name-of-the-correct-branch
# 取得 master 上的最新提交
git cherry-pick master
# 在 master 上刪除那個提交
git checkout master
git reset HEAD~ --hard
```