---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">๐ </font>SetStat</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- ์๋๋ก ํธ์ง -->


## SetStat(Int32, Single)
์ ๋์ ์คํฏ ๊ฐ์ ๋ณ๊ฒฝํฉ๋๋ค.

#### ์ ์ธ
```cs
public void SetStat(int type, float value)
```
#### ๋งค๊ฐ ๋ณ์(์ธ์)

|ํ์|์ด๋ฆ|์ค๋ช|
|:-|:-|:-|
|System.Int32|	type	|ํด๋น ์คํฏ()์ ํ์|
|System.Single|	value	|๋ณ๊ฒฝํ  ๊ฐ|

#### ์์ 
```lua
-- ATTACK = 0
-- DEFENSE = 1
-- MAGIC_ATTACK = 2
-- MAGIC_DEFENSE = 3
-- AGILITY = 4
-- LUCKY = 5
-- HP = 6
-- MP = 7

-- [์ฌ์ฉ์ ์ค์  ๋ฅ๋ ฅ์น (์ปค์คํ ์คํฏ)]

-- CUSTOM_1 = 101
-- ...
-- CUSTOM_32 = 132


-- HP๋ฅผ 999๋ก ์ค์ 
unit.SetStat(6, 999)

-- ATTACK์ 100์ผ๋ก ์ค์ 
unit.SetStat(0, 100)
```