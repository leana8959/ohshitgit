---
tags: tip
title: 靠，我犯了一個很嚴重的錯誤，拜托告訴我 Git 有個魔法時光機功能？！？
id: magic-time-machine
order: 1
---

```git
git reflog
# 你將看到一個清單，裡面是你在 git 裡所有分支裡做過的所有更動！
# 每一個項目都有一個索引 HEAD@{index}
# 找到在你犯錯的前一個項目
git reset HEAD@{index}
# 讚啦，魔法時光機萬歲
```

你可以用這個功能來找回你不小心刪掉的東西、取消你在這個 repo 的錯誤操作、取消一個有問題的 merge、又或是回到上一個還可以執行的版本。我超常用 `reflog`，超級無敵感謝那些推薦我加上這項的人們！