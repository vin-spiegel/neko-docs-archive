---
layout: default
title: <font color="#2c84fa">❒</font> onRefreshStats
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->


# onRefreshStats
유닛이 스탯을 새로고침 했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function(unit: ScriptUnit)
[1] unit: 새로고침 한 유닛
```

## 선언
```cs
public ScriptEventPublisher onRefreshStats { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

## 예제 
유닛의 스탯이 갱신되었을 때 알림 표시
```lua
function onRefreshStats(unit)
    unit.SendCenterLabel("Refresh Stats")
end

Server.onRefreshStats.Add(onRefreshStats)
```