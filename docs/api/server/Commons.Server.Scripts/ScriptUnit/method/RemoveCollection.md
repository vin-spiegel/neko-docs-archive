---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>RemoveCollection</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## RemoveCollection(Int32)
도감을 삭제하고, 삭제에 성공했는지를 반환합니다.

#### 선언
```cs
public bool RemoveCollection(int collectionDataID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|collectionDataID|데이터베이스의 도감 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|삭제 성공 여부 (성공: True, 실패: False)|

#### 예제: 유닛의 5번 도감 완료 이력을 삭제하기
```lua
unit.RemoveCollection(5)
```