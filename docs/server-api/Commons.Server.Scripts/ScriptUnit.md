---
layout: default
title: ScriptUnit
nav_order: 17
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptUnit 
유닛 클래스입니다.유닛의 모든 정보와 관련된 함수가 집합되어 있습니다.

#### 상속

```
↳ System.Object
    ↳ ScriptObject
        ↳ ScriptUnit
            ↳ ScriptPetUnit
```

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

```cs
Syntax
[MoonSharpUserData]
public class ScriptUnit : ScriptObject
```

## 프로퍼티

## agi
이 유닛의 민첩 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int agi { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## agility

이 유닛의 민첩 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int agility { get; }
```

#### 프로퍼티 값


|타입|설명|
|:-|:-|
|System.Int32|

## atk
이 유닛의 공격력 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int atk { get; }
```

#### 프로퍼티 값


|타입|설명|
|:-|:-|
|System.Int32|

## attack
이 유닛의 공격력 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int attack { get; }
```

#### 프로퍼티 값


|타입|설명|
|:-|:-|
|System.Int32|

## buffs
유닛의 버프를 [] 형식으로 얻어옵니다.

#### 선언
```cs
public ScriptUnitBuff[] buffs { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptUnitBuff[]|

## characterData
유닛의 데이터를 형식으로 얻어옵니다. 
```
유닛의 이름 : characterData.name
유닛의 메모 내용 : characterData.memo
유닛의 이동속도 : characterData.moveSpeed
유닛의 충돌 여부 : characterData.collision
유닛의 점프력 : characterData.jumpForce
```

#### 선언
```cs
public virtual TGameCharacter characterData { get; }
```

#### 프로퍼티 값


|타입|설명|
|:-|:-|
|TGameCharacter|

#### 예제
```lua
-- 유닛의 이름 : string characterData.name
-- 유닛의 메모 내용 : string characterData.memo
-- 유닛의 이동속도 : int characterData.moveSpeed
-- 유닛의 충돌 여부 : bool characterData.collision
-- 유닛의 점프력 : float characterData.jumpForce
```

## characterID
유닛의 캐릭터 ID를 얻어옵니다.

#### 선언
```cs
public virtual int characterID { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## cumulativeEXP
유닛의 누적 경험치를 얻어옵니다.

#### 선언
```cs
public virtual long cumulativeEXP { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|def|이 유닛의 방어력 스탯(능력치)을 얻어옵니다.|

#### 선언
```cs
public int def { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|defense|이 유닛의 방어력 스탯(능력치)을 얻어옵니다.|

#### 선언
```cs
public int defense { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|dirX|이 유닛의 방향 중 X 값을 얻어옵니다.|

#### 선언
```cs
public float dirX { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|dirY|이 유닛의 방향 중 Y 값을 얻어옵니다.|

#### 선언
```cs
public float dirY { get; set; }
```

#### 프로퍼티 값


|타입|설명|
|:-|:-|
|System.Single|exp|유닛의 현재 경험치를 얻어옵니다.|

#### 선언
```cs
public virtual long exp { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|fatigue|유닛의 현재 피로도를 얻어옵니다.|

#### 선언
```cs
public long fatigue { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|field|유닛이 접속해 있는 맵(필드)을 형식으로 얻어옵니다.|

#### 선언
```cs
public ScriptField field { get; }
```

#### 프로퍼티 값


|타입|설명|
|:-|:-|
|ScriptField|

## gameMoney
플레이어 유닛이 가진 골드를 얻어옵니다. 이 유닛이 형식이 아닐 경우 0이 #### 반환됩니다. 또한 값을 설정할 수도 없습니다.

#### 선언
```cs
public long gameMoney { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|hp|유닛의 현재 체력을 얻어옵니다.|

#### 선언
```cs
public long hp { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|	

## id
유닛의 ID를 얻어옵니다.

#### 선언
```cs
public long id { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|	

## initField
유닛이 처음 접속한 맵(필드)을 형식으로 얻어옵니다.

#### 선언
```cs
public ScriptField initField { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptField|

## isGM
이 플레이어가 게임 관리자(마스터)인지 #### 반환합니다

#### 선언
```cs
public bool isGM { get; }
```

#### 프로퍼티 값


|타입|설명|
|:-|:-|
|System.Boolean|	

## job
유닛의 직업을 얻어옵니다.

#### 선언
```cs
public virtual int job { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

## level
유닛의 레벨을 얻어옵니다.

#### 선언
```cs
public virtual int level { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

## lucky
이 유닛의 행운 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int lucky { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## luk
이 유닛의 행운 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int luk { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

## magicAtk
이 유닛의 마법 공격력 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int magicAtk { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

## magicAttack
이 유닛의 마법 공격력 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int magicAttack { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## magicDef
이 유닛의 마법 방어력 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int magicDef { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## magicDefense
이 유닛의 마법 방어력 스탯(능력치)을 얻어옵니다.

#### 선언
```cs
public int magicDefense { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

## mass
유닛의 무게를 얻어옵니다.

#### 선언
```cs
public float mass { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|	

## maxHP
유닛의 최대 체력을 얻어옵니다.

#### 선언
```cs
public long maxHP { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|	

## maxMP
유닛의 최대 마력을 얻어옵니다.

#### 선언
```cs
public long maxMP { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|	

## monsterData
유닛의 몬스터 데이터를 얻어옵니다. 이 유닛이 형식일 경우에만 올바르게 동작합니다. 
```lua
monsterData.name 이름
monsterData.dropMinGameMoney 최소금액
monsterData.dropMaxGameMoney 최대금액
monsterData.dropEXP 지급 경험치
monsterData.memo 메모내용
monsterData.maxHP 최대HP
monsterData.attack 공격력
monsterData.defense 방어력
monsterData.magicAttack 마법공격력
monsterData.magicDefense 마법방어력
monsterData.agility 민첩
monsterData.lucky 운
monsterData.minLevel 최소레벨
monsterData.maxLevel 최대레벨
monsterData.attackType 공격 타입 0 :None 1 : 선공격 2 : 반격
monsterData.moveSpeed 움직임 속도
monsterData.respawnTime 리스폰 시간
monsterData.moveStyle 움직임 타입 0 : 고정 1 : 랜덤
monsterData.collision 충돌여부
monsterData.attackTime 공격 시간
monsterData.teamTag 팀태그
monsterData.consumeFatigue 소모피로도
```

#### 선언
```cs
public TGameMonster monsterData { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|TGameMonster|

#### 예제
```lua
-- string monsterData.name => 이름
-- long monsterData.dropMinGameMoney => 최소 드랍 골드
-- long monsterData.dropMaxGameMoney => 최대 드랍 골드
-- long monsterData.dropEXP => 지급 경험치
-- string monsterData.memo => 메모
-- int monsterData.maxHP => 최대 HP
-- int monsterData.attack => 공격력
-- int monsterData.defense => 방어력
-- int monsterData.magicAttack => 마법 공격력
-- int monsterData.magicDefense => 마법 방어력
-- int monsterData.agility => 민첩
-- int monsterData.lucky => 행운
-- int monsterData.minLevel => 최소 레벨
-- int monsterData. maxLevel => 최대 레벨
-- int monsterData.attackType => 공격 유형 (0: None, 1: 선공격, 2: 반격)
-- int monsterData.moveSpeed => ​​이동 속도
-- int monsterData.respawnTime => 리스폰 시간
-- int monsterData.moveStyle => 이동 유형 (0: 고정, 1: 무작위)
-- bool monsterData .collision => 충돌 여부
-- int monsterData.attackTime => 공격 시간
-- uint monsterData.teamTag => 팀 태그
-- long monsterData.consumeFatigue => 피로도
```

## monsterID
유닛의 몬스터 ID를 얻어옵니다.

#### 선언
```cs
public int monsterID { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

## moveSpeed
유닛의 이동속도를 얻어옵니다.

#### 선언
```cs
public int moveSpeed { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

## mp
유닛의 현재 마력을 얻어옵니다.

#### 선언
```cs
public long mp { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|	

## name
유닛의 이름을 얻어옵니다.

#### 선언
```cs
public string name { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	

## nameColor
유닛 이름의 색을 얻어옵니다.

#### 선언
```cs
public uint nameColor { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.UInt32|	

## party
현재 유닛이 참가한 파티의 데이터를 얻어옵니다.

#### 선언
```cs
public ScriptParty party { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptParty|

## partyID
유닛의 파티 ID를 얻어옵니다.

#### 선언
```cs
public long partyID { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|	

## player
플레이어의 정보를 형식으로 얻어옵니다.

#### 선언
```cs
public ScriptRoomPlayer player { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptRoomPlayer|

## teamTag
유닛의 팀 태그를 얻어옵니다. (팀 태그를 `AND` 연산하여 동맹 여부를 파악할 수 있습니다.
하나라도 `AND` 되는 비트가 있을 시 동맹)

#### 선언
```cs
public uint teamTag { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.UInt32|	

#### 예제
```lua
-- 팀 태그를 AND 연산하여 동맹 여부를 파악할 수 있습니다.
-- (하나라도 AND 되는 비트가 있을 시 동맹)
```
## type
유닛의 종류(타입)를 얻어옵니다. 
0 = 플레이어
1 = 이벤트
2 = 몬스터

#### 선언
```cs
public int type { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|x|이 유닛의 위치 중 X 값을 얻어옵니다. (이 유닛의 X 좌표를 반환합니다)|

#### 선언
```cs
public float x { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|

## y
이 유닛의 위치 중 Y 값을 얻어옵니다. (이 유닛의 Y 좌표를 반환합니다)

#### 선언
```cs
public float y { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|	

## 함수
---

## AddBuff(Int32, ScriptUnit)
해당 유닛에 상태(Buff)를 추가합니다.

#### 선언
```cs
public void AddBuff(int buffID, ScriptUnit attacker = null)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|buffID|상태(Buff) ID|
|ScriptUnit|attacker|공격한 유닛|

#### 예제: 유닛에게 5번 버프를 추가
```lua
unit.AddBuff(5)
```

# AddDamage(Int32, Int32, Boolean)
이 유닛에게 피해(데미지)를 입힙니다. (공격자가 존재하지 않기 때문에 보상이 지급되지 않습니다)

#### 선언
```cs
public void AddDamage(int damage, int skillDataID = -1, bool critical = false)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|damage|피해량(데미지)|
|System.Int32|skillDataID|스킬의 공식을 사용시 공식을 적용할 스킬의 ID (기본값: -1(공식 미적용))|
|System.Boolean|critical|치명타(크리티컬)의 발생 유무|

#### 예제: 유닛에게 데미지 999를 입힙니다
```lua
unit.AddDamage(999)
```

## AddDamageBy(ScriptUnit, Int32, Int32, Boolean)
이 유닛에게 피해(데미지)를 입힙니다. (데미지를 받은 대상이 몬스터일 경우 보상이 지급됩니다)

#### 선언
```cs
public void AddDamageBy(ScriptUnit attacker, int damage, int skillDataID = -1, bool critical = false)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|attacker|공격자|
|System.Int32|damage|피해량(데미지)|
|System.Int32|skillDataID|스킬의 공식을 사용시 공식을 적용할 스킬의 ID (기본값: -1(공식 미적용))|
|System.Boolean|critical|치명타(크리티컬)의 발생 유무|

## AddEXP(Int64)
유닛에게 경험치를 지급합니다.

#### 선언
```cs
public virtual void AddEXP(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|지급할 경험치의 양|

#### 예제: 유닛에게 10000 경험치 지급
```lua
unit.AddEXP(10000)
```
## AddFatigue(Int64)
플레이어 유닛에게 피로도를 채워줍니다.

#### 선언
```cs
public void AddFatigue(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|채워줄 피로도의 양|

#### 예제: 유닛의 피로도를 10000 채웁니다
```lua
unit.AddFatigue(10000)
```
## AddGameMoney(Int64)
유닛에게 골드를 지급합니다.

#### 선언
```cs
public void AddGameMoney(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|지급할 골드의 양|

#### 예제: 유닛에게 10000 골드 지급
```lua
unit.AddGameMoney(10000)
```

## AddHP(Int64)
해당 유닛의 HP를 회복시킵니다.

#### 선언
```cs
public void AddHP(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|회복시킬 HP의 양|

#### 예제: 유닛의 HP를 500 회복
```lua
unit.AddHP(500)
```
## AddItem(Int32, Int32, Boolean)
유닛에 아이템을 추가합니다.

#### 선언
```cs
public void AddItem(int dataID, int count = 1, bool notify = true)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 아이템 ID|
|System.Int32|count|추가할 수량 (기본값: 1)|
|System.Boolean|notify|아이템 획득시에 알림을 사용할 것인지를 나타냅니다 (기본값: True) `Center Label` 형식으로 알림이 표기됩니다.|

#### 예제
```lua
-- 0번 ID의 아이템을 1개 추가하며 알림을 표시합니다.
unit.AddItem(0, 1, true)

-- 1번 ID의 아이템을 2개 추가하며 알림을 표시하지 않습니다.
unit.AddItem(1, 2)
```

## AddItemByTItem(TItem, Boolean)
유닛에게 형식으로 아이템을 지급합니다.

#### 선언
```cs
public bool AddItemByTItem(TItem item, bool notify = true)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|TItem|item|형식의 아이템|
|System.Boolean|notify|아이템 획득시에 알림을 사용할 것인지를 나타냅니다.(기본적으로 Center Label 형식으로 알림이 표기됩니다)|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

## AddMP(Int64)
해당 유닛의 MP를 회복시킵니다.

#### 선언
```cs
public void AddMP(long amount)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|회복시킬 MP의 양|

#### 예제: 유닛의 MP를 500 회복
```lua
unit.AddMP(500)
```
## AddPet(Int32, Int32, String)
신규 펫을 추가 등록하고 등록된 ID를 가져옵니다. 
- 등록이 실패할 경우 `-1`을 리턴합니다.

#### 선언
```cs
public int AddPet(int characterID = 0, int jobID = 0, string name = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|characterID|펫의 캐릭터 ID (기본값: 0)|
|System.Int32|jobID|펫의 직업 ID (기본값: 0)|
|System.String|name|펫의 이름 (기본값: 펫 캐릭터의 이름)|

#### 반환
|타입|설명|
|:-|:-|
|System.Int32|등록된 펫의 ID(등록 실패시 -1)|

## AddSkill(Int32, Int32, Boolean)
플레이어 유닛에게 스킬을 추가합니다.

#### 선언
```cs
public void AddSkill(int dataID, int level = 1, bool notify = true)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 스킬 ID|
|System.Int32|level|스킬의 레벨 (기본값: 1)|
|System.Boolean|notify|스킬 획득시에 알림을 사용할 것인지를 나타냅니다 (기본값: True) `Center Label` 형식으로 알림이 표기됩니다.|

#### 예제
```lua
-- 유닛에게 10레벨의 3번 스킬을 추가하며 알림을 표시합니다
unit.AddSkill(3, 10, true)

-- 유닛에게 5레벨의 7번 스킬을 추가하며 알림을 표시하지 않습니다
unit.AddSkill(7, 5, false)
``` 
## 참고 항목
---

## AddItem(Int32, Int32, Boolean)

## CancelPetSummon()
펫의 소환을 해제합니다.

#### 선언
```cs
public void CancelPetSummon()
```
#### 예제: 현재 소환하고 있는 펫을 소환 해제하기
```lua
unit.CancelPetSummon()
```
## ClearAllBuffs(Boolean)
해당 유닛의 버프를 모두 제거합니다.

#### 선언
```cs
public void ClearAllBuffs(bool clearBuffAnimations = true)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Boolean|clearBuffAnimations|버프 애니메이션을 중단할 것인지|

## ClearBuffAnimations()
해당 유닛의 버프 애니메이션을 모두 제거합니다.

#### 선언
```cs
public void ClearBuffAnimations()
```

## CountItem(Int32)
아이템의 ID를 통해 유닛이 해당 아이템을 몇개나 소유하고 있는지 알아옵니다.

#### 선언
```cs
public int CountItem(int dataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 아이템 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|유닛이 가지고 있던 아이템의 개수 (가지고 있지 않았다면 0을 반환합니다)|

#### 예제: 유닛이 5번 아이템을 몇개나 가지고 있는지 출력합니다
```lua
local cnt = unit.CountItem(5)
unit.SendCenterLabel("5번 아이템의 갯수: " .. cnt)
```
## DropItem(Int64, Int32)
유닛이 가지고있는 아이템을 땅에 떨어뜨립니다 (드랍합니다).

#### 선언
```cs
public void DropItem(long id, int count = 1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|id|제거할 아이템의 ID.데이터 베이스의 아이템ID 가 아닌 아이템만의 유니크 ID 입니다.|
|System.Int32|count|개수|

#### 예제
```lua
-- 유저 인벤토리에 있는 드랍 가능한 아이템 전부 드랍하기

local items = unit.player.GetItems()

for i = 1, #items do
    if items[i] ~= nil then
        unit.DropItem(items[i].id)
    end
end
```

## DropItemByDataID(Int32, Int32)
유닛이 가지고있는 아이템을 땅에 떨어뜨립니다 (드랍합니다).

#### 선언
```cs
public void DropItemByDataID(int dataID, int count = 1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 아이템 ID|
|System.Int32|count|개수|

#### 예제: 유저 인벤토리에 있는 데이터베이스상 5번 아이템을 1개 드랍하기
```lua
unit.DropItemByDataID(5, 1)
```
## EquipItem(Int64, Boolean)
유닛에 아이템을 장착시킵니다. (이 유닛이 가지고 있는 아이템만 장착이 가능합니다.)

#### 선언
```cs
public void EquipItem(long itemID, bool forced = false)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|itemID|아이템의 고유 ID (데이터 베이스의 ID 와는 다릅니다)|
|System.Boolean|forced|

#### 예제: 유닛에게 5번 아이템 장착시키기
```lua
unit.EquipItem(5)
```

## FireEvent(String, Object[])
클라이언트에게 해당 주제(Topic)로 이벤트를 발생시킵니다.

#### 선언
```cs
public void FireEvent(string topic, params object[] arguments)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|topic|보낼 주제(Topic)|
|System.Object[]|arguments|함께 전송할 인자(Argument)들|

#### 예제
```lua
-- ScriptServer.FireEvent() 와 사용법이 같지만
-- 해당 메서드는 이 플레이어에게만 이벤트를 보낸다
```

### GetAllRegistedPetData()
등록된 펫들의 데이터를 [] 형식으로 반환합니다.

#### 선언
```cs
public TOnlinePetData[] GetAllRegistedPetData()
```

#### 반환

|타입|설명|
|:-|:-|
|TOnlinePetData[]|등록된 펫들의 데이터가 담긴 [] 형식 배열|

## GetEquipItem(Int32)
해당 슬롯에 장착되어있는 아이템의 정보를 가져옵니다.

#### 선언
```cs
public TItem GetEquipItem(int equipSlot)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|equipSlot|장착 슬롯 (0 ~ 9)|

#### 반환
|타입|설명|
|:-|:-|
|TItem|형식의 아이템 정보|

#### 예제: 유닛이 장착중인 모자의 이름 출력하기
```lua
local item = unit.GetEquipItem(0)

if item ~= nil then
    local itemData = Server.GetItem(item.dataID)
    unit.SendCenterLabel(itemData.name)
else
    unit.SendCenterLabel("모자가 장착되지 않았습니다")
end
```
## GetRegistedPetDataByPetID(Int32)
등록된 펫의 데이터를 형식으로 반환합니다.

#### 선언
```cs
public TOnlinePetData GetRegistedPetDataByPetID(int petID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|petID|펫 ID|

#### 반환

|타입|설명|
|:-|:-|
|TOnlinePetData|등록된 펫의 데이터가 담긴 형식|

## GetRegistedPetID()
등록된 펫들의 ID를 `[]` 형식으로 반환합니다.

#### 선언
```cs
public int[] GetRegistedPetID()
```

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|[]|등록된 펫들의 ID가 담긴 [] 형식 배열|

#### 예제: 현재 등록된 펫들의 ID를 차례대로 모두 출력
```lua
local petIdList = unit.GetRegistedPetID()

for i = 1, #petIdList do
    if petIdList[i] ~= nil then
        unit.SendCenterLabel(petIdList[i])
    end
end
```

## GetSingleSummonedPet()
현재 소환 중인 펫을 가져옵니다.

#### 선언
```cs
public ScriptPetUnit GetSingleSummonedPet()
```
#### 반환

|타입|설명|
|:-|:-|
|ScriptPetUnit|펫 유닛을 형식으로 반환합니다.|

#### 예제: 현재 소환되어있는 펫 유닛을 가져와 이름 출력
```lua
local myPet = unit.GetSingleSummonedPet()

if myPet == nil then
    unit.SendCenterLabel("소환된 펫이 없습니다")
    return
end

unit.SendCenterLabel("현재 소환된 펫 이름: " .. myPet.name)
```

## GetSkill(Int32)
스킬의 ID를 통해 유닛의 스킬을 얻어옵니다.

#### 선언
```cs
public TSkill GetSkill(int dataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|network.TSkill|스킬을 형식으로 반환합니다.|

#### 예제: 유닛이 가진 스킬 중 데이터베이스 상 5번 스킬의 스킬 레벨을 출력
```lua
local skillInfo = unit.GetSkill(5)

if skillInfo == nil then
    unit.SendCenterLabel("5번 스킬이 없습니다")
else
    unit.SendCenterLabel('5번 스킬의 레벨: ' .. skillInfo.level)
end
```

## GetSkillLevel(Int32)
스킬의 ID를 통해 유닛의 해당 스킬 레벨을 알아옵니다.

#### 선언
```cs
public int GetSkillLevel(int dataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|스킬의 레벨 (스킬이 존재하지 않는다면 `-1`을 반환합니다)|

#### 예제
```lua
-- 유닛이 가진 스킬 중 데이터베이스 상 5번 스킬의 스킬 레벨을 출력
-- 스킬이 없다면 -1 반환

local skillLvl = unit.GetSkillLevel(5)
unit.SendCenterLabel(skillLvl)
```

## GetStat(Int32)
유닛의 능력치(스탯)을 얻어옵니다. 
```
ATTACK = 0
DEFENSE = 1
MAGIC_ATTACK = 2
MAGIC_DEFENSE = 3
AGILITY = 4
LUCKY = 5
HP = 6
MP = 7

[사용자 설정 능력치 (커스텀 스탯)] CUSTOM_1 = 101
...
CUSTOM_32 = 132
```
#### 선언
```cs
public float GetStat(int type)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|type|해당 스탯()의 타입|

#### 반환

|타입|설명|
|:-|:-|
|System.Single|	

#### 예제
```lua
-- ATTACK = 0
-- DEFENSE = 1
-- MAGIC_ATTACK = 2
-- MAGIC_DEFENSE = 3
-- AGILITY = 4
-- LUCKY = 5
-- HP = 6
-- MP = 7

-- [사용자 설정 능력치 (커스텀 스탯)]

-- CUSTOM_1 = 101
-- ...
-- CUSTOM_32 = 132


-- HP 가져오기
local unitHP = unit.GetStat(6)
-- Lucky 가져오기
local unitLucky = unit.GetStat(5)
```
## GetStringVar(Int32)
유닛의 문자열 변수 값을 얻어옵니다.

#### 선언
```cs
public string GetStringVar(int id)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.String|해당 변수의 값|

#### 예제: 유닛의 16번 문자열 변수를 출력
```lua
unit.SendCenterLabel(unit.GetStringVar(16))
```

## GetVar(Int32)
유닛의 변수 값을 얻어옵니다.

#### 선언
```cs
public long GetVar(int id)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int64|해당 변수의 값|

#### 예제: 유닛의 32번 변수를 출력
```lua
unit.SendCenterLabel(unit.GetVar(32))
```

## HasBuff(Int32)
해당 유닛이 상태(Buff)를 가지고 있는지 체크합니다.

#### 선언
```cs
public bool HasBuff(int buffID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|buffID|상태(Buff) ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|	

#### 예제: 유닛이 5번 버프를 가지고 있는지 검사
```lua
if unit.HasBuff(5) then
    unit.SendCenterLabel("5번 버프가 있다")
else
    unit.SendCenterLabel("5번 버프가 없다");
end
```
## HasSkill(Int32)
스킬의 ID를 통해 유닛의 스킬 유무를 알아옵니다.

#### 선언
```cs
public bool HasSkill(int dataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 스킬 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|스킬의 존재 유무 (있음: True, 없음: False)|

#### 예제: 유닛이 5번 스킬을 가지고 있는지 검사
```lua
if unit.HasSkill(5) then
    unit.SendCenterLabel("5번 스킬을 가지고 있습니다")
else
    unit.SendCenterLabel("5번 스킬이 없습니다")
end
```

## IsCollectionCompleted(Int32)
유닛이 해당 도감의 요소를 완료했는지를 반환합니다.

#### 선언
```cs
public bool IsCollectionCompleted(int collectionDataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|collectionDataID|데이터베이스의 도감 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|완료 여부 (완료: True, 미완료: False)|

#### 예제: 5번 도감이 완성되었는치 출력하기
```lua
if unit.IsCollectionCompleted(5) then
    unit.SendCenterLabel("5번 도감이 완성되어 있음")
else
    unit.SendCenterLabel("5번 도감이 미완성")
end
```
## IsEquippedItem(Int64)
유닛이 해당 아이템을 장착 중인지 알아냅니다.

#### 선언
```cs
public bool IsEquippedItem(long itemID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|itemID|아이템의 고유 ID (데이터 베이스의 ID 와는 다릅니다)|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|장착 여부 (장착 중일시: True, 아닐 시: False)|

#### 예제: 유닛의 인벤토리를 돌며 장착 중인 아이템 알려주기
```lua
local inven = unit.player.GetItems()

for i = 1, #inven do
    if inven[i] ~= nil then
        local itemData = Server.GetItem(inven[i].dataID)
        if unit.IsEquippedItem(inven[i].id) then
            unit.SendSay(i .. "." .. itemData.name .. ": 장착 중")
        else
            unit.SendSay(i .. "." .. itemData.name .. ": 미장착")
        end    
    end
end
```
## IsEquippedItemByDataID(Int32)
유닛이 해당 아이템을 장착 중인지 알아냅니다.

#### 선언
```cs
public bool IsEquippedItemByDataID(int itemDataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|itemDataID|데이터 베이스의 아이템 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|장착 여부 (장착 중일시: True, 아닐 시: False)|

#### 예제: 5번 아이템을 장착했는지 출력하기
```lua
if unit.IsEquippedItemByDataID(5) then
    unit.SendCenterLabel("5번 아이템 장착 중")
else
    unit.SendCenterLabel("5번 아이템 장착하지 않음")
end
```

## KnockbackFromUnit(ScriptUnit, Single, Single)
유닛에게 밀치기(넉백 Knock-back)를 적용합니다.
(밀친 대상의 유닛으로부터 멀어집니다)

#### 선언
```cs
public void KnockbackFromUnit(ScriptUnit from, float distance, float time = 0.5F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|from|밀친 대상|
|System.Single|distance|적용 거리|
|System.Single|time|적용 시간 (짧을수록 빠르게 밀어냅니다) (기본값: 0.5)|

#### 예제: 공격한 대상 나를 기준으로 밀치기
```lua
-- 해당 예제는 데미지 공식에서 사용되는 공식을 예제로 들었습니다

-- 방어자를 공격자로부터 0.5초간 2칸 만큼 밀어낸다
b.KnockbackFromUnit(a, 64, 0.5)
```
## LeaveField()
해당 필드를 떠납니다.

#### 선언
```cs
public void LeaveField()
```

## MakeKnockback(Single, Single)
유닛에게 밀치기(넉백 Knock-back)를 적용합니다.

#### 선언
```cs
public void MakeKnockback(float distance, float time)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|distance|적용 거리|
|System.Single|time|적용 시간 (짧을수록 빠르게 밀어냅니다)|

#### 예제: 유닛을 2초간 64(2칸) 만큼 넉백시키기
```lua
unit.MakeKnockback(64, 2)
```

## MakeSturn(Single)
유닛에게 스턴(Stun)을 적용시킵니다.

#### 선언
```cs
public void MakeSturn(float time)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|time|적용시간|

#### 예제: 유닛을 3초간 스턴시키기
```lua
unit.MakeSturn(3)
```

## PlayME(String, Single)
해당 ME를 재생합니다.

#### 선언
```cs
public void PlayME(string meID, float volume = 1F)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|meID|ME 이름|
|System.Single|volume|볼륨|

#### 예제: 유닛에게 ME 를 재생시킨다
```lua
unit.PlayME("MyMusicFile.ogg", 1.0)
```

## PlaySE(String, Single)
해당 SE를 재생합니다.

#### 선언
```cs
public void PlaySE(string seName, float volume = 1F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|seName|SE 이름|
|System.Single|volume|볼륨|

#### 예제: 유닛에게 SE 를 재생시킨다
```lua
unit.PlaySE("MyMusicFile.ogg", 1.0)
```

## PullFromUnit(ScriptUnit, Single, Single)
유닛에게 당기기를 적용합니다.(당긴 대상 유닛에게 끌려갑니다)

#### 선언
```cs
public void PullFromUnit(ScriptUnit from, float distance = 0F, float time = 0.5F)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|from|당긴 대상|
|System.Single|distance|간격 (0 일경우 완전히 내 위치까지 당겨집니다) (기본값: 0)|
|System.Single|time|적용 시간 (짧을수록 빠르게 당깁니다) (기본값: 0.5)|

#### 예제: 공격한 대상을 나를 기준으로 당겨오기
```lua
-- 해당 예제는 데미지 공식에서 사용되는 공식을 예제로 들었습니다

-- 방어자를 공격자 위치에서 0칸 떨어진 곳까지 0.5초간 당겨온다
b.PullFromUnit(a, 0, 0.5)
```

## RefreshStats()
유닛의 모든 능력치(스탯)를 다시 계산합니다.

#### 선언
```cs
public void RefreshStats()
```
#### 예제
```lua
-- 유닛의 능력치(스탯) 갱신하기

unit.RefreshStats()
```
## RemoveAllSkills()
유닛의 모든 스킬을 제거합니다.

#### 선언
```cs
public void RemoveAllSkills()
```
#### 예제: 유닛의 모든 스킬들을 삭제
```lua
unit.RemoveAllSkills()
```
## RemoveBuff(Int32)
해당 유닛의 상태(Buff)를 제거합니다.

#### 선언
```cs
public void RemoveBuff(int buffID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|buffID|상태(Buff) ID|

#### 예제: 유닛에서 5번 버프를 제거
```lua
unit.RemoveBuff(5)
```
## RemoveCollection(Int32)
도감을 삭제하고, 삭제에 성공했는지를 반환합니다.

#### 선언
```cs
public bool RemoveCollection(int collectionDataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|collectionDataID|데이터베이스의 도감 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|삭제 성공 여부 (성공: True, 실패: False)|

#### 예제: 유닛의 5번 도감 완료 이력을 삭제하기
```lua
unit.RemoveCollection(5)
```

## RemoveItem(Int32, Int32, Boolean, Boolean, Boolean)
플레이어 유닛으로부터 아이템을 제거합니다.

#### 선언
```cs
public bool RemoveItem(int dataID, int count = 1, bool notify = true, bool atomic = false, bool equippedItemExclude = false)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|제거할 아이템의 데이터베이스 아이템 ID|
|System.Int32|count|제거할 아이템의 개수|
|System.Boolean|notify|아이템을 제거했을때 공지를 사용할 것인지를 나타냅니다.|
|System.Boolean|atomic|이 인자가 활성화 되었을 때 제거할 아이템의 개수보다 가지고 있는 아이템의 개수가 적으면 false를 반환하고 함수를 종료합니다.|
|System.Boolean|equippedItemExclude|장착 중인 아이템은 제거 대상에서 제외할지를 나타냅니다.|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|	

#### 예제: 유닛의 인벤토리에서 데이터베이스 상 5번 아이템을 1개 제거합니다
```lua
unit.RemoveItem(5, 1)
```

## RemoveItemByID(Int64, Int32, Boolean, Boolean, Boolean)
플레이어 유닛으로부터 아이템을 제거합니다.

#### 선언
```cs
public bool RemoveItemByID(long id, int count = 1, bool notify = true, bool atomic = false, bool equippedItemExclude = false)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|id|제거할 아이템의 ID.데이터 베이스의 아이템ID 가 아닌 아이템만의 유니크 ID 입니다.|
|System.Int32|count|제거할 아이템의 개수|
|System.Boolean|notify|아이템을 제거했을때 공지를 사용할 것인지를 나타냅니다.|
|System.Boolean|atomic|이 인자가 활성화 되었을 때 제거할 아이템의 개수보다 가지고 있는 아이템의 개수가 적으면 false를 반환하고 함수를 종료합니다.|
|System.Boolean|equippedItemExclude|장착 중인 아이템은 제거 대상에서 제외할지를 나타냅니다.|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|	

#### 예제: 유닛의 인벤토리에서 ID: 5 인 아이템을 1개 제거합니다
```lua
unit.RemoveItem(5, 1)
```

## RemoveSkill(Int32)
스킬의 ID를 통해 유닛의 스킬을 제거합니다.

#### 선언
```cs
public void RemoveSkill(int dataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스상에서의 스킬 ID|

#### 예제: 유닛의 스킬 중 데이터베이스상 5번 스킬을 삭제하기
```lua
unit.RemoveSkill(5)
```

## RespawnAt(Single, Single)
지정된 좌표를 이용해서 유닛을 부활시킵니다.

#### 선언
```cs
public void RespawnAt(float x, float y)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|부활할 위치의 X 좌표|
|System.Single|y|부활할 위치의 Y 좌표|

#### 예제: 100, 200 위치에 유닛 부활시키기
```lua
unit.RespawnAt(100, 200)
```

## Say(String, UInt32)
해당 유닛이 말하게 합니다.

#### 선언
```cs
public void Say(string text, uint color = 4294967295U)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|말(텍스트)|
|System.UInt32|color|텍스트의 색 (기본값: 검정)|

#### 예제: 이 유닛이 "Hello Nekoland!" 라고 말하게 하기
```lua
unit.Say("Hello Nekoland!")

-- 빨간색
unit.Say("Hello Nekoland! (Red)", 0xFF0000)
-- 초록색
unit.Say("Hello Nekoland! (Green)", 0x00FF00)
-- 파란색
unit.Say("Hello Nekoland! (Blue)", 0x0000FF)
```

## SendCenterLabel(String)
해당 유닛의 화면 중심에 라벨을 표시합니다.(Center Label을 생성합니다.)

#### 선언
```cs
public void SendCenterLabel(string text)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|라벨에 표기할 말(텍스트)|

#### 예제: 유닛의 플레이어 화면 가운데 "Welcome to Nekoland!" 표시하기
```lua
unit.SendCenterLabel("Welcome to Nekoland!")
```

## SendSay(String, UInt32)
이 플레이어 유닛의 채팅창에만 추가되는 텍스트를 씁니다.

#### 선언
```cs
public void SendSay(string text, uint color = 4294967295U)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|말(텍스트)|
|System.UInt32|color|텍스트의 색 (기본값: 검정)|

#### 예제: 이 유닛의 `채팅창`에 "Welcome to Nekoland!" 라고 나오게 하기
```lua
unit.SendSay("Welcome to Nekoland!")
-- 빨간색
unit.SendSay("Welcome to Nekoland! (Red)", 0xFF0000)
-- 초록색
unit.SendSay("Welcome to Nekoland! (Green)", 0x00FF00)
-- 파란색
unit.SendSay("Welcome to Nekoland! (Blue)", 0x0000FF)
```
## SendUpdated(Boolean)
유닛의 정보를 갱신합니다.

#### 선언
```cs
public void SendUpdated(bool fixPosition = false)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Boolean|fixPosition|

#### 예제: 유닛이 갱신되었음을 클라이언트에게 알림
```lua
unit.SendUpdated()
```

## SerVar(Int32, Int64)
유닛의 변수 값을 설정합니다. 최대 65535 바이트까지 저장 가능합니다.

#### 선언
```cs
public void SerVar(int id, long value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.Int64|value|해당 변수의 값|

#### 예제
```lua
-- 사용을 권장하지 않습니다. ScriptUnit.SetVar() 함수를 사용하세요
```

## SetJob(Int32, Boolean)
직업 ID를 통해 유닛의 직업을 설정합니다.

#### 선언
```cs
public virtual void SetJob(int jobID, bool keepSkills = false)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|jobID|데이터 베이스의 직업 ID|
|System.Boolean|keepSkills|스킬의 유지 (기본값: True)|

#### 예제: 스킬을 유지하며 5번 직업으로 변경
```lua
unit.SetJob(5, true)

-- 스킬을 유지하지 않으면서 2번 직업으로 변경
unit.SetJob(2, false)
```
## SetPetUnit(ScriptUnit)
유닛의 펫을 설정합니다.

#### 선언
```cs
public void SetPetUnit(ScriptUnit pet)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|pet|형식의 펫 유닛|

## SetQuickSlot(Int32, Int32, Int32)
퀵슬롯에 등록될 아이템 및 스킬을 설정합니다.

#### 선언
```cs
public void SetQuickSlot(int type, int slotID, int dataID = -1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|type|0 : Clear, 1 : Item, 2 : Skill|
|System.Int32|slotID|0~7|
|System.Int32|dataID|데이타베이스 ID|

#### 예제: 유닛의 퀵슬롯 설정
```lua
-- 유닛의 0번 퀵슬롯을 비운다
unit.SetQuickSlot(0, 0)

-- 유닛의 1번 퀵슬롯에 3번 스킬을 올려둔다
unit.SetQuickSlot(2, 1, 3)

-- 유닛의 2번 퀵슬롯에 ID:5 인 아이템을 올려둔다
unit.SetQuickSlot(1, 2, 5)
```

## SetSkillLevel(Int32, Int32)
유닛의 스킬 레벨을 설정합니다.

#### 선언
```cs
public bool SetSkillLevel(int dataID, int level)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 스킬 ID|
|System.Int32|level|변경할 레벨|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|스킬 레벨 설정의 성공 여부 (성공시: True, 실패시: False)|

#### 예제
```lua
-- 유닛이 가진 스킬 중 데이터베이스 상 5번 스킬의 스킬 레벨을 10으로 설정

unit.SetSkillLevel(5, 10)
```
## SetStat(Int32, Single)
유닛의 스탯 값을 변경합니다.

#### 선언
```cs
public void SetStat(int type, float value)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|	type	|해당 스탯()의 타입|
|System.Single|	value	|변경할 값|

#### 예제
```lua
-- ATTACK = 0
-- DEFENSE = 1
-- MAGIC_ATTACK = 2
-- MAGIC_DEFENSE = 3
-- AGILITY = 4
-- LUCKY = 5
-- HP = 6
-- MP = 7

-- [사용자 설정 능력치 (커스텀 스탯)]

-- CUSTOM_1 = 101
-- ...
-- CUSTOM_32 = 132


-- HP를 999로 설정
unit.SetStat(6, 999)

-- ATTACK을 100으로 설정
unit.SetStat(0, 100)
```
## SetStringVar(Int32, String)
유닛의 문자열 변수 값을 설정합니다. 최대 65535 바이트까지 저장 가능합니다.

#### 선언
```cs
public bool SetStringVar(int id, string value)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.String|value|해당 변수의 값|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|	

#### 예제
```lua
-- 유닛의 16번 문자열 변수를 "Hello Unit!" 로 설정

unit.SetStringVar(16, "Hello Unit!")
```

## SetVar(Int32, Int64)
유닛의 변수 값을 설정합니다. 최대 65535 바이트까지 저장 가능합니다.

#### 선언
```cs
public void SetVar(int id, long value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.Int64|value|해당 변수의 값|

#### 예제
```lua
-- 유닛의 32번 변수를 64로 설정

unit.SetVar(32, 64)
ShowAnimation(Int32)
해당 유닛의 위치에 애니메이션을 재생합니다.

#### 선언
```cs
public void ShowAnimation(int animationID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|animationID|애니메이션의 ID|

#### 예제
```lua
-- 유닛에서 5번 애니메이션을 재생합니다

unit.ShowAnimation(5)
```
## SpawnAt(Single, Single)
지정된 좌표를 이용해서 유닛을 소환합니다.

#### 선언
```cs
public void SpawnAt(float x, float y)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|소환할 위치의 X 좌표|
|System.Single|y|소환할 위치의 Y 좌표|

#### 예제
```lua
-- 유닛을 100, 100에 소환시킨다

unit.SpawnAt(100, 100)
```
## SpawnAtField(Field, Single, Single)
형식의 필드에 지정된 좌표를 이용해서 유닛을 소환합니다.

#### 선언
```cs
public void SpawnAtField(Field f, float x, float y)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|Commons.Server.Field|f|형식의 필드|
|System.Single|x|소환할 위치의 X 좌표|
|System.Single|y|소환할 위치의 Y 좌표|

## SpawnAtFieldID(Int32, Single, Single, Int32)
필드의 ID를 이용해서 지정된 좌표에 유닛을 소환합니다.

#### 선언
```cs
public void SpawnAtFieldID(int mapID, float x, float y, int channelID = 0)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|mapID|소환할 필드의 ID|
|System.Single|x|소환할 위치의 X 좌표|
|System.Single|y|소환할 위치의 Y 좌표|
|System.Int32|channelID|소환할 위치의 Y 좌표|

#### 예제: 15번 맵의 1번 채널에 유닛 이동 시키기
```lua
unit.SpawnAtFieldID(15,4*15,4*16,1)
```
## SpawnPet(Int32, Single, Single, Int32, Int32, String)
펫을 소환합니다. 
- 같은 ID로 이미 소환되었던 경우 해당 펫의 정보로 소환됩니다.
- 소환되었던 이력이 없는 경우 해당 ID로 등록 후 소환됩니다.

#### 선언
```cs
public bool SpawnPet(int petID, float posX, float posY, int characterID = 0, int jobID = 0, string name = null)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|petID|소환할 펫의 ID|
|System.Single|posX|소환할 위치의 X 좌표|
|System.Single|posY|소환할 위치의 Y 좌표|
|System.Int32|characterID|신규 등록시 펫의 캐릭터 ID (기본값: 0)|
|System.Int32|jobID|신규 등록시 펫의 직업 ID (기본값: 0)|
|System.String|name|신규 등록시 펫의 이름 (기본값: 펫 캐릭터의 이름)|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|펫 소환 성공여부(성공: True, 실패: False)|

## StartGlobalEvent(Int32)
플레이어 유닛의 공용 이벤트를 시작합니다.

#### 선언
```cs
public void StartGlobalEvent(int id)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|공용 이벤트의 ID|

#### 예제: 유닛에서 5번 공용 이벤트 실행
```lua
unit.StartGlobalEvent(5)
```
## StopAnimation(Int32)
해당 유닛이 재생 중이던 애니메이션을 중단합니다.

#### 선언
```cs
public void StopAnimation(int animationID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|animationID애니메이션의 ID|

#### 예제: 유닛에서 실행 중이던 5번 애니메이션 실행 종료시키기
```lua
unit.StopAnimation(5)
```

## UnequipItem(Int64)
유닛의 장착중인 아이템을 장착 해제합니다.

#### 선언
```cs
public void UnequipItem(long itemID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|itemID|아이템의 고유 ID (데이터 베이스의 ID 와는 다릅니다)|

#### 예제: 유닛이 장착 중인 5번 아이템 장착 해제시키기
```lua
unit.UnequipItem(5)
```
## UnregisterPet(Int32)
펫의 ID를 통해 펫의 등록을 해제합니다.

#### 선언
```cs
public void UnregisterPet(int petID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|petID|등록 해제할 펫의 ID|

#### 예제: 0번 ID로 등록된 펫 등록 해제하기
```lua
-- Note: SpawnPet 함수로 펫을 소환할 떄 입력했던 펫 ID

unit.UnregisterPet(0)
```
## UseFatigue(Int64)
플레이어 유닛의 피로도를 사용합니다.

#### 선언
```cs
public bool UseFatigue(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|사용할 피로도의 양|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제
```lua
-- 유닛의 피로도를 100 사용합니다

unit.UseFatigue(100)
```

## UseGameMoney(Int64)
플레이어 유닛의 게임 골드를 사용합니다.

#### 선언
```cs
public bool UseGameMoney(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|사용할 골드의 양|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제: 유닛의 골드를 10000만큼 제거합니다
```lua
unit.UseGameMoney(10000)
```