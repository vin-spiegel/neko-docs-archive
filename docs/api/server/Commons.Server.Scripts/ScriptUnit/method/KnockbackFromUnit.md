---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>KnockbackFromUnit</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## KnockbackFromUnit(ScriptUnit, Single, Single)
유닛에게 밀치기(넉백 Knock-back)를 적용합니다.
(밀친 대상의 유닛으로부터 멀어집니다)

#### 선언
```cs
public void KnockbackFromUnit(ScriptUnit from, float distance, float time = 0.5F)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|ScriptUnit|from|밀친 대상|
|System.Single|distance|적용 거리|
|System.Single|time|적용 시간 (짧을수록 빠르게 밀어냅니다) (기본값: 0.5)|

#### 예제: 공격한 대상 나를 기준으로 밀치기
```lua
-- 해당 예제는 데미지 공식에서 사용되는 공식을 예제로 들었습니다

-- 방어자를 공격자로부터 0.5초간 2칸 만큼 밀어낸다
b.KnockbackFromUnit(a, 64, 0.5)
```