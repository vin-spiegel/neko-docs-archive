---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>PlayME</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## PlayME(String, Single)
해당 ME를 재생합니다.

#### 선언
```cs
public void PlayME(string meID, float volume = 1F)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|meID|ME 이름|
|System.Single|volume|볼륨|

#### 예제: 유닛에게 ME 를 재생시킨다
```lua
unit.PlayME("MyMusicFile.ogg", 1.0)
```