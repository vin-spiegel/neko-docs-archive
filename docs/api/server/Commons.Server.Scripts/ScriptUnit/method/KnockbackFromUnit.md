---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>KnockbackFromUnit</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->


## KnockbackFromUnit(ScriptUnit, Single, Single)
์ ๋์๊ฒ ๋ฐ์น๊ธฐ(๋๋ฐฑ Knock-back)๋ฅผ ์ ์ฉํฉ๋๋ค.
(๋ฐ์น ๋์์ ์ ๋์ผ๋ก๋ถํฐ ๋ฉ์ด์ง๋๋ค)

#### ์ ์ธ
```cs
public void KnockbackFromUnit(ScriptUnit from, float distance, float time = 0.5F)
```

#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|ScriptUnit|from|๋ฐ์น ๋์|
|System.Single|distance|์ ์ฉ ๊ฑฐ๋ฆฌ|
|System.Single|time|์ ์ฉ ์๊ฐ (์งง์์๋ก ๋น ๋ฅด๊ฒ ๋ฐ์ด๋๋๋ค) (๊ธฐ๋ณธ๊ฐ: 0.5)|

#### ์์ : ๊ณต๊ฒฉํ ๋์ ๋๋ฅผ ๊ธฐ์ค์ผ๋ก ๋ฐ์น๊ธฐ
```lua
-- ํด๋น ์์ ๋ ๋ฐ๋ฏธ์ง ๊ณต์์์ ์ฌ์ฉ๋๋ ๊ณต์์ ์์ ๋ก ๋ค์์ต๋๋ค

-- ๋ฐฉ์ด์๋ฅผ ๊ณต๊ฒฉ์๋ก๋ถํฐ 0.5์ด๊ฐ 2์นธ ๋งํผ ๋ฐ์ด๋ธ๋ค
b.KnockbackFromUnit(a, 64, 0.5)
```