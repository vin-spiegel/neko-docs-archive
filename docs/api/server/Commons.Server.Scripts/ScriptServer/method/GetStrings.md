---
layout: default
title: <font color="#2c84fa">𝑓</font> GetStrings
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetStrings()
데이터베이스 시스템 글자정보

#### 선언
```cs
public TGameStrings GetStrings()
```

#### 반환

|타입|설명|
|:-|:-|
|TGameStrings|데이터베이스 시스템 글자정보|

#### 예제: 데이터베이스 시스템에 작성한 용어 정보 가져오기
```lua
local myStrings = Server.GetStrings()
```