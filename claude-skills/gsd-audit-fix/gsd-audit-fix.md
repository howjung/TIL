# gsd-audit-fix

문제 발견 → 분류 → 수정 → 테스트 → 커밋 자동 파이프라인

- 분류 : GSD / 검증 / 리뷰 / 디버깅
- 호출 : Claude Code에서 `/gsd-audit-fix` (GSD 설치기로 설치된 스킬)

## 사용법
```
/gsd-audit-fix --source <audit-uat> [--severity <medium|high|all>] [--max N] [--dry-run]
```
- 대괄호 `[ ]` 는 생략 가능한 인자, `<>` 는 필수 값, `|` 는 택일이다
- 인자 없이 `/gsd-audit-fix` 만 입력해도 실행되며, 필요한 값은 Claude가 되묻는다

## 같은 분류의 스킬
- `gsd-verify-work` : 만든 기능을 대화형 UAT로 검수
- `gsd-code-review` : phase에서 바뀐 코드의 버그/보안/품질 리뷰
- `gsd-debug` : 컨텍스트가 초기화돼도 이어지는 체계적 디버깅
- `gsd-add-tests` : UAT 기준과 구현을 바탕으로 테스트 생성
- `gsd-validate-phase` : 검증(Nyquist) 빈틈을 소급 점검하고 채움
- `gsd-secure-phase` : 완료된 phase의 위협 대응이 코드에 있는지 소급 검증
- `gsd-ui-review` : 구현된 프론트엔드 6개 기준 시각 감사
- `gsd-eval-review` : AI phase의 평가 커버리지 감사, EVAL-REVIEW.md 생성
- `gsd-audit-uat` : 모든 phase의 미해결 UAT/검증 항목 교차 감사
- `gsd-forensics` : 실패한 GSD 워크플로 사후 분석

## 참고
- 전체 목록은 [README](../README.md) 참고
