---
layout: default
title: ScriptRect
nav_order: 14
parent: Commons.Server.Scripts
grand_parent: Server API
---

<!-- 아래에 문서 작성 -->

# Class ScriptRect 

<!-- new
{: .label .label-green } -->

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ ScriptRect
</div>


네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[MoonSharpUserData]
public class ScriptRect
```

## 프로퍼티
---

## height
세로 길이

#### 선언
```cs
public float height { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|

## width
가로 길이

#### 선언
```cs
public float width { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|

## x
위치 X

#### 선언
```cs
public float x { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|

## y
위치 Y

#### 선언
```cs
public float y { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|

## 함수
---

## New(Single, Single, Single, Single)
새 객체를 생성합니다.

#### 선언
```cs
public static ScriptRect New(float x, float y, float width, float height)
```

#### 매개 변수(인자)
|타입|이름|설명|
|:-|:-|:-|
|System.Single|x|위치 X|
|System.Single|y|위치 Y|
|System.Single|width|가로 길이|
|System.Single|height|세로 길이|

#### 반환
|타입|설명|
|ScriptRect|생성된 객체|