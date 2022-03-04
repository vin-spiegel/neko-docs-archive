---
layout: default
title: ScriptParty
nav_order: 9
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptParty 
파티 관련 클래스

<!-- new
{: .label .label-green } -->

#### 상속


<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ ScriptParty
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptParty : ScriptObject
```

## 프로퍼티
---

## id
고유 ID

#### 선언
```cs
public long id { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## masterPlayerID
파티 마스터의 ID

#### 선언
```cs
public long masterPlayerID { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## maxPlayer
파티의 최대 플레이어 수

#### 선언
```cs
public int maxPlayer { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## name
파티의 이름

#### 선언
```cs
public string name { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|

## players
파티 멤버 유닛을 배열 형태로 가져오기

#### 선언
```cs
public ScriptRoomPlayer[] players { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptRoomPlayer[]|

## 함수
---

## Destroy()
파티 파괴 (해산)

#### 선언
```cs
public void Destroy()
```

#### 예제: 내가 가입해 있는 파티 해산시키기
```lua
local party = unit.party
if party == nil then
    unit.SendCenterLabel('가입한 파티가 존재하지 않습니다')
    return
end

local players = party.players

for i = 1, #players do
    if players[i] ~= nil then
        party.KickParty(players[i])
    end
end

party.Destroy()
party.SendUpdated()

unit.SendCenterLabel('파티를 해산했습니다')
JoinParty(ScriptRoomPlayer)
```

## 파티 참가

#### 선언
```cs
public int JoinParty(ScriptRoomPlayer player)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptRoomPlayer|player|참가할 플레이어|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|형태의 결과값 출력|

#### 예제: 가장 가까운 플레이어 한명을 파티에 가입시킨다
```lua
if unit.party ~= nil then
    local targetUnit = unit.field.FindUnit(unit.x, unit.y, 2000,
    function(x)
        return true
    end, 0, unit)
    
    if targetUnit ~= nil then
        unit.party.JoinParty(targetUnit.player)
        print(unit.name .. '님의 파티에' .. targetUnit.name .. '님이 가입했습니다')
    else
        print('대상 유닛을 찾을 수 없습니다')
    end

else
    print('파티가 없습니다')
end
```

## KickParty(ScriptRoomPlayer)
파티 강제 퇴장 시키기

#### 선언
```cs
public bool KickParty(ScriptRoomPlayer player)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptRoomPlayer|player|퇴장 시킬 플레이어|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|성공 여부 (True / False)|

#### 예제: 나를 제외한 모든 파티원들을 파티에서 강제 퇴장시키기
```lua
-- 가입한 파티가 있는지 검사
if unit.party == nil then
    unit.SendCenterLabel('가입한 파티가 존재하지 않습니다')
    return;
end

-- 모든 파티원 목록, 파티원 수 구하기
local players = unit.party.players
local playerCount = #players

-- 파티원의 수가 1 이하일 때 (나 혼자 있다면) 예외처리
if playerCount <= 1 then
    unit.SendCenterLabel('파티에 다른 유저들이 존재하지 않습니다')
    return;
end

local outCount = 0
-- 파티원의 수만큼 순회하며 각 파티원들 퇴장
for i = 1, playerCount do
    if players[i] ~= unit.player and players[i] ~= nil then
        unit.party.KickParty(players[i])
        outCount = outCount + 1
    end
end

-- 알림 표시
unit.SendCenterLabel('유저 ' .. outCount .. '명을 파티에서 퇴장시켰습니다.')
```

## LeaveParty(ScriptRoomPlayer)
파티 떠나기

#### 선언
```cs
public bool LeaveParty(ScriptRoomPlayer player)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptRoomPlayer|player|플레이어|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|성공 여부 (True / False)|

#### 예제: 나를 제외한 모든 파티원들을 파티에서 떠나게 하기
```lua
-- 가입한 파티가 있는지 검사
if unit.party == nil then
    unit.SendCenterLabel('가입한 파티가 존재하지 않습니다')
    return;
end

-- 모든 파티원 목록, 파티원 수 구하기
local players = unit.party.players
local playerCount = #players

-- 파티원의 수가 1 이하일 때 (나 혼자 있다면) 예외처리
if playerCount <= 1 then
    unit.SendCenterLabel('파티에 다른 유저들이 존재하지 않습니다')
    return;
end

local outCount = 0
-- 파티원의 수만큼 순회하며 각 파티원들 파티에서 제외
for i = 1, playerCount do
    if players[i] ~= unit.player and players[i] ~= nil then
        unit.party.LeaveParty(players[i])
        outCount = outCount + 1
    end
end

-- 알림 표시
unit.SendCenterLabel('유저 ' .. outCount .. '명을 파티에서 내보냈습니다.')
```

## SendUpdated()
파티 갱신

#### 선언
```cs
public void SendUpdated()
```

#### 예제: 파티 내의 모든 플레이어들에게 파티 정보가 변경되었음을 알림
```lua
local party = unit.party

if party ~= nil then
    party.SendUpdated()
end
```