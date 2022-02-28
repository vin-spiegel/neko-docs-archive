---
layout: default
title: TGameCommonEvent
parent: network
grand_parent: Server API
nav_order: 6
---

# Class TGameCommonEvent

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameCommonEvent
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
public class TGameCommonEvent : IExtensible
## 생성자
TGameCommonEvent()

#### 선언
```cs
public TGameCommonEvent()
프로퍼티
conditionSwitch1ID

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "conditionSwitch1ID", DataFormat = DataFormat.TwosComplement)]
public int conditionSwitch1ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
l_name

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
network.LString	
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
page

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "page", DataFormat = DataFormat.Default)]
public TGameMapEventPage page { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
network.TGameMapEventPage	
startCondition

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "startCondition", DataFormat = DataFormat.TwosComplement)]
public int startCondition { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
targetPlayerSelector

#### 선언
```cs
[ProtoMember(7, Name = "targetPlayerSelector", DataFormat = DataFormat.TwosComplement)]
public List<int> targetPlayerSelector { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Collections.Generic.List<System.Int32>	
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
