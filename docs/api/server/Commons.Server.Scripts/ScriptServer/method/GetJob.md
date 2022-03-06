---
layout: default
title: <font color="#2c84fa">𝑓</font> GetJob
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetJob(Int32)
데이터베이스의 직업 정보

#### 선언
```cs
public TGameJob GetJob(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|직업 ID|

### 반환

|타입|설명|
|:-|:-|
|TGameJob|데이터베이스의 직업 정보|

#### 예제: 데이터베이스에 작성한 5번 직업 정보 가져오기
```lua
local myJob = Server.GetJob(5)
```
