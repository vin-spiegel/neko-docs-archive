---
layout: default
title: Invalidate()
parent: ScriptClan
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

# [ScriptClan](../../).Invalidate()
클랜 정보를 갱신합니다

네임스페이스: System
{: .text-zeta .no_toc .lh-0}
어셈블리: Creator.dll
{: .text-zeta .no_toc}

## 선언
```cs
public void Invalidate()
```

## 예제
현재 내 플레이어가 속한 클랜의 정보를 갱신합니다
```lua
local myClan = unit.player.clan
myClan.Invalidate()
```
