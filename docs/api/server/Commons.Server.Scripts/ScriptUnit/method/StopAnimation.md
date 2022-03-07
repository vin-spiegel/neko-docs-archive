---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>StopAnimation</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## StopAnimation(Int32)
해당 유닛이 재생 중이던 애니메이션을 중단합니다.

#### 선언
```cs
public void StopAnimation(int animationID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|animationID애니메이션의 ID|

#### 예제: 유닛에서 실행 중이던 5번 애니메이션 실행 종료시키기
```lua
unit.StopAnimation(5)
```