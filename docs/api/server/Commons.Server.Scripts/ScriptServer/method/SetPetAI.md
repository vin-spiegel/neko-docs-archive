---
layout: default
title: <font color="#2c84fa">𝑓 </font>SetPetAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SetPetAI(Int32, Closure)
펫 AI를 등록한다.

#### 선언
```cs
public void SetPetAI(int id, Closure c)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|펫 ID|
|MoonSharp.Interpreter.Closure|c|AI 함수|

#### 예제: 0번 펫의 AI 설정
```lua
Server.SetPetAI(0,
    function(pet, ai, event, data)
        -- 여기에 AI 코드를 삽입합니다
    end)
```