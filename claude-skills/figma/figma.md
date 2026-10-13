# figma

Figma 디자인을 코드로 옮기는 MCP 워크플로

## 설명
Figma MCP 서버로 디자인 컨텍스트, 스크린샷, 변수, 에셋을 가져와서 Figma 노드를 실제 프로젝트 코드로 변환하는 규칙을 정의한 스킬. OpenAI의 `openai/skills` 저장소에서 설치했다 (`npx skills add openai/skills --skill figma`).

## 언제 쓰나
- Figma URL이나 노드 ID가 포함된 구현 요청을 할 때
- 디자인을 코드로 옮기는 작업(design-to-code)을 할 때
- Figma MCP 설정이나 문제 해결이 필요할 때

## 필수 진행 순서 (건너뛰지 않기)
1. `get_design_context`로 해당 노드의 구조화된 정보를 먼저 가져온다
2. 응답이 너무 크거나 잘리면 `get_metadata`로 노드 지도를 보고, 필요한 노드만 `get_design_context`로 다시 가져온다
3. `get_screenshot`으로 구현할 변형(variant)의 시각 자료를 가져온다
4. 1~3을 모두 마친 뒤에만 필요한 에셋을 내려받고 구현을 시작한다
5. 결과물(보통 React + Tailwind)을 프로젝트의 규칙, 스타일, 프레임워크에 맞게 바꾼다 (색상 토큰, 컴포넌트, 타이포그래피 재사용)
6. 완료 전에 Figma와 1:1로 모양과 동작을 대조해 검증한다

## 구현 규칙
- Figma MCP가 주는 React + Tailwind는 디자인과 동작의 "표현"일 뿐 최종 코드 스타일이 아니다
- Tailwind 클래스는 가능하면 프로젝트의 유틸리티와 디자인 시스템 토큰으로 교체한다
- 버튼, 입력창, 아이콘 래퍼 같은 기존 컴포넌트를 중복 구현하지 않고 재사용한다
- 프로젝트의 색상 체계, 타이포 스케일, 간격 토큰을 일관되게 쓴다
- 저장소에 이미 있는 라우팅, 상태 관리, 데이터 패칭 패턴을 따른다
- 시각적으로 1:1 일치를 목표로 하되, 충돌하면 디자인 시스템 토큰을 우선하고 간격과 크기는 최소한만 조정한다

## 에셋 처리
- Figma MCP 서버의 assets 엔드포인트가 이미지와 SVG를 제공한다
- localhost 소스가 오면 그 이미지/SVG 소스를 그대로 쓴다
- 새 아이콘 패키지를 추가하지 않는다. 에셋은 모두 Figma 응답에 들어 있다
- localhost 소스가 제공되면 플레이스홀더를 쓰거나 만들지 않는다

## 링크 기반 요청
- 이 서버는 링크 기반이다. Figma 프레임/레이어 링크를 복사해서 클라이언트에 전달한다
- 클라이언트는 URL을 직접 열지 못하고 링크에서 노드 ID만 추출한다. 원하는 노드/변형을 정확히 가리키는 링크를 줘야 한다

## 참고 파일 (스킬 폴더 안)
- `references/figma-mcp-config.md`: 설정, 검증, 문제 해결, 링크 기반 사용 요령
- `references/figma-tools-and-prompts.md`: 도구 목록과 프레임워크/컴포넌트 선택, 메타데이터 조회용 프롬프트 패턴

## 호출 방법
- Claude Code에서 `/figma` 으로 직접 호출하거나, 관련 요청을 하면 자동으로 선택된다
- 요청에 스킬 이름을 넣으면 확실히 호출된다

## 요청 예시
- `figma 스킬로 이 프레임 구현해줘 https://www.figma.com/design/...?node-id=1-2`
- `Figma MCP 연결이 안 되는데 설정 확인해줘`

## 참고
- Figma 플러그인(`figma:figma-design-to-code` 등)에도 비슷한 스킬이 있어 기능이 겹친다
- 출처: https://github.com/openai/skills (Codex용 스킬 모음)
