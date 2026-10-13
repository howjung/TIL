# gsd-help

사용 가능한 GSD 명령과 사용법 표시

- 분류 : GSD / 시작 / 길 안내
- 호출 : Claude Code에서 `/gsd-help` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-help [--brief | --full | <topic> | --brief <topic>]
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-help` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-next` : 프로젝트 상태를 보고 다음 할 일로 안내
- `gsd-progress` : 진행 확인, 다음 단계 진행, 자유 입력 처리 (상황 파악용 통합 명령)
- `gsd-stats` : phase, 요구사항, git 지표, 타임라인 통계
- `gsd-new-project` : 새 프로젝트 초기화 + PROJECT.md 작성
- `gsd-onboard` : 기존 코드베이스 온보딩 (매핑 → 문서 수집 → 계획 설정)

## 참고
- 전체 목록은 [README](../README.md) 참고
