---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>MakeKnockback</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->



## MakeKnockback(Single, Single)
์ ๋์๊ฒ ๋ฐ์น๊ธฐ(๋๋ฐฑ Knock-back)๋ฅผ ์ ์ฉํฉ๋๋ค.

#### ์ ์ธ
```cs
public void MakeKnockback(float distance, float time)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Single|distance|์ ์ฉ ๊ฑฐ๋ฆฌ|
|System.Single|time|์ ์ฉ ์๊ฐ (์งง์์๋ก ๋น ๋ฅด๊ฒ ๋ฐ์ด๋๋๋ค)|

#### ์์ : ์ ๋์ 2์ด๊ฐ 64(2์นธ) ๋งํผ ๋๋ฐฑ์ํค๊ธฐ
```lua
unit.MakeKnockback(64, 2)
```