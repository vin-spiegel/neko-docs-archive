---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">❒ </font>teamTag</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## teamTag
유닛의 팀 태그를 얻어옵니다. (팀 태그를 `AND` 연산하여 동맹 여부를 파악할 수 있습니다.
하나라도 `AND` 되는 비트가 있을 시 동맹)

#### 선언
```cs
public uint teamTag { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.UInt32|	

#### 예제
```lua
-- 팀 태그를 AND 연산하여 동맹 여부를 파악할 수 있습니다.
-- (하나라도 AND 되는 비트가 있을 시 동맹)
```