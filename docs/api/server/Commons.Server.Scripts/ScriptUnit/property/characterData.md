---
layout: default
title: <font color="#2c84fa"> ❒ </font>characterData
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

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