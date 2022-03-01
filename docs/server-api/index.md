---
layout: default
title: Server API
has_children: true
nav_order: 3
# permalink: /docs/server-api
---
{:toc}

# 서버 스크립트

네코랜드 서버 스크립트에 대한 문서입니다
 
## Tips

보통 주체가 되는 플레이어 유닛을 찾을 수 있는 스크립트를 입력하는 공간에는 로컬 테이블에 `unit` 키워드가 존재합니다. 전역 공간에 생성한 변수들은 모든 스크립트 실행에 공유됩니다. 파일에 직업 적용한 스크립트에서 함수를 정의하고, 이벤트 실행시의 스크립트에서 해당 함수를 사용하는 방식도 가능합니다.

