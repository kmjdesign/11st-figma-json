# JSON 다운로드

11번가 화면에서 사용하는 Lottie 애니메이션 JSON 파일입니다. Figma 등 외부 도구에서 아래 다운로드 주소로 바로 가져다 씁니다.

## 구조

- 저장소의 폴더 안 파일이 **원본**입니다. 수정 이력이 여기에 남습니다.
- 릴리스 `v1.0.0`의 첨부 파일이 **배포본**입니다. Figma 등에서 쓰는 다운로드 주소는 이 첨부 파일을 가리킵니다. 첨부 파일에는 폴더가 없고 파일명만 있습니다.
- 현재 저장소 파일과 릴리스 첨부 파일은 내용이 동일합니다.

```
ai/        AI 관련
search/    통합검색 일반 (필요해질 때 추가)
common/    여러 화면에서 함께 쓰는 공용 모션 (필요해질 때 추가)
```

## 파일

### ai/

| 파일 | 크기(px) | 프레임 | 다운로드 주소 |
| --- | --- | --- | --- |
| `AI_character_bottomsheet.json` | 56 × 48 | 24fps, 0–56 | https://github.com/kmjdesign/11st-figma-json/releases/download/v1.0.0/AI_character_bottomsheet.json |
| `AI_collection_floating_arrow_motion.json` | 14 × 14 | 60fps, 0–120 | https://github.com/kmjdesign/11st-figma-json/releases/download/v1.0.0/AI_collection_floating_arrow_motion.json |
| `AI_icon_loading.json` | 250 × 200 | 60fps, 0–90 | https://github.com/kmjdesign/11st-figma-json/releases/download/v1.0.0/AI_icon_loading.json |
| `AI_keyword_loading_icon.json` | 250 × 200 | 60fps, 0–95 | https://github.com/kmjdesign/11st-figma-json/releases/download/v1.0.0/AI_keyword_loading_icon.json |

## 이름 규칙

### 폴더

- 서비스 영역 이름을 영문 소문자로 씁니다. 예: `ai`, `search`, `common`, `pdp`
- "어느 화면/영역에서 쓰나" 기준으로만 나눕니다. 모션 종류(loading, icon)로는 나누지 않습니다.

### 파일

형식: `접두어_대상_상태.json`

- **접두어**: 폴더 이름의 표기형. 약어는 대문자(`AI`), 일반 단어는 첫 글자만 대문자(`Search`, `Common`)
- **대상**: 무엇의 모션인지. 예: `icon`, `character`, `arrow`, `button`
- **상태/동작**: 어떤 상황인지. 예: `loading`, `bottomsheet`, `floating`, `tap`
- 접두어 뒤는 전부 소문자, 단어 사이는 밑줄(`_`)만 씁니다. 하이픈과 공백은 쓰지 않습니다.
- 단어 순서는 큰 것에서 작은 것으로: 영역 → 대상 → 상태
- 버전 번호(`_v2`, `_final`, `_patched`)나 날짜는 파일명에 넣지 않습니다. 버전은 릴리스가, 이력은 GitHub가 담당합니다.
- 크기·색상 변형이 동시에 필요하면 맨 뒤에 붙입니다. 예: `AI_icon_loading_small.json`, `AI_icon_loading_dark.json`

| 폴더 | 파일명 예시 | 읽는 법 |
| --- | --- | --- |
| `ai/` | `AI_icon_loading.json` | AI 영역, 아이콘, 로딩 중 |
| `search/` | `Search_icon_loading.json` | 검색 영역, 아이콘, 로딩 중 |
| `common/` | `Common_arrow_floating.json` | 공용, 화살표, 떠다니는 모션 |

### 한 번 배포한 파일명은 바꾸지 않습니다

릴리스 첨부 파일명이 곧 다운로드 주소이므로, 이름을 바꾸면 Figma 연결이 끊깁니다. 기존 파일은 규칙에 조금 맞지 않아도 그대로 두고, 규칙은 새 파일부터 적용합니다. 꼭 바꿔야 한다면 새 파일로 추가하고 Figma 쪽 주소를 바꾼 뒤 옛 파일을 지웁니다.

## 수정할 때

1. 저장소의 JSON 파일을 먼저 고치고 커밋합니다.
2. 릴리스 `v1.0.0`의 같은 이름 첨부 파일을 새 파일로 교체합니다. 파일명이 같으면 다운로드 주소가 바뀌지 않습니다.
3. 파일을 새로 추가할 때는 폴더에 올린 뒤 릴리스에도 첨부하고, 위 표에 한 줄 추가합니다. 새 폴더가 생기면 "파일" 아래에 섹션을 하나 추가합니다.
4. 릴리스 번호는 모든 다운로드 주소를 한꺼번에 바꿔야 하는 큰 개편이 있을 때만 올립니다.
