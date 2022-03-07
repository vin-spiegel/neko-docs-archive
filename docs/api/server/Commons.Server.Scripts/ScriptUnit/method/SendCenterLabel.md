---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SendCenterLabel</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->




## SendCenterLabel(String)
해당 유닛의 화면 중심에 라벨을 표시합니다.(Center Label을 생성합니다.)

#### 선언
```cs
public void SendCenterLabel(string text)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|text|라벨에 표기할 말(텍스트)|

#### 예제: 유닛의 플레이어 화면 가운데 "Welcome to Nekoland!" 표시하기
```lua
unit.SendCenterLabel("Welcome to Nekoland!")
```