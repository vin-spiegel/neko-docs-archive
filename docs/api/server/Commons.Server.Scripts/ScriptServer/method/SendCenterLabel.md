---
layout: default
title: <font color="#2c84fa">𝑓</font> SendCenterLabel
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SendCenterLabel(String)
가운데에 문자열을 표시합니다.

#### 선언
```cs
public void SendCenterLabel(string text)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|표시할 문자열|

#### 예제: 현재 내 게임에 접속한 모든 플레이어들의 화면에 "Hello Nekoland!" 문자열 표시하기
```lua
Server.SendCenterLabel("Hello Nekoland!")
```