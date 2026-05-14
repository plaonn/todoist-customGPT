# todoist-customGPT

Todoist 제어를 위한 Custom GPT 설정의 정본 저장소.

## 목적

이 저장소는 ChatGPT의 Todoist Assistant 커스텀 GPT를 구성하는 지침, Knowledge 문서, Actions schema를 관리한다.

실제 Custom GPT 설정 화면의 현재 상태를 assistant가 직접 읽을 수 없으므로, 이 저장소의 파일을 현재 상태 판단의 기준으로 사용한다.

## 파일 구조

```text
contents/
├─ instruction.md
├─ knowledge_operating_manual.md
└─ actions_api_schema.yaml
```

## 파일 역할

- `contents/instruction.md`: Custom GPT Instructions에 붙여넣는 본문
- `contents/knowledge_operating_manual.md`: Custom GPT Knowledge로 업로드하는 운영 매뉴얼
- `contents/actions_api_schema.yaml`: Custom GPT Actions에 등록하는 OpenAPI schema

## 운영 원칙

- 지침 수정 요청이 있으면 먼저 이 저장소의 현재 파일을 읽고 현재 상태를 판단한다.
- 변경은 관련 파일에만 최소 범위로 반영한다.
- Git commit history를 변경 이력으로 사용한다.
- 별도 `CHANGELOG.md`나 deploy 문서는 두지 않는다.
- GitHub Releases는 필요할 때만 버전 단위 요약에 사용한다.

## 적용 방법

이 저장소의 변경 사항은 Custom GPT에 자동 반영되지 않는다.

변경 후 필요한 파일을 Custom GPT Builder에 수동 반영한다.

1. `contents/instruction.md`를 Instructions에 반영한다.
2. `contents/knowledge_operating_manual.md`를 Knowledge에 반영한다.
3. `contents/actions_api_schema.yaml`을 Actions schema에 반영한다.
