# study_mcp

MCPサーバの学習用リポジトリです。

## 概要

[Model Context Protocol (MCP)](https://modelcontextprotocol.io/) の公式クイックスタートチュートリアルをベースにした学習用リポジトリです。

## ディレクトリ構成

```
study_mcp/
└── start/                        # MCP公式クイックスタートのサンプルコード
    └── weather/                  # 天気情報MCPサーバ（Python実装）
        ├── weather.py            # MCPサーバ本体
        ├── pyproject.toml        # プロジェクト設定・依存関係
        └── .python-version       # Python バージョン指定 (3.10)
```

## start/weather について

MCP の公式クイックスタートに従って実装されたシンプルな天気情報MCPサーバです。

### 使用技術

| 技術 | 詳細 |
|---|---|
| 言語 | Python 3.10+ |
| MCPフレームワーク | `FastMCP` (`mcp[cli]` >= 1.26.0) |
| HTTPクライアント | `httpx` >= 0.28.1 |
| パッケージ管理 | `uv` |
| トランスポート | stdio |
| データソース | [National Weather Service (NWS) API](https://api.weather.gov) |

### 提供ツール

#### `get_alerts`
米国の州コード（例: `CA`, `NY`）を受け取り、その州のアクティブな気象警報一覧を返します。

#### `get_forecast`
緯度・経度を受け取り、その地点の天気予報（直近5期間分）を返します。

### 実行方法

```bash
cd start/weather
uv run weather
```
