---
layout: default
title: TGameDropItem
parent: network
grand_parent: Server API
nav_order: 7
---

# Class TGameDropItem

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameDropItem
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
public class TGameDropItem : IExtensible
## 생성자
TGameDropItem()
#### 선언
```cs
public TGameDropItem()
프로퍼티
itemDataID
#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "itemDataID", DataFormat = DataFormat.TwosComplement)]
public int itemDataID { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
itemLevel
#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "itemLevel", DataFormat = DataFormat.TwosComplement)]
public int itemLevel { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
maxCount
#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "maxCount", DataFormat = DataFormat.TwosComplement)]
public int maxCount { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
minCount
#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "minCount", DataFormat = DataFormat.TwosComplement)]
public int minCount { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Int32	
percent
#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "percent", DataFormat = DataFormat.FixedSize)]
public float percent { get; set; }
#### 프로퍼티 값

|타입|설명|
System.Single	
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