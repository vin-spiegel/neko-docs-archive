---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>AddDamageBy</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->


## AddDamageBy(ScriptUnit, Int32, Int32, Boolean)
์ด ์ ๋์๊ฒ ํผํด(๋ฐ๋ฏธ์ง)๋ฅผ ์ํ๋๋ค. (๋ฐ๋ฏธ์ง๋ฅผ ๋ฐ์ ๋์์ด ๋ชฌ์คํฐ์ผ ๊ฒฝ์ฐ ๋ณด์์ด ์ง๊ธ๋ฉ๋๋ค)

#### ์ ์ธ
```cs
public void AddDamageBy(ScriptUnit attacker, int damage, int skillDataID = -1, bool critical = false)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|ScriptUnit|attacker|๊ณต๊ฒฉ์|
|System.Int32|damage|ํผํด๋(๋ฐ๋ฏธ์ง)|
|System.Int32|skillDataID|์คํฌ์ ๊ณต์์ ์ฌ์ฉ์ ๊ณต์์ ์ ์ฉํ  ์คํฌ์ ID (๊ธฐ๋ณธ๊ฐ: -1(๊ณต์ ๋ฏธ์ ์ฉ))|
|System.Boolean|critical|์น๋ชํ(ํฌ๋ฆฌํฐ์ปฌ)์ ๋ฐ์ ์ ๋ฌด|