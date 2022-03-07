---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddSkill</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## AddSkill(Int32, Int32, Boolean)
플레이어 유닛에게 스킬을 추가합니다.

#### 선언
```cs
public void AddSkill(int dataID, int level = 1, bool notify = true)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 스킬 ID|
|System.Int32|level|스킬의 레벨 (기본값: 1)|
|System.Boolean|notify|스킬 획득시에 알림을 사용할 것인지를 나타냅니다 (기본값: True) `Center Label` 형식으로 알림이 표기됩니다.|

#### 예제
```lua
-- 유닛에게 10레벨의 3번 스킬을 추가하며 알림을 표시합니다
unit.AddSkill(3, 10, true)

-- 유닛에게 5레벨의 7번 스킬을 추가하며 알림을 표시하지 않습니다
unit.AddSkill(7, 5, false)
``` 