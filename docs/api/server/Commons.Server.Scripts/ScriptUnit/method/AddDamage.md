---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>AddDamage</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


# AddDamage(Int32, Int32, Boolean)
μ΄ μ λμκ² νΌν΄(λ°λ―Έμ§)λ₯Ό μνλλ€. (κ³΅κ²©μκ° μ‘΄μ¬νμ§ μκΈ° λλ¬Έμ λ³΄μμ΄ μ§κΈλμ§ μμ΅λλ€)

#### μ μΈ
```cs
public void AddDamage(int damage, int skillDataID = -1, bool critical = false)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|damage|νΌν΄λ(λ°λ―Έμ§)|
|System.Int32|skillDataID|μ€ν¬μ κ³΅μμ μ¬μ©μ κ³΅μμ μ μ©ν  μ€ν¬μ ID (κΈ°λ³Έκ°: -1(κ³΅μ λ―Έμ μ©))|
|System.Boolean|critical|μΉλͺν(ν¬λ¦¬ν°μ»¬)μ λ°μ μ λ¬΄|

#### μμ : μ λμκ² λ°λ―Έμ§ 999λ₯Ό μνλλ€
```lua
unit.AddDamage(999)
```