---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>AddPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->



## AddPet(Int32, Int32, String)
์ ๊ท ํซ์ ์ถ๊ฐ ๋ฑ๋กํ๊ณ  ๋ฑ๋ก๋ ID๋ฅผ ๊ฐ์ ธ์ต๋๋ค. 
- ๋ฑ๋ก์ด ์คํจํ  ๊ฒฝ์ฐ `-1`์ ๋ฆฌํดํฉ๋๋ค.

#### ์ ์ธ
```cs
public int AddPet(int characterID = 0, int jobID = 0, string name = null)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|characterID|ํซ์ ์บ๋ฆญํฐ ID (๊ธฐ๋ณธ๊ฐ: 0)|
|System.Int32|jobID|ํซ์ ์ง์ ID (๊ธฐ๋ณธ๊ฐ: 0)|
|System.String|name|ํซ์ ์ด๋ฆ (๊ธฐ๋ณธ๊ฐ: ํซ ์บ๋ฆญํฐ์ ์ด๋ฆ)|

#### ๋ฐํ
|ํ์|์ค๋ช|
|:-|:-|
|System.Int32|๋ฑ๋ก๋ ํซ์ ID(๋ฑ๋ก ์คํจ์ -1)|