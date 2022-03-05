---
layout: default
title: <font color="#2c84fa">❒</font> rewardCallback
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## rewardCallback
몬스터가 죽었을 때의 커스텀 보상 공식 콜백 함수입니다. 

#### 콜백 함수의 형식
```lua
function( unit, monster, damage)
반환값: 없음
[1] unit: 몬스터를 죽인 유닛
[2] monster: 죽은 몬스터 유닛
[3] damage: 입힌 데미지
```

#### 선언
```cs
public Closure rewardCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 몬스터가 죽었을 때 몬스터를 죽인 유저에게 알림 표시, 1번 아이템 1개 지급
```lua
function rewardCallback(killer, monster, damage)
    killer.SendCenterLabel(monster.name .. " 몬스터를 처치했습니다. 입힌 데미지" .. damage)    
    killer.AddItem(1, 1)    
end

Server.rewardCallback = rewardCallback
```