---
layout: default
title: TGameMapStub
parent: network
grand_parent: Server API
nav_order: 11
---

# Class TGameMapStub

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameMapStub
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
public class TGameMapStub : IExtensible
## 생성자
TGameMapStub()

#### 선언
```cs
public TGameMapStub()
프로퍼티
channelCount

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "channelCount", DataFormat = DataFormat.TwosComplement)]
public int channelCount { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
children

#### 선언
```cs
[ProtoMember(3, Name = "children", DataFormat = DataFormat.Default)]
public List<TGameMapStub> children { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<TGameMapStub>	
id

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "id", DataFormat = DataFormat.TwosComplement)]
public int id { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
isFolder

#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "isFolder", DataFormat = DataFormat.Default)]
public bool isFolder { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
maxPlayers

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "maxPlayers", DataFormat = DataFormat.TwosComplement)]
public int maxPlayers { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
name

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
oldID

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "oldID", DataFormat = DataFormat.Default)]
public string oldID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
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