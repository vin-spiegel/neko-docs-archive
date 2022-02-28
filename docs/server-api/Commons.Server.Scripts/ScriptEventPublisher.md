---
layout: default
title: ScriptEventPublisher
parent: Commons.Server.Scripts
grand_parent: Server API
nav_order: 5
---

# Class ScriptEventPublisher 
{: .d-inline-block }

<!-- New
{: .label .label-green } -->

루아 스크립트 상의 함수를 이벤트 등록에 사용 가능하게 해주는 클래스. `ScriptEventPublisher` 는 각종 이벤트 등록/해제 객체의 기본 클래스이며, 직접 사용할 수는 없습니다

#### 상속

```markdown
↳ System.Object
    ↳ ScriptEventPublisher
```

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptEventPublisher
```

## 함수
---

## Add(Closure)
이 이벤트가 발생했을 때, 호출될 루아 함수를 등록한다.

#### 선언
```cs
public void Add(Closure c)
```

#### 매개 변수(인자)

|타입|이름|설명|
|MoonSharp.Interpreter.Closure|c|루아 함수|

#### 예제 1: Hello GetTopic 이벤트에 함수 등록/해제

```lua
function OnHello()
    -- do something
end
--이벤트 등록
Server.GetTopic("Hello").Add(OnHello)
--이벤트 해제
Server.GetTopic("Hello").Remove(OnHello)
```

## Call(Object[])
이 이벤트를 호출합니다

#### 선언
```cs
public void Call(params object[] args)
```

#### 매개 변수(인자)

|타입|이름|설명|
|System.Object[]|args|

#### 예제: `onTick` 이벤트에 함수 등록 후 호출
```lua
function OnTick()
    -- do something
end
-- 대상 이벤트 등록
Server.onTick.Add(OnTick)

-- 대상 이벤트 호출
Server.onTick.Call()

-- 대상 이벤트 삭제
Server.onTick.Remove(OnTick)
```

## Call2(Table, Object[])
이 이벤트를 호출한다.

#### 선언
```cs
public void Call2(Table localContext, params object[] args)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|MoonSharp.Interpreter.Table|localContext|
|System.Object[]|args|


## Remove(Closure)
등록한 루아 함수를 삭제한다.
(`Add` 함수를 이용해서 등록한 함수를 등록 해제하는 것)

### 선언
```cs
public void Remove(Closure c)
```

### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|MoonSharp.Interpreter.Closure|c|루아 함수|
