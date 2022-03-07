---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>PullFromUnit</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## PullFromUnit(ScriptUnit, Single, Single)
유닛에게 당기기를 적용합니다.(당긴 대상 유닛에게 끌려갑니다)

#### 선언
```cs
public void PullFromUnit(ScriptUnit from, float distance = 0F, float time = 0.5F)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|from|당긴 대상|
|System.Single|distance|간격 (0 일경우 완전히 내 위치까지 당겨집니다) (기본값: 0)|
|System.Single|time|적용 시간 (짧을수록 빠르게 당깁니다) (기본값: 0.5)|

#### 예제: 공격한 대상을 나를 기준으로 당겨오기
```lua
-- 해당 예제는 데미지 공식에서 사용되는 공식을 예제로 들었습니다

-- 방어자를 공격자 위치에서 0칸 떨어진 곳까지 0.5초간 당겨온다
b.PullFromUnit(a, 0, 0.5)
```