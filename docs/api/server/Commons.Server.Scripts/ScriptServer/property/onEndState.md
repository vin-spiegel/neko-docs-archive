---
layout: default
title: <font color="#2c84fa">❒</font> onEndState
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# onEndState
다른 State 실행 시, 기존 State가 종료될 때 호출되는 이벤트입니다. 

## 호출될 함수의 인자 형식
```lua
function(state)
```

[1] state: 해당 State의 번호

## 선언
```cs
public ScriptEventPublisher onEndState { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

## 예제
상태가 종료되었을 때 해당 상태가 종료되었음을 알려주기
```lua
function onEndState(state)
    Server.SendCenterLabel(state .. " 상태가 종료되었습니다")
end

Server.onEndState.Add(onEndState)
```