---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>StartGlobalEvent</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## StartGlobalEvent(Int32)
플레이어 유닛의 공용 이벤트를 시작합니다.

#### 선언
```cs
public void StartGlobalEvent(int id)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|공용 이벤트의 ID|

#### 예제: 유닛에서 5번 공용 이벤트 실행
```lua
unit.StartGlobalEvent(5)
```