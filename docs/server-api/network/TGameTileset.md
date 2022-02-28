---
layout: default
title: TGameTileset
parent: network
grand_parent: Server API
nav_order: 19
---

# Class TGameTileset

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameTileset
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
public class TGameTileset : IExtensible
```
## 생성자
---
## TGameTileset()

#### 선언
```cs
public TGameTileset()
```

## 프로퍼티
---
## autoTile1ID

#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "autoTile1ID", DataFormat = DataFormat.Default)]
public string autoTile1ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|autoTile2ID|

#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "autoTile2ID", DataFormat = DataFormat.Default)]
public string autoTile2ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|autoTile3ID|

#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "autoTile3ID", DataFormat = DataFormat.Default)]
public string autoTile3ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|autoTile4ID|

#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "autoTile4ID", DataFormat = DataFormat.Default)]
public string autoTile4ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|autoTile5ID|

#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "autoTile5ID", DataFormat = DataFormat.Default)]
public string autoTile5ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|autoTile6ID|

#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "autoTile6ID", DataFormat = DataFormat.Default)]
public string autoTile6ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|autoTile7ID|

#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "autoTile7ID", DataFormat = DataFormat.Default)]
public string autoTile7ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|bushes|

#### 선언
```cs
[ProtoMember(14, Name = "bushes", DataFormat = DataFormat.TwosComplement)]
public List<uint> bushes { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.UInt32>|fogID|

#### 선언
```cs
[ProtoMember(16, IsRequired = false, Name = "fogID", DataFormat = DataFormat.Default)]
public string fogID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|imageID|

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
[ProtoMember(27, IsRequired = false, Name = "l_name", DataFormat = DataFormat.Default)]
public LString l_name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|network.LString|movables|

#### 선언
```cs
[ProtoMember(11, Name = "movables", DataFormat = DataFormat.Default)]
public List<bool> movables { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.Boolean>|movables4Ways|

#### 선언
```cs
[ProtoMember(12, Name = "movables4Ways", DataFormat = DataFormat.TwosComplement)]
public List<uint> movables4Ways { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.UInt32>|name|

#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "name", DataFormat = DataFormat.Default)]
public string name { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|objects|

#### 선언
```cs
[ProtoMember(28, Name = "objects", DataFormat = DataFormat.Default)]
public List<TGameTilesetObject> objects { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<network.TGameTilesetObject>|panorama1|

#### 선언
```cs
[ProtoMember(18, IsRequired = false, Name = "panorama1", DataFormat = DataFormat.Default)]
public TGamePanorama panorama1 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|TGamePanorama|panorama1ID|

#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "panorama1ID", DataFormat = DataFormat.Default)]
public string panorama1ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|panorama2|

#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "panorama2", DataFormat = DataFormat.Default)]
public TGamePanorama panorama2 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|TGamePanorama|panorama2ID|

#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "panorama2ID", DataFormat = DataFormat.Default)]
public string panorama2ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|panorama3|

#### 선언
```cs
[ProtoMember(22, IsRequired = false, Name = "panorama3", DataFormat = DataFormat.Default)]
public TGamePanorama panorama3 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|TGamePanorama|panorama3ID|

#### 선언
```cs
[ProtoMember(21, IsRequired = false, Name = "panorama3ID", DataFormat = DataFormat.Default)]
public string panorama3ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|panorama4|

#### 선언
```cs
[ProtoMember(24, IsRequired = false, Name = "panorama4", DataFormat = DataFormat.Default)]
public TGamePanorama panorama4 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|TGamePanorama|panorama4ID|

#### 선언
```cs
[ProtoMember(23, IsRequired = false, Name = "panorama4ID", DataFormat = DataFormat.Default)]
public string panorama4ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|panorama5|

#### 선언
```cs
[ProtoMember(26, IsRequired = false, Name = "panorama5", DataFormat = DataFormat.Default)]
public TGamePanorama panorama5 { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|TGamePanorama|panorama5ID|

#### 선언
```cs
[ProtoMember(25, IsRequired = false, Name = "panorama5ID", DataFormat = DataFormat.Default)]
public string panorama5ID { get; set; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.String|priorities|

#### 선언
```cs
[ProtoMember(13, Name = "priorities", DataFormat = DataFormat.TwosComplement)]
public List<uint> priorities { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.UInt32>|tag|

#### 선언
```cs
[ProtoMember(15, Name = "tag", DataFormat = DataFormat.TwosComplement)]
public List<uint> tag { get; }
```
#### 프로퍼티 값

|타입|설명|
|:-|:-|
|System.Collections.Generic.List<System.UInt32>|

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