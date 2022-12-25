---
tags: tip
title: 厚，我得取消一個檔案的修改！
id: undo-a-file
order: 8
---

```git
# 用方向鍵上下瀏覧歷史，找到一個該檔案被修改前的提交
git log
# 記下該提交的 hash 值
git checkout [saved hash] -- path/to/file
# 現在該檔案的舊版本在你的暫存區了
git commit -m "Wow, you don't have to copy-paste to undo"
```

我的整個世界都在我學到這個的那瞬間徹底改變了。真的。好啦話說回來，到底哪個星球的人會覺得 `checkout --` 是一個還原檔案指令的好名字？ （對著 Linux Torvalds 折手指）