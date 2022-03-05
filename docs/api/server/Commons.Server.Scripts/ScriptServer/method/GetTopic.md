---
layout: default
title: <font color="#2c84fa">𝑓</font> GetTileset
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetTopic(String)
특정 topic에 대한 이벤트 콜백을 가져옵니다. 클라이언트에서 보낸 topic 이벤트를 처리합니다.

#### 선언
```cs
public ScriptEventPublisher GetTopic(string topic)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|topic|보낼 topic id|

#### 반환

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제 
```lua
-- 클라이언트에서 "Apple" 이란 주제로 FireEvent를 발송했을 때
-- 모든 클라이언트들에게 "Apple" 이란 메시지 표시하기

Server.GetTopic("Apple").Add(function()
    Server.SendCenterLabel("Apple")
end)

-- 클라이언트에서 "MyName" 이란 주제로 FireEvent를 발송했을 때
-- 모든 클라이언트들에게 같이 받은 인자 메시지를 표시하기

-- 클라이언트에서: Client.FireEvent("MyName", "Hello Server!")
-- 실행 시 출력: Hello Server!

Server.GetTopic("MyName").Add(function(name)
    Server.SendCenterLabel(name)
end)
```