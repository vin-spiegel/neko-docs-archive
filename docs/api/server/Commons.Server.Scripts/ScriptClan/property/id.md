---
layout: default
title: createdAt
parent: ScriptClan
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## id
고유 ID

네임스페이스: System
{: .text-zeta .no_toc .lh-0}
어셈블리: Creator.dll
{: .text-zeta .no_toc}

## 선언

```cs
public long id { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## 예제
현재 내 플레이어가 속한 클랜의 ID를 출력합니다.
```lua
local myClan = unit.player.clan
print(myClan.id)
```