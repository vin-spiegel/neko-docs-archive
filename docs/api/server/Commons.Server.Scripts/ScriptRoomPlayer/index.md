---
layout: default
title: ScriptRoomPlayer
nav_order: 15
parent: Commons.Server.Scripts
has_children: true
---

<!-- 아래에 문서 작성 -->

# Class ScriptRoomPlayer 
서버에서 게임 유저를 관리하는 단위입니다. 유저 한명에 대응됩니다.

<!-- new
{: .label .label-green } -->

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ ScriptRoomPlayer
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptRoomPlayer : ScriptObject
```

## 프로퍼티
---

## baseEXP
현재 플레이어의 레벨의 하나 전 레벨까지 필요한 총 경험치 양 

#### 선언
```cs
public long baseEXP { get; }
```

# 프로퍼티 값
|타입|설명|
|System.Int64|

#### 예제
```
-- 현재 플레이어의 레벨이 3 이고 경험치 요구량이
-- 1 레벨 => 2 레벨 요구 경험치: 10
-- 2 레벨 => 3 레벨 요구 경험치: 20
-- 3 레벨 => 4 레벨 요구 경험치: 30
-- 일 때 baseExp의 값은 30 (= 10 + 20)
```

## clan
플레이어가 현재 속해있는 클랜

#### 선언
```cs
public ScriptClan clan { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptClan|clanID|플레이어가 속해있는 클랜의 ID|

#### 선언
```cs
public long clanID { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## exp
이 플레이어의 현재 누적 경험치

#### 선언
```cs
public long exp { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## id
이 플레이어의 고유 ID

#### 선언
```cs
public long id { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## isGM
이 플레이어가 게임 관리자(마스터)인지 반환합니다

#### 선언
```cs
public bool isGM { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Boolean|

## langauge

#### 선언
```cs
public string langauge { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|

## level
이 플레이어의 레벨

#### 선언
```cs
public int level { get; }
```

#### 프로퍼티 값

|타입|설명|
|System.Int32|

## maxEXP
현재 플레이어의 레벨까지 필요한 총 경험치 양 
```
현재 플레이어의 레벨이 3 이고 경험치 요구량이
1 레벨 => 2 레벨 요구 경험치: 10
2 레벨 => 3 레벨 요구 경험치: 20
3 레벨 => 4 레벨 요구 경험치: 30
일 때 maxEXP의 값은 60. (10 + 20 + 30)
```

#### 선언
```cs
public long maxEXP { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## name
이 플레이어의 이름

#### 선언
```cs
public string name { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|

## score
설정한 스코어의 값

#### 선언
```cs
public int score { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## team 
팀 값 (0 ~ 3 = 팀1 ~ 팀4)

#### 선언
```cs
public int team { get; }
```

### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|

## unit
이 플레이어가 갖고있는 유닛 객체

#### 선언
```cs
public ScriptUnit unit { get; }
```

#### 프로퍼티 값

|타입|설명|
|ScriptUnit|

## wallet_address
이 플레이어의 Wallet address

#### 선언
```cs
public string wallet_address { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|

## 함수
---

## AddStorageItem(Int32, Int32, Int32)
플레이어 창고에 아이템 지급

#### 선언
```cs
public bool AddStorageItem(int storageID, int itemDataID, int count)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|storageID|창고 ID|
|System.Int32|itemDataID|아이템 데이터 ID|
|System.Int32|count|아이템 개수|

#### 반환

|타입|설명|
|System.Boolean|아이템 지급 성공 여부|

#### 예제: 플레이어의 0번 창고에 5번 아이템을 20개 추가합니다
```lua
local result = unit.player.AddStorageItem(0, 5, 20)

if result then
    unit.SendCenterLabel("추가 성공!")
else
    unit.SendCenterLabel("추가 실패..")
end
```

## FireEvent(String, Object[])
클라이언트로 Topic에 대한 이벤트를 보냅니다. `ScriptServer.FireEvent()` 와 사용법이 같지만, 해당 메서드는 **플레이어**에게만 이벤트를 보냅니다.

#### 선언
```cs
public void FireEvent(string topic, params object[] arguments)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|topic|보낼 Topic|
|System.Object[]|arguments|함께 보낼 인자들|

## GetItem(Int64)
플레이어가 가지고있는 아이템

#### 선언
```cs
public TItem GetItem(long id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|id|해당 아이템의 고유 ID|

#### 반환

|타입|설명|
|:-|:-|
|TItem|

#### 예제: 플레이어의 인벤토리에서 고유 ID가 10인 아이템 가져오기
```lua
local myItem = unit.player.GetItem(10)
```

## GetItems()
현재 플레이어가 가지고 있는 아이템들을 형식으로 반환합니다. 예) 해당 이벤트를 클릭했을때 밑의 스크립트 사용시 Titem 사용
print(unit.player.GetItems()[1])

#### 선언
```cs
public List<TItem> GetItems()
```

#### 반환

|타입|설명|
|System.Collections.Generic.List<TItem>|TItem 테이블|

#### 예제: 플레이어의 인벤토리 아이템 목록을 가져와서 모두 출력해준다
```lua
local invenItems = unit.player.GetItems()

-- 창고가 비었을 때의 처리
if #invenItems <= 0 then
    Server.SendSay(unit.name .. ' 님의 인벤토리는 비어있습니다')
    return
end

Server.SendSay(unit.name .. ' 님의 인벤토리 아이템 목록')

for i = 1, #invenItems do
    if invenItems[i] ~= nil then
        local titem = invenItems[i]
        local itemData = Server.GetItem(titem.dataID)
        
        if itemData ~= nil and titem.count ~= 0 then
            Server.SendSay(i .. ' : ' .. itemData.name .. ' ' .. titem.count .. '개')
        end
    end
end
```

## GetNFTs()
{: .d-inline-block }
New
{: .label .label-green }
#### 선언
```cs
public ScriptNFT[] GetNFTs()
```

#### 반환

|타입|설명|
|:-|:-|
|ScriptNFT[]|

## GetStorageItems(Int32)
플레이어의 창고 아이템 목록을 가져옵니다.

#### 선언
```cs
public List<TItem> GetStorageItems(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|불러올 창고 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<TItem>|

#### 예제: 플레이어의 0번 창고 아이템 목록을 가져와서 모두 출력해준다
```lua
local storageItems = unit.player.GetStorageItems(0)

-- 창고가 비었을 때의 처리
if #storageItems <= 0 then
    Server.SendSay(unit.name .. ' 님의 0번 창고는 비어있습니다')
    return
end

Server.SendSay(unit.name .. ' 님의 0번 창고 아이템 목록')

for i = 1, #storageItems do
    if storageItems[i] ~= nil then
        local titem = storageItems[i]
        local itemData = Server.GetItem(titem.dataID)
        
        if itemData ~= nil and titem.count ~= 0 then
            Server.SendSay(i .. ' : ' .. itemData.name .. ' ' .. titem.count .. '개')
        end
    end
end
```

## GetWalletAddress()
{: .d-inline-block }
New
{: .label .label-green }
플레이어의 지갑 주소

#### 선언
```cs
public string GetWalletAddress()
```

#### 반환

|타입|설명|
|:-|:-|
|System.String|

## GetWalletBalance(String)
{: .d-inline-block }
New
{: .label .label-green }
플레이어의 지갑의 가상화폐 금액 (단위 WEI)

#### 선언
```cs
public string GetWalletBalance(string chain)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|chain|메인넷 이름 (ethereum, matic, klaytn)|

#### 반환

|타입|설명|
|:-|:-|
|System.String|

## RemoveStorageItem(Int32, Int32, Int32)
플레이어 창고의 아이템 회수

#### 선언
```cs
public bool RemoveStorageItem(int storageID, int itemDataID, int count)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|storageID|창고 ID|
|System.Int32|itemDataID|아이템 데이터 ID|
|System.Int32|count|아이템 개수|

#### 반환

|타입|설명|
|System.Boolean|아이템 회수 성공 여부|

#### 예제: 플레이어의 0번 창고에서 5번 아이템을 20개 제거합니다
```lua
local result = unit.player.RemoveStorageItem(0, 5, 20)

if result == true then
    unit.SendCenterLabel("제거 성공!")
else
    unit.SendCenterLabel("제거 실패..")
end
```

## SendItemUpdated(TItem)
{: .d-inline-block }
New
{: .label .label-green }
현재 유닛이 가진 아이템 정보 갱신

#### 선언
```cs
public void SendItemUpdated(TItem item)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|TItem|item|갱신할 아이템|

#### 예제: `클라이언트`에 `ID:10`의 아이템이 변경되었다고 알리기
```lua
unit.player.SendItemUpdated(unit.player.GetItem(10))
```