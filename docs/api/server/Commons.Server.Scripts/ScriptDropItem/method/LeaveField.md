---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">π </font>LeaveField</div>
nav_order: 1
parent: ScriptDropItem
grand_parent: Commons.Server.Scripts
---

## LeaveField()
ν΄λΉ νλλ₯Ό λ λλ€. (νλμμ μμ΄ν μ­μ )

#### μ μΈ
```cs
public void LeaveField()
```

#### μμ 
```lua
-- νλ λ΄μ λͺ¨λ  λλ μμ΄νλ€μ νλμμ μμ±λλ€
if unit.field ~= nil then
    return
end

local dropItems = unit.field.dropItems

if #dropItems <= 0 then
    unit.SendCenterLabel('λ¨μ΄μ§ λλ μμ΄νμ΄ μμ΅λλ€')
    return    
end

local count = 0
for i = 1, #dropItems do
    if dropItems[i] ~= nil then
        dropItems[i].LeaveField()
        count = count + 1
    end
end

unit.SendCenterLabel(count .. 'κ°μ λλ μμ΄νμ μΉμ μ΅λλ€')
```