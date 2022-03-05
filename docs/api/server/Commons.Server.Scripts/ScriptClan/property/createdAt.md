---
layout: default
title: <font color="#2c84fa">❒</font> createdAt
parent: ScriptClan
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# [ScriptClan](../../).createdAt
클랜 생성일

네임스페이스: System
{: .text-zeta .no_toc .lh-0}
어셈블리: Creator.dll
{: .text-zeta .no_toc}

## 선언
```cs
public DateTime createdAt { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|System.DateTime|

## 예제
현재 내 플레이어가 속한 클랜의 생성된 시간을 출력합니다
```lua
local myClan = unit.player.clan
print(myClan.createdAt.ToLocalTime().ToString())
```
