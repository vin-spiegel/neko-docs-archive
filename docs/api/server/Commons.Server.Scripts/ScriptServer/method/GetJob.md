---
layout: default
title: <font color="#2c84fa">π</font> GetJob
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetJob(Int32)
λ°μ΄ν°λ² μ΄μ€μ μ§μ μ λ³΄

#### μ μΈ
```cs
public TGameJob GetJob(int id)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|μ§μ ID|

### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|TGameJob|λ°μ΄ν°λ² μ΄μ€μ μ§μ μ λ³΄|

#### μμ : λ°μ΄ν°λ² μ΄μ€μ μμ±ν 5λ² μ§μ μ λ³΄ κ°μ Έμ€κΈ°
```lua
local myJob = Server.GetJob(5)
```
