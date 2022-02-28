---
layout: default
title: TGameAnimation
parent: network
grand_parent: Server API
nav_order: 1
---

# Class TGameAnimation

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameAnimation
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
public class TGameAnimation : IExtensible
```
## 생성자
---

## TGameAnimation()

#### 선언
```cs
public TGameAnimation()
```
## 프로퍼티
---
## commands

#### 선언
```cs
[ProtoMember(4, Name = "commands", DataFormat = DataFormat.Default)]
public List<TGameAnimationCommand> commands { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<TGameAnimationCommand>|imageID|

#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "imageID", DataFormat = DataFormat.Default)]
public string imageID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|l_name|

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|network.LString|name|

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|persistentTeleport|

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "persistentTeleport", DataFormat = DataFormat.Default)]
public bool persistentTeleport { get; set; }
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