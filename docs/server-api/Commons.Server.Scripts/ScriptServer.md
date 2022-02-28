---
layout: default
title: ScriptServer
nav_order: 16
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptServer 
Server 객체로 참조할 수 있는 클래스 입니다. 유저가 접속했을때, 떠났을때, 대화할때 등 모든 게임에 관련된 **이벤트 리스너**가 있습니다.

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ ScriptServer
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptServer : NekoEventListener
```

## 프로퍼티
---

## createClan
클랜이 생성되었을 때의 콜백 함수입니다. 

#### 콜백 함수의 형식

```lua
function(player: ScriptRoomPlayer, name: string, joinType: number)
```

|이름|타입|설명|
|:-|:-|:-|
|player|ScriptRoomPlayer|클랜을 만든 플레이어|
|name|string|클랜의 이름|
|joinType|number|클랜의 가입 형식 0: 즉시 가입, 1: 가입 요청, 2: 비공개|

#### 반환값

|타입|설명|
|:-|:-|
|boolean|클랜 생성이 성공했는지 (`true`: 클랜 생성 성공, `false`: 클랜 생성 실패)|

#### 선언
```cs
public Closure createClan { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제 1: `boolean` 값 반환을 이용한 클랜 생성 성공/실패 여부 결정
```lua
function createClan(player, clanName, joinType)
    local noticeText = player.name ' 님이 ' .. clanName .. '클랜을 창설했습니다!'
    Server.SendCenterLabel(noticeText)
    
    -- False 반환시 클랜 생성을 막는다
    return true
end

Server.createClan = createClan
```

#### 예제 2: 문자열 반환을 이용한 클랜 생성 실패 여부 보내주기
```lua
function createClan(player, clanName, joinType)
    local noticeText = player.name ' 님이 ' .. clanName .. '클랜을 창설했습니다!'
    Server.SendCenterLabel(noticeText)
    
    -- 아래와 같이 문자열을 반환하게 되면 클라이언트에 메시지 박스가 표시된다.
    return "Error: 클랜 생성에 실패했습니다"
end
Server.createClan = createClan
```

## damageCallback

유닛의 데미지 계산 공식 콜백 함수입니다. (데미지 공식을 커스텀 할 수 있습니다.) 

#### 콜백 함수의 형식 
```lua
function(from: ScriptUnit, to: ScriptUnit, damage: number, skillDataID: number)
```

|이름|타입|설명|
|:-|:-|:-|
|from|ScriptUnit|공격 유닛|
|to|ScriptUnit|대상 유닛|
|damage|number|공격의 데미지|
|skillDataID|number|스킬의 데이터 ID|

#### 반환값

|타입|설명|
|:-|:-|
|number|계산된 데미지|

#### 선언
```cs
public Closure damageCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 데미지를 입힐때 발생하는 이벤트 만들기
```lua
Server.damageCallback = function(a, b, damage, skillDataID, critical, visible)
    -- 데미지 계산 (공격자의 공격력 - 방어자의 방어력)
    damage = a.atk - b.def

    -- 데미지가 0일경우 데미지 표시를 출력하지 않음
    if damage <= 0  then
        visible = false
    end

    -- 데미지, 크리 여부, 폰트 출력 여부
    return damage, critical, visible
end
```

## fields
현재 게임에 생성된 모든 맵(필드)를 가져옵니다.

#### 선언
```cs
public ScriptField[] fields { get; }
```

#### 프로퍼티 값

|타입|설명|
|ScriptField[]|

## onAddItem
아이템이 추가되었을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식 
```lua
function(unit: ScriptUnit, item: TItem)
```

|이름|타입|설명|
|:-|:-|:-|
|unit|ScriptUnit|아이템이 추가된 유닛|
|item|TItem|추가된 아이템|

#### 선언
```cs
public ScriptEventPublisher onAddItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 아이템 획득 시 이벤트 추가하기
```lua
function onAddItem(unit, titem)
    print(scriptUnit.name)
    print(titem.dataID)
end

Server.onAddItem.Add(onAddItem)
```

## onBuyGameMoneyItem
유닛이 골드(게임 머니)로 아이템을 샀을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function(unit: ScriptUnit, itemID: number, count: number)
```
[1] unit: 아이템을 산 유닛
[2] itemID: 산 아이템의 ID
[3] count: 산 아이템의 개수

#### 선언
```cs
public ScriptEventPublisher onBuyGameMoneyItem { get; }
```

#### 프로퍼티 값
|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 플레이어가 아이템을 샀을 때 유닛의 이름, 아이템 ID, 갯수 출력하기
```lua
function onBuyGameMoneyItem(unit, itemID, count)
    print(string.format("%s, %s, %s", unit.name, itemID, count))
end

Server.onBuyGameMoneyItem.Add(onBuyGameMoneyItem)
```

## onBuyItem
유저가 큐브 결제로 게임 내 유료 아이템을 구매했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( player, itemID, amount, cashPrice)
```

[1] player: 구매한 플레이어
[2] itemID: 구매한 아이템의 ID
[3] amount: 구매한 아이템의 개수 
[4] cashPrice: 사용한 큐브의 개수

#### 선언
```cs
public ScriptEventPublisher onBuyItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 유저가 큐브 상품을 구매했을 때 유저의 화면에 "상품을 구매해주셔서 감사합니다!" 출력하기
```lua
function onBuyItem(player, itemID, amount)
    local numberItemID = tonumber(itemID)
    local itemData = Server.GetItem(numberItemID)
    
    if itemData ~= nil then
        player.unit.SendCenterLabel(player.name .. "님 [" .. itemData.name .. "] 상품을 구매해주셔서 감사합니다!")
    end
end

Server.onBuyItem.Add(onBuyItem)
```

## onEndState
다른 State 실행 시, 기존 State가 종료될 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function(state: number)
[1] state: 해당 State의 번호
```

#### 선언
```cs
public ScriptEventPublisher onEndState { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 상태가 종료되었을 때 해당 상태가 종료되었음을 알려주기
```lua
function onEndState(state)
    Server.SendCenterLabel(state .. " 상태가 종료되었습니다")
end

Server.onEndState.Add(onEndState)
```

## onJoinPlayer
게임에 플레이어가 들어왔을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( player)
[1] player: 접속한 플레이어
```

#### 선언
```cs
public ScriptEventPublisher onJoinPlayer { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 플레이어가 접속했을 때 그 유저에게 "Hello [유저이름]!" 출력하기
```lua
function onJoinPlayer(player)
    player.unit.SendCenterLabel("Hello " .. player.name .. "!")
end

Server.onJoinPlayer.Add(onJoinPlayer)
```

## onLeavePlayer
플레이어가 게임을 나갔을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( player)
[1] player: 나간 플레이어
```

#### 선언
```cs
public ScriptEventPublisher onLeavePlayer { get; }
```

#### 프로퍼티 값

|타입|설명|
|ScriptEventPublisher|

#### 예제: 플레이어가 나갔을 때 서버 전체에게 해당 유저가 나갔음을 알리기
```lua
-- Tip: 단 해당 함수는 네트워크 불안정 등의 요소를 고려해, 유저와의 연결이 끊긴 후 180초(3분) 뒤에 호출됩니다

function onLeavePlayer(player)
    Server.SendCenterLabel(player.name .. "님이 나갔습니다")
end

Server.onLeavePlayer.Add(onLeavePlayer)
```

## onPetUnitLevelUp
펫 유닛이 레벨 업 했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( unit, level)
[1] unit: 레벨 업한 펫 유닛
[2] level: 펫 레벨
```

#### 선언
```cs
public ScriptEventPublisher onPetUnitLevelUp { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 펫 레벨업시 메세지 출력
```lua
function onPetUnitLevelUp(pet, level)
    Server.SendCenterLabel("펫 " .. pet.name .. "이(가) " .. level .. "레벨이 되었습니다")
end

Server.onPetUnitLevelUp.Add(onPetUnitLevelUp)
```

## onRefreshStats
유닛이 스탯을 새로고침 했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function(unit: ScriptUnit)
[1] unit: 새로고침 한 유닛
```

#### 선언
```cs
public ScriptEventPublisher onRefreshStats { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 유닛의 스탯이 갱신되었을 때 알림 표시
```lua
function onRefreshStats(unit)
    unit.SendCenterLabel("Refresh Stats")
end

Server.onRefreshStats.Add(onRefreshStats)
```

## onRemoveItem
아이템이 제거되었을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( unit, item)
[1] unit: 아이템이 제거된 유닛
[2] item: 제거된 아이템
```

#### 선언
```cs
public ScriptEventPublisher onRemoveItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 아이템 제거시 이벤트
```lua
function onRemoveItem(scriptUnit, titem) 
    print(scriptUnit.name)
    print(titem.id)
    print(titem.dataID)
end

Server.onRemoveItem.Add(onRemoveItem)
```

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

## onSellGameMoneyItem
유닛이 골드(게임 머니) 아이템을 팔았을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( unit, itemID, count)
[1] unit: 아이템을 판 유닛
[2] itemID: 판 아이템의 ID
[3] count: 판 아이템의 개수
```

#### #### 선언
```cs
public ScriptEventPublisher onSellGameMoneyItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 플레이어가 아이템을 팔았을 때 유닛의 이름, 아이템 ID, 갯수 출력하기
```lua
function onSellGameMoneyItem(unit, itemID, count)
    print(string.format("%s, %s, %s", unit.name, itemID, count))
end

Server.onSellGameMoneyItem.Add(onSellGameMoneyItem)
```

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

#### onTick
매 프레임마다 호출되는 이벤트입니다. 호출될 함수의 인자 형식: function( dt)
[1] dt: Delta time

#### 선언
```cs
public ScriptEventPublisher onTick { get; }
```

#### 프로퍼티 값

|타입|설명|
|ScriptEventPublisher|

#### 예제: 매 프레임마다 채팅창에 "Tick! ([횟수])" 표시하기
```lua
-- Tip: onTick 이벤트는 호출 횟수가 많은 이벤트입니다
-- 이벤트 사용 횟수가 많아지거나, 내부 로직이 실행되는데 시간이 오래 걸린다면
-- 서버에 부하가 갈 수 있으므로 최적화를 한 후 사용해야 합니다.

count = 0
function onTick(deltaTime)
    Server.SendSay("Tick! (" .. count .. ")")
    count = count + 1
end

Server.onTick.Add(onTick)
```

## onTradeDone
거래가 정상적으로 완료 되었을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식 
```lua
function( sender, receiver, senderItems, receiverItems)
[1] sender: 거래를 시작한 유닛
[2] receiver: 거래를 받은 유닛
[3] senderItems: 거래를 시작한 유닛이 보낸 아이템 정보 TItem
[4] receiverItems: 거래를 받은 유닛이 보낸 아이템 정보 TItem
```

#### 선언
```cs
public ScriptEventPublisher onTradeDone { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 두 유저의 거래가 성공했을 때 채팅창에 출력하기
```lua
function onTradeDone(sender, receiver, senderItems, receiverItems)
    -- 거래를 진행한 두 유저의 정보 출력
    Server.SendSay("거래를 시작한 유닛 :" .. sender.name)
    Server.SendSay("거래를 수락한 유닛 :" .. receiver.name)
    
    -- 거래를 시작한 유닛이 보낸 아이템들을 출력
    Server.SendSay("시작한 유닛이 보낸 아이템")
    
    for i = 1, #senderItems do
        local itemData = Server.GetItem(senderItems[i].dataID)
        if itemData ~= nil then
            Server.SendSay(itemData.name)
        end
    end

    -- 거래를 수락한 유닛이 보낸 아이템들을 출력
    Server.SendSay("수락한 유닛이 보낸 아이템")
    
    for i = 1, #receiverItems do
        local itemData = Server.GetItem(receiverItems[i].dataID)
        if itemData ~= nil then
            Server.SendSay(itemData.name)
        end
    end
end

-- 이벤트에 등록
Server.onTradeDone.Add(onTradeDone)
```

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

## onUnitLevelUp
유닛이 레벨 업 했을 때 호출되는 이벤트입니다. 

#### 호출 될 함수의 인자 형식
```lua
function( unit)
[1] unit: 레벨 업 한 유닛
```

#### 선언
```cs
public ScriptEventPublisher onUnitLevelUp { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 플레이어가 특정 레벨에 도달했을 때 보상 지급
```lua
function onUnitLevelUp(target, level)
    -- 타겟이 50레벨을 달성했으면 서버 전체에 알림을 띄우고 1번 아이템을 지급한다.
    if target.level == 50 then
        Server.SendCenterLabel(target.name .. '님이 ' .. level .. '이 되었습니다!')
        target.AddItem(1)
    -- 55레벨을 달성했으면 5번스킬과 5000게임머니를 지급한다. 
    elseif target.level == 55 then
        target.AddSkill(5)
        target.AddGameMoney(5000)
    end
end
 
Server.onUnitLevelUp.Add(onUnitLevelUp)
```

## onUseItem
유닛이 아이템을 사용했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( unit, item)
[1] unit: 아이템을 사용한 유닛
[2] item: 사용한 아이템
```

#### 선언
```cs
public ScriptEventPublisher onUseItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 아이템 사용 시 아이템을 사용한 유저의 이름과 아이템 번호 출력하기
```lua
function onUseItem(unit, item)
    unit.SendCenterLabel(unit.name .. ": " .. item.dataID)
end

Server.onUseItem.Add(onUseItem)
```

## playerJoinPartyCallback
유닛이 파티에 참가할 때 호출되는 콜백 함수입니다. 

#### 콜백 함수의 형식
```lua
function( player, party)
반환값: 유닛이 파티에 참가되었는가 (True: 참가, False: 참가하지 못함)
[1] player: 참가할 유닛
[2] party: 참가할 파티
```

#### 선언
```cs
public Closure playerJoinPartyCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 파티 입장 때 발생하는 이벤트
```lua
Server.playerJoinPartyCallback = function(scriptRoomPlayer,scriptParty)
    print(scriptRoomPlayer.unit.name)
    print(scriptParty.maxPlayer)

    -- true 를 반환 시, 파티에 입장됩니다
    -- 조건에 따라서 true/false를 이용해 파티 입장을 막을 수 있습니다
    return true
end
```

## playerLeavePartyCallback
유닛이 파티에서 나갈 때 호출되는 콜백 함수입니다. 

#### 콜백 함수의 형식
```lua
function( player, party)
반환값: 없음
[1] player: 파티에서 나갈 유닛
[2] party: 나갈 파티
```

#### 선언
```cs
public Closure playerLeavePartyCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 파티를 나갈 때 발생하는 이벤트

```lua
Server.playerLeavePartyCallback = function(scriptRoomPlayer,scriptParty)
    print(scriptRoomPlayer.unit.name)
    print(scriptParty.maxPlayer)
end
```

## players
현재 게임에 접속한 players들을 가져옵니다.

#### 선언
```cs
public ScriptRoomPlayer[] players { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptRoomPlayer[]|

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

## sayCallback
플레이어가 말했을 때의 콜백 함수입니다. 

#### 콜백 함수의 형식
```lua
function( player, text)
반환값: 플레이어가 말한 내용이 적용 되는지 (True: 대사 적용, False: 대사 무시)
[1] player: 말한 플레이어
[2] text: 플레이어가 말한 대사
```

#### 선언
```cs
public Closure sayCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제 1: 금지어 필터링 예제
```lua
function badwordFillter(player, text)
    if string.contains(text, "금지어") then
        player.unit.SendCenterLabel("금지어는 사용하실 수 없습니다.")
        return false
    else
        return true    
    end
end

Server.sayCallback = badwordFillter
```
#### 예제 2: "#hi" 라고 입력하면 서버의 모든 유저들에게 인삿말 표시
```lua
function customCommand(player, text)
    if text == "#hi" then
        Server.SendCenterLabel(player.name .. ": 안녕!")
        return false
    end

    return true
end

Server.sayCallback = customCommand
```

## 함수
---

## CreateDropItem(Int32, Int32, Int32)
드랍 아이템 생성

#### 선언
```cs
public ScriptDropItem CreateDropItem(int dataID, int count, int level = 0)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|아이템 데이터 ID|
|System.Int32|count|개수|
|System.Int32|level|아이템 레벨 (기본: 0)|

#### 반환

|타입|설명|
|:-|:-|
|ScriptDropItem|

#### 예제
```lua
-- Tip: 생성한 드랍 아이템은 필드에 추가시켜야 주울 수 있습니다

-- 획득하면 5번 아이템을 3개 가질 수 있는 드랍 아이템을 생성합니다
local myDropItem = Server.CreateDropItem(5, 3)

-- 현재 내 유닛이 있는 필드의 2칸 위에 드랍 아이템 추가
unit.field.JoinDropItem(myDropItem, Point(unit.x, unit.y + 64))

-- 바로 유닛한테 줍게 하기
myDropItem.Acquire(unit)
```

## CreateEventUnit(String, String)
특정한 이름을 가진 EventUnit을 생성합니다.
**사용되지 않는 함수입니다. 추후에 개편될 수 있습니다**

#### 선언
```cs
public ScriptUnit CreateEventUnit(string name, string characterImageID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|name|이름|
|System.String|characterImageID|이미지 ID|

|반환|
|:-|:-|
|타입|설명|
|ScriptUnit|

## CreateField(Int32)
특정 맵 ID의 필드를 임시로 생성합니다.

#### 선언
```cs
public ScriptField CreateField(int mapID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|mapID|생성할 맵 데이터 ID|

#### 반환

|타입|설명|
|:-|:-|
|ScriptField|

#### 예제: 5번 맵의 임시 필드를 생성합니다
```lua
local myField = Server.CreateField(5)
```

## CreateItem(Int32, Int32)
아이템 생성

#### 선언
```cs
public TItem CreateItem(int dataID, int count)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스 ID|
|System.Int32|count|개수|

#### 반환

|타입|설명|
|:-|:-|
|TItem|

#### 예제: 5번 아이템을 3개 생성 후 유닛에게 추가하기
```lua
local myItem = Server.CreateItem(5, 3)
unit.AddItemByTItem(myItem)
```

## CreateParty(String, Int32)
파티 생성

#### 선언
```cs
public ScriptParty CreateParty(string name = "", int maxPlayer = 4)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|name|파티의 이름|
|System.Int32|maxPlayer|파티의 최대 플레이어 수 (기본: 4명, 최대: 4명)|

#### 반환

|타입|설명|
|:-|:-|
|ScriptParty|파티 정보|

#### 예제: 최대 인원이 4명인 새 파티를 생성합니다
```lua
local myParty = Server.CreateParty("Nekoland Party!", 4)
```

## ExportAverage()
스크립트 작동 시간 측정 경로는 해당 프로젝트이며 `ScriptPlayTimeAverage.txt` 의 이름으로 나옵니다. 테스트 플레이에서만 사용가능합니다.

#### 선언
```cs
public void ExportAverage()
```

## FireEvent(String, Object[])
클라이언트로 topic에 대해 이벤트를 보냅니다.

#### 선언
```cs
public void FireEvent(string topic, params object[] arguments)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|topic|보낼 topic id|
|System.Object[]|arguments|함께보낼 인자들|

### 예제: 모든 클라이언트들에게 "MyName" 이라는 `주제`로 이벤트를 발송하고 인자로 'Hello Client!'문자열도 같이 전송합니다
```lua
Server.FireEvent("MyName", "Hello Client!")

-- 해당 이벤트를 클라이언트에서 받으려면
-- 아래와 같은 코드를 사용해보세요

Client.GetTopic("MyName").Add(function(name)
    print(name)
end)
```

## GetAnimation(Int32)
데이터베이스의 애니메이션 정보

#### 선언
```cs
public TGameAnimation GetAnimation(int id)`
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|애니메이션 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameAnimation|데이터베이스의 애니메이션 정보|

#### 예제: 데이터베이스에 작성한 5번 애니메이션 정보 가져오기
```lua
local myAni = Server.GetAnimation(5)
```

## GetBuff(Int32)
데이터베이스의 상태(버프) 정보

#### 선언
```cs
public TGameBuff GetBuff(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|상태(버프)ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameBuff|데이터베이스의 상태 정보|

#### 예제: 데이터베이스에 작성한 5번 상태(버프) 정보 가져오기
```lua
local myBuff = Server.GetBuff(5)
```

## GetCharacter(Int32)
데이터베이스의 캐릭터정보

#### 선언
```cs
public TGameCharacter GetCharacter(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|캐릭터 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameCharacter|데이터베이스 캐릭터 정보|

#### 예제: 데이터베이스에 작성한 5번 캐릭터 정보 가져오기
```lua
local myCh = Server.GetCharacter(5)
```

## GetClanRankings(Int32, Boolean, Boolean)
{: .d-inline-block }

New
{: .label .label-green }

#### 선언
```cs
public ScriptRankingRow[] GetClanRankings(int type, bool weekly, bool desc)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|type|
|System.Boolean|weekly|
|System.Boolean|desc|

#### 반환

|타입|설명|
|:-|:-|
|ScriptRankingRow[]|

#### GetCommonEvent(Int32)
데이터베이스의 공용이벤트정보

#### 선언
```cs
public TGameCommonEvent GetCommonEvent(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|이벤트 ID|

#### 반환    

|타입|설명|
|:-|:-|
|TGameCommonEvent|공용이벤트정보|

#### 예제: 데이터베이스에 작성한 5번 공용 이벤트 정보 가져오기
```lua
local myComEvent = Server.GetCommonEvent(5)
```

## GetField(Int32, Int32)
특정 맵 ID의 필드를 가져옵니다.

#### 선언
```cs
public ScriptField GetField(int mapID, int channelID = -1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|mapID|가져올 맵 데이터 ID|
|System.Int32|channelID|채널 ID|

#### 반환

|타입|설명|
|:-|:-|
|ScriptField|

#### 예제: 5번 맵의 필드를 가져옵니다
```lua
local myField = Server.GetField(5)
```

## GetItem(Int32)
데이터베이스의 아이템 정보

#### 선언
```cs
public TGameItem GetItem(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|아이템 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameItem|데이터베이스 아이템 정보|

#### 예제: 데이터베이스에 작성한 5번 아이템 정보 가져오기
```lua
local myItem = Server.GetItem(5)
```

## GetJob(Int32)
데이터베이스의 직업 정보

#### 선언
```cs
public TGameJob GetJob(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|직업 ID|

### 반환

|타입|설명|
|:-|:-|
|TGameJob|데이터베이스의 직업 정보|

#### 예제: 데이터베이스에 작성한 5번 직업 정보 가져오기
```lua
local myJob = Server.GetJob(5)
```

## GetMap(Int32, TGameMapStub)
맵 데이터 정보

#### 선언
```cs
public TGameMapStub GetMap(int id, TGameMapStub parent = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|맵 iD|
|TGameMapStub|parent|기본 null 선택된 맵의 부모|

#### 반환

|타입|설명|
|:-|:-|
|TGameMapStub|맵 데이터 정보|

#### 예제: 5번 ID를 가진 맵의 정보를 가져오기
```lua
-- PC 또는 모바일 스튜디오 맵 편집기에서 #00 형식으로 나오는 것이 맵의 ID입니다

local myMap = Server.GetMap(5)
```

## GetMonster(Int32)
데이터베이스의 몬스터 정보

#### 선언
```cs
public TGameMonster GetMonster(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|몬스터 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameMonster|데이터베이스의 몬스터 정보|

#### 예제: 데이터베이스에 작성한 5번 몬스터 정보 가져오기
```lua
local myMonster = Server.GetMonster(5)
```

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

## GetPetAI(Int32)
펫 AI를 가져온다.

#### 선언
```cs
public Closure GetPetAI(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|펫 ID|

### 반환

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 0번 펫의 AI 함수 가져오기
```lua
local aiFunc = Server.GetPetAI(0)
```

#### GetRankings(Int32, Boolean, Boolean)
{: .d-inline-block }

New
{: .label .label-green }

#### 선언
```cs
public ScriptRankingRow[] GetRankings(int type, bool weekly, bool desc)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|type|
|System.Boolean|weekly|
|System.Boolean|desc|

#### 반환

|타입|설명|
|:-|:-|
|ScriptRankingRow[]|

## GetSkill(Int32)
데이터베이스의 스킬 정보

#### 선언
```cs
public TGameSkill GetSkill(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameSkill|데이터베이스의 스킬 정보|

#### 예제: 데이터베이스에 작성한 5번 스킬 정보 가져오기
```lua
local mySkill = Server.GetSkill(5)
```

## GetStrings()
데이터베이스 시스템 글자정보

#### 선언
```cs
public TGameStrings GetStrings()
```

#### 반환

|타입|설명|
|:-|:-|
|TGameStrings|데이터베이스 시스템 글자정보|

#### 예제: 데이터베이스 시스템에 작성한 용어 정보 가져오기
```lua
local myStrings = Server.GetStrings()
```

## GetTileset(Int32)
데이터베이스의 타일셋 정보

#### 선언
```cs
public TGameTileset GetTileset(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|타일셋 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameTileset|데이터베이스의 타일셋 정보|

#### 예제: 데이터베이스에 작성한 5번 타일셋 정보 가져오기
```lua
local myTileset = Server.GetTileset(5)
```

## GetTopic(String)
특정 topic에 대한 이벤트 콜백을 가져옵니다. 클라이언트에서 보낸 topic 이벤트를 처리합니다.

#### 선언
```cs
public ScriptEventPublisher GetTopic(string topic)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|topic|보낼 topic id|

#### 반환

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제 
```lua
-- 클라이언트에서 "Apple" 이란 주제로 FireEvent를 발송했을 때
-- 모든 클라이언트들에게 "Apple" 이란 메시지 표시하기

Server.GetTopic("Apple").Add(function()
    Server.SendCenterLabel("Apple")
end)

-- 클라이언트에서 "MyName" 이란 주제로 FireEvent를 발송했을 때
-- 모든 클라이언트들에게 같이 받은 인자 메시지를 표시하기

-- 클라이언트에서: Client.FireEvent("MyName", "Hello Server!")
-- 실행 시 출력: Hello Server!

Server.GetTopic("MyName").Add(function(name)
    Server.SendCenterLabel(name)
end)
```

## GetWorldStringVar(Int32)
월드 변수 값을 가져온다.

#### 선언
```cs
public string GetWorldStringVar(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.String|

#### 예제: 4번 월드 문자열 변수의 값 출력
```lua
local v = Server.GetWorldStringVar(4)
Server.SendCenterLabel("4번 월드 문자열 변수의 값: " .. v)
```

## GetWorldVar(Int32)
월드 변수 값을 가져온다.

#### 선언
```cs
public long GetWorldVar(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int64|

#### 예제: 4번 월드 변수의 값 출력하기
```lua
local v = Server.GetWorldVar(4)

Server.SendCenterLabel('4번 월드 변수의 값: ' .. v)
```

## HttpGet(String, Closure)
Http GET 요청을 보내고, 데이터를 가져온다.

#### 선언
```cs
public bool HttpGet(string url, Closure callback)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|url|url|
|MoonSharp.Interpreter.Closure|callback|가져온 데이터 처리 콜백|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제: Http GET 을 이용해서 웹 페이지에서 데이터를 받아오기
```lua
Server.HttpGet('http://nekoland.net/', function (res)
    print(res)
end)
```

## HttpPost(String, Table, Closure)
Http POST 요청을 보내고, 데이터를 가져온다.

#### 선언
```cs
public bool HttpPost(string url, Table data, Closure callback)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|url|url|
|MoonSharp.Interpreter.Table|data|루아 Table 형식 데이터|
|MoonSharp.Interpreter.Closure|callback|가져온 데이터 처리 콜백|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제: t 라는 테이블을 만들고, 보낼 POST 요청 데이터 넣기
```lua
local t = {}
t.id = 1234
t.name = "Hello"

-- http://naver.com URL로 요청 보내고, res로 데이터 받기
Server.HttpGet('http://naver.com', t, function(res)
  print(res) -- 웹페이지가 반환한 결과 텍스트가 출력됩니다.
end)

-- 웹 서버에서 데이터 받기

-- POST로 요청을 받을 경우, 아래와 같이 데이터를 출력할 수 있습니다.
-- 이 데이터를 MySQL과 같은 데이터베이스에 넣어, 영구보관할 수 있습니다.

<?php
echo $_POST["id"];
echo $_POST["name"];

echo "잘 받았습니다!";
?>

-- Server.HttpGet 에서 보낸 데이터가 웹 서버에 잘 도착하였는지를 확인하기 위한 코드입니다. 
-- 위 서버 스크립트 예재의 print(res) 에 의해 “1234Hello잘 받았습니다!” 가 출력됩니다.
```

## RunLater(Closure, Single)
t 초 후에, callback 함수를 실행합니다.

#### 선언
```cs
public void RunLater(Closure callback, float t)
```

#### 매개 변수(인자)

|타입|이름|설명|
|MoonSharp.Interpreter.Closure|callback|실행할 함수|
|System.Single|t|실행까지 대기시간 (초)|

#### 예제: 5초 뒤에 모든 클라이언트들에게 메시지를 전송하기
```lua
Server.RunLater(function()
    Server.SendCenterLabel('5초 지남!')
end, 5)
```

## SendCenterLabel(String)
가운데에 문자열을 표시합니다.

#### 선언
```cs
public void SendCenterLabel(string text)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|표시할 문자열|

#### 예제: 현재 내 게임에 접속한 모든 플레이어들의 화면에 "Hello Nekoland!" 문자열 표시하기
```lua
Server.SendCenterLabel("Hello Nekoland!")
```

## SendSay(String, UInt32)
채팅창에 메세지를 표시합니다.

#### 선언
```cs
public void SendSay(string text, uint color = 4294967295U)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|표시할 메세지|
|System.UInt32|color|색깔|

#### 예제: 게임 채팅창에 "Hello Nekoland!" 메시지를 표시합니다
```lua
Server.SendSay("Hello Nekoland!")
```

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

## SetWorldStringVar(Int32, String)
월드 변수 값을 설정한다.

#### 선언
```cs
public void SetWorldStringVar(int id, string value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.String|value|값|

#### 예제: 4번 월드 문자열 변수에 "Hello Nekoland!" 문자열 저장
```lua
Server.SetWorldStringVar(4, "Hello Nekoland!")
```

## SetWorldVar(Int32, Int64)
월드 변수 값을 설정한다.

#### 선언
```cs
public void SetWorldVar(int id, long value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.Int64|value|값|

#### 예제: 4번 월드 변수를 7로 설정
```lua
Server.SetWorldVar(4, 7)
```

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