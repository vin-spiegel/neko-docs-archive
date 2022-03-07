---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetRegistedPetID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## GetRegistedPetID()
등록된 펫들의 ID를 `[]` 형식으로 반환합니다.

#### 선언
```cs
public int[] GetRegistedPetID()
```

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|[]|등록된 펫들의 ID가 담긴 [] 형식 배열|

#### 예제: 현재 등록된 펫들의 ID를 차례대로 모두 출력
```lua
local petIdList = unit.GetRegistedPetID()

for i = 1, #petIdList do
    if petIdList[i] ~= nil then
        unit.SendCenterLabel(petIdList[i])
    end
end
```