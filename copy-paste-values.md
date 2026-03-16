# Kiro ワークショップ コピペ値一覧

ハンズオン中にコピー＆ペーストで使用する値をまとめています。

---

## Kiro体験：Kiro でアプリケーションの変換(既存アプリケーションの構築)

### Step3.アプリケーション起動(p.29)
```bash
mvn jetty:run
```
### Step4.アプリケーションにアクセスしてみる(p.30)
```
http://localhost:8081/demo-struts1/login.do
```

| 項目 | 値 |
|------|-----|
| ユーザー名 | `demo_test1` |
| パスワード | `mypassword` |

---
## Kiro体験：Kiro でアプリケーションの変換(Vibeチャットで既存アプリケーション解析)

### Step2.解析をVibeで実施(p.38)
>以下のプロンプトをVibeチャットに入力
```
既存のStruts1アプリケーションの分析を行い、要件定義書と設計書作成を行いたいです。

Struts1 で書かれたコードは全て demo_struts1 ディレクトリの中にあります。
分析結果を構造化された要件定義書「struts_app_requirements.md」と 設計書「struts_app_design.md」として作成してください。
```
### Step4.解析結果に対して、より詳細化（1/2）(p.40)
>以下のプロンプトをVibeチャットに入力
```
分析結果から作成された設計書要件定義書「struts_app_requirements.md」。以下の点について詳細化してください：

1. セキュリティ実装の現状
```

### Step4.解析結果に対して、より詳細化（2/2）(p.41)
>以下のプロンプトをVibeチャットに入力
```
分析結果から作成された設計書要件定義書「struts_app_requirements.md」。
非機能要件は簡素化してください。
```

---
## Kiro体験：Kiro でアプリケーションの変換(Specチャットで新規アプリケーション構築)

### Step2.Specモードで仕様駆動開発(p.50)
>以下のプロンプトをVibeチャットに入力
```
あなたの役割: あなたは熟練したプロダクトマネージャーです。

既存のStruts1アプリケーションをSpring Boot CRUDへ移行したいです。

既存のStruts1アプリケーションの要件定義書は「struts_app_requirements.md」、設計書は「struts_app_design.md」です。

簡略化して、各文書を作成してください

Spring boot で置き換えたコードは完全に別のディレクトリ 「demo-spring-boot」というものを作ってそこに全てのコードを配置してください。

/.kiro/specではなく、.kiro/specを確認してください
```

---
## 自由時間

### 例1：MCPを設定
> mcp.jsonファイルを置換

```json
{
  "mcpServers": {
    "fetch": {
      "command": "uvx",
      "args": ["mcp-server-fetch"],
      "env": {},
      "disabled": true,
      "autoApprove": []
    },
    "awslabs.aws-documentation-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.aws-documentation-mcp-server@latest"],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR",
        "AWS_DOCUMENTATION_PARTITION": "aws",
        "MCP_USER_AGENT": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36"
      },
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

> Vibeチャットへのプロンプト例
```
Auroraのアップグレードを教えて
```
```
AWSの可用性について教えて
```
```
コンテナ使いたいんだけど、リファレンスアーキテクチャあるか
```
---

### 例2：Kiro Powerを設定
> Vibeチャットへのプロンプト例
```
Auroraの性能が出ない
```
```
Auroraのバージョンアップの手段教えて、止めたくないです
```
```
AuroraのSLAを99.9%にできるか
```
---

### 例3：AWS CLIを設定
> Vibeチャットへのプロンプト例
```
cliを利用してアカウント内の今月の想定料金教えて。また、削減できる料金はあるか
```
