# gsd-inbox

열린 GitHub 이슈/PR을 템플릿/기여 가이드 기준으로 분류·검토

- 분류 : GSD / Git / 배포
- 호출 : Claude Code에서 `/gsd-inbox` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-inbox [--issues] [--prs] [--label] [--close-incomplete] [--repo owner/repo]
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-inbox` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-ship` : PR 생성, 리뷰 실행, 머지 준비
- `gsd-pr-branch` : `.planning/` 커밋을 뺀 깨끗한 PR 브랜치 생성
- `gsd-undo` : phase/plan 커밋을 의존성 확인 후 안전하게 되돌림

## 참고
- 전체 목록은 [README](../README.md) 참고
