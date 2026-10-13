# mcp-builder

MCP 서버 제작 가이드

## 설명
LLM이 외부 서비스와 상호작용할 수 있게 하는 고품질 MCP(Model Context Protocol) 서버를 만드는 가이드. Python(FastMCP)과 Node/TypeScript(MCP SDK)를 다룬다.

## 언제 쓰나
- 외부 API나 서비스를 Claude에 연결하는 MCP 서버를 만들 때
- 기존 MCP 서버의 도구 설계를 개선할 때

## 호출 방법
- Claude Code에서 `/mcp-builder` 으로 직접 호출하거나, 관련 요청을 하면 자동으로 선택된다
- 요청에 스킬 이름을 넣으면 확실히 호출된다

## 요청 예시
- `mcp-builder로 날씨 API MCP 서버 만들어줘 (TypeScript)`
- `Notion용 MCP 서버를 FastMCP로 만들고 싶어`
