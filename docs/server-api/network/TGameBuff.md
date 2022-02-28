---
layout: default
title: TGameBuff
parent: network
grand_parent: Server API
nav_order: 3
---

# Class TGameBuff

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameBuff
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
public class TGameBuff : IExtensible
## 생성자
TGameBuff()
#### 선언
```cs
public TGameBuff()
프로퍼티
damageFormula
#### 선언
```cs
[ProtoMember(12, IsRequired = false, Name = "damageFormula", DataFormat = DataFormat.Default)]
public string damageFormula { get; set; }
#### 프로퍼티 값

|타입|설명|
System.String	
damageType
#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "damageType", DataFormat = DataFormat.TwosComplement)]
public int damageType { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
debuffCondition
#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "debuffCondition", DataFormat = DataFormat.TwosComplement)]
public int debuffCondition { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
debuffTime
#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "debuffTime", DataFormat = DataFormat.TwosComplement)]
public int debuffTime { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
desc
#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "desc", DataFormat = DataFormat.Default)]
public string desc { get; set; }
#### 프로퍼티 값

|타입|설명|
System.String	
hasCritical
#### 선언
```cs
[ProtoMember(13, IsRequired = false, Name = "hasCritical", DataFormat = DataFormat.Default)]
public bool hasCritical { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Boolean	
iconID
#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "iconID", DataFormat = DataFormat.Default)]
public string iconID { get; set; }
#### 프로퍼티 값

|타입|설명|
System.String	
isRemoveBuff
#### 선언
```cs
[ProtoMember(18, IsRequired = false, Name = "isRemoveBuff", DataFormat = DataFormat.Default)]
public bool isRemoveBuff { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Boolean	
l_desc
#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "l_desc", DataFormat = DataFormat.Default)]
public LString l_desc { get; set; }
#### 프로퍼티 값

|타입|설명|
network.LString	
l_name
#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
#### 프로퍼티 값

|타입|설명|
network.LString	
memo
#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "memo", DataFormat = DataFormat.Default)]
public string memo { get; set; }
#### 프로퍼티 값

|타입|설명|
System.String	
name
#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
#### 프로퍼티 값

|타입|설명|
System.String	
oldTraits
#### 선언
```cs
[ProtoMember(10, Name = "oldTraits", DataFormat = DataFormat.Default)]
public List<TGameTrait> oldTraits { get; }
#### 프로퍼티 값

|타입|설명|
System.Collections.Generic.List<network.TGameTrait>	
showAnimation
#### 선언
```cs
[ProtoMember(15, IsRequired = false, Name = "showAnimation", DataFormat = DataFormat.Default)]
public bool showAnimation { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Boolean	
showAnimationID
#### 선언
```cs
[ProtoMember(16, IsRequired = false, Name = "showAnimationID", DataFormat = DataFormat.TwosComplement)]
public int showAnimationID { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
tickTime
#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "tickTime", DataFormat = DataFormat.FixedSize)]
public float tickTime { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Single	
traits
#### 선언
```cs
[ProtoMember(14, Name = "traits", DataFormat = DataFormat.Default)]
public List<TGameMapEventCommand> traits { get; }
#### 프로퍼티 값

|타입|설명|
System.Collections.Generic.List<network.TGameMapEventCommand>	
type
#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "type", DataFormat = DataFormat.TwosComplement)]
public int type { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
명시적 인터페이스 구현
IExtensible.GetExtensionObject(Boolean)
#### 선언
```cs
IExtension IExtensible.GetExtensionObject(bool createIfMissing)
매개 변수(인자)
타입	이름	설명
System.Boolean	createIfMissing	
반환

|타입|설명|
ProtoBuf.IExtension	
구현
ProtoBuf.IExtensible
확장 함수
Utility.Clone<T>(T)
Utility.DumpProtobufBase64<T>(T, System.Boolean)
Utility.DumpProtobuf<T>(T, System.Boolean)