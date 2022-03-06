---
layout: default
title: <font color="#2c84fa">❒ </font>onStartState
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->


## onStartState
특정 State를 실행했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( state)
[1] state: 해당 State의 번호
```

#### 선언
```cs
public ScriptEventPublisher onStartState { get; }
```

#### 프로퍼티 값

|타입|설명|
|ScriptEventPublisher|

#### 예제: 새 상태가 시작되었을 때 해당 상태가 시작되었음을 알려주기
```lua
function onStartState(state)
    Server.SendCenterLabel(state .. " 상태가 시작되었습니다")
end

Server.onStartState.Add(onStartState)
```
