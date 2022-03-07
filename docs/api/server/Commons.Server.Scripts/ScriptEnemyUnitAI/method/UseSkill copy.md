---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">𝑓 </font>UseSkillToPosition</div>
nav_order: 1
parent: ScriptEnemyUnitAI
grand_parent: Commons.Server.Scripts
---

## UseSkillToPosition(Int32, ScriptPoint, ScriptPoint)
몬스터가 스킬을 사용한다.

#### 선언
```cs
public void UseSkillToPosition(int skillID, ScriptPoint dirPosition = null, ScriptPoint pos = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|skillID|사용할 스킬 ID|
|ScriptPoint|dirPosition|스킬이 나아갈 위치|
|ScriptPoint|pos|스킬의 위치|