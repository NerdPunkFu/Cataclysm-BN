---
title: 문법적 성별
---

NPC 대화(및 기타 문자열)의 경우 일부 언어의 경우 대화 참가자의 성별에 따라 대체 번역이 필요할 수
있습니다. 이 두 가지 초기 구성은 다음과 같습니다.

1. 대화를 정의하는 json 파일에 관련 성별이 나열되어 있어야 합니다. 참고:
   [NPC 문서](../../mod/json/reference/creatures/npcs).
2. 각 언어는 `data/raw/languages.json`에 있는 언어 항목의 `genders` 목록을 통해 사용하고자 하는
   성별을 지정해야 합니다. 성별이 필요하다는 확신이 들 때까지는 성별을 추가하지 않는 것이 좋습니다.
   현재 선택 가능한 항목은 다음과 같습니다: `m`(남성), `f`(여성), `n`(중성). 현재 지원되는 성별과
   다른 성별이 필요한 경우 `src/language.h`의 관련 참고 사항을 참조하세요.

이렇게 하면 메시지 컨텍스트에 지정된 성별에 따라 관련 대화 행이 번역에 여러 번 표시됩니다. 예를 들어
`npc:m`의 컨텍스트는 대화에 참여한 NPC가 남성이라는 것을 나타냅니다.

기술적인 제한으로 인해 지원되는 모든 성별이 컨텍스트로 표시되지만, 해당 언어의 문법적 성별 목록에
나열된 성별에 대한 번역만 제공하면 됩니다.

게임의 다른 부분에는 문법적 성별에 대한 다양한 임시 해결책이 있으므로 다른 문자열에 대해 다른
컨텍스트가 표시되어도 놀라지 마세요.
