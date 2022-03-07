---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">𝑓 </font>LeaveField</div>
nav_order: 1
parent: ScriptDropItem
grand_parent: Commons.Server.Scripts
---

## LeaveField()
해당 필드를 떠난다. (필드에서 아이템 삭제)

#### 선언
```cs
public void LeaveField()
```

#### 예제
```lua
-- 필드 내의 모든 드랍 아이템들을 필드에서 없앱니다
if unit.field ~= nil then
    return
end

local dropItems = unit.field.dropItems

if #dropItems <= 0 then
    unit.SendCenterLabel('떨어진 드랍 아이템이 없습니다')
    return    
end

local count = 0
for i = 1, #dropItems do
    if dropItems[i] ~= nil then
        dropItems[i].LeaveField()
        count = count + 1
    end
end

unit.SendCenterLabel(count .. '개의 드랍 아이템을 치웠습니다')
```