---
layout: default
title: ScriptUnit
nav_order: 17
parent: Commons.Server.Scripts
has_children: true
---

<!-- 아래에 문서 작성 -->

# Class ScriptUnit 
유닛 클래스입니다.유닛의 모든 정보와 관련된 함수가 집합되어 있습니다.

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ ScriptUnit<br/>
　　　↳ <a href = "../ScriptPetUnit">ScriptPetUnit</a><br/>
</div>

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

## 함수
---

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
```

# ShowAnimation(Int32)
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