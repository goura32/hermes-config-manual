# 環境変数 → 設定項目 マッピング

Hermes Agentの全138環境変数とconfig.yamlの各設定項目との対応関係。

> **最終更新**: 2026-05-25

---

## 1. 設定値（環境変数で直接上書き）

エージェント・表示の核心パラメータ。

| 環境変数名 | config.yamlキー | 型 | デフォルト値 | 説明 | 備考 |
|-----------|----------------|----|-------------|------|------|
| `HERMES_MAX_ITERATIONS` | `agent.max_iterations` | int | `90` | 1対1の対話における最大ツール呼び出し繰り返し回数 | 子エージェントの`agent.max_iterations`には影響しない |
| `HERMES_PREFILL_MESSAGES_FILE` | `agent.prefill_messages_file` | str | `-` | ファイルパス。few-shotプリマイング用のJSON | デフォルト: 空白文字列 |
| `HERMES_EPHEMERAL_SYSTEM_PROMPT` | `agent.ephemeral_system_prompt` | str | `-` | システムプロンプト。API呼び出し時に動的注入 | セッションに保存されない |
| `HERMES_TOOL_PROGRESS` | `display.tool_progress` | str | `-` | ツール進捗表示モード | **(非推奨)** display.tool_progressの使用を推奨 |
| `HERMES_TOOL_PROGRESS_MODE` | `display.tool_progress.mode` | str | `-` | ツール進捗モード | **(非推奨)** display.tool_progress.modeの使用を推奨 |

---

## 2. モデルプロバイダー（APIキー / エンドポイント）

各プロバイダーの認証情報とベースURL上書き。

