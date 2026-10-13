# Claude 스킬 사용 설명서

`~/.claude/skills` 에 설치된 스킬 77개의 사용 설명서. 스킬 이름마다 폴더가 있다.

- 일반 스킬은 직접 작성한 설명서, GSD 스킬은 스킬 메타데이터(인자 힌트)를 바탕으로 정리한 설명서다

## 일반 스킬

| 스킬 | 설명 |
|---|---|
| [`agent-browser`](agent-browser/agent-browser.md) | 웹 브라우저 자동화 CLI |
| [`design-taste-frontend`](design-taste-frontend/design-taste-frontend.md) | 템플릿 티 나지 않는 프론트엔드 제작 |
| [`find-skills`](find-skills/find-skills.md) | 설치 가능한 스킬 찾기/설치 |
| [`mcp-builder`](mcp-builder/mcp-builder.md) | MCP 서버 제작 가이드 |
| [`ui-ux-pro-max`](ui-ux-pro-max/ui-ux-pro-max.md) | UI/UX 디자인 인텔리전스 (디자인 시스템, 리뷰, 컴포넌트) |

## GSD / Git / 배포

| 스킬 | 설명 |
|---|---|
| [`gsd-inbox`](gsd-inbox/gsd-inbox.md) | 열린 GitHub 이슈/PR을 템플릿/기여 가이드 기준으로 분류·검토 |
| [`gsd-pr-branch`](gsd-pr-branch/gsd-pr-branch.md) | `.planning/` 커밋을 뺀 깨끗한 PR 브랜치 생성 |
| [`gsd-ship`](gsd-ship/gsd-ship.md) | PR 생성, 리뷰 실행, 머지 준비 |
| [`gsd-undo`](gsd-undo/gsd-undo.md) | phase/plan 커밋을 의존성 확인 후 안전하게 되돌림 |

## GSD / 검증 / 리뷰 / 디버깅

| 스킬 | 설명 |
|---|---|
| [`gsd-add-tests`](gsd-add-tests/gsd-add-tests.md) | UAT 기준과 구현을 바탕으로 테스트 생성 |
| [`gsd-audit-fix`](gsd-audit-fix/gsd-audit-fix.md) | 문제 발견 → 분류 → 수정 → 테스트 → 커밋 자동 파이프라인 |
| [`gsd-audit-uat`](gsd-audit-uat/gsd-audit-uat.md) | 모든 phase의 미해결 UAT/검증 항목 교차 감사 |
| [`gsd-code-review`](gsd-code-review/gsd-code-review.md) | phase에서 바뀐 코드의 버그/보안/품질 리뷰 |
| [`gsd-debug`](gsd-debug/gsd-debug.md) | 컨텍스트가 초기화돼도 이어지는 체계적 디버깅 |
| [`gsd-eval-review`](gsd-eval-review/gsd-eval-review.md) | AI phase의 평가 커버리지 감사, EVAL-REVIEW.md 생성 |
| [`gsd-forensics`](gsd-forensics/gsd-forensics.md) | 실패한 GSD 워크플로 사후 분석 |
| [`gsd-secure-phase`](gsd-secure-phase/gsd-secure-phase.md) | 완료된 phase의 위협 대응이 코드에 있는지 소급 검증 |
| [`gsd-ui-review`](gsd-ui-review/gsd-ui-review.md) | 구현된 프론트엔드 6개 기준 시각 감사 |
| [`gsd-validate-phase`](gsd-validate-phase/gsd-validate-phase.md) | 검증(Nyquist) 빈틈을 소급 점검하고 채움 |
| [`gsd-verify-work`](gsd-verify-work/gsd-verify-work.md) | 만든 기능을 대화형 UAT로 검수 |

## GSD / 계획 단계

| 스킬 | 설명 |
|---|---|
| [`gsd-ai-integration-phase`](gsd-ai-integration-phase/gsd-ai-integration-phase.md) | AI 시스템 구축 phase용 AI-SPEC.md 설계 계약 생성 |
| [`gsd-discuss-phase`](gsd-discuss-phase/gsd-discuss-phase.md) | 계획 전에 적응형 질문으로 phase 맥락 수집 |
| [`gsd-mvp-phase`](gsd-mvp-phase/gsd-mvp-phase.md) | phase를 세로 MVP 조각(유저 스토리, SPIDR 분할)으로 계획 |
| [`gsd-plan-phase`](gsd-plan-phase/gsd-plan-phase.md) | 상세 PLAN.md 작성 + 검증 루프 |
| [`gsd-plan-review-convergence`](gsd-plan-review-convergence/gsd-plan-review-convergence.md) | 여러 AI 리뷰 우려가 해소될 때까지 재계획 |
| [`gsd-review`](gsd-review/gsd-review.md) | 외부 AI CLI에 계획 교차 리뷰 요청 |
| [`gsd-spec-phase`](gsd-spec-phase/gsd-spec-phase.md) | 모호함 점수화로 "무엇을 만들지" SPEC.md 확정 |
| [`gsd-ui-phase`](gsd-ui-phase/gsd-ui-phase.md) | 프론트엔드 phase용 UI 디자인 계약(UI-SPEC.md) 생성 |
| [`gsd-ultraplan-phase`](gsd-ultraplan-phase/gsd-ultraplan-phase.md) | [베타] 계획을 Claude Code ultraplan 클라우드에 맡기고 브라우저에서 검토 후 가져오기 |

