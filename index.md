---
title: 시작하기
layout: home
has_children: true
nav_order: 1
---

<br/>

네코랜드 Docs 아카이브
{: .fs-10 .fw_700 .text-center .lh-tight }
네코랜드 Lua 스크립팅에 대한 내용을 담은 비공식 Docs 입니다
{: .fs-6 .fw-300 .text-center .lh-tight }

<br/>

<div align="center" class= "fs-7">
    <button type="button" class="btn mr-5 btn-purple" onclick="location.href='docs/getting-start/what-is-script'">시작하기</button>
    <button type="button" class="btn btn-outline" onclick="location.href='https://github.com/vin-spiegel/neko-docs-archive'">GitHub</button>
</div>

<br/><br/>

<div class="code-example" markdown="1">
<p style="font-size:20px"><strong>간단한 API</strong></p>

네코랜드 스튜디오 스크립트는 간단한 API로 이루어져 있습니다. 예제를 따라하며 내 게임에 스크립트를 넣어보세요.
</div>
```lua
function sendHello(player)
    player.unit.SendCenterLabel("Hello " .. player.name .. "!")
end

Server.onJoinPlayer.Add(sendHello)
```

<div class="code-example" markdown="1">
<p style="font-size:20px"><strong>쉬운 적용</strong></p>

네코랜드 스크립트는 스튜디오에서 스크립트를 적용시킬 수도 있고, 파일에 직접 넣어 적용 할 수도 있습니다. 또 채팅창에서도 스크립트를 바로 작성 해볼 수 있습니다
</div>
```lua
--채팅창에 입력
/script print("Hello world")
```