| 環境変数名 | config.yamlキー | 型 | 説明 | URL |
|-----------|----------------|----|------|-----|
| `OLLAMA_API_KEY` | `model.api_key` | str | Ollama CloudのAPIキー | https://ollama.com/settings |
| `OLLAMA_BASE_URL` | `model.base_url` | str | Ollama CloudのベースURL | - |
| `OPENROUTER_API_KEY` | `providers._DEFAULT_.api_key` | str | OpenRouterのAPIキー | https://openrouter.ai/keys |
| `HF_TOKEN` | `providers._DEFAULT_.hf_token` | str | Hugging Faceトークン | https://huggingface.co/settings/tokens |
| `GOOGLE_API_KEY` | `providers.google.api_key` | str | Google AI Studio APIキー | https://aistudio.google.com/app/apikey |
| `ANTHROPIC_API_KEY` | `providers.anthropic.api_key` | str | Anthropic APIキー | - |
| `ANTHROPIC_BASE_URL` | `providers.anthropic.base_url` | str | Anthropic APIのカスタムエンドポイント | - |
| `ANTHROPIC_TOKEN` | `providers.anthropic.token` | str | Anthropicの旧形式トークン | ANTHROPIC_API_KEYと同じ用途 |
| `XAI_API_KEY` | `providers.xai.api_key` | str | xAI APIキー | https://console.x.ai/ |
| `XAI_BASE_URL` | `providers.xai.base_url` | str | xAI APIのカスタムエンドポイント | - |
| `MINIMAX_API_KEY` | `providers.minimax.api_key` | str | MiniMax APIキー（国際） | https://www.minimax.io/ |
| `MINIMAX_BASE_URL` | `providers.minimax.base_url` | str | MiniMax APIのカスタムエンドポイント | - |
| `MINIMAX_CN_API_KEY` | `providers.minimax.api_key_cn` | str | MiniMax APIキー（中国） | https://www.minimax.com/ |
| `MINIMAX_CN_BASE_URL` | `providers.minimax.base_url_cn` | str | MiniMax APIの中国エンドポイント | - |
| `KIMI_API_KEY` | `providers.kimi.api_key` | str | Kimi APIキー | https://platform.moonshot.cn/ |
| `KIMI_BASE_URL` | `providers.kimi.base_url` | str | Kimi APIのカスタムエンドポイント | - |
| `KIMI_CN_API_KEY` | `providers.kimi.api_key_cn` | str | Kimi APIキー（中国） | https://platform.moonshot.cn/ |
| `DEEPSEEK_API_KEY` | `providers.deepseek.api_key` | str | DeepSeek APIキー | https://platform.deepseek.com/api_keys |
| `DEEPSEEK_BASE_URL` | `providers.deepseek.base_url` | str | DeepSeek APIのカスタムエンドポイント | - |
| `GLM_API_KEY` | `providers.glm.api_key` | str | GLM/Z.AI APIキー | https://z.ai/ |
| `GLM_BASE_URL` | `providers.glm.base_url` | str | GLM APIのカスタムエンドポイント | - |
| `ZAI_API_KEY` | `providers.zai.api_key` | str | Z.AI APIキー（GLMの別名） | https://z.ai/ |
| `Z_AI_API_KEY` | `providers.zai.api_key` | str | Z.AI APIキー（GLMの別名） | https://z.ai/ |
| `DASHSCOPE_API_KEY` | `providers.dashscope.api_key` | str | DashScope APIキー（Alibaba） | https://modelstudio.console.alibabacloud |
| `DASHSCOPE_BASE_URL` | `providers.dashscope.base_url` | str | DashScope APIのカスタムエンドポイント | - |
| `NVIDIA_API_KEY` | `providers.nvidia.api_key` | str | NVIDIA NIM APIキー | https://build.nvidia.com/ |
| `NVIDIA_BASE_URL` | `providers.nvidia.base_url` | str | NVIDIA NIM APIのカスタムエンドポイント | - |
| `GEMINI_API_KEY` | `providers.gemini.api_key` | str | Gemini APIキー | https://aistudio.google.com/app/apikey |
| `GEMINI_BASE_URL` | `providers.gemini.base_url` | str | Gemini APIのカスタムエンドポイント | - |
| `XIAOMI_API_KEY` | `providers.xiaomi.api_key` | str | Xiaomi MiMo APIキー | https://platform.xiaomimimo.com |
| `XIAOMI_BASE_URL` | `providers.xiaomi.base_url` | str | Xiaomi MiMo APIのカスタムエンドポイント | - |
| `GMI_API_KEY` | `providers.gmi.api_key` | str | GMI Cloud APIキー | https://www.gmicloud.ai/ |
| `GMI_BASE_URL` | `providers.gmi.base_url` | str | GMI Cloud APIのカスタムエンドポイント | - |
| `ARCEEAI_API_KEY` | `providers.arcee.api_key` | str | Arcee AI APIキー | https://chat.arcee.ai/ |
| `ARCEE_BASE_URL` | `providers.arcee.base_url` | str | Arcee AI APIのカスタムエンドポイント | - |
| `AZURE_FOUNDRY_API_KEY` | `providers.azure.api_key` | str | Azure Foundry APIキー | https://ai.azure.com/ |
| `AZURE_FOUNDRY_BASE_URL` | `providers.azure.api_base` | str | Azure Foundry APIベースURL | https://ai.azure.com/ |

---

## 3. メッセージングプラットフォーム

各プラットフォームの認証、アクセス制御、接続先設定。

### Telegram / Discord / Slack

| 環境変数名 | config.yamlキー | 型 | 説明 | URL |
|-----------|----------------|----|------|-----|
| `TELEGRAM_BOT_TOKEN` | `telegram.bot_token` | str | Telegramボットトークン | https://t.me/BotFather |
| `TELEGRAM_ALLOWED_USERS` | `telegram.allowed_users` | str | 許可TelegramユーザーID（カンマ区切り） | https://t.me/userinfobot |
| `TELEGRAM_PROXY` | `telegram.proxy_url` | str | Telegram接続プロキシURL | - |
| `DISCORD_BOT_TOKEN` | `discord.bot_token` | str | Discordボットトークン | https://discord.com/developers/applications |
| `DISCORD_ALLOWED_USERS` | `discord.allowed_users` | str | 許可DiscordユーザーID（カンマ区切り） | - |
| `SLACK_BOT_TOKEN` | `slack.bot_token` | str | Slackボットトークン | https://api.slack.com/apps |
| `SLACK_APP_TOKEN` | `slack.app_token` | str | Slackアプリトークン | https://api.slack.com/apps |

### Gateway / Webhook

