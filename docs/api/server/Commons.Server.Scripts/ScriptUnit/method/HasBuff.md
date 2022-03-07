---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>HasBuff</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## HasBuff(Int32)
해당 유닛이 상태(Buff)를 가지고 있는지 체크합니다.

#### 선언
```cs
public bool HasBuff(int buffID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|buffID|상태(Buff) ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|	

#### 예제: 유닛이 5번 버프를 가지고 있는지 검사
```lua
if unit.HasBuff(5) then
    unit.SendCenterLabel("5번 버프가 있다")
else
    unit.SendCenterLabel("5번 버프가 없다");
end
```