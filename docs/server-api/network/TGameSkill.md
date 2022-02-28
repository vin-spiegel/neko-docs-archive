---
layout: default
title: TGameSkill
parent: network
grand_parent: Server API
nav_order: 15
---

# Class TGameSkill

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameSkill
</div>

구현: ProtoBuf.IExtensible
{: .text-zeta}

네임스페이스: [network](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

#### Syntax
```cs
[Serializable]
public class TGameSkill : IExtensible
## 생성자
---
TGameSkill()

#### 선언
```cs
public TGameSkill()
프로퍼티
actionName

#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "actionName", DataFormat = DataFormat.Default)]
public string actionName { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	
animationID

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "animationID", DataFormat = DataFormat.TwosComplement)]
public int animationID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
consumeHP

#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "consumeHP", DataFormat = DataFormat.TwosComplement)]
public int consumeHP { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
consumeMP

#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "consumeMP", DataFormat = DataFormat.TwosComplement)]
public int consumeMP { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
coolTime

#### 선언
```cs
[ProtoMember(16, IsRequired = false, Name = "coolTime", DataFormat = DataFormat.FixedSize)]
public float coolTime { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|	
criticalPercent

#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "criticalPercent", DataFormat = DataFormat.FixedSize)]
public float criticalPercent { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|	
damageFormula

#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "damageFormula", DataFormat = DataFormat.Default)]
public string damageFormula { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	
damageType

#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "damageType", DataFormat = DataFormat.TwosComplement)]
public int damageType { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
desc

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "desc", DataFormat = DataFormat.Default)]
public string desc { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	
hasCritical

#### 선언
```cs
[ProtoMember(12, IsRequired = false, Name = "hasCritical", DataFormat = DataFormat.Default)]
public bool hasCritical { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Boolean|	
iconID

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "iconID", DataFormat = DataFormat.Default)]
public string iconID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	
l_desc

#### 선언
```cs
[ProtoMember(21, IsRequired = false, Name = "l_desc", DataFormat = DataFormat.Default)]
public LString l_desc { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|network.LString|	
l_name

#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|network.LString|	
memo

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "memo", DataFormat = DataFormat.Default)]
public string memo { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	
name

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	
oldTraits

#### 선언
```cs
[ProtoMember(15, Name = "oldTraits", DataFormat = DataFormat.Default)]
public List<TGameTrait> oldTraits { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<network.TGameTrait>	
sturnEnable

#### 선언
```cs
[ProtoMember(24, IsRequired = false, Name = "sturnEnable", DataFormat = DataFormat.Default)]
public bool sturnEnable { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Boolean|	
sturnTarget

#### 선언
```cs
[ProtoMember(25, IsRequired = false, Name = "sturnTarget", DataFormat = DataFormat.TwosComplement)]
public int sturnTarget { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
sturnTime

#### 선언
```cs
[ProtoMember(26, IsRequired = false, Name = "sturnTime", DataFormat = DataFormat.FixedSize)]
public float sturnTime { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Single|	
traits

#### 선언
```cs
[ProtoMember(18, Name = "traits", DataFormat = DataFormat.Default)]
public List<TGameMapEventCommand> traits { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<network.TGameMapEventCommand>	
type

#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "type", DataFormat = DataFormat.TwosComplement)]
public int type { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
useTarget

#### 선언
```cs
[ProtoMember(23, IsRequired = false, Name = "useTarget", DataFormat = DataFormat.TwosComplement)]
public int useTarget { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
useType

#### 선언
```cs
[ProtoMember(22, IsRequired = false, Name = "useType", DataFormat = DataFormat.TwosComplement)]
public int useType { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	
## 명시적 인터페이스 구현
---
IExtensible.GetExtensionObject(Boolean)

#### 선언
```cs
IExtension IExtensible.GetExtensionObject(bool createIfMissing)
```
### 매개 변수 (인자)
|타입|이름|설명|
|:-|:-|:-|
|System.Boolean|	createIfMissing	

#### 반환

|타입|설명|
|:-|:-|
|ProtoBuf.IExtension|

## 구현
ProtoBuf.IExtensible
{: .text-zeta}
## 확장 함수
Utility.Clone<T>(T)
{: .text-zeta}
Utility.DumpProtobufBase64<T>(T, System.Boolean)
{: .text-zeta}
Utility.DumpProtobuf<T>(T, System.Boolean)
{: .text-zeta}