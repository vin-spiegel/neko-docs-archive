---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>IsCollectionCompleted</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## IsCollectionCompleted(Int32)
유닛이 해당 도감의 요소를 완료했는지를 반환합니다.

#### 선언
```cs
public bool IsCollectionCompleted(int collectionDataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|collectionDataID|데이터베이스의 도감 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|완료 여부 (완료: True, 미완료: False)|

#### 예제: 5번 도감이 완성되었는치 출력하기
```lua
if unit.IsCollectionCompleted(5) then
    unit.SendCenterLabel("5번 도감이 완성되어 있음")
else
    unit.SendCenterLabel("5번 도감이 미완성")
end
```