---
layout: default
title: <font color="#2c84fa">𝑓</font> SendSay
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SendSay(String, UInt32)
채팅창에 메세지를 표시합니다.

#### 선언
```cs
public void SendSay(string text, uint color = 4294967295U)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|표시할 메세지|
|System.UInt32|color|색깔|

#### 예제: 게임 채팅창에 "Hello Nekoland!" 메시지를 표시합니다
```lua
Server.SendSay("Hello Nekoland!")
```