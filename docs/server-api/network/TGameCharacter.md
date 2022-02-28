---
layout: default
title: TGameCharacter
parent: network
grand_parent: Server API
nav_order: 4
---

# Class TGameCharacter

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameCharacter
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
public class TGameCharacter : IExtensible
## 생성자
TGameCharacter()
#### 선언
```cs
public TGameCharacter()
프로퍼티
collision
#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "collision", DataFormat = DataFormat.Default)]
public bool collision { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
footstepSoundID
#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "footstepSoundID", DataFormat = DataFormat.Default)]
public string footstepSoundID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
imageID
#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "imageID", DataFormat = DataFormat.Default)]
public string imageID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
jumpForce
#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "jumpForce", DataFormat = DataFormat.FixedSize)]
public float jumpForce { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
l_name
#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
network.LString	
memo
#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "memo", DataFormat = DataFormat.Default)]
public string memo { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
moveSpeed
#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "moveSpeed", DataFormat = DataFormat.TwosComplement)]
public int moveSpeed { get; set; }
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
traits
#### 선언
```cs
[ProtoMember(7, Name = "traits", DataFormat = DataFormat.Default)]
public List<TGameMapEventCommand> traits { get; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<network.TGameMapEventCommand>	
type
#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "type", DataFormat = DataFormat.TwosComplement)]
public int type { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
useCloudCharacter
#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "useCloudCharacter", DataFormat = DataFormat.Default)]
public bool useCloudCharacter { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
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