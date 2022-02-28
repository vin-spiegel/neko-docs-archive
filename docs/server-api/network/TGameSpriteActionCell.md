---
layout: default
title: TGameSpriteActionCell
parent: network
grand_parent: Server API
nav_order: 17
---

# Class TGameSpriteActionCell

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameSpriteActionCell
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
public class TGameSpriteActionCell : IExtensible
## 생성자
TGameSpriteActionCell()

#### 선언
```cs
public TGameSpriteActionCell()
프로퍼티
height

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "height", DataFormat = DataFormat.TwosComplement)]
public int height { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
width

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "width", DataFormat = DataFormat.TwosComplement)]
public int width { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
x

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "x", DataFormat = DataFormat.TwosComplement)]
public int x { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
y

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "y", DataFormat = DataFormat.TwosComplement)]
public int y { get; set; }
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