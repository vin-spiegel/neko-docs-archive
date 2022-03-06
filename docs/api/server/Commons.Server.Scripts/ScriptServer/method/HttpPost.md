---
layout: default
title: <font color="#2c84fa">𝑓</font> HttpPost
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## HttpPost(String, Table, Closure)
Http POST 요청을 보내고, 데이터를 가져온다.

#### 선언
```cs
public bool HttpPost(string url, Table data, Closure callback)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.String|url|url|
|MoonSharp.Interpreter.Table|data|루아 Table 형식 데이터|
|MoonSharp.Interpreter.Closure|callback|가져온 데이터 처리 콜백|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제: t 라는 테이블을 만들고, 보낼 POST 요청 데이터 넣기
```lua
local t = {}
t.id = 1234
t.name = "Hello"

-- http://naver.com URL로 요청 보내고, res로 데이터 받기
Server.HttpGet('http://naver.com', t, function(res)
  print(res) -- 웹페이지가 반환한 결과 텍스트가 출력됩니다.
end)

-- 웹 서버에서 데이터 받기

-- POST로 요청을 받을 경우, 아래와 같이 데이터를 출력할 수 있습니다.
-- 이 데이터를 MySQL과 같은 데이터베이스에 넣어, 영구보관할 수 있습니다.

<?php
echo $_POST["id"];
echo $_POST["name"];

echo "잘 받았습니다!";
?>

-- Server.HttpGet 에서 보낸 데이터가 웹 서버에 잘 도착하였는지를 확인하기 위한 코드입니다. 
-- 위 서버 스크립트 예재의 print(res) 에 의해 “1234Hello잘 받았습니다!” 가 출력됩니다.
```
