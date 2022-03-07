---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetEquipItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## GetEquipItem(Int32)
해당 슬롯에 장착되어있는 아이템의 정보를 가져옵니다.

#### 선언
```cs
public TItem GetEquipItem(int equipSlot)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|equipSlot|장착 슬롯 (0 ~ 9)|

#### 반환
|타입|설명|
|:-|:-|
|TItem|형식의 아이템 정보|

#### 예제: 유닛이 장착중인 모자의 이름 출력하기
```lua
local item = unit.GetEquipItem(0)

if item ~= nil then
    local itemData = Server.GetItem(item.dataID)
    unit.SendCenterLabel(itemData.name)
else
    unit.SendCenterLabel("모자가 장착되지 않았습니다")
end
```