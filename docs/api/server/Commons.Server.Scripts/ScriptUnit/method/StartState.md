---
layout: default
title: <font color="#2c84fa">𝑓</font> StartState
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## StartState(Int32, Single)
`time` 시간 후에, 특정한 `state` 를 실행합니다.

#### 선언
```cs
public void StartState(int state, float time = 0F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|state|state 숫자|
|System.Single|time|실행 시간|

#### 예제: 5초 뒤에 7번 State를 시작
```lua
-- Server.onStartState, Server.onEndState 로 연동해서 사용

Server.StartState(7, 5)
```