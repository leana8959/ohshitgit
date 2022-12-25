---
tags: tip
title: 靠，我在提交完之後才想起來還有個東西要改！
id: change-last-commit
order: 2
---

```git
# 完成你的修改
git add . # 或加入指定的檔案
git commit --amend --no-edit
# 現在你最新的 commit 包含了你剛剛的修改!
# 警告：不要 amend 公開的 commit
```

我常常在提交後執行測試或 linter 時遇到這種情況「幹，我忘了在等號後放空格」。你也可以提交一個新的 commit，再執行 `rebase -i` 來合併這兩個 commit，不過相較之下 amend 快了幾十萬倍。

*警告：你絕對不應該在一個公開／共用的分支上 amend 已被推送的 commit！你只應該對你本機分支 amend，不然你會很慘。*