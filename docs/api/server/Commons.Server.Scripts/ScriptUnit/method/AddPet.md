---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## AddPet(Int32, Int32, String)
신규 펫을 추가 등록하고 등록된 ID를 가져옵니다. 
- 등록이 실패할 경우 `-1`을 리턴합니다.

#### 선언
```cs
public int AddPet(int characterID = 0, int jobID = 0, string name = null)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|characterID|펫의 캐릭터 ID (기본값: 0)|
|System.Int32|jobID|펫의 직업 ID (기본값: 0)|
|System.String|name|펫의 이름 (기본값: 펫 캐릭터의 이름)|

#### 반환
|타입|설명|
|:-|:-|
|System.Int32|등록된 펫의 ID(등록 실패시 -1)|