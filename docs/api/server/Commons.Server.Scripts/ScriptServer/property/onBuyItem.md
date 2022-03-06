---
layout: default
title: <font color="#2c84fa">❒</font> onBuyItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# onBuyItem
유저가 큐브 결제로 게임 내 유료 아이템을 구매했을 때 호출되는 이벤트입니다. 

## 호출될 함수의 인자 형식
```lua
function(player, itemID, amount, cashPrice)
```
|이름|타입|설명|
|:-|:-|:-|
|player|ScriptRoomPlayer|구매한 플레이어|
|itemID|number|구매한 아이템의 ID|
|amount|number|구매한 아이템의 개수|
|cashPrice|number|사용한 큐브의 개수|

## 선언
```cs
public ScriptEventPublisher onBuyItem { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

## 예제
유저가 큐브 상품을 구매했을 때 유저의 화면에 "상품을 구매해주셔서 감사합니다!" 출력하기
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