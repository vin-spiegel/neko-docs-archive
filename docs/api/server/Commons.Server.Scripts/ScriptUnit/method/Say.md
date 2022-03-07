---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>Say</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## Say(String, UInt32)
해당 유닛이 말하게 합니다.

#### 선언
```cs
public void Say(string text, uint color = 4294967295U)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|말(텍스트)|
|System.UInt32|color|텍스트의 색 (기본값: 검정)|

#### 예제: 이 유닛이 "Hello Nekoland!" 라고 말하게 하기
```lua
unit.Say("Hello Nekoland!")

-- 빨간색
unit.Say("Hello Nekoland! (Red)", 0xFF0000)
-- 초록색
unit.Say("Hello Nekoland! (Green)", 0x00FF00)
-- 파란색
unit.Say("Hello Nekoland! (Blue)", 0x0000FF)
```