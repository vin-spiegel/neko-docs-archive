---
layout: default
title: <font color="#2c84fa">๐</font> GetMonster
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## GetMonster(Int32)
๋ฐ์ดํฐ๋ฒ ์ด์ค์ ๋ชฌ์คํฐ ์ ๋ณด

#### ์ ์ธ
```cs
public TGameMonster GetMonster(int id)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|id|๋ชฌ์คํฐ ID|

#### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|TGameMonster|๋ฐ์ดํฐ๋ฒ ์ด์ค์ ๋ชฌ์คํฐ ์ ๋ณด|

#### ์์ : ๋ฐ์ดํฐ๋ฒ ์ด์ค์ ์์ฑํ 5๋ฒ ๋ชฌ์คํฐ ์ ๋ณด ๊ฐ์ ธ์ค๊ธฐ
```lua
local myMonster = Server.GetMonster(5)
```