## GSD / 네임스페이스 (묶음 진입점)

| 스킬 | 설명 |
|---|---|
| [`gsd-ns-context`](gsd-ns-context/gsd-ns-context.md) | 코드베이스 정보: map, graphify, docs, learnings, mempalace |
| [`gsd-ns-ideate`](gsd-ns-ideate/gsd-ns-ideate.md) | 아이디어 포착: explore, sketch, spike, spec, capture |
| [`gsd-ns-manage`](gsd-ns-manage/gsd-ns-manage.md) | 관리: config, workspace, workstreams, thread, update, ship, inbox |
| [`gsd-ns-project`](gsd-ns-project/gsd-ns-project.md) | 프로젝트 수명주기: 마일스톤, 감사, 요약 |
| [`gsd-ns-review`](gsd-ns-review/gsd-ns-review.md) | 품질 관문: code review, debug, audit, security, eval, ui |
| [`gsd-ns-workflow`](gsd-ns-workflow/gsd-ns-workflow.md) | 워크플로: discuss, plan, execute, verify, phase, progress |

## GSD / 설정 / 유지보수

| 스킬 | 설명 |
|---|---|
| [`gsd-config`](gsd-config/gsd-config.md) | 워크플로 토글, 고급 옵션, 연동, 모델 프로필 설정 |
| [`gsd-health`](gsd-health/gsd-health.md) | planning 디렉터리 상태 진단 및 복구 |
| [`gsd-settings`](gsd-settings/gsd-settings.md) | 워크플로 토글과 모델 프로필 설정 |
| [`gsd-surface`](gsd-surface/gsd-surface.md) | 노출할 스킬 프로필 적용/목록/클러스터 끄기 (재설치 없이) |
| [`gsd-update`](gsd-update/gsd-update.md) | GSD 최신 버전 업데이트 + 변경 내역 표시 |

## GSD / 세션 이어가기 / 작업 공간

| 스킬 | 설명 |
|---|---|
| [`gsd-pause-work`](gsd-pause-work/gsd-pause-work.md) | 작업 중단 시 컨텍스트 인수인계 문서 작성 |
| [`gsd-resume-work`](gsd-resume-work/gsd-resume-work.md) | 이전 세션 맥락을 복원해서 재개 |
| [`gsd-thread`](gsd-thread/gsd-thread.md) | 세션을 넘나드는 지속 컨텍스트 스레드 관리 |
| [`gsd-workspace`](gsd-workspace/gsd-workspace.md) | 격리된 작업공간 생성/목록/삭제 |
| [`gsd-workstreams`](gsd-workstreams/gsd-workstreams.md) | 병렬 작업 흐름 목록/생성/전환/상태/완료/재개 |

## GSD / 시작 / 길 안내

| 스킬 | 설명 |
|---|---|
| [`gsd-help`](gsd-help/gsd-help.md) | 사용 가능한 GSD 명령과 사용법 표시 |
| [`gsd-new-project`](gsd-new-project/gsd-new-project.md) | 새 프로젝트 초기화 + PROJECT.md 작성 |
| [`gsd-next`](gsd-next/gsd-next.md) | 프로젝트 상태를 보고 다음 할 일로 안내 |
| [`gsd-onboard`](gsd-onboard/gsd-onboard.md) | 기존 코드베이스 온보딩 (매핑 → 문서 수집 → 계획 설정) |
| [`gsd-progress`](gsd-progress/gsd-progress.md) | 진행 확인, 다음 단계 진행, 자유 입력 처리 (상황 파악용 통합 명령) |
| [`gsd-stats`](gsd-stats/gsd-stats.md) | phase, 요구사항, git 지표, 타임라인 통계 |

## GSD / 실행

