---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>PlaySE</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## PlaySE(String, Single)
ν΄λΉ SEλ₯Ό μ¬μν©λλ€.

#### μ μΈ
```cs
public void PlaySE(string seName, float volume = 1F)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.String|seName|SE μ΄λ¦|
|System.Single|volume|λ³Όλ₯¨|

#### μμ : μ λμκ² SE λ₯Ό μ¬μμν¨λ€
```lua
unit.PlaySE("MyMusicFile.ogg", 1.0)
```