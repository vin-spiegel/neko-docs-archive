---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">𝑓 </font>SetNearTarget</div>
nav_order: 1
parent: ScriptEnemyUnitAI
grand_parent: Commons.Server.Scripts
---

## SetNearTarget(Int32, Single)
현재 몬스터가 있는 맵에서 가장 가까운 유닛을 타겟으로 지정한다.

#### 선언
```cs
public void SetNearTarget(int findType = -1, float dist = 200F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|findType|탐색할 유닛 타입 0 : 플레이어, 1 : 이벤트 유닛 , 2 : 적|
|System.Single|dist|탐색할 유닛 거리 (기본값: 200)|