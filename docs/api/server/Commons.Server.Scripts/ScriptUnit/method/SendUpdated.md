---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SendUpdated</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SendUpdated(Boolean)
유닛의 정보를 갱신합니다.

#### 선언
```cs
public void SendUpdated(bool fixPosition = false)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Boolean|fixPosition|

#### 예제: 유닛이 갱신되었음을 클라이언트에게 알림
```lua
unit.SendUpdated()
```