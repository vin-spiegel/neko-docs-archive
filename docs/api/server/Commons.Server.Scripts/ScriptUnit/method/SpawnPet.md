---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SpawnPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SpawnPet(Int32, Single, Single, Int32, Int32, String)
펫을 소환합니다. 
- 같은 ID로 이미 소환되었던 경우 해당 펫의 정보로 소환됩니다.
- 소환되었던 이력이 없는 경우 해당 ID로 등록 후 소환됩니다.

#### 선언
```cs
public bool SpawnPet(int petID, float posX, float posY, int characterID = 0, int jobID = 0, string name = null)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|petID|소환할 펫의 ID|
|System.Single|posX|소환할 위치의 X 좌표|
|System.Single|posY|소환할 위치의 Y 좌표|
|System.Int32|characterID|신규 등록시 펫의 캐릭터 ID (기본값: 0)|
|System.Int32|jobID|신규 등록시 펫의 직업 ID (기본값: 0)|
|System.String|name|신규 등록시 펫의 이름 (기본값: 펫 캐릭터의 이름)|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|펫 소환 성공여부(성공: True, 실패: False)|
