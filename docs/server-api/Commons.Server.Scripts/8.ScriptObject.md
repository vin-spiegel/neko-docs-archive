---
layout: default
title: ScriptObject
nav_order: 8
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptObject 

<!-- new
{: .label .label-green } -->

커스텀 데이터를 사용 가능한 스크립트 오브젝트입니다. 예를들어 몬스터 AI 스크립트 중
ai.customData.test = 1 처럼 커스텀 변수 설정이 가능합니다.

#### 상속

```
↳ System.Object
    ↳ ScriptObject
        ↳ ScriptClan
        ↳ ScriptDropItem
        ↳ ScriptField
        ↳ ScriptParty
        ↳ ScriptRoomPlayer
        ↳ ScriptUnit
        ↳ ScriptUnitBuff
```

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
public class ScriptObject
```

## 프로퍼티
---

## customData
커스텀 데이터 테이블

#### 선언
```cs
public Table customData { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Table|