---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>PullFromUnit</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->

## PullFromUnit(ScriptUnit, Single, Single)
์ ๋์๊ฒ ๋น๊ธฐ๊ธฐ๋ฅผ ์ ์ฉํฉ๋๋ค.(๋น๊ธด ๋์ ์ ๋์๊ฒ ๋๋ ค๊ฐ๋๋ค)

#### ์ ์ธ
```cs
public void PullFromUnit(ScriptUnit from, float distance = 0F, float time = 0.5F)
```
#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|ScriptUnit|from|๋น๊ธด ๋์|
|System.Single|distance|๊ฐ๊ฒฉ (0 ์ผ๊ฒฝ์ฐ ์์ ํ ๋ด ์์น๊น์ง ๋น๊ฒจ์ง๋๋ค) (๊ธฐ๋ณธ๊ฐ: 0)|
|System.Single|time|์ ์ฉ ์๊ฐ (์งง์์๋ก ๋น ๋ฅด๊ฒ ๋น๊น๋๋ค) (๊ธฐ๋ณธ๊ฐ: 0.5)|

#### ์์ : ๊ณต๊ฒฉํ ๋์์ ๋๋ฅผ ๊ธฐ์ค์ผ๋ก ๋น๊ฒจ์ค๊ธฐ
```lua
-- ํด๋น ์์ ๋ ๋ฐ๋ฏธ์ง ๊ณต์์์ ์ฌ์ฉ๋๋ ๊ณต์์ ์์ ๋ก ๋ค์์ต๋๋ค

-- ๋ฐฉ์ด์๋ฅผ ๊ณต๊ฒฉ์ ์์น์์ 0์นธ ๋จ์ด์ง ๊ณณ๊น์ง 0.5์ด๊ฐ ๋น๊ฒจ์จ๋ค
b.PullFromUnit(a, 0, 0.5)
```