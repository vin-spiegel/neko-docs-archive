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

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ ScriptObject<br/>
　　↳ <a href = "../ScriptClan">ScriptClan</a><br/>
　　↳ <a href = "../ScriptDropItem">ScriptDropItem</a><br/>
　　↳ <a href = "../ScriptField">ScriptField</a><br/>
　　↳ <a href = "../ScriptParty">ScriptParty</a><br/>
　　↳ <a href = "../ScriptRoomPlayer">ScriptRoomPlayer</a><br/>
　　↳ <a href = "../ScriptUnit">ScriptUnit</a><br/>
　　↳ <a href = "../ScriptUnitBuff">ScriptUnitBuff</a><br/>
</div>


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