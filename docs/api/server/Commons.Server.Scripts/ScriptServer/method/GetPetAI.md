---
layout: default
title: <font color="#2c84fa">𝑓</font> GetPetAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## GetPetAI(Int32)
펫 AI를 가져온다.

#### 선언
```cs
public Closure GetPetAI(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|펫 ID|

### 반환

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 0번 펫의 AI 함수 가져오기
```lua
local aiFunc = Server.GetPetAI(0)
```