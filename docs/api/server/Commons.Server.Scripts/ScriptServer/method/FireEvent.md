---
layout: default
title: <font color="#2c84fa">๐</font> FireEvent
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## FireEvent(String, Object[])
ํด๋ผ์ด์ธํธ๋ก topic์ ๋ํด ์ด๋ฒคํธ๋ฅผ ๋ณด๋๋๋ค.

#### ์ ์ธ
```cs
public void FireEvent(string topic, params object[] arguments)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.String|topic|๋ณด๋ผ topic id|
|System.Object[]|arguments|ํจ๊ป๋ณด๋ผ ์ธ์๋ค|

### ์์ : ๋ชจ๋  ํด๋ผ์ด์ธํธ๋ค์๊ฒ "MyName" ์ด๋ผ๋ `์ฃผ์ `๋ก ์ด๋ฒคํธ๋ฅผ ๋ฐ์กํ๊ณ  ์ธ์๋ก 'Hello Client!'๋ฌธ์์ด๋ ๊ฐ์ด ์ ์กํฉ๋๋ค
```lua
Server.FireEvent("MyName", "Hello Client!")

-- ํด๋น ์ด๋ฒคํธ๋ฅผ ํด๋ผ์ด์ธํธ์์ ๋ฐ์ผ๋ ค๋ฉด
-- ์๋์ ๊ฐ์ ์ฝ๋๋ฅผ ์ฌ์ฉํด๋ณด์ธ์

Client.GetTopic("MyName").Add(function(name)
    print(name)
end)
```
