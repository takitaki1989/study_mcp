# CLAUDE.md

このファイルはClaude Codeがこのリポジトリで作業する際の参考情報です。

## リポジトリの目的

MCPサーバの学習用リポジトリ。Model Context Protocol (MCP) の公式クイックスタートをベースに、MCPサーバの実装を学ぶ。

## 現在の構成

### start/weather

- MCP公式クイックスタートのサンプルをそのまま収録したもの
- `FastMCP` を使ったシンプルなMCPサーバ実装
- 米国国家気象局（NWS）APIを使って天気情報を提供する
- トランスポートは `stdio`

#### 提供ツール
- `get_alerts(state: str)` — 州コードを受け取り気象警報を返す
- `get_forecast(latitude: float, longitude: float)` — 緯度経度を受け取り天気予報を返す

## 開発環境

- Python 3.10
- パッケージ管理: `uv`
- リンター: `ruff`

## コマンド

```bash
# 依存関係インストール
cd start/weather && uv sync

# サーバ起動
uv run weather

# リント
uv run ruff check .
```
