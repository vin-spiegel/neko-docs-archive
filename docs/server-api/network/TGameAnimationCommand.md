---
layout: default
title: TGameAnimationCommand
parent: network
grand_parent: Server API
nav_order: 2
---

# Class TGameAnimationCommand

#### 상속
<div class="code-example" markdown="1" style = "font-size:0.8em;">
↳ System.Object<br/>
　↳ TGameAnimationCommand
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
public class TGameAnimationCommand : IExtensible
## 생성자
TGameAnimationCommand()
#### 선언
```cs
public TGameAnimationCommand()
프로퍼티
actionName
#### 선언
```cs
[ProtoMember(19, IsRequired = false, Name = "actionName", DataFormat = DataFormat.Default)]
public string actionName { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
collisionAnimationID
#### 선언
```cs
[ProtoMember(14, IsRequired = false, Name = "collisionAnimationID", DataFormat = DataFormat.TwosComplement)]
public int collisionAnimationID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
collisionOffsetX
#### 선언
```cs
[ProtoMember(36, IsRequired = false, Name = "collisionOffsetX", DataFormat = DataFormat.FixedSize)]
public float collisionOffsetX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
collisionOffsetY
#### 선언
```cs
[ProtoMember(37, IsRequired = false, Name = "collisionOffsetY", DataFormat = DataFormat.FixedSize)]
public float collisionOffsetY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
collisionRadius
#### 선언
```cs
[ProtoMember(13, IsRequired = false, Name = "collisionRadius", DataFormat = DataFormat.FixedSize)]
public float collisionRadius { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
collisionWall
#### 선언
```cs
[ProtoMember(27, IsRequired = false, Name = "collisionWall", DataFormat = DataFormat.Default)]
public bool collisionWall { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
deleteOnCollision
#### 선언
```cs
[ProtoMember(26, IsRequired = false, Name = "deleteOnCollision", DataFormat = DataFormat.Default)]
public bool deleteOnCollision { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
directionSync
#### 선언
```cs
[ProtoMember(39, IsRequired = false, Name = "directionSync", DataFormat = DataFormat.Default)]
public bool directionSync { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
endColor
#### 선언
```cs
[ProtoMember(8, IsRequired = false, Name = "endColor", DataFormat = DataFormat.TwosComplement)]
public uint endColor { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.UInt32	
endScaleX
#### 선언
```cs
[ProtoMember(17, IsRequired = false, Name = "endScaleX", DataFormat = DataFormat.FixedSize)]
public float endScaleX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
endScaleY
#### 선언
```cs
[ProtoMember(18, IsRequired = false, Name = "endScaleY", DataFormat = DataFormat.FixedSize)]
public float endScaleY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
followUnit
#### 선언
```cs
[ProtoMember(35, IsRequired = false, Name = "followUnit", DataFormat = DataFormat.Default)]
public bool followUnit { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
gravityX
#### 선언
```cs
[ProtoMember(5, IsRequired = false, Name = "gravityX", DataFormat = DataFormat.FixedSize)]
public float gravityX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
gravityY
#### 선언
```cs
[ProtoMember(6, IsRequired = false, Name = "gravityY", DataFormat = DataFormat.FixedSize)]
public float gravityY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
includeEnemy
#### 선언
```cs
[ProtoMember(33, IsRequired = false, Name = "includeEnemy", DataFormat = DataFormat.Default)]
public bool includeEnemy { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
includeSameTeam
#### 선언
```cs
[ProtoMember(32, IsRequired = false, Name = "includeSameTeam", DataFormat = DataFormat.Default)]
public bool includeSameTeam { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
includeSelf
#### 선언
```cs
[ProtoMember(31, IsRequired = false, Name = "includeSelf", DataFormat = DataFormat.Default)]
public bool includeSelf { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
lifetime
#### 선언
```cs
[ProtoMember(20, IsRequired = false, Name = "lifetime", DataFormat = DataFormat.FixedSize)]
public float lifetime { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
maxCollisions
#### 선언
```cs
[ProtoMember(30, IsRequired = false, Name = "maxCollisions", DataFormat = DataFormat.TwosComplement)]
public int maxCollisions { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
moveSpeedX
#### 선언
```cs
[ProtoMember(3, IsRequired = false, Name = "moveSpeedX", DataFormat = DataFormat.FixedSize)]
public float moveSpeedX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
moveSpeedY
#### 선언
```cs
[ProtoMember(4, IsRequired = false, Name = "moveSpeedY", DataFormat = DataFormat.FixedSize)]
public float moveSpeedY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
playCommonEventID
#### 선언
```cs
[ProtoMember(29, IsRequired = false, Name = "playCommonEventID", DataFormat = DataFormat.TwosComplement)]
public int playCommonEventID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
randomOffsetX
#### 선언
```cs
[ProtoMember(11, IsRequired = false, Name = "randomOffsetX", DataFormat = DataFormat.FixedSize)]
public float randomOffsetX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
randomOffsetY
#### 선언
```cs
[ProtoMember(12, IsRequired = false, Name = "randomOffsetY", DataFormat = DataFormat.FixedSize)]
public float randomOffsetY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
rotationByFront
#### 선언
```cs
[ProtoMember(34, IsRequired = false, Name = "rotationByFront", DataFormat = DataFormat.FixedSize)]
public float rotationByFront { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
rotationToDir
#### 선언
```cs
[ProtoMember(28, IsRequired = false, Name = "rotationToDir", DataFormat = DataFormat.Default)]
public bool rotationToDir { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
sortingBack
#### 선언
```cs
[ProtoMember(38, IsRequired = false, Name = "sortingBack", DataFormat = DataFormat.Default)]
public bool sortingBack { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Boolean	
soundID
#### 선언
```cs
[ProtoMember(23, IsRequired = false, Name = "soundID", DataFormat = DataFormat.Default)]
public string soundID { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.String	
startColor
#### 선언
```cs
[ProtoMember(7, IsRequired = false, Name = "startColor", DataFormat = DataFormat.TwosComplement)]
public uint startColor { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.UInt32	
startDirOffsetX
#### 선언
```cs
[ProtoMember(9, IsRequired = false, Name = "startDirOffsetX", DataFormat = DataFormat.FixedSize)]
public float startDirOffsetX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
startDirOffsetY
#### 선언
```cs
[ProtoMember(10, IsRequired = false, Name = "startDirOffsetY", DataFormat = DataFormat.FixedSize)]
public float startDirOffsetY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
startOffsetX
#### 선언
```cs
[ProtoMember(24, IsRequired = false, Name = "startOffsetX", DataFormat = DataFormat.FixedSize)]
public float startOffsetX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
startOffsetY
#### 선언
```cs
[ProtoMember(25, IsRequired = false, Name = "startOffsetY", DataFormat = DataFormat.FixedSize)]
public float startOffsetY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
startScaleX
#### 선언
```cs
[ProtoMember(15, IsRequired = false, Name = "startScaleX", DataFormat = DataFormat.FixedSize)]
public float startScaleX { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
startScaleY
#### 선언
```cs
[ProtoMember(16, IsRequired = false, Name = "startScaleY", DataFormat = DataFormat.FixedSize)]
public float startScaleY { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
targetFlashColor
#### 선언
```cs
[ProtoMember(21, IsRequired = false, Name = "targetFlashColor", DataFormat = DataFormat.TwosComplement)]
public uint targetFlashColor { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.UInt32	
targetFlashTime
#### 선언
```cs
[ProtoMember(22, IsRequired = false, Name = "targetFlashTime", DataFormat = DataFormat.FixedSize)]
public float targetFlashTime { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
time
#### 선언
```cs
[ProtoMember(1, IsRequired = false, Name = "time", DataFormat = DataFormat.FixedSize)]
public float time { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Single	
type
#### 선언
```cs
[ProtoMember(2, IsRequired = false, Name = "type", DataFormat = DataFormat.TwosComplement)]
public int type { get; set; }
#### 프로퍼티 값

|타입|설명|
|:-|:-|
System.Int32	
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