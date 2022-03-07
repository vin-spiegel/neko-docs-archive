---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>DropItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## DropItem(Int64, Int32)
유닛이 가지고있는 아이템을 땅에 떨어뜨립니다 (드랍합니다).

#### 선언
```cs
public void DropItem(long id, int count = 1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|id|제거할 아이템의 ID.데이터 베이스의 아이템ID 가 아닌 아이템만의 유니크 ID 입니다.|
|System.Int32|count|개수|

#### 예제
```lua
-- 유저 인벤토리에 있는 드랍 가능한 아이템 전부 드랍하기

local items = unit.player.GetItems()

for i = 1, #items do
    if items[i] ~= nil then
        unit.DropItem(items[i].id)
    end
end
```