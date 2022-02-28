---
layout: default
title: ScriptField
nav_order: 6
parent: Commons.Server.Scripts
grand_parent: Server API
# permalink: /docs/server-api/Commons.Server.Scripts/ScriptField
---

# Class ScriptField 
{: .d-inline-block }

<!-- New
{: .label .label-green } -->

서버에서 맵을 관리하는 객체 입니다. 하나의 맵에 대응됩니다.

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ ScriptField
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptField : ScriptObject, NekoEventListener
```

## 프로퍼티
---

## channelID
이 맵의 채널 ID

#### 선언
```cs
public int channelID { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## dataID
이 맵의 데이터 ID

#### 선언
```cs
public int dataID { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## dropItems
해당 필드에 있는 모든 드랍 아이템을 배열 형식으로 가져옵니다.

#### 선언
```cs
public ScriptDropItem[] dropItems { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptDropItem[]|

## height
이 맵의 세로 크기

#### 선언
```cs
public int height { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## maxPlayers
필드의 최대 플레이어 수

#### 선언
```cs
public uint maxPlayers { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.UInt32|

## name
이 맵의 이름

#### 선언
```cs
public string name { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|

## onJoinDropItem
해당 필드에 드랍 아이템이 들어왔을 때 호출되는 이벤트입니다.

#### 호출될 함수의 인자 형식

```lua
function(field: ScriptField, dropItem: ScriptDropItem)
```

|이름|타입|설명|
|:-|:-|:-|
|field|[ScriptField](../6.ScriptField)|해당 필드|
|dropItem|[ScriptDropItem](../3.ScriptDropItem)|드랍된 아이템|

#### 선언
```cs
public ScriptEventPublisher onJoinDropItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|[ScriptEventPublisher](../5.ScriptEventPublisher)|

#### 예제: 필드에 드랍 아이템이 추가되었을 때 필드에 있는 모든 플레이어들에게 알림 표시하기
```lua
-- Note: 해당 예제는 재귀적으로 동작할 수 있습니다

-- 드랍 아이템이 실제 떨어졌을 때의 콜백
function onJoinDropItem(field, dropItem)
    if dropItem == nil then
        return
    end
    
    local itemData = Server.GetItem(dropItem.titem.dataID)
    if itemData ~= nil then
        field.SendCenterLabel(itemData.name .. " 아이템이 땅에 떨어졌습니다!")
    end
end


-- 대상 필드에 콜백을 등록하는 함수
function registerCallback()
    local field = Server.GetField(6)

    -- 필드가 생성되었다면 콜백 등록
    if field ~= nil then
        field.onJoinDropItem.Add(onJoinDropItem)
    else
        -- 생성되지 않았다면 다시 1초를 기다린 후 콜백 등록을 시도한다
        Server.RunLater(registerCallback, 1)
    end
end


-- 등록 함수를 1초 뒤에 실행한다 (스크립트가 실행되는 시점에 아직 필드가 생성되지 않았을 수도 있다)
Server.RunLater(registerCallback, 1)
```

## onJoinField
해당 필드에 유닛이 들어왔을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식: 
```lua
function(field: ScriptField, unit: ScriptUnit)
```

|이름|타입|설명|
|:-|:-|:-|
|field|[ScriptField](../6.ScriptField)|해당 필드|
|unit|[ScriptUnit](../17.ScriptUnit)|필드에 들어온 유닛|

#### 선언
```cs
public ScriptEventPublisher onJoinField { get; }
```

#### 프로퍼티 값

|타입|설명|
|[ScriptEventPublisher](../5.ScriptEventPublisher)|

#### 예제: 특정 맵에 입장시 이름 출력, 서버전체 메세지 보내기
```lua
function onJoinField()
    function onJoinField_1(field, unit)
        unit.SendCenterLabel(field.name) -- 유닛에게 잠시 필드이름을 표시한다.
        if #field.playerUnits > 10 then -- #은 테이블의 길이를 의미한다.
            Server.SendSay(field.name .. "에 11명 이상의 유저가 모였습니다!!")
        end
    end

    local map = Server.GetField(1)
    if map ~= nil then
        -- 1번 필드에 입장시 onJoinField_1 함수를 호출한다.
        map.onJoinField.Add(onJoinField_1)
    end
end

-- 1초후 onJoinField 함수를 실행합니다. 맵이 생성되지 않았을 수 있기 떄문에 nil을 참조하는 것을 방지하기 위한 방법입니다.
Server.RunLater(onJoinField, 1) 
```

## onLeaveDropItem
해당 필드에 드랍 아이템이 나갔을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function(field: ScriptUnit, dropItem: ScriptDropItem)
```

|이름|타입|설명|
|:-|:-|:-|
|field|[ScriptField](../6.ScriptField)|해당 필드|
|dropItem|[ScriptDropItem](../3.ScriptDropItem)|드랍된 아이템|

#### 선언
```cs
public ScriptEventPublisher onLeaveDropItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|[ScriptEventPublisher](../5.ScriptEventPublisher)|

#### 예제: 필드에서 드랍 아이템이 나갔을 때 필드에 있는 모든 플레이어들에게 알림 표시하기
```lua
-- Note: 해당 예제는 재귀적으로 동작할 수 있습니다

-- 드랍 아이템이 나갔을 때의 콜백
function onLeaveDropItem(field, dropItem)
    if dropItem == nil then
        return
    end
    
    local itemData = Server.GetItem(dropItem.titem.dataID)
    if itemData ~= nil then
        field.SendCenterLabel(itemData.name .. " 아이템이 필드에서 사라졌습니다!")
    end
end


-- 대상 필드에 콜백을 등록하는 함수
function registerCallback()
    local field = Server.GetField(6)

    -- 필드가 생성되었다면 콜백 등록
    if field ~= nil then
        field.onLeaveDropItem.Add(onLeaveDropItem)
    else
        -- 생성되지 않았다면 다시 1초를 기다린 후 콜백 등록을 시도한다
        Server.RunLater(registerCallback, 1)
    end
end


-- 등록 함수를 1초 뒤에 실행한다 (스크립트가 실행되는 시점에 아직 필드가 생성되지 않았을 수도 있다)
Server.RunLater(registerCallback, 1)
```

## onLeaveField
해당 필드에서 유닛이 나갔을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식 
```lua
function(field: ScriptField, unit: ScriptUnit)
```

|이름|타입|설명|
|:-|:-|:-|
|field|[ScriptField](../6.ScriptField)|해당 필드|
|unit|[ScriptUnit](../17.ScriptUnit)|필드를 나간 유닛|

#### 선언
```cs
public ScriptEventPublisher onLeaveField { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|[ScriptEventPublisher](../5.ScriptEventPublisher)|

#### 예제: 특정 맵에서 나갈시 처리
```lua
function onLeaveField(map,unit)
    print('떠난다 : ' .. map.name .. ' ' ..unit.name)
    Server.SetWorldVar(10, Server.GetWorldVar(10) - 1)
end

Server.GetField(5).onLeaveField.Add(onLeaveField)
```

## playerCount
이 맵의 플레이어 유닛 개수

#### 선언
```cs
public int playerCount { get; }
```

#### 프로퍼티 값

타입	설명
System.Int32


## playerUnits
해당 필드에 있는 모든 플레이어 유닛을 배열 형식으로 가져옵니다.

#### 선언
```cs
public ScriptUnit[] playerUnits { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)[]|

## units
해당 필드에 있는 모든 유닛을 배열 형식으로 가져옵니다.

#### 선언
```cs
public ScriptUnit[] units { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)[]|
|width|이 맵의 가로 크기|

#### 선언
```cs
public int width { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## 함수
---

## FindMaximumUnit(Single, Single, Single, Closure, Int32, ScriptUnit)
현재 필드에서 가장 큰 조건에 맞는 유닛을 가져옵니다.

#### 선언
```cs
public ScriptUnit FindMaximumUnit(float x, float y, float dist, Closure func, int findType = -1, ScriptUnit without = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|거리를 찾는 기준이 될 유닛의 위치 X|
|System.Single|y|거리를 찾는 기준이 될 유닛의 위치 Y|
|System.Single|dist|찾는 거리 범위|
|MoonSharp.Interpreter.Closure|func|실행할 스크립트 함수|
|System.Int32|findType|탐색할 유닛 타입 0 : 플레이어, 1 : 이벤트 유닛 , 2 : 적|
|[ScriptUnit](../17.ScriptUnit)|without|제외할 유닛|

#### 반환

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|유닛|

#### 예제: 거리 300 이내의 이벤트 몬스터 유닛들 중 가장 HP가 많은 몬스터 유닛의 이름 출력
```lua
local monsterUnit = unit.field.FindMaximumUnit(unit.x, unit.y, 300, 
    function(x)
        return x.hp
    end
    , 2, unit)

if monsterUnit == nil then
    unit.SendCenterLabel("몬스터 유닛이 거리 300 보다 멀리 있거나 존재하지 않습니다")
    return
end

unit.SendCenterLabel("HP가 가장 많은 몬스터 유닛: " .. monsterUnit.name)
```

## FindMinimumUnit(Single, Single, Single, Closure, Int32, ScriptUnit)
현재 필드에서 가장 작은 조건에 맞는 유닛을 가져옵니다.

#### 선언
```cs
public ScriptUnit FindMinimumUnit(float x, float y, float dist, Closure func, int findType = -1, ScriptUnit without = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|거리를 찾는 기준이 될 유닛의 위치 X|
|System.Single|y|거리를 찾는 기준이 될 유닛의 위치 Y|
|System.Single|dist|찾는 거리 범위|
|MoonSharp.Interpreter.Closure|func|실행할 스크립트 함수|
|System.Int32|findType|탐색할 유닛 타입 0 : 플레이어, 1 : 이벤트 유닛 , 2 : 적|
|[ScriptUnit](../17.ScriptUnit)|without|제외할 유닛|

#### 반환

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|유닛|

#### 예제: 거리 300 이내의 이벤트 몬스터 유닛들 중 가장 HP가 적은 몬스터 유닛의 이름 출력
```lua
local monsterUnit = unit.field.FindMinimumUnit(unit.x, unit.y, 300, 
    function(x)
        return x.hp
    end
    , 2, unit)

if monsterUnit == nil then
    unit.SendCenterLabel("몬스터 유닛이 거리 300 보다 멀리 있거나 존재하지 않습니다")
    return
end

unit.SendCenterLabel("HP가 가장 적은 몬스터 유닛: " .. monsterUnit.name)
```

## FindNearDropItem(Single, Single, Single)
현재 필드에서 지정된 위치와 가장 가까운 드롭 아이템을 가져옵니다.

#### 선언
```cs
public ScriptDropItem FindNearDropItem(float x, float y, float dist)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|거리를 찾는 기준이 될 유닛의 위치 X|
|System.Single|y|거리를 찾는 기준이 될 유닛의 위치 Y|
|System.Single|dist|찾을 거리 범위|

#### 반환

|타입|설명|
|:-|:-|
|[ScriptDropItem](../3.ScriptDropItem)|드롭된 아이템|

#### 예제: 거리 400 이내의 가장 가까운 드랍 아이템을 줍는다
```lua
local nearDropItem = unit.field.FindNearDropItem(unit.x, unit.y, 400)

if nearDropItem == nil then
    unit.SendCenterLabel("거리 400 이내에 드랍 아이템이 존재하지 않습니다")
    return
end
nearDropItem.Acquire(unit)
```

## FindNearUnit(Single, Single, Single, Int32, ScriptUnit)
현재 필드에서 지정된 위치와 가장 가까운 유닛을 가져옵니다.

#### 선언
```cs
public ScriptUnit FindNearUnit(float x, float y, float dist, int findType = -1, ScriptUnit without = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|거리를 찾는 기준이 될 유닛의 위치 X|
|System.Single|y|거리를 찾는 기준이 될 유닛의 위치 Y|
|System.Single|dist|찾는 거리 범위|
|System.Int32|findType|탐색할 유닛 타입 0 : 플레이어, 1 : 이벤트 유닛 , 2 : 적|
|[ScriptUnit](../17.ScriptUnit)|without|제외할 유닛|

#### 반환

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|유닛|

#### 예제: 가장 가까이 있는 이벤트 유닛의 이름 출력하기
```lua
local nearEventUnit = unit.field.FindNearUnit(unit.x, unit.y, 100, 1, unit)

if nearEventUnit == nil then
    unit.SendCenterLabel("이벤트 유닛이 거리 100 보다 멀리 있거나 존재하지 않습니다")
    return
end

unit.SendCenterLabel("가장 가까이 있는 이벤트 유닛 :" .. nearEventUnit.name)
```

## FindUnit(Single, Single, Single, Closure, Int32, ScriptUnit)
현재 필드에서 해당 조건에 맞는 유닛을 찾아서 가져옵니다.

#### 선언
```cs
public ScriptUnit FindUnit(float x, float y, float dist, Closure func, int findType = -1, ScriptUnit without = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|거리를 찾는 기준이 될 위치 X|
|System.Single|y|거리를 찾는 기준이 될 위치 Y|
|System.Single|dist|찾는 거리 범위|
|MoonSharp.Interpreter.Closure|func|실행할 스크립트 함수|
|System.Int32|findType|탐색할 유닛 타입 0 : 플레이어, 1 : 이벤트 유닛 , 2 : 적|
|[ScriptUnit](../17.ScriptUnit)|without|제외할 유닛|

#### 반환

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|유닛|

#### 예제: 거리 100 이내의 이름이 EV001 인 이벤트 유닛을 찾아 그 유닛의 ID를 출력하기
```lua
local eventUnit = unit.field.FindUnit(unit.x, unit.y, 100, 
    function(x)
        return x.name == 'EV001'
    end
    , 1, unit)

if eventUnit == nil then
    unit.SendCenterLabel("이름이 EV001인 유닛이 거리 100 보다 멀리 있거나 존재하지 않습니다")
    return
end

unit.SendCenterLabel("EV001의 ID: " .. eventUnit.id)
```

## GetEventUnitByName(String)
해당 필드에 있는 이벤트 유닛을 가져옵니다.

#### 선언
```cs
public ScriptUnit GetEventUnitByName(string name)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|name|이벤트 유닛의 이름|

#### 반환

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|유닛|

#### 예제: 현재 필드에서 EV001 이란 이름을 가진 이벤트 유닛을 가져오기
```lua
local eventUnit = unit.field.GetEventUnitByName("EV001")
```

## GetFieldVar(Int32)
필드 변수의 값을 가져옵니다.

#### 선언
```cs
public long GetFieldVar(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int64|값|

#### 예제: 현재 속한 필드의 5번 필드 변수출력
```lua
unit.SendCenterLabel('5번 변수: ' ..  unit.field.GetFieldVar(5))
```

## GetTerrainTag(Single, Single)
필드 Tag의 값을 가져옵니다.

#### 선언
```cs
public int GetTerrainTag(float posX, float posY)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|posX|
|System.Single|posY|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|값|

## GetUnit(Int64)
해당 필드에 있는 유닛을 유닛 ID를 통해 가져옵니다.

#### 선언
```cs
public ScriptUnit GetUnit(long id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|id|유닛의 ID|

#### 반환

|타입|설명|
|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|유닛|

#### 예제: 현재 있는 필드의 5번 ID를 가진 유닛을 가져온다
```lua
local otherUnit = unit.field.GetUnit(5)
print(otherUnit)
```

## JoinDropItem(ScriptDropItem, ScriptPoint)
특정 드랍 아이템을 이 필드에 접속시킵니다.

#### 선언
```cs
public void JoinDropItem(ScriptDropItem dropItem, ScriptPoint position = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|[ScriptDropItem](../3.ScriptDropItem)|dropItem|해당 객체|
|[ScriptPoint](../12.ScriptPoint)|position|접속 시의 아이템 좌표|

#### 예제: 내 유닛의 2칸 위에, 5번 아이템을 드랍 아이템으로 생성
```lua
local dropItem = Server.CreateDropItem(5, 1)
unit.field.JoinDropItem(dropItem, Point(unit.x, unit.y + 64))
```

## JoinUnit(ScriptUnit, ScriptPoint)
특정 유닛을 이 필드에 접속시킵니다.

#### 선언
```cs
public void JoinUnit(ScriptUnit unit, ScriptPoint position = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|unit|해당 유닛의 객체|
|[ScriptPoint](../12.ScriptPoint)|position|접속 시의 유닛 좌표|

#### 예제: 2번 맵의 임시 필드를 만들고 해당 필드에 플레이어를 이동
```lua
Server.CreateField(2)
Server.GetField(2).JoinUnit(unit, Point(unit.x, unit.y))
```

## SendCenterLabel(String)
CenterLabel을 표시합니다.

#### 선언
```cs
public void SendCenterLabel(string text)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|라벨에 표시할 텍스트|

#### 예제: 현재 필드의 모든 플레이어들에게 "Hello Field!" 문자열 표시
```lua
unit.field.SendCenterLabel("Hello Field!")
```

## SetFieldVar(Int32, Int64)
필드 변수의 값을 설정합니다.

#### 선언
```cs
public void SetFieldVar(int id, long value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.Int64|value|값|

#### 예제: 현재 속한 필드의 5번 필드 변수를 64라는 값으로 설정
```lua
unit.field.SetFieldVar(5, 64)
```

## SpawnEnemy(Int32, Single, Single)
몬스터를 소환합니다.

#### 선언
```cs
public bool SpawnEnemy(int dataID, float x, float y)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|몬스터의 ID|
|System.Single|x|소환할 위치 X|
|System.Single|y|소환할 위치 Y|

#### 반환

|타입|설명|
|System.Boolean|성공 여부 (True / False)|

#### 예제
```lua
-- 현재 내가 있는 필드의 2칸 위에 3번 몬스터 소환
unit.field.SpawnEnemy(3, unit.x, unit.y + 64)
```