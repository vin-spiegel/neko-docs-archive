---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SpawnAtFieldID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SpawnAtFieldID(Int32, Single, Single, Int32)
필드의 ID를 이용해서 지정된 좌표에 유닛을 소환합니다.

#### 선언
```cs
public void SpawnAtFieldID(int mapID, float x, float y, int channelID = 0)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|mapID|소환할 필드의 ID|
|System.Single|x|소환할 위치의 X 좌표|
|System.Single|y|소환할 위치의 Y 좌표|
|System.Int32|channelID|소환할 위치의 Y 좌표|

#### 예제: 15번 맵의 1번 채널에 유닛 이동 시키기
```lua
unit.SpawnAtFieldID(15,4*15,4*16,1)
```