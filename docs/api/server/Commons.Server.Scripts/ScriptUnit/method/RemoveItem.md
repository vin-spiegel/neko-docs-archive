---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>RemoveItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## RemoveItem(Int32, Int32, Boolean, Boolean, Boolean)
플레이어 유닛으로부터 아이템을 제거합니다.

#### 선언
```cs
public bool RemoveItem(int dataID, int count = 1, bool notify = true, bool atomic = false, bool equippedItemExclude = false)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|제거할 아이템의 데이터베이스 아이템 ID|
|System.Int32|count|제거할 아이템의 개수|
|System.Boolean|notify|아이템을 제거했을때 공지를 사용할 것인지를 나타냅니다.|
|System.Boolean|atomic|이 인자가 활성화 되었을 때 제거할 아이템의 개수보다 가지고 있는 아이템의 개수가 적으면 false를 반환하고 함수를 종료합니다.|
|System.Boolean|equippedItemExclude|장착 중인 아이템은 제거 대상에서 제외할지를 나타냅니다.|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|	

#### 예제: 유닛의 인벤토리에서 데이터베이스 상 5번 아이템을 1개 제거합니다
```lua
unit.RemoveItem(5, 1)
```