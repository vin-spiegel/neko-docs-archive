---
layout: default
title: ScriptServer
nav_order: 16
has_children: true
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptServer 
Server 객체로 참조할 수 있는 클래스 입니다. 유저가 접속했을때, 떠났을때, 대화할때 등 모든 게임에 관련된 **이벤트 리스너**가 있습니다.

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ ScriptServer
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptServer : NekoEventListener
```

## 프로퍼티
---

## 함수
---


## SetMonsterAI(Int32, Closure)
몬스터 AI를 등록한다. 몬스터의 ID 를 이용해, 해당 몬스터의 AI를 등록한다.

#### 선언
```cs
public void SetMonsterAI(int id, Closure c)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|몬스터의 ID|
|MoonSharp.Interpreter.Closure|c|AI 함수|

#### 예제: 0번 몬스터의 AI 설정
```lua
Server.SetMonsterAI(0,
    function(monster, ai, event, data)
        -- 여기에 AI 코드를 삽입합니다
    end)
```

## SetPetAI(Int32, Closure)
펫 AI를 등록한다.

#### 선언
```cs
public void SetPetAI(int id, Closure c)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|펫 ID|
|MoonSharp.Interpreter.Closure|c|AI 함수|

#### 예제: 0번 펫의 AI 설정
```lua
Server.SetPetAI(0,
    function(pet, ai, event, data)
        -- 여기에 AI 코드를 삽입합니다
    end)
```

## SetWorldStringVar(Int32, String)
월드 변수 값을 설정한다.

#### 선언
```cs
public void SetWorldStringVar(int id, string value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.String|value|값|

#### 예제: 4번 월드 문자열 변수에 "Hello Nekoland!" 문자열 저장
```lua
Server.SetWorldStringVar(4, "Hello Nekoland!")
```

## SetWorldVar(Int32, Int64)
월드 변수 값을 설정한다.

#### 선언
```cs
public void SetWorldVar(int id, long value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.Int64|value|값|

#### 예제: 4번 월드 변수를 7로 설정
```lua
Server.SetWorldVar(4, 7)
```

## StartState(Int32, Single)
`time` 시간 후에, 특정한 `state` 를 실행합니다.

#### 선언
```cs
public void StartState(int state, float time = 0F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|state|state 숫자|
|System.Single|time|실행 시간|

#### 예제: 5초 뒤에 7번 State를 시작
```lua
-- Server.onStartState, Server.onEndState 로 연동해서 사용

Server.StartState(7, 5)
```