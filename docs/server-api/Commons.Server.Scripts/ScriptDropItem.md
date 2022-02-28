---
layout: default
title: ScriptDropItem
parent: Commons.Server.Scripts
grand_parent: Server API
nav_order: 3
# permalink: /docs/server-api/Commons.Server.Scripts/ScriptDropItem
---

# Class ScriptDropItem 
{: .d-inline-block }

<!-- New
{: .label .label-green } -->

드롭된 아이템을 나타내는 스크립트 클래스입니다.

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ <a href = "../ScriptObject">ScriptObject</a><br/>
　　↳ ScriptDropItem
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptDropItem : ScriptObject
```

## 프로퍼티
<!-- {: .d-inline-block } -->
---

## dropUnitID

떨어트린 유닛의 ID

#### 선언
```cs
public long dropUnitID { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## field

소속 필드

#### 선언
```cs
public ScriptField field { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|[ScriptField](../6.ScriptField)|

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

## ownerUnitID

소유 유닛의 ID

#### 선언
```cs
public long ownerUnitID { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|

## posX

위치 X

#### 선언
```cs
public float posX { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|

## posY

위치 Y

#### 선언
```cs
public float posY { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|

## titem

아이템 정보

#### 선언
```cs
public TItem titem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|[TItem](../../network/20.TItem)|

## 함수
---

## Acquire(ScriptUnit)

해당 아이템을 특정 Unit이 가져갈 수 있게한다.

#### 선언
```cs
public int Acquire(ScriptUnit unit)
```

### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|unit|객체|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|

#### 예제
```lua
-- 새 5번 드랍 아이템을 생성하고 플레이어한테 획득시킨다

local dropItem = Server.CreateDropItem(5, 1)
unit.field.JoinDropItem(dropItem)
dropItem.Acquire(unit)
```

## LeaveField()
해당 필드를 떠난다. (필드에서 아이템 삭제)

#### 선언
```cs
public void LeaveField()
```

#### 예제
```lua
-- 필드 내의 모든 드랍 아이템들을 필드에서 없앱니다
if unit.field ~= nil then
    return
end

local dropItems = unit.field.dropItems

if #dropItems <= 0 then
    unit.SendCenterLabel('떨어진 드랍 아이템이 없습니다')
    return    
end

local count = 0
for i = 1, #dropItems do
    if dropItems[i] ~= nil then
        dropItems[i].LeaveField()
        count = count + 1
    end
end

unit.SendCenterLabel(count .. '개의 드랍 아이템을 치웠습니다')
```