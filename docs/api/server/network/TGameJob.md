---
layout: default
title: TGameJob
parent: network
grand_parent: Server API
nav_order: 9
---

# Class TGameJob

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameJob
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
public class TGameJob : IExtensible
```
## 생성자
---
## TGameJob()

#### 선언
```cs
public TGameJob()
```
## 프로퍼티
---
## agilities

#### 선언
```cs
[ProtoMember(10, Name = "agilities", DataFormat = DataFormat.TwosComplement)]
public List<int> agilities { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|attacks|

#### 선언
```cs
[ProtoMember(6, Name = "attacks", DataFormat = DataFormat.TwosComplement)]
public List<int> attacks { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|defenses|

#### 선언
```cs
[ProtoMember(7, Name = "defenses", DataFormat = DataFormat.TwosComplement)]
public List<int> defenses { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|exps|

#### 선언
```cs
[ProtoMember(3, Name = "exps", DataFormat = DataFormat.TwosComplement)]
public List<int> exps { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|l_name|

#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|network.LString|learnSkills|

#### 선언
```cs
[ProtoMember(12, Name = "learnSkills", DataFormat = DataFormat.Default)]
public List<TSkill> learnSkills { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<network.TSkill>|luckies|

#### 선언
```cs
[ProtoMember(11, Name = "luckies", DataFormat = DataFormat.TwosComplement)]
public List<int> luckies { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|magicAttacks|

#### 선언
```cs
[ProtoMember(8, Name = "magicAttacks", DataFormat = DataFormat.TwosComplement)]
public List<int> magicAttacks { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|magicDefenses|

#### 선언
```cs
[ProtoMember(9, Name = "magicDefenses", DataFormat = DataFormat.TwosComplement)]
public List<int> magicDefenses { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|maxHPs|

#### 선언
```cs
[ProtoMember(4, Name = "maxHPs", DataFormat = DataFormat.TwosComplement)]
public List<int> maxHPs { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|maxLevel|

#### 선언
```cs
[ProtoMember(16, IsRequired = false, Name = "maxLevel", DataFormat = DataFormat.TwosComplement)]
public int maxLevel { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Int32|maxMPs|

#### 선언
```cs
[ProtoMember(5, Name = "maxMPs", DataFormat = DataFormat.TwosComplement)]
public List<int> maxMPs { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Int32>|memo|

#### 선언
```cs
[ProtoMember(14, IsRequired = false, Name = "memo", DataFormat = DataFormat.Default)]
public string memo { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|name|

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|oldTraits|

#### 선언
```cs
[ProtoMember(13, Name = "oldTraits", DataFormat = DataFormat.Default)]
public List<TGameTrait> oldTraits { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<network.TGameTrait>|traits|

#### 선언
```cs
[ProtoMember(15, Name = "traits", DataFormat = DataFormat.Default)]
public List<TGameMapEventCommand> traits { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<network.TGameMapEventCommand>|

## 명시적 인터페이스 구현
---
IExtensible.GetExtensionObject(Boolean)

#### 선언
```cs
IExtension IExtensible.GetExtensionObject(bool createIfMissing)
```
### 매개 변수 (인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Boolean|createIfMissing	|

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