---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>PlayME</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## PlayME(String, Single)
ν΄λΉ MEλ₯Ό μ¬μν©λλ€.

#### μ μΈ
```cs
public void PlayME(string meID, float volume = 1F)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.String|meID|ME μ΄λ¦|
|System.Single|volume|λ³Όλ₯¨|

#### μμ : μ λμκ² ME λ₯Ό μ¬μμν¨λ€
```lua
unit.PlayME("MyMusicFile.ogg", 1.0)
```