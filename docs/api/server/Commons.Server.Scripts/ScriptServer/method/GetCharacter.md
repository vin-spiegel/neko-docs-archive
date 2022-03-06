---
layout: default
title: <font color="#2c84fa">𝑓</font> GetCharacter
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## GetCharacter(Int32)
데이터베이스의 캐릭터정보

#### 선언
```cs
public TGameCharacter GetCharacter(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|캐릭터 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameCharacter|데이터베이스 캐릭터 정보|

#### 예제: 데이터베이스에 작성한 5번 캐릭터 정보 가져오기
```lua
local myCh = Server.GetCharacter(5)
```