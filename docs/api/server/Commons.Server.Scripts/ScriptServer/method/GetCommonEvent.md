---
layout: default
title: <font color="#2c84fa">𝑓</font> GetCommonEvent
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

# GetCommonEvent(Int32)
데이터베이스의 공용이벤트정보

#### 선언
```cs
public TGameCommonEvent GetCommonEvent(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|이벤트 ID|

#### 반환    

|타입|설명|
|:-|:-|
|TGameCommonEvent|공용이벤트정보|

#### 예제: 데이터베이스에 작성한 5번 공용 이벤트 정보 가져오기
```lua
local myComEvent = Server.GetCommonEvent(5)
```