| 環境変数名 | config.yamlキー | 型 | 説明 | 備考 |
|-----------|----------------|----|------|------|
| `GATEWAY_PROXY_URL` | `gateway.proxy_url` | str | リモートHermes APIサーバーのプロキシURL | - |
| `GATEWAY_PROXY_KEY` | `gateway.proxy_key` | str | プロキシ認証のベアラートークン | - |
| `GATEWAY_ALLOW_ALL_USERS` | `gateway.allow_all_users` | bool | 全ユーザーのボットアクセスを許可 | デフォルト: true |
| `WEBHOOK_ENABLED` | `webhook.enabled` | bool | Webhookの有効化 | デフォルト: false |
| `WEBHOOK_PORT` | `webhook.port` | int | Webhook HTTPサーバーポート | デフォルト: 8644 |
| `WEBHOOK_SECRET` | `webhook.secret` | str | WebhookのHMAC秘密鍵 | - |

### IRC / Matrix / Mattermost

| 環境変数名 | config.yamlキー | 型 | 説明 | URL |
|-----------|----------------|----|------|-----|
| `IRC_SERVER` | `irc.server` | str | IRCサーバーホスト名 | 例: irc.libera.chat |
| `IRC_CHANNEL` | `irc.channel` | str | IRCチャンネル名 | 例: #hermes |
| `IRC_NICKNAME` | `irc.nickname` | str | IRCニックネーム | デフォルト: hermes-bot |
| `IRC_NICKSERV_PASSWORD` | `irc.nickserv_password` | str | NickServ認証パスワード | - |
| `IRC_SERVER_PASSWORD` | `irc.server_password` | str | IRCサーバーパスワード | - |
| `MATRIX_HOMESERVER` | `matrix.homeserver` | str | MatrixホームサーバーURL | https://matrix.org/ecosystem/servers/ |
| `MATRIX_USER_ID` | `matrix.user_id` | str | MatrixユーザーID | - |
| `MATRIX_ACCESS_TOKEN` | `matrix.access_token` | str | Matrixアクセストークン | - |
| `MATRIX_RECOVERY_KEY` | `matrix.recovery_key` | str | Matrixリカバリーキー | - |
| `MATRIX_DEVICE_ID` | `matrix.device_id` | str | 安定したMatrixデバイスID | - |
| `MATRIX_ALLOWED_USERS` | `matrix.allowed_users` | str | 許可MatrixユーザーID（カンマ区切り） | - |
| `MATRIX_FREE_RESPONSE_ROOMS` | `matrix.free_response_rooms` | str | 自由応答するMatrixルーム | - |
| `MATRIX_DM_AUTO_THREAD` | `matrix.dm_auto_thread` | bool | DMで自動スレッド作成 | デフォルト: true |
| `MATRIX_AUTO_THREAD` | `matrix.auto_thread` | bool |入室で自動スレッド作成 | デフォルト: true |
| `MATRIX_REQUIRE_MENTION` | `matrix.require_mention` | bool | Matrixでのメンション必須 | デフォルト: true |
| `MATTERMOST_URL` | `mattermost.url` | str | MattermostサーバーURL | https://mattermost.com/deploy/ |
| `MATTERMOST_TOKEN` | `mattermost.token` | str | Mattermostボット/パーソナルアクセストークン | - |
| `MATTERMOST_FREE_RESPONSE_CHANNELS` | `mattermost.free_response_channels` | str | 自由応答するMattermostチャンネル | - |
| `MATTERMOST_ALLOWED_USERS` | `mattermost.allowed_users` | str | 許可MattermostユーザーID（カンマ区切り） | - |
| `MATTERMOST_REQUIRE_MENTION` | `mattermost.require_mention` | bool | Mattermostでのメンション必須 | デフォルト: true |

### BlueBubbles / QQ

