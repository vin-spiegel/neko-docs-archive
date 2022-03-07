---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>RespawnAt</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## RespawnAt(Single, Single)
지정된 좌표를 이용해서 유닛을 부활시킵니다.

#### 선언
```cs
public void RespawnAt(float x, float y)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|부활할 위치의 X 좌표|
|System.Single|y|부활할 위치의 Y 좌표|

#### 예제: 100, 200 위치에 유닛 부활시키기
```lua
unit.RespawnAt(100, 200)
```