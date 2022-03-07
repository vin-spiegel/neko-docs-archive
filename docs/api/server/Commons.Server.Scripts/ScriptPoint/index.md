---
layout: default
title: ScriptPoint
nav_order: 12
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptPoint 
점에 대한 정보를 보관하는 스크립트 클래스입니다.

<!-- new
{: .label .label-green } -->

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ ScriptPoint
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptPoint
```

## 프로퍼티
---

## x

#### 선언
```cs
public float x { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|System.Single|

## y

#### 선언
```cs
public float y { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|System.Single|

## 함수
---

## New(Single, Single)
새 객체를 생성합니다.

#### 선언
```cs
public static ScriptPoint New(float x, float y)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|위치 X|
|System.Single|y|위치 Y|

#### 반환

|타입|설명|
|:-|:-|
|ScriptPoint|생성된 객체|