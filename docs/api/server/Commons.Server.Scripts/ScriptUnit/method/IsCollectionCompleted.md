---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>IsCollectionCompleted</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## IsCollectionCompleted(Int32)
μ λμ΄ ν΄λΉ λκ°μ μμλ₯Ό μλ£νλμ§λ₯Ό λ°νν©λλ€.

#### μ μΈ
```cs
public bool IsCollectionCompleted(int collectionDataID)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|collectionDataID|λ°μ΄ν°λ² μ΄μ€μ λκ° ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|μλ£ μ¬λΆ (μλ£: True, λ―Έμλ£: False)|

#### μμ : 5λ² λκ°μ΄ μμ±λμλμΉ μΆλ ₯νκΈ°
```lua
if unit.IsCollectionCompleted(5) then
    unit.SendCenterLabel("5λ² λκ°μ΄ μμ±λμ΄ μμ")
else
    unit.SendCenterLabel("5λ² λκ°μ΄ λ―Έμμ±")
end
```