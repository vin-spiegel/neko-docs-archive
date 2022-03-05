---
layout: default
title: <font color="#2c84fa">❒</font> damageCallback
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# damageCallback
유닛의 데미지 계산 공식 콜백 함수입니다. (데미지 공식을 커스텀 할 수 있습니다.) 

## 콜백 함수의 형식 
```lua
function(from, to, damage, skillDataID)
```

|이름|타입|설명|
|:-|:-|:-|
|from|ScriptUnit|공격 유닛|
|to|ScriptUnit|대상 유닛|
|damage|number|공격의 데미지|
|skillDataID|number|스킬의 데이터 ID|

## 반환값

|타입|설명|
|:-|:-|
|number|계산된 데미지|

## 선언
```cs
public Closure damageCallback { get; set; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

## 예제 
데미지를 입힐때 발생하는 이벤트 만들기
```lua
Server.damageCallback = function(a, b, damage, skillDataID, critical, visible)
    -- 데미지 계산 (공격자의 공격력 - 방어자의 방어력)
    damage = a.atk - b.def

    -- 데미지가 0일경우 데미지 표시를 출력하지 않음
    if damage <= 0  then
        visible = false
    end

    -- 데미지, 크리 여부, 폰트 출력 여부
    return damage, critical, visible
end
```