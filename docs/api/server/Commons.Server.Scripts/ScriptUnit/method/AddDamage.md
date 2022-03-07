---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddDamage</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


# AddDamage(Int32, Int32, Boolean)
이 유닛에게 피해(데미지)를 입힙니다. (공격자가 존재하지 않기 때문에 보상이 지급되지 않습니다)

#### 선언
```cs
public void AddDamage(int damage, int skillDataID = -1, bool critical = false)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|damage|피해량(데미지)|
|System.Int32|skillDataID|스킬의 공식을 사용시 공식을 적용할 스킬의 ID (기본값: -1(공식 미적용))|
|System.Boolean|critical|치명타(크리티컬)의 발생 유무|

#### 예제: 유닛에게 데미지 999를 입힙니다
```lua
unit.AddDamage(999)
```