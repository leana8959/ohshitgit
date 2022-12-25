---
tags: tip
title: 我他媽的不幹了。
id: fuck-this-noise
note: this should always be the last one in the list, so setting order to 20 so I don't have to re-name/re-order it
order: 20
---

```git
cd ..
sudo rm -r fucking-git-repo-dir
git clone https://some.github.url/fucking-git-repo-dir.git
cd fucking-git-repo-dir
```
謝謝 Eric V. 提供這則建議。如果你對使用 `sudo` 不滿的話，可以去找他踹共。

好啦認真認真，如果你的分支真的被徹底的毀了，然後你想要中規中矩的把你的本機倉儲重設成遠端倉儲的狀態，試試下面的方法。請注意，你無法取消以下操作！

```git
# 取得 origin 的最新狀態
git fetch origin
git checkout master
git reset --hard origin/master
# 刪除未被追蹤的檔案
git clean -d --force
# 對每個廢掉的分支都進行同樣的操作
```