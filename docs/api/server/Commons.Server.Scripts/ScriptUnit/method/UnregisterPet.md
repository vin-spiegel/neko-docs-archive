---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>UnregisterPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## UnregisterPet(Int32)
펫의 ID를 통해 펫의 등록을 해제합니다.

#### 선언
```cs
public void UnregisterPet(int petID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|petID|등록 해제할 펫의 ID|

#### 예제: 0번 ID로 등록된 펫 등록 해제하기
```lua
-- Note: SpawnPet 함수로 펫을 소환할 떄 입력했던 펫 ID

unit.UnregisterPet(0)
```