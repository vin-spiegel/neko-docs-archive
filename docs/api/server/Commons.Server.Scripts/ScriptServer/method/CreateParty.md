---
layout: default
title: <font color="#2c84fa">𝑓</font> CreateParty
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## CreateParty(String, Int32)
파티 생성

#### 선언
```cs
public ScriptParty CreateParty(string name = "", int maxPlayer = 4)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|name|파티의 이름|
|System.Int32|maxPlayer|파티의 최대 플레이어 수 (기본: 4명, 최대: 4명)|

#### 반환

|타입|설명|
|:-|:-|
|ScriptParty|파티 정보|

#### 예제: 최대 인원이 4명인 새 파티를 생성합니다
```lua
local myParty = Server.CreateParty("Nekoland Party!", 4)
```