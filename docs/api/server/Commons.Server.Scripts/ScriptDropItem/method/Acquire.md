---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">𝑓 </font>Acquire</div>
nav_order: 1
parent: ScriptDropItem
grand_parent: Commons.Server.Scripts
---

## Acquire(ScriptUnit)

해당 아이템을 특정 Unit이 가져갈 수 있게한다.

#### 선언
```cs
public int Acquire(ScriptUnit unit)
```

### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|unit|객체|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|

#### 예제
새 5번 드랍 아이템을 생성하고 플레이어한테 획득시킨다
```lua
local dropItem = Server.CreateDropItem(5, 1)
unit.field.JoinDropItem(dropItem)
dropItem.Acquire(unit)
```