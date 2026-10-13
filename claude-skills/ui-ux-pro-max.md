# ui-ux-pro-max 스킬 사용 설명서

UI/UX 디자인 인텔리전스 스킬. 로컬 데이터(스타일 79개, 팔레트 192개, 폰트 조합 74개, UX 가이드라인 119개, 아이콘 105개, GSAP 프리셋 17개, 차트 25종, 스택 22종)를 검색해서 디자인 방향과 구현 가이드를 추천해 준다.

## 1. 언제 쓰나
- 새 페이지/프로젝트의 디자인 시스템 생성 (스타일, 색상, 폰트, 레이아웃)
- 기존 UI의 접근성/UX/일관성 리뷰
- 컴포넌트 구현 및 수정 (버튼, 폼, 내비게이션, 차트 등)
- 반응형, 애니메이션, 다크 모드 작업
- 백엔드, API, DB, 인프라처럼 화면과 무관한 작업에는 쓰지 않는다

## 2. 호출 방법
- Claude Code : `/ui-ux-pro-max` 입력, 또는 UI 작업을 요청하면 자동 적용
- Claude 앱 : Settings → Capabilities → Skills에서 zip 업로드 후 토글 ON, 요청에 스킬 이름을 넣으면 확실히 호출됨
- `/ui-ux-pro-max`만 입력하면 요청이 없어서 되묻기만 하므로, 요청 내용을 함께 적는다

## 3. 요청 예시
- `치과 예약 서비스 랜딩 페이지 디자인 시스템 만들어줘 (Next.js)`
- `~/projects/dashboard UI를 접근성 중심으로 리뷰해줘`
- `모바일 피트니스 앱 홈 화면, 다크 모드, 밀도 높게`
- 제품 종류, 스타일 키워드, 스택을 함께 적을수록 결과가 정확해진다

## 4. 내부 검색 모드 (`scripts/search.py`)
- `--design-system` : 새 페이지/프로젝트의 전체 디자인 방향
  - `python scripts/search.py "beauty spa wellness" --design-system -p "Serenity Spa"`
- `--domain <도메인>` : 개별 주제 검색 (product, style, color, typography, ux, chart, landing, icons, gsap 등)
  - `python scripts/search.py "error summary validation" --domain ux`
- `--stack <스택>` : 스택별 구현 가이드 (react, nextjs, vue, swiftui, flutter, html-tailwind 등)
  - `python scripts/search.py "chip badge overflow" --stack html-tailwind`

## 5. 옵션
- 디자인 다이얼 (1~10) : `--variance`(미니멀↔대담), `--motion`(은은↔복잡), `--density`(여백 넓음↔촘촘함)
- 디자인 시스템 저장 : `--persist --output-dir <프로젝트 루트>` → `design-system/<프로젝트>/MASTER.md` 생성
  - 페이지별 규칙은 `--page "dashboard"`로 `pages/` 폴더에 저장
  - 이미 `MASTER.md`가 있으면 덮어쓰지 않고, `--force`는 명시적으로 허락했을 때만 사용

## 6. 팁
- 새 프로젝트는 디자인 시스템 생성 → 컴포넌트 구현 순서로 진행
- 검색 결과가 이상하면 `color 도메인으로 다시 검색해줘`처럼 도메인을 지정
- Claude 앱에서는 코드 실행이 켜져 있어야 `search.py`가 돌아간다 (꺼져 있으면 `SKILL.md`와 `references/` 가이드만 사용)
- Claude 앱용 zip은 `SKILL.md`의 경로를 `scripts/search.py` 상대 경로로 바꿔야 하고, 스킬 폴더에서 실행해야 한다 (Claude Code용 원본은 `${CLAUDE_PLUGIN_ROOT}` 경로 사용)
