---
layout: default
title: ScriptColor
parent: Commons.Server.Scripts
grand_parent: Server API
nav_order: 2
---

# Class ScriptColor

색을 나타내는 스크립트 클래스입니다.

#### 상속

<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ ScriptColor
</div>

네임스페이스: [Commons.Server.Scripts](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax

```cs
[MoonSharpUserData]
public class ScriptColor
```

#### 예제

```lua
-- 빨간색을 가진 Color 객체 만들기

local myRedColor = Color(255, 0, 0)
```

## 프로퍼티
---


## a
투명도

#### 선언

```cs
public int a { get; set; }
```

#### 프로퍼티 값

|타입	  |설명 |
|:-------|:---|
|System.Int32 |   |

## b
파란색

#### 선언

```cs
public int b { get; set; }
```

#### 프로퍼티 값

|타입	  |설명 |
|:-------|:---|
|System.Int32 |   |

## g
초록색

#### 선언

```cs
public int g { get; set; }
```

#### 프로퍼티 값

|타입	  |설명 |
|:-------|:---|
|System.Int32 |   |

## r
빨간색

#### 선언
```cs
public int r { get; set; }
```

#### 프로퍼티 값

|타입	  |설명 |
|:-------|:---|
|System.Int32 |   |	

## 함수

## New(Int32, Int32, Int32, Int32)

새 객체를 생성합니다.

#### 선언
```cs
public static ScriptColor New(int r, int g, int b, int a = 255)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:--|:--|:---|
|System.Int32|r|빨간색 (0 ~ 255)|
|System.Int32|g|초록색 (0 ~ 255)|
|System.Int32|b|파란색 (0 ~ 255)|
|System.Int32|a|투명도 (0 ~ 255) (기본: 255)|

#### 반환

|타입|설명|
|:--|:--|
|[ScriptColor](/ScriptColor)| |