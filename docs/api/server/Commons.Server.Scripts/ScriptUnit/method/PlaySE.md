---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>PlaySE</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## PlaySE(String, Single)
해당 SE를 재생합니다.

#### 선언
```cs
public void PlaySE(string seName, float volume = 1F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|seName|SE 이름|
|System.Single|volume|볼륨|

#### 예제: 유닛에게 SE 를 재생시킨다
```lua
unit.PlaySE("MyMusicFile.ogg", 1.0)
```