---
layout: default
title: <font color="#2c84fa">๐</font> SetMonsterAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## SetMonsterAI(Int32, Closure)
๋ชฌ์คํฐ AI๋ฅผ ๋ฑ๋กํ๋ค. ๋ชฌ์คํฐ์ ID ๋ฅผ ์ด์ฉํด, ํด๋น ๋ชฌ์คํฐ์ AI๋ฅผ ๋ฑ๋กํ๋ค.

#### ์ ์ธ
```cs
public void SetMonsterAI(int id, Closure c)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|id|๋ชฌ์คํฐ์ ID|
|MoonSharp.Interpreter.Closure|c|AI ํจ์|

#### ์์ : 0๋ฒ ๋ชฌ์คํฐ์ AI ์ค์ 
```lua
Server.SetMonsterAI(0,
    function(monster, ai, event, data)
        -- ์ฌ๊ธฐ์ AI ์ฝ๋๋ฅผ ์ฝ์ํฉ๋๋ค
    end)
```