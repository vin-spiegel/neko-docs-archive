---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">𝑓 </font>UseSkill</div>
nav_order: 1
parent: ScriptEnemyUnitAI
grand_parent: Commons.Server.Scripts
---

## UseSkill(Int32, ScriptPoint, ScriptPoint)
몬스터가 스킬을 사용한다.

#### 선언
```cs
public void UseSkill(int skillID, ScriptPoint dir = null, ScriptPoint pos = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|skillID|사용할 스킬 ID|
|ScriptPoint|dir|스킬의 방향|
|ScriptPoint|pos|스킬의 위치|