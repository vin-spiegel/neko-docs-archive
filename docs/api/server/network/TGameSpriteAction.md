---
layout: default
title: TGameSpriteAction
parent: network
grand_parent: Server API
nav_order: 16
---

# Class TGameSpriteAction

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameSpriteAction
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
public class TGameSpriteAction : IExtensible
```
## 생성자
---
## TGameSpriteAction()

#### 선언
```cs
public TGameSpriteAction()
```
## 프로퍼티
---
## delay

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "delay", DataFormat = DataFormat.TwosComplement)]
public int delay { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|loop|

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "loop", DataFormat = DataFormat.Default)]
public bool loop { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Boolean|name|

#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|nodes|

#### 선언
```cs
[ProtoMember(3, Name = "nodes", DataFormat = DataFormat.Default)]
public List<TGameSpriteActionCell> nodes { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<TGameSpriteActionCell>|

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