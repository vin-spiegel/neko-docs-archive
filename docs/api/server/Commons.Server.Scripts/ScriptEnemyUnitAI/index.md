---
layout: default
title: ScriptEnemyUnitAI
has_children: true
parent: Commons.Server.Scripts
nav_order: 4
---

# Class ScriptEnemyUnitAI 
{: .d-inline-block }

<!-- New
{: .label .label-green } -->

몬스터의 AI 컨트롤을 나타내는 스크립트 클래스입니다.

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ Commons.Server.Scripts.ScriptUnitAI
　　　↳ ScriptEnemyUnitAI
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptEnemyUnitAI : ScriptUnitAI
```

#### 예제 1: 몬스터 AI 적용 방법
```lua
function customEnemyAI(enemy, ai, event, data)
    -- 최초 몬스터 AI 등록시 실행
    if (event == AI_INIT) then
        ai.customData.test = 1;
    end

    if (event == AI_UPDATE) then
        -- 현재 필드의 유닛들중에서 조건에 해당하는 유닛 반환
        -- 예) 유닛 hp 가 100보다 작은 녀석이 있다면 가져온다
        -- ai.SetTargetUnit(
        --     enemy.field.FindUnit(enemy.x, enemy.y, 200,
        --     function(u)
        --         return u.hp <= 100
        --     end, 0, enemy))
        
        -- 현재 필드의 유닛들중에서 가장 작은 조건에 해당하는 유닛 반환
        -- 예)플레이어 유닛중에서 hp가 가장 적은 녀석을 가지고 온다
        -- ai.SetTargetUnit(
        --     enemy.field.FindMinimumUnit(enemy.x, enemy.y, 200,
        --     function(u)
        --             return u.hp
        --     end, 0, enemy))

        -- 현재 필드의 유닛들중에서 가장 큰 조건에 해당하는 유닛 반환
        -- 예) 플레이어 유닛 중에서 hp가 가장 많은 녀석을 가지고 온다
        -- ai.SetTargetUnit(
        --      enemy.field.FindMaximumUnit(enemy.x, enemy.y, 200,
        --      function(u)
        --          return u.hp
        --      end, 0, enemy))

        -- 타겟이 안 정해졌을 때 가장 가까운 플레이어 타겟으로 지정
        if (ai.GetTargetUnit() == nil) then
            ai.SetNearTarget(0, 200)
        end

        -- 맵에 플레이어가 하나도 없으면 null 세팅
        if (enemy.field.playerCount <= 0) then
            ai.SetTargetUnit(nil)
        -- 타겟이었던 플레이어가 맵을 나가면 타겟 다시 지정
        elseif (enemy.field.GetUnit(ai.GetTargetUnitID()) == nil) then
            ai.SetNearTarget(0, 200)
        end

        -- 타겟이 있을경우 타겟 방향 공격
        ai.UseSkill(22);

        -- 왼쪽 방향 공격
        ai.UseSkill(22, Point(-1, 0))

        -- 오른쪽 방향 공격
        ai.UseSkill(22, Point(1, 0))

        -- 위쪽 방향 공격
        ai.UseSkill(22, Point(0, 1))

        -- 아래쪽 방향 공격
        ai.UseSkill(22, Point(0, -1))

        -- 해당 위치 방향으로 공격
        ai.UseSkillToPosition(24, Point(150, -150))
        
        -- 타겟이 없을경우 예외처리
        if (ai.GetTargetUnit() == nil) then
            return
        end
        
        -- 타겟의 hp에 따른 추적 활성화/비활성화
        if (ai.GetTargetUnit().hp <= 150) then
            ai.SetFollowTarget(false)
        else
            ai.SetFollowTarget(true)
        end
        
    end

    if (event == AI_ATTACKED) then
        enemy.Say('공격당했다. \n데미지: ' .. data.damage 
                    .. '\n스킬ID: '.. data.skillDataID
                    .. '\n크리티컬여부: ' .. (data.critical and 'true' or 'false'))
                
        --공격한 유닛이 없을경우 예외처리
        if (ai.GetAttackedUnit() == nil) then
            return
        end

        -- 공격한 유닛의 hp를 확인해서 100보다 작다면 타겟 변경
        if (ai.GetAttackedUnit().hp <= 100) then
            ai.SetTargetUnit(ai.GetAttackedUnit()) 
        end

    end

    if (event == AI_DEAD) then
        Server.SendSay('죽었다')
        
        -- 죽임을 당한 후 특정 위치에서의 부활
        enemy.RespawnAt(150,-150)
    end
