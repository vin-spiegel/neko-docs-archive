---
layout: default
title: TGameItem
parent: network
grand_parent: Server API
nav_order: 8
---

# Class TGameItem

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameItem
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
public class TGameItem : IExtensible
## 생성자
TGameItem()
#### 선언
```cs
public TGameItem()
프로퍼티
actionName
#### 선언
```cs
[ProtoMember(24, IsRequired = false, Name = "actionName", DataFormat = DataFormat.Default)]
public string actionName { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
agility
#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "agility", DataFormat = DataFormat.TwosComplement)]
public int agility { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
animationID
#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "animationID", DataFormat = DataFormat.TwosComplement)]
public int animationID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
attack
#### 선언
```cs
[ProtoMember(16, IsRequired = false, Name = "attack", DataFormat = DataFormat.TwosComplement)]
public int attack { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
buyerPrice
#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "buyerPrice", DataFormat = DataFormat.TwosComplement)]
public int buyerPrice { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
canDrop
#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "canDrop", DataFormat = DataFormat.Default)]
public bool canDrop { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
canExchangeTrade
#### 선언
```cs
[ProtoMember(32, IsRequired = false, Name = "canExchangeTrade", DataFormat = DataFormat.Default)]
public bool canExchangeTrade { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
canSell
#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "canSell", DataFormat = DataFormat.Default)]
public bool canSell { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
canStorage
#### 선언
```cs
[ProtoMember(30, IsRequired = false, Name = "canStorage", DataFormat = DataFormat.Default)]
public bool canStorage { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
canTrade
#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "canTrade", DataFormat = DataFormat.Default)]
public bool canTrade { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
coolTime
#### 선언
```cs
[ProtoMember(26, IsRequired = false, Name = "coolTime", DataFormat = DataFormat.FixedSize)]
public float coolTime { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
damageFormula
#### 선언
```cs
[ProtoMember(13, IsRequired = false, Name = "damageFormula", DataFormat = DataFormat.Default)]
public string damageFormula { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
damageType
#### 선언
```cs
[ProtoMember(12, IsRequired = false, Name = "damageType", DataFormat = DataFormat.TwosComplement)]
public int damageType { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
defense
#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "defense", DataFormat = DataFormat.TwosComplement)]
public int defense { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
desc
#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "desc", DataFormat = DataFormat.Default)]
public string desc { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
hasCritical
#### 선언
```cs
[ProtoMember(14, IsRequired = false, Name = "hasCritical", DataFormat = DataFormat.Default)]
public bool hasCritical { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
imageID
#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "imageID", DataFormat = DataFormat.Default)]
public string imageID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
l_desc
#### 선언
```cs
[ProtoMember(29, IsRequired = false, Name = "l_desc", DataFormat = DataFormat.Default)]
public LString l_desc { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
network.LString	
l_name
#### 선언
```cs
[ProtoMember(28, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
network.LString	
lucky
#### 선언
```cs
[ProtoMember(21, IsRequired = false, Name = "lucky", DataFormat = DataFormat.TwosComplement)]
public int lucky { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
magicAttack
#### 선언
```cs
[ProtoMember(18, IsRequired = false, Name = "magicAttack", DataFormat = DataFormat.TwosComplement)]
public int magicAttack { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
magicDefense
#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "magicDefense", DataFormat = DataFormat.TwosComplement)]
public int magicDefense { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
maxCount
#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "maxCount", DataFormat = DataFormat.TwosComplement)]
public int maxCount { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
maxHP
#### 선언
```cs
[ProtoMember(22, IsRequired = false, Name = "maxHP", DataFormat = DataFormat.TwosComplement)]
public int maxHP { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
maxMP
#### 선언
```cs
[ProtoMember(23, IsRequired = false, Name = "maxMP", DataFormat = DataFormat.TwosComplement)]
public int maxMP { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
memo
#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "memo", DataFormat = DataFormat.Default)]
public string memo { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
name
#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
notConsumed
#### 선언
```cs
[ProtoMember(33, IsRequired = false, Name = "notConsumed", DataFormat = DataFormat.Default)]
public bool notConsumed { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
oldTraits
#### 선언
```cs
[ProtoMember(15, Name = "oldTraits", DataFormat = DataFormat.Default)]
public List<TGameTrait> oldTraits { get; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<network.TGameTrait>	
sellerPrice
#### 선언
```cs
[ProtoMember(27, IsRequired = false, Name = "sellerPrice", DataFormat = DataFormat.TwosComplement)]
public int sellerPrice { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
spineImageID
#### 선언
```cs
[ProtoMember(31, IsRequired = false, Name = "spineImageID", DataFormat = DataFormat.Default)]
public string spineImageID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
traits
#### 선언
```cs
[ProtoMember(25, Name = "traits", DataFormat = DataFormat.Default)]
public List<TGameMapEventCommand> traits { get; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<network.TGameMapEventCommand>	
type
#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "type", DataFormat = DataFormat.TwosComplement)]
public int type { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
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
|:-|:-|
ProtoBuf.IExtension	
구현
ProtoBuf.IExtensible
확장 함수
Utility.JobCheck(network.TGameItem, System.Int32)
Utility.Clone<T>(T)
Utility.DumpProtobufBase64<T>(T, System.Boolean)
Utility.DumpProtobuf<T>(T, System.Boolean)
