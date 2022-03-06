---
layout: default
title: <font color="#2c84fa">❒</font> onRemoveItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# onRemoveItem
아이템이 제거되었을 때 호출되는 이벤트입니다. 

## 호출될 함수의 인자 형식
```lua
function( unit, item)
[1] unit: 아이템이 제거된 유닛
[2] item: 제거된 아이템
```

## 선언
```cs
public ScriptEventPublisher onRemoveItem { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

## 예제 
아이템 제거시 이벤트
```lua
function onRemoveItem(scriptUnit, titem) 
    print(scriptUnit.name)
    print(titem.id)
    print(titem.dataID)
end

Server.onRemoveItem.Add(onRemoveItem)
```