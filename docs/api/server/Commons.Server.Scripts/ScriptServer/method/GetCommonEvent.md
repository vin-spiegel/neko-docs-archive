---
layout: default
title: <font color="#2c84fa">๐</font> GetCommonEvent
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

# GetCommonEvent(Int32)
๋ฐ์ดํฐ๋ฒ ์ด์ค์ ๊ณต์ฉ์ด๋ฒคํธ์ ๋ณด

#### ์ ์ธ
```cs
public TGameCommonEvent GetCommonEvent(int id)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|id|์ด๋ฒคํธ ID|

#### ๋ฐํ    

|ํ์|์ค๋ช|
|:-|:-|
|TGameCommonEvent|๊ณต์ฉ์ด๋ฒคํธ์ ๋ณด|

#### ์์ : ๋ฐ์ดํฐ๋ฒ ์ด์ค์ ์์ฑํ 5๋ฒ ๊ณต์ฉ ์ด๋ฒคํธ ์ ๋ณด ๊ฐ์ ธ์ค๊ธฐ
```lua
local myComEvent = Server.GetCommonEvent(5)
```