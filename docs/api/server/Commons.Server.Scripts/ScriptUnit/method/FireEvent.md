---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>FireEvent</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## FireEvent(String, Object[])
클라이언트에게 해당 주제(Topic)로 이벤트를 발생시킵니다.

#### 선언
```cs
public void FireEvent(string topic, params object[] arguments)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|topic|보낼 주제(Topic)|
|System.Object[]|arguments|함께 전송할 인자(Argument)들|

#### 예제
```lua
-- ScriptServer.FireEvent() 와 사용법이 같지만
-- 해당 메서드는 이 플레이어에게만 이벤트를 보낸다
```