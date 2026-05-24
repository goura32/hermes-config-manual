# メッセージングプラットフォーム統合設定

Slack, Discord, WhatsApp, Telegram, Mattermost, Matrix それぞれの
接続設定、承認チャット/チャンネルの制御、メンションの要件などを設定。

---

## `slack`

- **Type:** `dict`
- **Default:** {4 keys: require_mention, free_response_channels, allowed_channels, channel_prompts}

#### `slack.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `slack.free_response_channels`

- **Type:** `str`
- **Default value:** ""

#### `slack.allowed_channels`

- **Type:** `str`
- **Default value:** ""

#### `slack.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

## `discord`

- **Type:** `dict`
- **Default:** {13 keys: require_mention, free_response_channels, allowed_channels, auto_thread, thread_require_mention}

#### `discord.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `discord.free_response_channels`

- **Type:** `str`
- **Default value:** ""

#### `discord.allowed_channels`

- **Type:** `str`
- **Default value:** ""

#### `discord.auto_thread`

- **Type:** `bool`
- **Default value:** true

#### `discord.thread_require_mention`

- **Type:** `bool`
- **Default value:** false

#### `discord.history_backfill`

- **Type:** `bool`
- **Default value:** true

#### `discord.history_backfill_limit`

- **Type:** `int`
- **Default value:** 50

#### `discord.reactions`

- **Type:** `bool`
- **Default value:** true

#### `discord.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `discord.dm_role_auth_guild`

- **Type:** `str`
- **Default value:** ""

#### `discord.server_actions`

- **Type:** `str`
- **Default value:** ""

#### `discord.allow_any_attachment`

- **Type:** `bool`
- **Default value:** false

#### `discord.max_attachment_bytes`

- **Type:** `int`
- **Default value:** 33554432

## `whatsapp`

- **Type:** `dict`
- **Default:** {0 keys: }

## `telegram`

- **Type:** `dict`
- **Default:** {3 keys: reactions, channel_prompts, allowed_chats}

#### `telegram.reactions`

- **Type:** `bool`
- **Default value:** false

#### `telegram.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `telegram.allowed_chats`

- **Type:** `str`
- **Default value:** ""

## `mattermost`

- **Type:** `dict`
- **Default:** {4 keys: require_mention, free_response_channels, allowed_channels, channel_prompts}

#### `mattermost.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `mattermost.free_response_channels`

- **Type:** `str`
- **Default value:** ""

#### `mattermost.allowed_channels`

- **Type:** `str`
- **Default value:** ""

#### `mattermost.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

## `matrix`

- **Type:** `dict`
- **Default:** {3 keys: require_mention, free_response_rooms, allowed_rooms}

#### `matrix.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `matrix.free_response_rooms`

- **Type:** `str`
- **Default value:** ""

#### `matrix.allowed_rooms`

- **Type:** `str`
- **Default value:** ""

---

### 音声関係設定

## `tts`

- **Type:** `dict`
- **Default:** {8 keys: provider, edge, elevenlabs, openai, xai}

#### `tts.provider`

- **Type:** `str`
- **Default value:** "edge"

#### `tts.edge`

- **Type:** `dict`
- **Default value:** {1 keys: voice}

### Sub-keys of `edge`

##### `tts.edge.voice`

- **Type:** `str`
- **Default value:** "en-US-AriaNeural"


#### `tts.elevenlabs`

- **Type:** `dict`
- **Default value:** {2 keys: voice_id, model_id}

### Sub-keys of `elevenlabs`

##### `tts.elevenlabs.voice_id`

- **Type:** `str`
- **Default value:** "pNInz6obpgDQGcFmaJgB"

##### `tts.elevenlabs.model_id`

- **Type:** `str`
- **Default value:** "eleven_multilingual_v2"


#### `tts.openai`

- **Type:** `dict`
- **Default value:** {2 keys: model, voice}

### Sub-keys of `openai`

##### `tts.openai.model`

- **Type:** `str`
- **Default value:** "gpt-4o-mini-tts"

##### `tts.openai.voice`

- **Type:** `str`
- **Default value:** "alloy"


#### `tts.xai`

- **Type:** `dict`
- **Default value:** {4 keys: voice_id, language, sample_rate, bit_rate}

### Sub-keys of `xai`

##### `tts.xai.voice_id`

- **Type:** `str`
- **Default value:** "eve"

##### `tts.xai.language`

- **Type:** `str`
- **Default value:** "en"

##### `tts.xai.sample_rate`

- **Type:** `int`
- **Default value:** 24000

##### `tts.xai.bit_rate`

- **Type:** `int`
- **Default value:** 128000


#### `tts.mistral`

- **Type:** `dict`
- **Default value:** {2 keys: model, voice_id}

### Sub-keys of `mistral`

##### `tts.mistral.model`

- **Type:** `str`
- **Default value:** "voxtral-mini-tts-2603"

##### `tts.mistral.voice_id`

- **Type:** `str`
- **Default value:** "c69964a6-ab8b-4f8a-9465-ec0925096ec8"


#### `tts.neutts`

- **Type:** `dict`
- **Default value:** {4 keys: ref_audio, ref_text, model, device}

### Sub-keys of `neutts`

##### `tts.neutts.ref_audio`

- **Type:** `str`
- **Default value:** ""

##### `tts.neutts.ref_text`

- **Type:** `str`
- **Default value:** ""

##### `tts.neutts.model`

- **Type:** `str`
- **Default value:** "neuphonic/neutts-air-q4-gguf"

##### `tts.neutts.device`

- **Type:** `str`
- **Default value:** "cpu"


#### `tts.piper`

- **Type:** `dict`
- **Default value:** {1 keys: voice}

### Sub-keys of `piper`

##### `tts.piper.voice`

- **Type:** `str`
- **Default value:** "en_US-lessac-medium"


## `stt`

- **Type:** `dict`
- **Default:** {5 keys: enabled, provider, local, openai, mistral}

#### `stt.enabled`

- **Type:** `bool`
- **Default value:** true

#### `stt.provider`

- **Type:** `str`
- **Default value:** "local"

#### `stt.local`

- **Type:** `dict`
- **Default value:** {2 keys: model, language}

### Sub-keys of `local`

##### `stt.local.model`

- **Type:** `str`
- **Default value:** "base"

##### `stt.local.language`

- **Type:** `str`
- **Default value:** ""


#### `stt.openai`

- **Type:** `dict`
- **Default value:** {1 keys: model}

### Sub-keys of `openai`

##### `stt.openai.model`

- **Type:** `str`
- **Default value:** "whisper-1"


#### `stt.mistral`

- **Type:** `dict`
- **Default value:** {1 keys: model}

### Sub-keys of `mistral`

##### `stt.mistral.model`

- **Type:** `str`
- **Default value:** "voxtral-mini-latest"


## `voice`

- **Type:** `dict`
- **Default:** {6 keys: record_key, max_recording_seconds, auto_tts, beep_enabled, silence_threshold}

#### `voice.record_key`

- **Type:** `str`
- **Default value:** "ctrl+b"

#### `voice.max_recording_seconds`

- **Type:** `int`
- **Default value:** 120

#### `voice.auto_tts`

- **Type:** `bool`
- **Default value:** false

#### `voice.beep_enabled`

- **Type:** `bool`
- **Default value:** true

#### `voice.silence_threshold`

- **Type:** `int`
- **Default value:** 200

#### `voice.silence_duration`

- **Type:** `float`
- **Default value:** 3.0
