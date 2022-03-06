---
layout: default
title: <font color="#2c84fa">❒</font> onAddItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# onAddItem
아이템이 추가되었을 때 호출되는 이벤트입니다. 

## 호출될 함수의 인자 형식 
```lua
function(unit, item)
```

|이름|타입|설명|
|:-|:-|:-|
|unit|ScriptUnit|아이템이 추가된 유닛|
|item|TItem|추가된 아이템|

## 선언
```cs
public ScriptEventPublisher onAddItem { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

## 예제 
아이템 획득 시 이벤트 추가하기
```lua
function onAddItem(unit, titem)
    print(scriptUnit.name)
    print(titem.dataID)
end

Server.onAddItem.Add(onAddItem)
```