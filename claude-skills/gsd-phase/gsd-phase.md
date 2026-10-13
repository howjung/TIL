# gsd-phase

ROADMAP.md의 phase 추가/삽입/삭제/수정

- 분류 : GSD / 프로젝트 / 마일스톤 / phase 관리
- 호출 : Claude Code에서 `/gsd-phase` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-phase [--insert | --remove | --edit] <phase-name-or-number>
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-phase` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-new-milestone` : 새 마일스톤 시작, PROJECT.md 갱신
- `gsd-complete-milestone` : 완료된 마일스톤 보관, 다음 버전 준비
- `gsd-audit-milestone` : 보관 전에 원래 의도 대비 완료 여부 점검
- `gsd-milestone-summary` : 마일스톤 산출물로 전체 요약 생성 (온보딩/리뷰용)
- `gsd-review-backlog` : 백로그 항목 검토 후 활성 마일스톤으로 승격
- `gsd-manager` : 여러 phase를 한 터미널에서 관리하는 지휘 화면
- `gsd-cleanup` : 끝난 마일스톤의 phase 폴더 보관 처리

## 참고
- 전체 목록은 [README](../README.md) 참고
