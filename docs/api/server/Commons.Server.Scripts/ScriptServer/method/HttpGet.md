---
layout: default
title: <font color="#2c84fa">๐</font> HttpGet
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## HttpGet(String, Closure)
Http GET ์์ฒญ์ ๋ณด๋ด๊ณ , ๋ฐ์ดํฐ๋ฅผ ๊ฐ์ ธ์จ๋ค.

#### ์ ์ธ
```cs
public bool HttpGet(string url, Closure callback)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.String|url|url|
|MoonSharp.Interpreter.Closure|callback|๊ฐ์ ธ์จ ๋ฐ์ดํฐ ์ฒ๋ฆฌ ์ฝ๋ฐฑ|

#### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|System.Boolean|

#### ์์ : Http GET ์ ์ด์ฉํด์ ์น ํ์ด์ง์์ ๋ฐ์ดํฐ๋ฅผ ๋ฐ์์ค๊ธฐ
```lua
Server.HttpGet('http://nekoland.net/', function (res)
    print(res)
end)
```