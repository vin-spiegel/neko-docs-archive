---
layout: default
title: <font color="#2c84fa">๐</font> GetCharacter
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->


## GetCharacter(Int32)
๋ฐ์ดํฐ๋ฒ ์ด์ค์ ์บ๋ฆญํฐ์ ๋ณด

#### ์ ์ธ
```cs
public TGameCharacter GetCharacter(int id)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|id|์บ๋ฆญํฐ ID|

#### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|TGameCharacter|๋ฐ์ดํฐ๋ฒ ์ด์ค ์บ๋ฆญํฐ ์ ๋ณด|

#### ์์ : ๋ฐ์ดํฐ๋ฒ ์ด์ค์ ์์ฑํ 5๋ฒ ์บ๋ฆญํฐ ์ ๋ณด ๊ฐ์ ธ์ค๊ธฐ
```lua
local myCh = Server.GetCharacter(5)
```