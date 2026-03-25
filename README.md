# ColabCraw

Google Colab에서 OpenClaw를 실험적으로 사용하고, Gmail 기반 메일 요약/답장 초안 워크플로를 검증하기 위한 저장소입니다.

## 무엇을 하려는 저장소인가?

ColabCraw는 두 가지 방향을 다룹니다.

1. **Google Colab에서 OpenClaw를 테스트하기**
2. **Gmail 메일을 읽고 답장 초안을 자동으로 만드는 흐름 실험하기**

핵심 목표는 다음과 같습니다.

- Colab 환경에서 OpenClaw 설치 및 실행 가능성 확인
- Gmail 메일 요약 자동화
- 답장 초안 자동 생성
- 실제 발송은 하지 않고, 우선은 사람이 검토할 수 있는 형태로 저장

## 왜 이걸 하나?

OpenClaw는 보통 로컬 머신이나 서버 환경에서 더 자연스럽게 운영되지만,
Colab은 빠른 실험, 개념 검증, 데모 제작에 꽤 유용합니다.

또한 메일 처리 측면에서는 다음 흐름이 유용합니다.

- 새 메일 읽기
- 중요한 메일만 추리기
- 짧게 요약하기
- 답장 초안 만들기
- 실제 발송은 사람 확인 후 진행하기

즉, 단순한 메일 자동발송이 아니라
**"읽기 → 요약 → 초안 생성 → 사람 검토"** 흐름을 만드는 것이 목적입니다.

## 현재 정리된 방향

### Gmail 워크플로
- Gmail 메일 읽기
- 안 읽은 메일 요약
- 메일별 답장 초안 생성
- 필요하면 Gmail Draft로 임시 저장
- 실제 발송은 자동으로 하지 않음

### GitHub 활용 아이디어
이전에는 메일 1개당 이슈 1개를 만들고,
이슈 댓글에 답장 초안을 남기는 흐름도 검토했습니다.

관련 문서는 아래에 남겨두었습니다.
- `docs/email-issue-workflow.md`
- `.github/ISSUE_TEMPLATE/email_from_gmail.md`
- `.github/labels-plan.md`
- `.github/comment-templates.md`

다만 현재는 더 단순하게,
**GitHub보다 Gmail Draft 중심 흐름**이 더 적합한 방향으로 보고 있습니다.

## 포함된 파일

- `docs/email-issue-workflow.md` : Gmail → GitHub Issue → 답장 초안 워크플로 문서
- `.github/ISSUE_TEMPLATE/email_from_gmail.md` : 메일 이슈 템플릿
- `.github/labels-plan.md` : 라벨 설계안
- `.github/comment-templates.md` : 코멘트 템플릿

## 추천 운영 원칙

- 자동은 **초안 생성까지**
- 실제 발송은 **반드시 사람 승인 후**
- 광고성 메일은 기본적으로 초안 생성 생략 가능
- 민감한 메일은 더 보수적으로 처리

## 앞으로 붙일 수 있는 것

- Colab notebook 예제
- Gmail Draft 자동 생성 스크립트
- 메일 중요도 분류 규칙
- 업무 메일 전용 답장 템플릿
- 실제 발송 전 검토 워크플로

## 관련 링크

- OpenClaw: https://github.com/openclaw/openclaw
- Docs: https://docs.openclaw.ai
