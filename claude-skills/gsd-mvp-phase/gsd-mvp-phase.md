# gsd-mvp-phase

phase를 세로 MVP 조각(유저 스토리, SPIDR 분할)으로 계획

- 분류 : GSD / 계획 단계
- 호출 : Claude Code에서 `/gsd-mvp-phase` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-mvp-phase <phase-number>
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-mvp-phase` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-discuss-phase` : 계획 전에 적응형 질문으로 phase 맥락 수집
- `gsd-spec-phase` : 모호함 점수화로 "무엇을 만들지" SPEC.md 확정
- `gsd-plan-phase` : 상세 PLAN.md 작성 + 검증 루프
- `gsd-ui-phase` : 프론트엔드 phase용 UI 디자인 계약(UI-SPEC.md) 생성
- `gsd-ai-integration-phase` : AI 시스템 구축 phase용 AI-SPEC.md 설계 계약 생성
- `gsd-plan-review-convergence` : 여러 AI 리뷰 우려가 해소될 때까지 재계획
- `gsd-ultraplan-phase` : [베타] 계획을 Claude Code ultraplan 클라우드에 맡기고 브라우저에서 검토 후 가져오기
- `gsd-review` : 외부 AI CLI에 계획 교차 리뷰 요청

## 참고
- 전체 목록은 [README](../README.md) 참고