| 스킬 | 설명 |
|---|---|
| [`gsd-autonomous`](gsd-autonomous/gsd-autonomous.md) | 남은 phase를 논의→계획→실행까지 자동 진행 |
| [`gsd-execute-phase`](gsd-execute-phase/gsd-execute-phase.md) | phase의 모든 plan을 의존성 기반 웨이브로 병렬 실행 |
| [`gsd-fast`](gsd-fast/gsd-fast.md) | 사소한 작업을 서브에이전트/계획 없이 즉시 처리 |
| [`gsd-quick`](gsd-quick/gsd-quick.md) | 원자적 커밋/상태 추적은 유지하며 작은 작업을 빠르게 실행 |
| [`gsd-quick-batch`](gsd-quick-batch/gsd-quick-batch.md) | quick 작업 여러 개를 묶어 계획/실행/병합 |

## GSD / 아이디어 / 탐색

| 스킬 | 설명 |
|---|---|
| [`gsd-capture`](gsd-capture/gsd-capture.md) | 아이디어/할 일/메모/씨앗을 알맞은 곳에 저장 |
| [`gsd-explore`](gsd-explore/gsd-explore.md) | 계획 확정 전 소크라테스식 아이디어 정리와 라우팅 |
| [`gsd-extract-learnings`](gsd-extract-learnings/gsd-extract-learnings.md) | 끝난 phase에서 결정/교훈/패턴/놀라운 점 추출 |
| [`gsd-sketch`](gsd-sketch/gsd-sketch.md) | 버리는 HTML 목업으로 UI 아이디어 스케치 |
| [`gsd-spike`](gsd-spike/gsd-spike.md) | 직접 실험으로 아이디어 검증 |

## GSD / 코드베이스 / 문서 / 기억

| 스킬 | 설명 |
|---|---|
| [`gsd-docs-update`](gsd-docs-update/gsd-docs-update.md) | 코드와 대조 검증하며 프로젝트 문서 생성/갱신 |
| [`gsd-graphify`](gsd-graphify/gsd-graphify.md) | `.planning/graphs/` 프로젝트 지식 그래프 생성/조회 |
| [`gsd-import`](gsd-import/gsd-import.md) | 외부 계획을 프로젝트 결정과 충돌 검사 후 가져옴 |
| [`gsd-ingest-docs`](gsd-ingest-docs/gsd-ingest-docs.md) | 기존 ADR/PRD/SPEC 문서로 `.planning/` 구성 또는 병합 |
| [`gsd-map-codebase`](gsd-map-codebase/gsd-map-codebase.md) | 병렬 매퍼로 `.planning/codebase/` 분석 문서 생성 |
| [`gsd-mempalace-capture`](gsd-mempalace-capture/gsd-mempalace-capture.md) | phase 산출물을 MemPalace에 저장, 결정 사실을 시간축 KG에 반영 |
| [`gsd-mempalace-recall`](gsd-mempalace-recall/gsd-mempalace-recall.md) | 계획 전에 MemPalace에서 결정/패턴/놀라운 점 회상 |
| [`gsd-profile-user`](gsd-profile-user/gsd-profile-user.md) | 개발자 행동 프로필 생성, Claude가 찾을 수 있는 산출물 작성 |

## GSD / 프로젝트 / 마일스톤 / phase 관리

| 스킬 | 설명 |
|---|---|
| [`gsd-audit-milestone`](gsd-audit-milestone/gsd-audit-milestone.md) | 보관 전에 원래 의도 대비 완료 여부 점검 |
| [`gsd-cleanup`](gsd-cleanup/gsd-cleanup.md) | 끝난 마일스톤의 phase 폴더 보관 처리 |
| [`gsd-complete-milestone`](gsd-complete-milestone/gsd-complete-milestone.md) | 완료된 마일스톤 보관, 다음 버전 준비 |
| [`gsd-manager`](gsd-manager/gsd-manager.md) | 여러 phase를 한 터미널에서 관리하는 지휘 화면 |
| [`gsd-milestone-summary`](gsd-milestone-summary/gsd-milestone-summary.md) | 마일스톤 산출물로 전체 요약 생성 (온보딩/리뷰용) |
| [`gsd-new-milestone`](gsd-new-milestone/gsd-new-milestone.md) | 새 마일스톤 시작, PROJECT.md 갱신 |
| [`gsd-phase`](gsd-phase/gsd-phase.md) | ROADMAP.md의 phase 추가/삽입/삭제/수정 |
| [`gsd-review-backlog`](gsd-review-backlog/gsd-review-backlog.md) | 백로그 항목 검토 후 활성 마일스톤으로 승격 |
