---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">❒ </font>monsterData</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->





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