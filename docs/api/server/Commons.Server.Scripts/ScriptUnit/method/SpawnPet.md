---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>SpawnPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## SpawnPet(Int32, Single, Single, Int32, Int32, String)
ν«μ μνν©λλ€. 
- κ°μ IDλ‘ μ΄λ―Έ μνλμλ κ²½μ° ν΄λΉ ν«μ μ λ³΄λ‘ μνλ©λλ€.
- μνλμλ μ΄λ ₯μ΄ μλ κ²½μ° ν΄λΉ IDλ‘ λ±λ‘ ν μνλ©λλ€.

#### μ μΈ
```cs
public bool SpawnPet(int petID, float posX, float posY, int characterID = 0, int jobID = 0, string name = null)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|petID|μνν  ν«μ ID|
|System.Single|posX|μνν  μμΉμ X μ’ν|
|System.Single|posY|μνν  μμΉμ Y μ’ν|
|System.Int32|characterID|μ κ· λ±λ‘μ ν«μ μΊλ¦­ν° ID (κΈ°λ³Έκ°: 0)|
|System.Int32|jobID|μ κ· λ±λ‘μ ν«μ μ§μ ID (κΈ°λ³Έκ°: 0)|
|System.String|name|μ κ· λ±λ‘μ ν«μ μ΄λ¦ (κΈ°λ³Έκ°: ν« μΊλ¦­ν°μ μ΄λ¦)|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|ν« μν μ±κ³΅μ¬λΆ(μ±κ³΅: True, μ€ν¨: False)|
