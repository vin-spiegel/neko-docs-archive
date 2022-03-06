---
layout: default
title: <font color="#2c84fa">𝑓</font> FireEvent
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## FireEvent(String, Object[])
클라이언트로 topic에 대해 이벤트를 보냅니다.

#### 선언
```cs
public void FireEvent(string topic, params object[] arguments)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|topic|보낼 topic id|
|System.Object[]|arguments|함께보낼 인자들|

### 예제: 모든 클라이언트들에게 "MyName" 이라는 `주제`로 이벤트를 발송하고 인자로 'Hello Client!'문자열도 같이 전송합니다
```lua
Server.FireEvent("MyName", "Hello Client!")

-- 해당 이벤트를 클라이언트에서 받으려면
-- 아래와 같은 코드를 사용해보세요

Client.GetTopic("MyName").Add(function(name)
    print(name)
end)
```
