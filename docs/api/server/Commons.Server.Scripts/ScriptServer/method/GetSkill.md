---
layout: default
title: <font color="#2c84fa">𝑓</font> GetSkill
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetSkill(Int32)
데이터베이스의 스킬 정보

#### 선언
```cs
public TGameSkill GetSkill(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameSkill|데이터베이스의 스킬 정보|

#### 예제: 데이터베이스에 작성한 5번 스킬 정보 가져오기
```lua
local mySkill = Server.GetSkill(5)
```