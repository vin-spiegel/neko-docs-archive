---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## AddItem(Int32, Int32, Boolean)
유닛에 아이템을 추가합니다.

#### 선언
```cs
public void AddItem(int dataID, int count = 1, bool notify = true)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 아이템 ID|
|System.Int32|count|추가할 수량 (기본값: 1)|
|System.Boolean|notify|아이템 획득시에 알림을 사용할 것인지를 나타냅니다 (기본값: True) `Center Label` 형식으로 알림이 표기됩니다.|

#### 예제
```lua
-- 0번 ID의 아이템을 1개 추가하며 알림을 표시합니다.
unit.AddItem(0, 1, true)

-- 1번 ID의 아이템을 2개 추가하며 알림을 표시하지 않습니다.
unit.AddItem(1, 2)
```