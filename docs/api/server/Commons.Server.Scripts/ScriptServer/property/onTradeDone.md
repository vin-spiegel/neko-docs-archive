---
layout: default
title: <font color="#2c84fa">❒</font> onTradeDone
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

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