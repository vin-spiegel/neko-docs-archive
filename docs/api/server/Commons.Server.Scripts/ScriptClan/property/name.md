---
layout: default
title: name
parent: ScriptClan
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# [ScriptClan](../../).name
클랜의 고유 이름

네임스페이스: System
{: .text-zeta .no_toc .lh-0}
어셈블리: Creator.dll
{: .text-zeta .no_toc}

## 선언
```cs
public string name { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|

## 예제
현재 내 플레이어가 속한 클랜의 이름을 출력합니다.
```lua
local myClan = unit.player.clan
print(myClan.name)
```
