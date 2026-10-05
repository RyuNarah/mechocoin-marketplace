# MechoCoin Marketplace

MechoCoin을 Claude Code에서 쓰기 위한 플러그인 마켓플레이스입니다.

## 플러그인

| 이름 | 하는 일 |
| --- | --- |
| `mechocoin` | MechoCoin 앱이 함께 설치하는 MCP 서버(`%LOCALAPPDATA%\MechoCoin\mecho-mcp.exe`)를 등록합니다. |

`mecho-mcp.exe`는 앱 설치 파일에 들어 있으므로, 먼저 MechoCoin 앱을 설치해야 합니다.

## 설치

```sh
/plugin marketplace add RyuNarah/mechocoin-marketplace
/plugin install mechocoin@mechocoin
```

설치한 뒤 Claude Code를 다시 시작하면 `mechocoin` MCP 서버가 붙습니다. 첫 호출은 `sign_in`입니다.
