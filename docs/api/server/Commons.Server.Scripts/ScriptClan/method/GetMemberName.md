---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>GetMemberName</div>
parent: ScriptClan
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

# [ScriptClan](../../).GetMemberName(Int64)
ID๋ก ๋ฉค๋ฒ ์ด๋ฆ ๊ฐ์ ธ์ค๊ธฐ

๋ค์์คํ์ด์ค: System
{: .text-zeta .no_toc}
์ด์๋ธ๋ฆฌ: Creator.dll
{: .text-zeta .no_toc}

## ์ ์ธ
```cs
public string GetMemberName(long id)
```

## ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.String|id|ํด๋น ๋ฉค๋ฒID|

## ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|System.String|

## ์์ 
ID๊ฐ 1์ธ ํด๋ ๋งด๋ฒ ์ด๋ฆ ์ถ๋ ฅํ๊ธฐ
```lua
local myClan = unit.player.clan
print(myClan.GetMemberName(1))
```