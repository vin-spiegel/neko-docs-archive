---
layout: default
title: TGameLayoutPage
parent: network
grand_parent: Server API
nav_order: 10
---

# Class TGameLayoutPage

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameLayoutPage
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
public class TGameLayoutPage : IExtensible
## 생성자
TGameLayoutPage()
#### 선언
```cs
public TGameLayoutPage()
프로퍼티
autoRun
#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "autoRun", DataFormat = DataFormat.Default)]
public bool autoRun { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
controls
#### 선언
```cs
[ProtoMember(3, Name = "controls", DataFormat = DataFormat.Default)]
public List<TGameLayoutControl> controls { get; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<network.TGameLayoutControl>	
height
#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "height", DataFormat = DataFormat.TwosComplement)]
public int height { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
id
#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "id", DataFormat = DataFormat.TwosComplement)]
public int id { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
landscape
#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "landscape", DataFormat = DataFormat.Default)]
public bool landscape { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
name
#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
width
#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "width", DataFormat = DataFormat.TwosComplement)]
public int width { get; set; }
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