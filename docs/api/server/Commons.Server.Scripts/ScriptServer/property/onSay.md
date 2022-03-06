---
layout: default
title: <font color="#2c84fa">❒</font> onSay
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## onSay
플레이어가 말했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( unit, text)
[1] unit: 말한 플레이어
[2] text: 플레이어가 말한 내용
```

### 선언
```cs
public ScriptEventPublisher onSay { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 유저가 말했을때, 말한 내용 중 "Hello" 라는 내용이 포함되어있다면 "Hello!" 라고 표시해주기
```lua
function onSay(unit, text)
    if string.match(text, "Hello") then
        unit.SendCenterLabel("Hello!")
    end
end

Server.onSay.Add(onSay)
```