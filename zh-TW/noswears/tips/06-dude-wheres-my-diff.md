---
tags: tip
title: 厚，diff 怎麼什麼都不顯示？！
id: dude-wheres-my-diff
order: 6
---
如果 `diff` 在修改檔案後什麼都不顯示，你的修改可能已經被新增到暫存區了。你得多用一個特別參數才能看到新的修改。

```git
git diff --staged
```

檔案在這 &macr;\\\_(ツ)\_/&macr; (我知道這是個功能，不是個 bug，但是第一次遇到的時候你八成還是會想把電腦砸了！)