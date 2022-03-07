---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>ShowAnimation</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


# ShowAnimation(Int32)
해당 유닛의 위치에 애니메이션을 재생합니다.

#### 선언
```cs
public void ShowAnimation(int animationID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|animationID|애니메이션의 ID|

#### 예제
```lua
-- 유닛에서 5번 애니메이션을 재생합니다

unit.ShowAnimation(5)
```