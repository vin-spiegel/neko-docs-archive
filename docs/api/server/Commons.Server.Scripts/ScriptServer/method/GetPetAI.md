---
layout: default
title: <font color="#2c84fa">๐</font> GetPetAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->


## GetPetAI(Int32)
ํซ AI๋ฅผ ๊ฐ์ ธ์จ๋ค.

#### ์ ์ธ
```cs
public Closure GetPetAI(int id)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|id|ํซ ID|

### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### ์์ : 0๋ฒ ํซ์ AI ํจ์ ๊ฐ์ ธ์ค๊ธฐ
```lua
local aiFunc = Server.GetPetAI(0)
```