---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SetJob</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## SetJob(Int32, Boolean)
직업 ID를 통해 유닛의 직업을 설정합니다.

#### 선언
```cs
public virtual void SetJob(int jobID, bool keepSkills = false)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|jobID|데이터 베이스의 직업 ID|
|System.Boolean|keepSkills|스킬의 유지 (기본값: True)|

#### 예제: 스킬을 유지하며 5번 직업으로 변경
```lua
unit.SetJob(5, true)

-- 스킬을 유지하지 않으면서 2번 직업으로 변경
unit.SetJob(2, false)
```