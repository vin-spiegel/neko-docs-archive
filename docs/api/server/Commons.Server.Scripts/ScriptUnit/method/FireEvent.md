---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>FireEvent</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->



## FireEvent(String, Object[])
ํด๋ผ์ด์ธํธ์๊ฒ ํด๋น ์ฃผ์ (Topic)๋ก ์ด๋ฒคํธ๋ฅผ ๋ฐ์์ํต๋๋ค.

#### ์ ์ธ
```cs
public void FireEvent(string topic, params object[] arguments)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.String|topic|๋ณด๋ผ ์ฃผ์ (Topic)|
|System.Object[]|arguments|ํจ๊ป ์ ์กํ  ์ธ์(Argument)๋ค|

#### ์์ 
```lua
-- ScriptServer.FireEvent() ์ ์ฌ์ฉ๋ฒ์ด ๊ฐ์ง๋ง
-- ํด๋น ๋ฉ์๋๋ ์ด ํ๋ ์ด์ด์๊ฒ๋ง ์ด๋ฒคํธ๋ฅผ ๋ณด๋ธ๋ค
```