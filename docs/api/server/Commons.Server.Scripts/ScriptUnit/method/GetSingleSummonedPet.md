---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetSingleSummonedPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## GetSingleSummonedPet()
현재 소환 중인 펫을 가져옵니다.

#### 선언
```cs
public ScriptPetUnit GetSingleSummonedPet()
```
#### 반환

|타입|설명|
|:-|:-|
|ScriptPetUnit|펫 유닛을 형식으로 반환합니다.|

#### 예제: 현재 소환되어있는 펫 유닛을 가져와 이름 출력
```lua
local myPet = unit.GetSingleSummonedPet()

if myPet == nil then
    unit.SendCenterLabel("소환된 펫이 없습니다")
    return
end

unit.SendCenterLabel("현재 소환된 펫 이름: " .. myPet.name)
```