---
layout: default
title: TGameCollection
parent: network
grand_parent: Server API
nav_order: 5
---

# Class TGameCollection

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameCollection
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
public class TGameCollection : IExtensible
```
## 생성자
TGameCollection()

#### 선언
```cs
public TGameCollection()
```
## 프로퍼티
---
## desc

#### 선언
```cs
[ProtoMember(18, IsRequired = false, Name = "desc", DataFormat = DataFormat.Default)]
public string desc { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|iconID|

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "iconID", DataFormat = DataFormat.Default)]
public string iconID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|itemCount1|

#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "itemCount1", DataFormat = DataFormat.TwosComplement)]
public int itemCount1 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|itemCount2|

#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "itemCount2", DataFormat = DataFormat.TwosComplement)]
public int itemCount2 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|itemCount3|

#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "itemCount3", DataFormat = DataFormat.TwosComplement)]
public int itemCount3 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|itemCount4|

#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "itemCount4", DataFormat = DataFormat.TwosComplement)]
public int itemCount4 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|itemID1|

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "itemID1", DataFormat = DataFormat.TwosComplement)]
public int itemID1 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|itemID2|

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "itemID2", DataFormat = DataFormat.TwosComplement)]
public int itemID2 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|itemID3|

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "itemID3", DataFormat = DataFormat.TwosComplement)]
public int itemID3 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|itemID4|

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "itemID4", DataFormat = DataFormat.TwosComplement)]
public int itemID4 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|l_desc|

#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "l_desc", DataFormat = DataFormat.Default)]
public LString l_desc { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|network.LString|l_name|

#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|network.LString|memo|

#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "memo", DataFormat = DataFormat.Default)]
public string memo { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|name|

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|rewardGameMoney|

#### 선언
```cs
[ProtoMember(15, IsRequired = false, Name = "rewardGameMoney", DataFormat = DataFormat.TwosComplement)]
public long rewardGameMoney { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|rewardItemCount1|

#### 선언
```cs
[ProtoMember(13, IsRequired = false, Name = "rewardItemCount1", DataFormat = DataFormat.TwosComplement)]
public int rewardItemCount1 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|rewardItemCount2|

#### 선언
```cs
[ProtoMember(14, IsRequired = false, Name = "rewardItemCount2", DataFormat = DataFormat.TwosComplement)]
public int rewardItemCount2 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|rewardItemID1|

#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "rewardItemID1", DataFormat = DataFormat.TwosComplement)]
public int rewardItemID1 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|rewardItemID2|

#### 선언
```cs
[ProtoMember(12, IsRequired = false, Name = "rewardItemID2", DataFormat = DataFormat.TwosComplement)]
public int rewardItemID2 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|traits|

#### 선언
```cs
[ProtoMember(16, Name = "traits", DataFormat = DataFormat.Default)]
public List<TGameMapEventCommand> traits { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<network.TGameMapEventCommand>|

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
ProtoBuf.IExtensible