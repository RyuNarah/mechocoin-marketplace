# MechoCoin Marketplace

MechoCoin을 Claude Code에서 쓰기 위한 플러그인 마켓플레이스입니다.

## 플러그인

| 이름 | 하는 일 |
| --- | --- |
| `mechocoin` | MechoCoin 앱이 함께 설치하는 MCP 서버(`%LOCALAPPDATA%\MechoCoin\mecho-mcp.exe`)를 등록하고, `indicator-converter` 스킬을 더합니다. |

`mecho-mcp.exe`는 앱 설치 파일에 들어 있으므로, 먼저 MechoCoin 앱을 설치해야 합니다.

## 설치

```sh
/plugin marketplace add RyuNarah/mechocoin-marketplace
/plugin install mechocoin@mechocoin
```

설치한 뒤 `/reload-plugins`를 실행하거나 Claude Code를 다시 시작하면 `plugin:mechocoin:mechocoin` MCP 서버가 붙습니다. 첫 호출은 `sign_in`입니다.

## 스킬

- `indicator-converter` — TradingView Pine 스크립트를 MechoCoin의 내 지표로 옮깁니다. 전략 블록이 읽을 반환 값을 사용자와 함께 정하고, 모습 탭에 보일 것을 정하고, 지원하는 문법으로 이식한 뒤 `check_indicator`로 검사하고 `create_indicator`로 저장합니다. 스크립트를 주면서 "MechoCoin 지표로 넣어줘"라고 하면 됩니다.
