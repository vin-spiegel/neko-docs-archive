---
layout: default
title: <font color="#2c84fa">๐</font> HttpPost
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->


## HttpPost(String, Table, Closure)
Http POST ์์ฒญ์ ๋ณด๋ด๊ณ , ๋ฐ์ดํฐ๋ฅผ ๊ฐ์ ธ์จ๋ค.

#### ์ ์ธ
```cs
public bool HttpPost(string url, Table data, Closure callback)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.String|url|url|
|MoonSharp.Interpreter.Table|data|๋ฃจ์ Table ํ์ ๋ฐ์ดํฐ|
|MoonSharp.Interpreter.Closure|callback|๊ฐ์ ธ์จ ๋ฐ์ดํฐ ์ฒ๋ฆฌ ์ฝ๋ฐฑ|

#### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|System.Boolean|

#### ์์ : t ๋ผ๋ ํ์ด๋ธ์ ๋ง๋ค๊ณ , ๋ณด๋ผ POST ์์ฒญ ๋ฐ์ดํฐ ๋ฃ๊ธฐ
```lua
local t = {}
t.id = 1234
t.name = "Hello"

-- http://naver.com URL๋ก ์์ฒญ ๋ณด๋ด๊ณ , res๋ก ๋ฐ์ดํฐ ๋ฐ๊ธฐ
Server.HttpGet('http://naver.com', t, function(res)
  print(res) -- ์นํ์ด์ง๊ฐ ๋ฐํํ ๊ฒฐ๊ณผ ํ์คํธ๊ฐ ์ถ๋ ฅ๋ฉ๋๋ค.
end)

-- ์น ์๋ฒ์์ ๋ฐ์ดํฐ ๋ฐ๊ธฐ

-- POST๋ก ์์ฒญ์ ๋ฐ์ ๊ฒฝ์ฐ, ์๋์ ๊ฐ์ด ๋ฐ์ดํฐ๋ฅผ ์ถ๋ ฅํ  ์ ์์ต๋๋ค.
-- ์ด ๋ฐ์ดํฐ๋ฅผ MySQL๊ณผ ๊ฐ์ ๋ฐ์ดํฐ๋ฒ ์ด์ค์ ๋ฃ์ด, ์๊ตฌ๋ณด๊ดํ  ์ ์์ต๋๋ค.

<?php
echo $_POST["id"];
echo $_POST["name"];

echo "์ ๋ฐ์์ต๋๋ค!";
?>

-- Server.HttpGet ์์ ๋ณด๋ธ ๋ฐ์ดํฐ๊ฐ ์น ์๋ฒ์ ์ ๋์ฐฉํ์๋์ง๋ฅผ ํ์ธํ๊ธฐ ์ํ ์ฝ๋์๋๋ค. 
-- ์ ์๋ฒ ์คํฌ๋ฆฝํธ ์์ฌ์ print(res) ์ ์ํด โ1234Hello์ ๋ฐ์์ต๋๋ค!โ ๊ฐ ์ถ๋ ฅ๋ฉ๋๋ค.
```
