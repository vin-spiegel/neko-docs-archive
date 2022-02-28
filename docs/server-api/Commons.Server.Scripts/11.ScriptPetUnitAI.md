---
layout: default
title: ScriptPetUnitAI
nav_order: 11
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptPetUnitAI 
펫의 AI를 나타내는 스크립트 클래스입니다.

<!-- new
{: .label .label-green } -->

#### 상속

```
↳ System.Object
    ↳ ScriptObject
        ↳ Commons.Server.Scripts.ScriptUnitAI
            ↳ ScriptPetUnitAI
```

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptPetUnitAI : ScriptUnitAI
```

#### 예제 1
```lua
-- 펫 AI 지정

Server.SetPetAI(
        21, -- 펫이 될 캐릭터 id
        function(pet,ai,event)

                -- 최초 PetAI 등록시 실행
                if(event == AI_INIT) then
                        ai.customData.timer = 1;
                end

                -- 2초마다 실행
                if (event == AI_UPDATE) then
                        -- 200만큼 거리가 멀어지면 주인을 따라감 
                        -- 400만큼 멀어지면 주인의 위치로 순간이동
                        -- ai.SetFollowMaster(true, 200, 400)

                        -- 타겟이 없으면 주인을 따라다님
                        if (ai.GetTargetUnit() == nil) then
                                ai.SetFollowMaster(true, 200, 400)
                        end

                        -- 기본100,200
                        -- ai.SetFollowMaster(true)

                        -- 가장 가까운 적 유닛을 타겟으로 지정
                        ai.SetNearTarget(2, 200) 

                        -- 펫의 타겟이 존재한다면 스킬 사용
                        -- 스킬은 기본적으로 타겟을 향해 발사됨
                        if (ai.GetTargetUnit() ~=nil) then
                                -- 타겟이 정해지면 따라다니는것을 멈춤
                                ai.SetFollowMaster(false)
                                ai.StopMove()

                                -- 타겟이 정해지면 타겟을 따라다니면서 공격
                                ai.MoveToPosition(ai.GetTargetUnit().x,ai.GetTargetUnit().y)
                                -- 주인에게 버프추가
                                ai.AddMasterBuff(15)
                                -- 타겟 방향으로 발사
                                ai.UseSkill(23) 
                                -- 펫의 주인 위치에서 타겟 방향으로 발사
                                ai.UseSkill(
                                22
                                ,nil
                                ,Point(ai.GetMasterUnit().x,ai.GetMasterUnit().y))
                        end

                        -- 커스텀 데이터를 이용한 타이머 6초에 한번씩 주위의 드롭된아이템 획득
                        ai.customData.timer = ai.customData.timer + 1;
                        if (ai.customData.timer == 3) then
                                -- 반경 100의 거리 안에 들어오는 드롭 아이템 획득
                                ai.AcquireNearDropItem(100)
                                ai.customData.timer = 0;
                        end
                end
        end
)
```

## 함수
---

## AcquireNearDropItem(Single)
지정된 거리 내에서 가장 가까운 아이템을 먹는다

#### 선언
```cs
public bool AcquireNearDropItem(float dist = 200F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|dist|탐색할 유닛 거리 (기본값: 200)|

#### 반환
|타입|설명|
|:-|:-|
|System.Boolean|

## AddMasterBuff(Int32)
해당 유닛이 상태를 가지고 있는지 체크합니다.

#### 선언
```cs
public void AddMasterBuff(int buffID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|System.Int32|buffID|

## Distance(Single, Single, Single, Single)
두 유닛 사이의 거리 계산

#### 선언
```cs
public double Distance(float pos1X, float pos1Y, float pos2X, float pos2Y)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|pos1X|1의 좌표 X|
|System.Single|pos1Y|1의 좌표 Y|
|System.Single|pos2X|2의 좌표 X|
|System.Single|pos2Y|2의 좌표 Y|

#### 반환

|타입|설명|
|:-|:-|
|System.Double|

## DistanceSquard(Single, Single, Single, Single)
두 유닛 사이의 거리 계산의 제곱

#### 선언
```cs
public double DistanceSquard(float pos1X, float pos1Y, float pos2X, float pos2Y)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|pos1X|1의 좌표 X|
|System.Single|pos1Y|1의 좌표 Y|
|System.Single|pos2X|2의 좌표 X|
|System.Single|pos2Y|2의 좌표 Y|

#### 반환

|타입|설명|
|System.Double|

## GetMasterUnit()
현재 펫의 주인 유닛을 가져온다.

#### 선언
```cs
public ScriptUnit GetMasterUnit()
```

## 반환

|타입|설명|
|:-|:-|
|ScriptUnit|

## GetTargetUnit()
현재 펫의 타겟 유닛을 가져온다.
(현재 펫이 목표로 삼고 있는 유닛)

#### 선언
```cs
public ScriptUnit GetTargetUnit()
```

#### 반환

|타입|설명|
|ScriptUnit|

## GetTargetUnitID()
현재 펫의 타깃 ID를 가져온다.

#### 선언
```cs
public long GetTargetUnitID()
```

#### 반환

|타입|설명|
|System.Int64|

## MoveToPosition(Single, Single)
펫을 해당 위치로 이동 시킨다.

#### 선언
```cs
public void MoveToPosition(float posx, float posy)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|posx|이동할 위치 X|
|System.Single|posy|이동할 위치 Y|

## SetFollowMaster(Boolean, Single, Single)
플레이어 유닛을 따라 다닐것인지 설정

#### 선언
```cs
public void SetFollowMaster(bool enable, float followDist = 100F, float teleportDist = 200F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Boolean|enable|활성화 (True / False)|
|System.Single|followDist|펫과 플레이어의 거리가 followDist 만큼 떨어졌을 때 펫이 따라다닌다|
|System.Single|teleportDist|펫과 플레이어의 거리가 teleportDist 만큼 떨어졌을 때 플레이어의 위치로 순간이동한다|

## SetNearTarget(Int32, Single)
현재 몬스터가 있는 맵에서 가장 가까운 유닛을 타겟으로 지정한다.

#### 선언
```cs
public void SetNearTarget(int findType = -1, float dist = 200F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|System.Int32|findType|탐색할 유닛 타입 0 : 플레이어, 1 : 이벤트 유닛 , 2 : 적|
|System.Single|dist|탐색할 유닛 거리 (기본값: 200)|

## SetTargetUnit(ScriptUnit)
펫의 타겟을 설정한다

#### 선언
```cs
public void SetTargetUnit(ScriptUnit unit)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|unit|펫의 타겟이 될 유닛|

## SetTargetUnitID(Int64)
유닛 ID로 펫의 타겟을 설정한다

#### 선언
```cs
public void SetTargetUnitID(long unitID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|unitID|펫의 타겟이 될 유닛의 ID|

## StopMove()
이동하는 펫을 멈춘다.

#### 선언
```cs
public void StopMove()
```

## UseSkill(Int32, ScriptPoint, ScriptPoint)
펫이 스킬을 사용한다.

#### 선언
```cs
public void UseSkill(int skillID, ScriptPoint dir = null, ScriptPoint pos = null)
매개 변수(인자)
```

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|skillID|사용할 스킬 ID|
|ScriptPoint|dir|스킬의 방향|
|ScriptPoint|pos|스킬의 시작 위치|

## UseSkillToPosition(Int32, ScriptPoint, ScriptPoint)
펫이 스킬을 사용한다.

#### 선언
```cs
public void UseSkillToPosition(int skillID, ScriptPoint dirPosition = null, ScriptPoint pos = null)
```

## 매개 변수(인자)

|타입|이름|설명|
|System.Int32|skillID|사용할 스킬 ID|
|ScriptPoint|dirPosition|스킬이 나아갈 위치|
|ScriptPoint|pos|스킬의 시작 위치|

