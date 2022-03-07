---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetSkill</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetSkill(Int32)
스킬의 ID를 통해 유닛의 스킬을 얻어옵니다.

#### 선언
```cs
public TSkill GetSkill(int dataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|network.TSkill|스킬을 형식으로 반환합니다.|

#### 예제: 유닛이 가진 스킬 중 데이터베이스 상 5번 스킬의 스킬 레벨을 출력
```lua
local skillInfo = unit.GetSkill(5)

if skillInfo == nil then
    unit.SendCenterLabel("5번 스킬이 없습니다")
else
    unit.SendCenterLabel('5번 스킬의 레벨: ' .. skillInfo.level)
end
```