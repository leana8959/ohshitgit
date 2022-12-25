---
tags: tip
title: 厚，我不小心提交到 master 裡了！我應該提交到一個新的分支的！
id: accidental-commit-master
order: 4
---

```git
# 建立一個跟目前 master 一致的分支
git branch some-new-branch-name
# 刪除 master 分支裡最新的提交
git reset HEAD~ --hard
git checkout some-new-branch-name
# 你的提交現在在這個分支上了 :)
```

註：如果你已經推送這個提交至一個公開／共用的分支，然後試過其他方法了，你可能需要執行 `git reset HEAD@{number-of-commits-back}` 而不是 `git reset HEAD~`。哭哭。另外，這個方法是很多很多人推薦給我的，比我原本的方法還更簡潔，謝謝你們！