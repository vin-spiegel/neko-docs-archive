---
layout: default
title: <font color="#2c84fa">๐</font> GetTileset
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## GetTopic(String)
ํน์  topic์ ๋ํ ์ด๋ฒคํธ ์ฝ๋ฐฑ์ ๊ฐ์ ธ์ต๋๋ค. ํด๋ผ์ด์ธํธ์์ ๋ณด๋ธ topic ์ด๋ฒคํธ๋ฅผ ์ฒ๋ฆฌํฉ๋๋ค.

#### ์ ์ธ
```cs
public ScriptEventPublisher GetTopic(string topic)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.String|topic|๋ณด๋ผ topic id|

#### ๋ฐํ

|ํ์|์ค๋ช|
|:-|:-|
|ScriptEventPublisher|

#### ์์  
```lua
-- ํด๋ผ์ด์ธํธ์์ "Apple" ์ด๋ ์ฃผ์ ๋ก FireEvent๋ฅผ ๋ฐ์กํ์ ๋
-- ๋ชจ๋  ํด๋ผ์ด์ธํธ๋ค์๊ฒ "Apple" ์ด๋ ๋ฉ์์ง ํ์ํ๊ธฐ

Server.GetTopic("Apple").Add(function()
    Server.SendCenterLabel("Apple")
end)

-- ํด๋ผ์ด์ธํธ์์ "MyName" ์ด๋ ์ฃผ์ ๋ก FireEvent๋ฅผ ๋ฐ์กํ์ ๋
-- ๋ชจ๋  ํด๋ผ์ด์ธํธ๋ค์๊ฒ ๊ฐ์ด ๋ฐ์ ์ธ์ ๋ฉ์์ง๋ฅผ ํ์ํ๊ธฐ

-- ํด๋ผ์ด์ธํธ์์: Client.FireEvent("MyName", "Hello Server!")
-- ์คํ ์ ์ถ๋ ฅ: Hello Server!

Server.GetTopic("MyName").Add(function(name)
    Server.SendCenterLabel(name)
end)
```