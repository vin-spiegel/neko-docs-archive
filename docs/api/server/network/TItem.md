---
layout: default
title: TItem
parent: network
grand_parent: Server API
nav_order: 20
---

# Class TItem

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TItem
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
public class TItem : IExtensible
```
## 생성자
---
## TItem()

#### 선언
```cs
public TItem()
```
## 프로퍼티
---
## count

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "count", DataFormat = DataFormat.TwosComplement)]
public int count { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|dataID|

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "dataID", DataFormat = DataFormat.TwosComplement)]
public int dataID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|id|

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "id", DataFormat = DataFormat.TwosComplement)]
public long id { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|index|

#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "index", DataFormat = DataFormat.TwosComplement)]
public int index { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|inTrade|

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "inTrade", DataFormat = DataFormat.Default)]
public bool inTrade { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Boolean|level|

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "level", DataFormat = DataFormat.TwosComplement)]
public int level { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|locked|

#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "locked", DataFormat = DataFormat.Default)]
public bool locked { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Boolean|nftTokenID|

#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "nftTokenID", DataFormat = DataFormat.TwosComplement)]
public long nftTokenID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|options|

#### 선언
```cs
[ProtoMember(6, Name = "options", DataFormat = DataFormat.Default)]
public List<TItemOption> options { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<TItemOption>|useCloudResource|

#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "useCloudResource", DataFormat = DataFormat.Default)]
public bool useCloudResource { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Boolean|	

## 명시적 인터페이스 구현
---
## IExtensible.GetExtensionObject(Boolean)

#### 선언
```cs
IExtension IExtensible.GetExtensionObject(bool createIfMissing)
```
### 매개 변수 (인자)
|타입|이름|설명|
|:-|:-|:-|
|System.Boolean|createIfMissing|

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