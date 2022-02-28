---
layout: default
title: TOnlinePetData
parent: network
grand_parent: Server API
nav_order: 22
---

# Class TOnlinePetData

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TOnlinePetData
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
public class TOnlinePetData : IExtensible
```
## 생성자
---
TOnlinePetData()

#### 선언
```cs
public TOnlinePetData()
프로퍼티
characterID

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "characterID", DataFormat = DataFormat.TwosComplement)]
public int characterID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|exp|

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "exp", DataFormat = DataFormat.TwosComplement)]
public long exp { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|id|

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "id", DataFormat = DataFormat.TwosComplement)]
public int id { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|jobID|

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "jobID", DataFormat = DataFormat.TwosComplement)]
public int jobID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|level|

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "level", DataFormat = DataFormat.TwosComplement)]
public int level { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|name|

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|	

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