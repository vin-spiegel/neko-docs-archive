---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>HasSkill</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## HasSkill(Int32)
스킬의 ID를 통해 유닛의 스킬 유무를 알아옵니다.

#### 선언
```cs
public bool HasSkill(int dataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|스킬의 존재 유무 (있음: True, 없음: False)|

#### 예제: 유닛이 5번 스킬을 가지고 있는지 검사
```lua
if unit.HasSkill(5) then
    unit.SendCenterLabel("5번 스킬을 가지고 있습니다")
else
    unit.SendCenterLabel("5번 스킬이 없습니다")
end
```