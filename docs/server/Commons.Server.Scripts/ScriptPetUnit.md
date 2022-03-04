---
layout: default
title: ScriptPetUnit
nav_order: 10
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptPetUnit 
펫을 나타내는 스크립트 클래스입니다.

<!-- new
{: .label .label-green } -->

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ <a href = "../ScriptUnit">ScriptUnit</a><br/>
　　　↳ ScriptPetUnit
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptPetUnit : ScriptUnit
```

## 프로퍼티

## characterData
펫 유닛의 캐릭터 데이터 

|프로퍼티 이름|타입|설명|
|:-|:-|:-|
|characterData.name|string|캐릭터이름|
|characterData.memo|string|메모내용|
|characterData.moveSpeed|int|움직임 속도|
|characterData.collision|bool|충돌 여부|
|characterData.jumpForce|float|점프힘|


#### 선언
```cs
public override TGameCharacter characterData { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|TGameCharacter|

#### 재정의
ScriptUnit.characterData

#### 예제
```lua
-- 유닛의 이름 : string characterData.name
-- 유닛의 메모 내용 : string characterData.memo
-- 유닛의 이동속도 : int characterData.moveSpeed
-- 유닛의 충돌 여부 : bool characterData.collision
-- 유닛의 점프력 : float characterData.jumpForce
```

## characterID
펫 유닛의 캐릭터 ID

#### 선언
```cs
public override int characterID { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

#### 재정의
ScriptUnit.characterID

## cumulativeEXP
펫의 누적 경험치

#### 선언
```cs
public override long cumulativeEXP { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

#### 재정의
ScriptUnit.cumulativeEXP

## exp
펫의 현재 경험치

#### 선언
```cs
public override long exp { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

#### 재정의
ScriptUnit.exp

## job
펫 유닛의 직업

#### 선언
```cs
public override int job { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

#### 재정의
ScriptUnit.job

## level
펫의 현재 레벨

#### 선언
```cs
public override int level { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

#### 재정의
ScriptUnit.level

## petID
펫 유닛의 주인에게 등록된 ID

#### 선언
```cs
public int petID { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## 함수
---

## AddEXP(Int64)
펫 경험치 지급

#### 선언
```cs
public override void AddEXP(long amount)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|증가시킬 양|

#### 재정의
ScriptUnit.AddEXP(Int64)

#### 예제: 현재 플레이어 유닛의 소환된 펫에게 경험치 10000 지급
```lua
-- 플레이어에게 먼저 펫을 소환시킨 후 아래 예제를 이벤트 유닛에 넣고 실행해보세요
local myPet = unit.GetSingleSummonedPet()
myPet.AddEXP(10000)
```

## ResetPetLevelEXP()
펫 레벨 초기화

#### 선언
```cs
public void ResetPetLevelEXP()
```

#### 예제: 현재 플레이어 유닛의 소환된 펫의 레벨, 경험치를 초기화
```lua
-- 플레이어에게 먼저 펫을 소환시킨 후
-- 아래 예제를 이벤트 유닛에 넣고 실행해보세요

local myPet = unit.GetSingleSummonedPet()
myPet.ResetPetLevelEXP()
```

## SetJob(Int32, Boolean)
펫 직업 변경시 스킬의 유지 여부

#### 선언
```cs
public override void SetJob(int jobID, bool keepSkills = false)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|jobID|직업 ID|
|System.Boolean|keepSkills|같은 스킬 유지 여부 (기본: True)|

#### 재정의
ScriptUnit.SetJob(Int32, Boolean)

#### 예제: 현재 내 펫의 직업을 5번으로 설정
```lua
-- 플레이어에게 먼저 펫을 소환시킨 후
-- 아래 예제를 이벤트 유닛에 넣고 실행해보세요

local myPet = unit.GetSingleSummonedPet()
myPet.SetJob(5)
```