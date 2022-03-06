---
layout: default
title: <font color="#2c84fa">𝑓</font> HttpGet
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## HttpGet(String, Closure)
Http GET 요청을 보내고, 데이터를 가져온다.

#### 선언
```cs
public bool HttpGet(string url, Closure callback)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|url|url|
|MoonSharp.Interpreter.Closure|callback|가져온 데이터 처리 콜백|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제: Http GET 을 이용해서 웹 페이지에서 데이터를 받아오기
```lua
Server.HttpGet('http://nekoland.net/', function (res)
    print(res)
end)
```