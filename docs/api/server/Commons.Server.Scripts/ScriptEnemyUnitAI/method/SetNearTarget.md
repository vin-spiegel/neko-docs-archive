---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">π </font>SetNearTarget</div>
nav_order: 1
parent: ScriptEnemyUnitAI
grand_parent: Commons.Server.Scripts
---

## SetNearTarget(Int32, Single)
νμ¬ λͺ¬μ€ν°κ° μλ λ§΅μμ κ°μ₯ κ°κΉμ΄ μ λμ νκ²μΌλ‘ μ§μ νλ€.

#### μ μΈ
```cs
public void SetNearTarget(int findType = -1, float dist = 200F)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|findType|νμν  μ λ νμ 0 : νλ μ΄μ΄, 1 : μ΄λ²€νΈ μ λ , 2 : μ |
|System.Single|dist|νμν  μ λ κ±°λ¦¬ (κΈ°λ³Έκ°: 200)|