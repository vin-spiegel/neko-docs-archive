---
layout: default
title: <font color="#2c84fa">𝑓</font> SetMonsterAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SetMonsterAI(Int32, Closure)
몬스터 AI를 등록한다. 몬스터의 ID 를 이용해, 해당 몬스터의 AI를 등록한다.

#### 선언
```cs
public void SetMonsterAI(int id, Closure c)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|몬스터의 ID|
|MoonSharp.Interpreter.Closure|c|AI 함수|

#### 예제: 0번 몬스터의 AI 설정
```lua
Server.SetMonsterAI(0,
    function(monster, ai, event, data)
        -- 여기에 AI 코드를 삽입합니다
    end)
```