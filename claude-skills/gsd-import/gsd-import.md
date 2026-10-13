# gsd-import

외부 계획을 프로젝트 결정과 충돌 검사 후 가져옴

- 분류 : GSD / 코드베이스 / 문서 / 기억
- 호출 : Claude Code에서 `/gsd-import` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-import --from <filepath> | --from-gsd2
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-import` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-map-codebase` : 병렬 매퍼로 `.planning/codebase/` 분석 문서 생성
- `gsd-ingest-docs` : 기존 ADR/PRD/SPEC 문서로 `.planning/` 구성 또는 병합
- `gsd-docs-update` : 코드와 대조 검증하며 프로젝트 문서 생성/갱신
- `gsd-graphify` : `.planning/graphs/` 프로젝트 지식 그래프 생성/조회
- `gsd-mempalace-capture` : phase 산출물을 MemPalace에 저장, 결정 사실을 시간축 KG에 반영
- `gsd-mempalace-recall` : 계획 전에 MemPalace에서 결정/패턴/놀라운 점 회상
- `gsd-profile-user` : 개발자 행동 프로필 생성, Claude가 찾을 수 있는 산출물 작성

## 참고
- 전체 목록은 [README](../README.md) 참고
