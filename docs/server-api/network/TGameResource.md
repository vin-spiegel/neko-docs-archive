---
layout: default
title: TGameResource
parent: network
grand_parent: Server API
nav_order: 14
---

# Class TGameResource

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameResource
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
public class TGameResource : IExtensible
## 생성자
TGameResource()

#### 선언
```cs
public TGameResource()
프로퍼티
actions

#### 선언
```cs
[ProtoMember(5, Name = "actions", DataFormat = DataFormat.Default)]
public List<TGameSpriteAction> actions { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<TGameSpriteAction>	
ambientIntansity

#### 선언
```cs
[ProtoMember(14, IsRequired = false, Name = "ambientIntansity", DataFormat = DataFormat.TwosComplement)]
public int ambientIntansity { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
ambientOffsetX

#### 선언
```cs
[ProtoMember(15, IsRequired = false, Name = "ambientOffsetX", DataFormat = DataFormat.TwosComplement)]
public int ambientOffsetX { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
ambientOffsetY

#### 선언
```cs
[ProtoMember(16, IsRequired = false, Name = "ambientOffsetY", DataFormat = DataFormat.TwosComplement)]
public int ambientOffsetY { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
collisionHeight

#### 선언
```cs
[ProtoMember(22, IsRequired = false, Name = "collisionHeight", DataFormat = DataFormat.TwosComplement)]
public int collisionHeight { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
collisionOffsetX

#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "collisionOffsetX", DataFormat = DataFormat.TwosComplement)]
public int collisionOffsetX { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
collisionOffsetY

#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "collisionOffsetY", DataFormat = DataFormat.TwosComplement)]
public int collisionOffsetY { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
collisionWidth

#### 선언
```cs
[ProtoMember(21, IsRequired = false, Name = "collisionWidth", DataFormat = DataFormat.TwosComplement)]
public int collisionWidth { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
enableNineSliced

#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "enableNineSliced", DataFormat = DataFormat.Default)]
public bool enableNineSliced { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
folder

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "folder", DataFormat = DataFormat.Default)]
public string folder { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
id

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "id", DataFormat = DataFormat.Default)]
public string id { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
name

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
nameOffsetX

#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "nameOffsetX", DataFormat = DataFormat.TwosComplement)]
public int nameOffsetX { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
nameOffsetY

#### 선언
```cs
[ProtoMember(18, IsRequired = false, Name = "nameOffsetY", DataFormat = DataFormat.TwosComplement)]
public int nameOffsetY { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
nameScale

#### 선언
```cs
[ProtoMember(23, IsRequired = false, Name = "nameScale", DataFormat = DataFormat.FixedSize)]
public float nameScale { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
spriteBorderBottom

#### 선언
```cs
[ProtoMember(13, IsRequired = false, Name = "spriteBorderBottom", DataFormat = DataFormat.TwosComplement)]
public int spriteBorderBottom { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
spriteBorderLeft

#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "spriteBorderLeft", DataFormat = DataFormat.TwosComplement)]
public int spriteBorderLeft { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
spriteBorderRight

#### 선언
```cs
[ProtoMember(12, IsRequired = false, Name = "spriteBorderRight", DataFormat = DataFormat.TwosComplement)]
public int spriteBorderRight { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
spriteBorderTop

#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "spriteBorderTop", DataFormat = DataFormat.TwosComplement)]
public int spriteBorderTop { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
spriteCellX

#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "spriteCellX", DataFormat = DataFormat.TwosComplement)]
public int spriteCellX { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
spriteCellY

#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "spriteCellY", DataFormat = DataFormat.TwosComplement)]
public int spriteCellY { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
spriteType

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "spriteType", DataFormat = DataFormat.TwosComplement)]
public int spriteType { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
type

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "type", DataFormat = DataFormat.TwosComplement)]
public int type { get; set; }
```
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
Utility.Clone<T>(T)
Utility.DumpProtobufBase64<T>(T, System.Boolean)
Utility.DumpProtobuf<T>(T, System.Boolean)