end

Server.SetEnemyAI(
    22, --AI를 적용할 몬스터의 인덱스
    customMonsterAI)
```

#### 예제 2: 선공격 몬스터

```lua
function firstAttack(enemy, ai, event, data)
    if (event == 0) then -- 2초마다 실행되는 이벤트
    
        -- 맵에 플레이어가 하나도 없으면 null 세팅
        if enemy.field.playerCount <= 0 then
            ai.SetTargetUnit(nil)
            
        -- 타겟이 없거나, 기존 타겟이던 unit이 맵을 나갔거나, x값 또는 y값의 차이의 절댓값이 300을 넘어서면
        -- 타겟을 nil로 초기화하고 200 범위 내에서 타겟을 설정
        elseif (ai.GetTargetUnit() == nil)
               or (enemy.field.GetUnit(ai.GetTargetUnitID()) == nil)
               or (math.abs(enemy.x - enemy.field.GetUnit(ai.GetTargetUnitID()).x) >= 300) 
               or (math.abs(enemy.y - enemy.field.GetUnit(ai.GetTargetUnitID()).y) >= 300) then
            
            if ai.GetTargetUnit() ~= nil then
                enemy.say('타겟이 사라졌군..')
            end
            
            ai.SetFollowTarget(false) --타겟이 사라졌으면 추적을 비활성화 
            ai.SetTargetUnit(nil)
            ai.SetNearTarget(0,200)

            -- 주변을 탐색 후 타겟을 찾았으면 (nil이 아니면), 추적을 활성화(true), 메세지출력
            if ai.GetTargetUnit() ~= nil then 
                ai.SetFollowTarget(true) 
                enemy.say('타겟 발견! \n추적 시작!')
            end
        end
        
        --타겟이 있으면 타겟 방향을 향해 10번 스킬을 발사
        if ai.GetTargetUnit() ~= nil then
            ai.UseSkill(10)
        end
        
        --타겟이 없을경우 예외처리
        if ai.GetTargetUnit() == nil then
            return
        end
        
    end
    
    if (event == 1) then -- 몬스터가 공격을 받을때마다 실행되는 이벤트
        -- 공격한 유닛이 없을경우 예외처리
        if ai.GetAttackedUnit() == nil then
            return
        else
            -- 기존 타겟 유닛과 공격 유닛이 같지 않을때, 공격을 한 유닛을 타겟으로 지정 또는 변경하고 추격
            if ai.GetTargetUnit() ~= ai.GetAttackedUnit() then 
                ai.SetTargetUnit(ai.GetAttackedUnit())
                ai.SetFollowTarget(true)
                enemy.say('새로운 공격자를 추적한다..')
            end
            
            -- 몬스터가 공격당할시 10% 확률로 5번 공격 기술을 시전하고 서버 전체에 메세지 출력
            if math.random(0,99) <= 9 then
                ai.UseSkill(5)
                Server.SendCenterLabel('<color=#FF0000>크롸롸!!</color>\n멍청한 보스 배던이 울부짖습니다!')
            end
        end
    end
end
Server.SetMonsterAI(1, firstAttack) -- 1번 몬스터에게 firstAttack 적용
```

## 프로퍼티
---


## 함수
---



