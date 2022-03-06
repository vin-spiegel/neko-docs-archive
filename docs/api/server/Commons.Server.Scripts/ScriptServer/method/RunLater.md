---
layout: default
title: <font color="#2c84fa">𝑓</font> RunLater
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## RunLater(Closure, Single)
t 초 후에, callback 함수를 실행합니다.

#### 선언
```cs
public void RunLater(Closure callback, float t)
```

#### 매개 변수(인자)

|타입|이름|설명|
|MoonSharp.Interpreter.Closure|callback|실행할 함수|
|System.Single|t|실행까지 대기시간 (초)|

#### 예제: 5초 뒤에 모든 클라이언트들에게 메시지를 전송하기
```lua
Server.RunLater(function()
    Server.SendCenterLabel('5초 지남!')
end, 5)
```