---
layout: default
title: <font color="#2c84fa">π</font> StartState
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## StartState(Int32, Single)
`time` μκ° νμ, νΉμ ν `state` λ₯Ό μ€νν©λλ€.

#### μ μΈ
```cs
public void StartState(int state, float time = 0F)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|state|state μ«μ|
|System.Single|time|μ€ν μκ°|

#### μμ : 5μ΄ λ€μ 7λ² Stateλ₯Ό μμ
```lua
-- Server.onStartState, Server.onEndState λ‘ μ°λν΄μ μ¬μ©

Server.StartState(7, 5)
```