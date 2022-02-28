---
layout: default
title: TGameMonster
parent: network
grand_parent: Server API
nav_order: 12
---

# Class TGameMonster

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameMonster
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
public class TGameMonster : IExtensible
## 생성자
TGameMonster()
#### 선언
```cs
public TGameMonster()
프로퍼티
agility
#### 선언
```cs
[ProtoMember(15, IsRequired = false, Name = "agility", DataFormat = DataFormat.TwosComplement)]
public int agility { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
attack
#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "attack", DataFormat = DataFormat.TwosComplement)]
public int attack { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
attackOffsetX
#### 선언
```cs
[ProtoMember(31, IsRequired = false, Name = "attackOffsetX", DataFormat = DataFormat.TwosComplement)]
public int attackOffsetX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
attackOffsetY
#### 선언
```cs
[ProtoMember(32, IsRequired = false, Name = "attackOffsetY", DataFormat = DataFormat.TwosComplement)]
public int attackOffsetY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
attackRange
#### 선언
```cs
[ProtoMember(29, IsRequired = false, Name = "attackRange", DataFormat = DataFormat.TwosComplement)]
public int attackRange { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
attackTime
#### 선언
```cs
[ProtoMember(26, IsRequired = false, Name = "attackTime", DataFormat = DataFormat.FixedSize)]
public float attackTime { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
attackType
#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "attackType", DataFormat = DataFormat.TwosComplement)]
public int attackType { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
collision
#### 선언
```cs
[ProtoMember(24, IsRequired = false, Name = "collision", DataFormat = DataFormat.Default)]
public bool collision { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
collisionWithMap
#### 선언
```cs
[ProtoMember(33, IsRequired = false, Name = "collisionWithMap", DataFormat = DataFormat.Default)]
public bool collisionWithMap { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
consumeFatigue
#### 선언
```cs
[ProtoMember(28, IsRequired = false, Name = "consumeFatigue", DataFormat = DataFormat.TwosComplement)]
public long consumeFatigue { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int64	
defense
#### 선언
```cs
[ProtoMember(12, IsRequired = false, Name = "defense", DataFormat = DataFormat.TwosComplement)]
public int defense { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
dropEXP
#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "dropEXP", DataFormat = DataFormat.TwosComplement)]
public long dropEXP { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int64	
dropItems
#### 선언
```cs
[ProtoMember(4, Name = "dropItems", DataFormat = DataFormat.Default)]
public List<TGameDropItem> dropItems { get; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<TGameDropItem>	
dropMaxGameMoney
#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "dropMaxGameMoney", DataFormat = DataFormat.TwosComplement)]
public long dropMaxGameMoney { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int64	
dropMinGameMoney
#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "dropMinGameMoney", DataFormat = DataFormat.TwosComplement)]
public long dropMinGameMoney { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int64	
imageID
#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "imageID", DataFormat = DataFormat.Default)]
public string imageID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
isDirectGiveItem
#### 선언
```cs
[ProtoMember(35, IsRequired = false, Name = "isDirectGiveItem", DataFormat = DataFormat.Default)]
public bool isDirectGiveItem { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
l_name
#### 선언
```cs
[ProtoMember(34, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
network.LString	
lucky
#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "lucky", DataFormat = DataFormat.TwosComplement)]
public int lucky { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
magicAttack
#### 선언
```cs
[ProtoMember(13, IsRequired = false, Name = "magicAttack", DataFormat = DataFormat.TwosComplement)]
public int magicAttack { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
magicDefense
#### 선언
```cs
[ProtoMember(14, IsRequired = false, Name = "magicDefense", DataFormat = DataFormat.TwosComplement)]
public int magicDefense { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
maxHP
#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "maxHP", DataFormat = DataFormat.TwosComplement)]
public int maxHP { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
maxLevel
#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "maxLevel", DataFormat = DataFormat.TwosComplement)]
public int maxLevel { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
maxMP
#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "maxMP", DataFormat = DataFormat.TwosComplement)]
public int maxMP { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
memo
#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "memo", DataFormat = DataFormat.Default)]
public string memo { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
minLevel
#### 선언
```cs
[ProtoMember(18, IsRequired = false, Name = "minLevel", DataFormat = DataFormat.TwosComplement)]
public int minLevel { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
moveSpeed
#### 선언
```cs
[ProtoMember(21, IsRequired = false, Name = "moveSpeed", DataFormat = DataFormat.TwosComplement)]
public int moveSpeed { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
moveStyle
#### 선언
```cs
[ProtoMember(23, IsRequired = false, Name = "moveStyle", DataFormat = DataFormat.TwosComplement)]
public int moveStyle { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
name
#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
respawnTime
#### 선언
```cs
[ProtoMember(22, IsRequired = false, Name = "respawnTime", DataFormat = DataFormat.TwosComplement)]
public int respawnTime { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
teamTag
#### 선언
```cs
[ProtoMember(27, IsRequired = false, Name = "teamTag", DataFormat = DataFormat.TwosComplement)]
public uint teamTag { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.UInt32	
traits
#### 선언
```cs
[ProtoMember(25, Name = "traits", DataFormat = DataFormat.Default)]
public List<TGameMapEventCommand> traits { get; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<network.TGameMapEventCommand>	
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
Utility.Clone<T>(T)
Utility.DumpProtobufBase64<T>(T, System.Boolean)
Utility.DumpProtobuf<T>(T, System.Boolean)