| 環境変数名 | config.yamlキー | 型 | 説明 | URL |
|-----------|----------------|----|------|-----|
| `BLUEBUBBLES_SERVER_URL` | `bluebubbles.server_url` | str | BlueBubblesサーバーURL | https://bluebubbles.app/ |
| `BLUEBUBBLES_PASSWORD` | `bluebubbles.password` | str | BlueBubblesサーバーパスワード | - |
| `BLUEBUBBLES_ALLOWED_USERS` | `bluebubbles.allowed_users` | str | 許可BlueBubblesユーザーIDリスト | - |
| `BLUEBUBBLES_ALLOW_ALL_USERS` | `bluebubbles.allow_all_users` | bool | 全ユーザー許可 | デフォルト: false |
| `QQ_APP_ID` | `qq.app_id` | str | QQボットApp ID | https://q.qq.com |
| `QQ_CLIENT_SECRET` | `qq.client_secret` | str | QQボットClient Secret | - |
| `QQ_SANDBOX` | `qq.sandbox` | bool | QQサンボックスモード（開発用） | デフォルト: false |
| `QQ_ALLOWED_USERS` | `qq.allowed_users` | str | 許可QQユーザーID（カンマ区切り） | - |
| `QQ_ALLOW_ALL_USERS` | `qq.allow_all_users` | bool | 全QQユーザー許可 | デフォルト: false |
| `QQ_GROUP_ALLOWED_USERS` | `qq.group_allowed_users` | str | 許可QQグループID（カンマ区切り） | - |
| `QQBOT_HOME_CHANNEL` | `qq.home_channel` | str | QQボットのデフォルトチャネル | - |
| `QQBOT_HOME_CHANNEL_NAME` | `qq.home_channel_name` | str | QQボットのホームチャネル表示名 | - |

---

## 4. ツール固有の設定

検索、ブラウザ、音声、スキル固有の設定。

### 検索ツール

| 環境変数名 | config.yamlキー | 型 | 説明 | URL |
|-----------|----------------|----|------|-----|
| `BRAVE_SEARCH_API_KEY` | `web_search.brave.api_key` | str | Brave Search APIキー | https://brave.com/search/api/ |
| `SEARXNG_URL` | `web_search.searxng_url` | str | 自前SearXNGインスタンスURL | https://searxng.github.io/searxng/ |
| `FIRECRAWL_API_KEY` | `web_search.firecrawl.api_key` | str | Firecrawl APIキー | https://firecrawl.dev/ |
| `FIRECRAWL_API_URL` | `web_search.firecrawl.api_url` | str | FirecrawlカスタムAPI URL | - |
| `FIRECRAWL_BROWSER_TTL` | `web_search.firecrawl_browser_ttl` | int | FirecrawlセッションTTL（秒） | - |
| `FIRECRAWL_GATEWAY_URL` | `web_search.firecrawl_gateway_url` | str | FirecrawlゲートウェイURL | - |
| `PARALLEL_API_KEY` | `web_search.parallel.api_key` | str | Parallel APIキー | https://parallel.ai/ |
| `TAVILY_API_KEY` | `web_search.tavily.api_key` | str | Tavily APIキー | https://app.tavily.com/home |
| `EXA_API_KEY` | `web_search.exa.api_key` | str | Exa APIキー | https://exa.ai/ |

### ブラウザ

| 環境変数名 | config.yamlキー | 型 | 説明 | URL |
|-----------|----------------|----|------|-----|
| `AGENT_BROWSER_ENGINE` | `agent.browser_engine` | str | ブラウザエンジン (auto/chrome/firefox) | https://github.com/vercel-labs/agent-browser-engine |
| `BROWSERBASE_API_KEY` | `browser.browserbase.api_key` | str | Browserbase APIキー | https://browserbase.com/ |
| `BROWSERBASE_PROJECT_ID` | `browser.browserbase.project_id` | str | BrowserbaseプロジェクトID | https://browserbase.com/ |
| `BROWSER_USE_API_KEY` | `browser.browseruse.api_key` | str | Browser Use APIキー | https://browser-use.com/ |
| `CAMOFOX_URL` | `browser.camofox_url` | str | CamofoxブラウザサーバーURL | https://github.com/jo-inc/camofox-browser |

### スキル・ツール

