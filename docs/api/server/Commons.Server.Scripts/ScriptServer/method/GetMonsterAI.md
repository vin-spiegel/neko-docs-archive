---
layout: default
title: <font color="#2c84fa">𝑓</font> GetMonsterAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetMonsterAI(Int32)
몬스터 AI를 가져온다.

#### 선언
```cs
public Closure GetMonsterAI(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|몬스터의 ID|

#### 반환

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 0번 몬스터의 AI 함수 가져오기
```lua
local aiFunc = Server.GetMonsterAI(0)
```