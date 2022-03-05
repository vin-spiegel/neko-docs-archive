---
layout: default
title: <font color="#2c84fa">𝑓</font> GetMap
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetMap(Int32, TGameMapStub)
맵 데이터 정보

#### 선언
```cs
public TGameMapStub GetMap(int id, TGameMapStub parent = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|맵 iD|
|TGameMapStub|parent|기본 null 선택된 맵의 부모|

#### 반환

|타입|설명|
|:-|:-|
|TGameMapStub|맵 데이터 정보|

#### 예제: 5번 ID를 가진 맵의 정보를 가져오기
```lua
-- PC 또는 모바일 스튜디오 맵 편집기에서 #00 형식으로 나오는 것이 맵의 ID입니다

local myMap = Server.GetMap(5)
```