---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddDamageBy</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## AddDamageBy(ScriptUnit, Int32, Int32, Boolean)
이 유닛에게 피해(데미지)를 입힙니다. (데미지를 받은 대상이 몬스터일 경우 보상이 지급됩니다)

#### 선언
```cs
public void AddDamageBy(ScriptUnit attacker, int damage, int skillDataID = -1, bool critical = false)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|attacker|공격자|
|System.Int32|damage|피해량(데미지)|
|System.Int32|skillDataID|스킬의 공식을 사용시 공식을 적용할 스킬의 ID (기본값: -1(공식 미적용))|
|System.Boolean|critical|치명타(크리티컬)의 발생 유무|