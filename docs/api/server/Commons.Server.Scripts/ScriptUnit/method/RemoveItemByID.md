---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>RemoveItemByID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## RemoveItemByID(Int64, Int32, Boolean, Boolean, Boolean)
νλ μ΄μ΄ μ λμΌλ‘λΆν° μμ΄νμ μ κ±°ν©λλ€.

#### μ μΈ
```cs
public bool RemoveItemByID(long id, int count = 1, bool notify = true, bool atomic = false, bool equippedItemExclude = false)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int64|id|μ κ±°ν  μμ΄νμ ID.λ°μ΄ν° λ² μ΄μ€μ μμ΄νID κ° μλ μμ΄νλ§μ μ λν¬ ID μλλ€.|
|System.Int32|count|μ κ±°ν  μμ΄νμ κ°μ|
|System.Boolean|notify|μμ΄νμ μ κ±°νμλ κ³΅μ§λ₯Ό μ¬μ©ν  κ²μΈμ§λ₯Ό λνλλλ€.|
|System.Boolean|atomic|μ΄ μΈμκ° νμ±ν λμμ λ μ κ±°ν  μμ΄νμ κ°μλ³΄λ€ κ°μ§κ³  μλ μμ΄νμ κ°μκ° μ μΌλ©΄ falseλ₯Ό λ°ννκ³  ν¨μλ₯Ό μ’λ£ν©λλ€.|
|System.Boolean|equippedItemExclude|μ₯μ°© μ€μΈ μμ΄νμ μ κ±° λμμμ μ μΈν μ§λ₯Ό λνλλλ€.|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|	

#### μμ : μ λμ μΈλ²€ν λ¦¬μμ ID: 5 μΈ μμ΄νμ 1κ° μ κ±°ν©λλ€
```lua
unit.RemoveItem(5, 1)
```