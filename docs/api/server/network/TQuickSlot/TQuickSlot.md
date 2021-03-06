---
layout: default
title: TQuickSlot
parent: network
grand_parent: Server API
nav_order: 23
---

# Class TQuickSlot

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TQuickSlot
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
public class TQuickSlot : IExtensible
```

## 생성자
---
## TQuickSlot()

#### 선언
```cs
public TQuickSlot()
```
## 프로퍼티
---
## itemID

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "itemID", DataFormat = DataFormat.TwosComplement)]
public long itemID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int64|skillDataID|

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "skillDataID", DataFormat = DataFormat.TwosComplement)]
public int skillDataID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|	

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