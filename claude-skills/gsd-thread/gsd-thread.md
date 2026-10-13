# gsd-thread

세션을 넘나드는 지속 컨텍스트 스레드 관리

- 분류 : GSD / 세션 이어가기 / 작업 공간
- 호출 : Claude Code에서 `/gsd-thread` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-thread [list [--open | --resolved] | close <slug> | status <slug> | name | description]
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-thread` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-pause-work` : 작업 중단 시 컨텍스트 인수인계 문서 작성
- `gsd-resume-work` : 이전 세션 맥락을 복원해서 재개
- `gsd-workspace` : 격리된 작업공간 생성/목록/삭제
- `gsd-workstreams` : 병렬 작업 흐름 목록/생성/전환/상태/완료/재개

## 참고
- 전체 목록은 [README](../README.md) 참고
