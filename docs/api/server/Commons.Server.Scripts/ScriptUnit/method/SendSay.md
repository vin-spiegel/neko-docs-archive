---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SendSay</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## SendSay(String, UInt32)
이 플레이어 유닛의 채팅창에만 추가되는 텍스트를 씁니다.

#### 선언
```cs
public void SendSay(string text, uint color = 4294967295U)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|말(텍스트)|
|System.UInt32|color|텍스트의 색 (기본값: 검정)|

#### 예제: 이 유닛의 `채팅창`에 "Welcome to Nekoland!" 라고 나오게 하기
```lua
unit.SendSay("Welcome to Nekoland!")
-- 빨간색
unit.SendSay("Welcome to Nekoland! (Red)", 0xFF0000)
-- 초록색
unit.SendSay("Welcome to Nekoland! (Green)", 0x00FF00)
-- 파란색
unit.SendSay("Welcome to Nekoland! (Blue)", 0x0000FF)
```