---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SetSkillLevel</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## SetSkillLevel(Int32, Int32)
유닛의 스킬 레벨을 설정합니다.

#### 선언
```cs
public bool SetSkillLevel(int dataID, int level)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 스킬 ID|
|System.Int32|level|변경할 레벨|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|스킬 레벨 설정의 성공 여부 (성공시: True, 실패시: False)|

#### 예제
```lua
-- 유닛이 가진 스킬 중 데이터베이스 상 5번 스킬의 스킬 레벨을 10으로 설정

unit.SetSkillLevel(5, 10)
```