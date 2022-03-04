---
layout: default
title: GetMemberName(Int64)
parent: ScriptClan
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

# [ScriptClan](../../).GetMemberName(Int64)
ID로 멤버 이름 가져오기

네임스페이스: System
{: .text-zeta .no_toc}
어셈블리: Creator.dll
{: .text-zeta .no_toc}

## 선언
```cs
public string GetMemberName(long id)
```

## 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|id|해당 멤버ID|

## 반환

|타입|설명|
|:-|:-|
|System.String|

## 예제
ID가 1인 클랜 맴버 이름 출력하기
```lua
local myClan = unit.player.clan
print(myClan.GetMemberName(1))
```