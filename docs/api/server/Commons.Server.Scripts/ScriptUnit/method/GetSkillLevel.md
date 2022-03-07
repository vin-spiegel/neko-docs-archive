---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetSkillLevel</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetSkillLevel(Int32)
스킬의 ID를 통해 유닛의 해당 스킬 레벨을 알아옵니다.

#### 선언
```cs
public int GetSkillLevel(int dataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|스킬의 레벨 (스킬이 존재하지 않는다면 `-1`을 반환합니다)|

#### 예제
```lua
-- 유닛이 가진 스킬 중 데이터베이스 상 5번 스킬의 스킬 레벨을 출력
-- 스킬이 없다면 -1 반환

local skillLvl = unit.GetSkillLevel(5)
unit.SendCenterLabel(skillLvl)
```