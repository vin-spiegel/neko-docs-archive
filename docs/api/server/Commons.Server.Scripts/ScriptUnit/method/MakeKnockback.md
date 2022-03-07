---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>MakeKnockback</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## MakeKnockback(Single, Single)
유닛에게 밀치기(넉백 Knock-back)를 적용합니다.

#### 선언
```cs
public void MakeKnockback(float distance, float time)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Single|distance|적용 거리|
|System.Single|time|적용 시간 (짧을수록 빠르게 밀어냅니다)|

#### 예제: 유닛을 2초간 64(2칸) 만큼 넉백시키기
```lua
unit.MakeKnockback(64, 2)
```