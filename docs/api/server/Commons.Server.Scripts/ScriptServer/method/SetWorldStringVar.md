---
layout: default
title: <font color="#2c84fa">π </font>SetWorldStringVar
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## SetWorldStringVar(Int32, String)
μλ λ³μ κ°μ μ€μ νλ€.

#### μ μΈ
```cs
public void SetWorldStringVar(int id, string value)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|λ³μ ID|
|System.String|value|κ°|

#### μμ : 4λ² μλ λ¬Έμμ΄ λ³μμ "Hello Nekoland!" λ¬Έμμ΄ μ μ₯
```lua
Server.SetWorldStringVar(4, "Hello Nekoland!")
```
