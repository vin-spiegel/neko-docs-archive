---
layout: default
title: <font color="#2c84fa">๐</font> GetMonsterAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## GetMonsterAI(Int32)
๋ชฌ์คํฐ AI๋ฅผ ๊ฐ์ ธ์จ๋ค.

#### ์ ์ธ
```cs
public Closure GetMonsterAI(int id)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|id|๋ชฌ์คํฐ์ ID|

#### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### ์์ : 0๋ฒ ๋ชฌ์คํฐ์ AI ํจ์ ๊ฐ์ ธ์ค๊ธฐ
```lua
local aiFunc = Server.GetMonsterAI(0)
```