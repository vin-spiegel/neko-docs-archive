---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>IsEquippedItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## IsEquippedItem(Int64)
유닛이 해당 아이템을 장착 중인지 알아냅니다.

#### 선언
```cs
public bool IsEquippedItem(long itemID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|itemID|아이템의 고유 ID (데이터 베이스의 ID 와는 다릅니다)|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|장착 여부 (장착 중일시: True, 아닐 시: False)|

#### 예제: 유닛의 인벤토리를 돌며 장착 중인 아이템 알려주기
```lua
local inven = unit.player.GetItems()

for i = 1, #inven do
    if inven[i] ~= nil then
        local itemData = Server.GetItem(inven[i].dataID)
        if unit.IsEquippedItem(inven[i].id) then
            unit.SendSay(i .. "." .. itemData.name .. ": 장착 중")
        else
            unit.SendSay(i .. "." .. itemData.name .. ": 미장착")
        end    
    end
end
```