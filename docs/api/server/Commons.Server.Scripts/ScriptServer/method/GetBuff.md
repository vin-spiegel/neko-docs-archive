---
layout: default
title: <font color="#2c84fa">𝑓</font> GetBuff
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## GetBuff(Int32)
데이터베이스의 상태(버프) 정보

#### 선언
```cs
public TGameBuff GetBuff(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|상태(버프)ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameBuff|데이터베이스의 상태 정보|

#### 예제: 데이터베이스에 작성한 5번 상태(버프) 정보 가져오기
```lua
local myBuff = Server.GetBuff(5)
```