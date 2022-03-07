---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SpawnAt</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## SpawnAt(Single, Single)
지정된 좌표를 이용해서 유닛을 소환합니다.

#### 선언
```cs
public void SpawnAt(float x, float y)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|소환할 위치의 X 좌표|
|System.Single|y|소환할 위치의 Y 좌표|

#### 예제
```lua
-- 유닛을 100, 100에 소환시킨다

unit.SpawnAt(100, 100)
```