---
layout: default
title: <font color="#2c84fa">๐</font> GetMap
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## GetMap(Int32, TGameMapStub)
๋งต ๋ฐ์ดํฐ ์ ๋ณด

#### ์ ์ธ
```cs
public TGameMapStub GetMap(int id, TGameMapStub parent = null)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|id|๋งต iD|
|TGameMapStub|parent|๊ธฐ๋ณธ null ์ ํ๋ ๋งต์ ๋ถ๋ชจ|

#### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|TGameMapStub|๋งต ๋ฐ์ดํฐ ์ ๋ณด|

#### ์์ : 5๋ฒ ID๋ฅผ ๊ฐ์ง ๋งต์ ์ ๋ณด๋ฅผ ๊ฐ์ ธ์ค๊ธฐ
```lua
-- PC ๋๋ ๋ชจ๋ฐ์ผ ์คํ๋์ค ๋งต ํธ์ง๊ธฐ์์ #00 ํ์์ผ๋ก ๋์ค๋ ๊ฒ์ด ๋งต์ ID์๋๋ค

local myMap = Server.GetMap(5)
```