---
layout: default
title: ScriptClan
parent: Commons.Server.Scripts
grand_parent: Server API
nav_order: 1
---

# Class ScriptClan

클랜에 관련된 스크립트 클래스입니다


#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ ScriptDropItem
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax

```cs
[MoonSharpUserData]
public class ScriptClan : ScriptObject
```

## 프로퍼티
---

## createdAt

클랜 생성일

#### 선언

```cs
public DateTime createdAt { get; }
```

#### 프로퍼티 값

|타입            |설명  |
|:--------------|:-----|
|System.DateTime|      |

#### 예제

```lua
-- 현재 내 플레이어가 속한 클랜의 생성된 시간을 출력합니다.
local myClan = unit.player.clan
print(myClan.createdAt.ToLocalTime().ToString())
```

## id

고유 ID

#### 선언

```cs
public long id { get; }
```

#### 프로퍼티 값

|타입         |설명   |
|:------------|:-----|
|System.Int64|       |

#### 예제

```lua
-- 현재 내 플레이어가 속한 클랜의 ID를 출력합니다.

local myClan = unit.player.clan
print(myClan.id)
```

## masterPlayerID

클랜 마스터의 ID

#### 선언

```cs
public long masterPlayerID { get; }
```

#### 프로퍼티 값

|타입         |설명   |
|:------------|:-----|
|System.Int64|       |

## memberIDs

멤버 ID를 배열로 가져오기

#### 선언

```cs
public long[] memberIDs { get; }
```

#### 프로퍼티 값

|타입         |설명       |
|:------------|:---------|
|System.Int64[]|         |

## name

고유 이름

#### 선언

```cs
public string name { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|

#### 예제

```lua
-- 현재 내 플레이어가 속한 클랜의 이름을 출력합니다.

local myClan = unit.player.clan
print(myClan.name)
```

## 함수
---

## GetMemberName(Int64)

ID로 멤버 이름 가져오기

#### 선언

```cs
public string GetMemberName(long id)
```

#### 매개 변수(인자)

|타입          |이름       |설명       |
|:------------|:---------|:------------|
|System.String|id          |해당 멤버ID  |

#### 반환

|타입          |설명       |
|:------------|:---------|
|System.String|          |

#### 예제

```lua
-- ID가 1인 클랜 맴버 이름 출력하기

local myClan = unit.player.clan
print(myClan.GetMemberName(1))
```

## Invalidate()

클랜 정보 갱신

#### 선언

```cs
public void Invalidate()
```

#### 예제

```lua
-- 현재 내 플레이어가 속한 클랜의 정보를 갱신

local myClan = unit.player.clan
myClan.Invalidate()
```