| 環境変数名 | config.yamlキー | 型 | 説明 | URL |
|-----------|----------------|----|------|-----|
| `ELEVENLABS_API_KEY` | `tts.elevenlabs_api_key` | str | ElevenLabs APIキー | https://elevenlabs.io/ |
| `VOICE_TOOLS_OPENAI_KEY` | `stt.openai_key` | str | OpenAI APIキー（音声学習用） | https://platform.openai.com/api-keys |
| `MISTRAL_API_KEY` | `stt.mistral_api_key` | str | Mistral APIキー | https://console.mistral.ai/ |
| `OPENCODE_GO_API_KEY` | `opencode.go_api_key` | str | OpenCode Go APIキー | https://opencode.ai/auth |
| `OPENCODE_ZEN_API_KEY` | `opencode.zen_api_key` | str | OpenCode Zen APIキー | https://opencode.ai/auth |
| `FAL_KEY` | `image_gen.fal_api_key` | str | FAL APIキー | https://fal.ai/ |
| `HUGGINGFACE_TOKEN` | `huggingface.token` | str | Hugging Faceトークン | https://huggingface.co/settings/tokens |
| `GITHUB_TOKEN` | `github.token` | str | GitHubトークン | https://github.com/settings/tokens |
| `AIRTABLE_API_KEY` | `airtable.api_key` | str | Airtableパーソナルアクセストークン | https://airtable.com/create/tokens |
| `LINEAR_API_KEY` | `linear.api_key` | str | Linear APIキー | https://linear.app/settings/account/security |
| `NOTION_API_KEY` | `notion.api_key` | str | Notion統合トークン | https://www.notion.so/my-integrations |
| `TENOR_API_KEY` | `gif_search.tenor.api_key` | str | Tenor GIF検索APIキー | https://developers.google.com/tenor/guides/create_key |
| `HONCHO_API_KEY` | `honcho.api_key` | str | Honcho APIキー | https://app.honcho.dev |
| `HONCHO_BASE_URL` | `honcho.base_url` | str | 自前HonchoベースURL | - |
| `TOOL_GATEWAY_DOMAIN` | `tool_gateway.domain` | str | ツールゲートウェイドメイン | - |
| `TOOL_GATEWAY_SCHEME` | `tool_gateway.scheme` | str | ツールゲートウェイスキーム | デフォルト: https |
| `TOOL_GATEWAY_USER_TOKEN` | `tool_gateway.user_token` | str | ツールゲートウェイ認証トークン | - |

---

## 5. システム設定

| 環境変数名 | config.yamlキー | 型 | 説明 | 備考 |
|-----------|----------------|----|------|------|
| `SUDO_PASSWORD` | `terminal.sudo_password` | str | terminalコマンドのsudoパスワード | 明示的空白でプロンプトスキップ |
| `HERMES_HOME` | `-` | str | Hermesホームディレクトリパス | config.yamlの読み込み元 |
| `HERMES_HOME_MODE` | `-` | str | Hermesホームモード | - |
| `HERMES_CONTAINER` | `-` | str | コンテナランタイム検出 | - |
| `HERMES_DEV` | `-` | str | 開発モードフラグ | - |
| `HERMES_MANAGED` | `-` | str | 管理環境フラグ | - |
| `HERMES_TIMEZONE` | `agent.timezone` | str | タイムゾーン | - |

---

## 6. 環境変数カテゴリ統計

| カテゴリ | 数 | 環境変数名 |
|---------|---|-----------|
| **messaging** | 51 | Telegram, Discord, Slack, IRC, Matrix, Mattermost, BlueBubbles, QQ |
| **provider** | 50 | Ollama, OpenRouter, HuggingFace, Google, Anthropic, xAI, NVIDIA, DeepSeek, Kimi, MiniMax, GLM, DashScope, GMI, Arcee, Azure, Gemini, Xiaomi |
| **tool** | 27 | Brave, SearXNG, Firecrawl, Parallel, Tavily, Exa, Browser, ElevenLabs, OpenAI VOICE, Mistral, OpenCode, FAL, GitHub, Honcho, TOOL_GATEWAY |
| **setting** | 6 | HERMES_MAX_ITERATIONS, HERMES_PREFILL_MESSAGES_FILE, HERMES_EPHEMERAL_SYSTEM_PROMPT, HERMES_TOOL_PROGRESS, HERMES_TOOL_PROGRESS_MODE, SUDO_PASSWORD |
| **skill** | 4 | Airtable, Linear, Notion, Tenor |

**合計 132 環境変数**（config.pyの`OPTIONAL_ENV_VARS`より）

---

## 補足: HERMES_ プレフィックス変数のみへの制限

**重要**: `HERMES_`で始まる環境変数のみを実行時に変更可能。

`HERMES_MAX_ITERATIONS` → `agent.max_iterations` のように、プレフィックスを抜いた名前がconfigのキーに対応する。

その他の環境変数（`API_SERVER_*`, `DISCORD_BOT_TOKEN`等）は固定値として読み込まれ、実行時の上書きは行われない。
