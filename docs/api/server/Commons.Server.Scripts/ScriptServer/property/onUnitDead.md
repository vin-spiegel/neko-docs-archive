---
layout: default
title: <font color="#2c84fa">❒</font> onUnitDead
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## onUnitDead
유닛이 죽었을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식

```lua
function(target: ScriptUnit, attacker: ScriptUnit)
[1] target: 죽은 유닛
[2] attacker: 공격한 유닛 (nil 이면 자살)
```

#### 선언
```cs
public ScriptEventPublisher onUnitDead { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: PVP로 유저를 죽였을때, 서버 전체 메시지 출력 및 보상 지급
```lua
function onUnitDead(target, attacker)
    -- PlayerUnit 일 경우
    if target.type == 0 and attacker.type == 0 then
        Server.SendCenterLabel(target.name..'을(를) \n'..attacker.name..'이(가) 죽였다.')
        
        -- 공격자에게 100 골드을 준다
        attacker.AddGameMoney(100)

        -- 공격자에게 50% 확률로 1번 아이템을 준다
        if rand(1, 100) <= 50 then
            attacker.AddItem(1)
        end
    end
end

-- Server.onUnitDead에 onUnitDead함수를 추가한다.
Server.onUnitDead.Add(onUnitDead)
```