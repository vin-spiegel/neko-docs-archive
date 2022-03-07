---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>UnequipItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## UnequipItem(Int64)
유닛의 장착중인 아이템을 장착 해제합니다.

#### 선언
```cs
public void UnequipItem(long itemID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|itemID|아이템의 고유 ID (데이터 베이스의 ID 와는 다릅니다)|

#### 예제: 유닛이 장착 중인 5번 아이템 장착 해제시키기
```lua
unit.UnequipItem(5)
```