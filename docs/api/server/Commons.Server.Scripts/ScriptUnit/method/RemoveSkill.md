---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>RemoveSkill</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## RemoveSkill(Int32)
스킬의 ID를 통해 유닛의 스킬을 제거합니다.

#### 선언
```cs
public void RemoveSkill(int dataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스상에서의 스킬 ID|

#### 예제: 유닛의 스킬 중 데이터베이스상 5번 스킬을 삭제하기
```lua
unit.RemoveSkill(5)
```
