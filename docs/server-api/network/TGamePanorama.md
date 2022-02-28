---
layout: default
title: TGamePanorama
parent: network
grand_parent: Server API
nav_order: 13
---

# Class TGamePanorama

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGamePanorama
</div>

구현: ProtoBuf.IExtensible
{: .text-zeta}

네임스페이스: [network](../)
{: .text-zeta}

어셈블리: Creator.dll
{: .text-zeta}

Syntax
[Serializable]
public class TGamePanorama : IExtensible
생성자
TGamePanorama()
선언
public TGamePanorama()
프로퍼티
distanceX
선언
[ProtoMember(9, IsRequired = false, Name = "distanceX", DataFormat = DataFormat.FixedSize)]
public float distanceX { get; set; }
프로퍼티 값
타입	설명
System.Single	
distanceY
선언
[ProtoMember(10, IsRequired = false, Name = "distanceY", DataFormat = DataFormat.FixedSize)]
public float distanceY { get; set; }
프로퍼티 값
타입	설명
System.Single	
gapX
선언
[ProtoMember(5, IsRequired = false, Name = "gapX", DataFormat = DataFormat.FixedSize)]
public float gapX { get; set; }
프로퍼티 값
타입	설명
System.Single	
gapY
선언
[ProtoMember(6, IsRequired = false, Name = "gapY", DataFormat = DataFormat.FixedSize)]
public float gapY { get; set; }
프로퍼티 값
타입	설명
System.Single	
loopX
선언
[ProtoMember(7, IsRequired = false, Name = "loopX", DataFormat = DataFormat.Default)]
public bool loopX { get; set; }
프로퍼티 값
타입	설명
System.Boolean	
loopY
선언
[ProtoMember(8, IsRequired = false, Name = "loopY", DataFormat = DataFormat.Default)]
public bool loopY { get; set; }
프로퍼티 값
타입	설명
System.Boolean	
offsetX
선언
[ProtoMember(3, IsRequired = false, Name = "offsetX", DataFormat = DataFormat.FixedSize)]
public float offsetX { get; set; }
프로퍼티 값
타입	설명
System.Single	
offsetY
선언
[ProtoMember(4, IsRequired = false, Name = "offsetY", DataFormat = DataFormat.FixedSize)]
public float offsetY { get; set; }
프로퍼티 값
타입	설명
System.Single	
scaleX
선언
[ProtoMember(1, IsRequired = false, Name = "scaleX", DataFormat = DataFormat.FixedSize)]
public float scaleX { get; set; }
프로퍼티 값
타입	설명
System.Single	
scaleY
선언
[ProtoMember(2, IsRequired = false, Name = "scaleY", DataFormat = DataFormat.FixedSize)]
public float scaleY { get; set; }
프로퍼티 값
타입	설명
System.Single	
명시적 인터페이스 구현
IExtensible.GetExtensionObject(Boolean)
선언
IExtension IExtensible.GetExtensionObject(bool createIfMissing)
매개 변수(인자)
타입	이름	설명
System.Boolean	createIfMissing	
반환
타입	설명
ProtoBuf.IExtension	
구현
ProtoBuf.IExtensible
확장 함수
Utility.Clone<T>(T)
Utility.DumpProtobufBase64<T>(T, System.Boolean)
Utility.DumpProtobuf<T>(T, System.Boolean)