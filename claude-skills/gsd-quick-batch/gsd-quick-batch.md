# gsd-quick-batch

quick 작업 여러 개를 묶어 계획/실행/병합

- 분류 : GSD / 실행
- 호출 : Claude Code에서 `/gsd-quick-batch` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-quick-batch [--file <path>] [--jobs auto|N] [--validate] [--research] [--resume <batch-id>] [task list]
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-quick-batch` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-execute-phase` : phase의 모든 plan을 의존성 기반 웨이브로 병렬 실행
- `gsd-autonomous` : 남은 phase를 논의→계획→실행까지 자동 진행
- `gsd-quick` : 원자적 커밋/상태 추적은 유지하며 작은 작업을 빠르게 실행
- `gsd-fast` : 사소한 작업을 서브에이전트/계획 없이 즉시 처리

## 참고
- 전체 목록은 [README](../README.md) 참고
