# UI・表示・プライバシー設定

ターミナル上での表示形式（コンパクト/フル）、ダッシュボードのテーマ、
PII（個人識別情報）の検出・マスキングなどのプライバシー設定。

---

## `display`

- **Type:** `dict`
- **Default:** {27 keys: compact, personality, resume_display, busy_input_mode, tui_auto_resume_recent}

#### `display.compact`

- **Type:** `bool`
- **Default value:** false

#### `display.personality`

- **Type:** `str`
- **Default value:** "kawaii"

#### `display.resume_display`

- **Type:** `str`
- **Default value:** "full"

#### `display.busy_input_mode`

- **Type:** `str`
- **Default value:** "interrupt"

#### `display.tui_auto_resume_recent`

- **Type:** `bool`
- **Default value:** false

#### `display.bell_on_complete`

- **Type:** `bool`
- **Default value:** false

#### `display.show_reasoning`

- **Type:** `bool`
- **Default value:** false

#### `display.streaming`

- **Type:** `bool`
- **Default value:** false

#### `display.timestamps`

- **Type:** `bool`
- **Default value:** false

#### `display.final_response_markdown`

- **Type:** `str`
- **Default value:** "strip"

#### `display.persistent_output`

- **Type:** `bool`
- **Default value:** true

#### `display.persistent_output_max_lines`

- **Type:** `int`
- **Default value:** 200

#### `display.inline_diffs`

- **Type:** `bool`
- **Default value:** true

#### `display.file_mutation_verifier`

- **Type:** `bool`
- **Default value:** true

#### `display.show_cost`

- **Type:** `bool`
- **Default value:** false

#### `display.skin`

- **Type:** `str`
- **Default value:** "default"

#### `display.language`

- **Type:** `str`
- **Default value:** "en"

#### `display.tui_status_indicator`

- **Type:** `str`
- **Default value:** "kaomoji"

#### `display.user_message_preview`

- **Type:** `dict`
- **Default value:** {2 keys: first_lines, last_lines}

### Sub-keys of `user_message_preview`

##### `display.user_message_preview.first_lines`

- **Type:** `int`
- **Default value:** 2

##### `display.user_message_preview.last_lines`

- **Type:** `int`
- **Default value:** 2


#### `display.interim_assistant_messages`

- **Type:** `bool`
- **Default value:** true

#### `display.tool_progress_command`

- **Type:** `bool`
- **Default value:** false

#### `display.tool_progress_overrides`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `display.tool_preview_length`

- **Type:** `int`
- **Default value:** 0

#### `display.ephemeral_system_ttl`

- **Type:** `int`
- **Default value:** 0

#### `display.platforms`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `display.runtime_footer`

- **Type:** `dict`
- **Default value:** {2 keys: enabled, fields}

### Sub-keys of `runtime_footer`

##### `display.runtime_footer.enabled`

- **Type:** `bool`
- **Default value:** false

##### `display.runtime_footer.fields`

- **Type:** `list`
- **Default value:** ["model", "context_pct", "cwd"]


#### `display.copy_shortcut`

- **Type:** `str`
- **Default value:** "auto"

## `dashboard`

- **Type:** `dict`
- **Default:** {2 keys: theme, show_token_analytics}

#### `dashboard.theme`

- **Type:** `str`
- **Default value:** "default"

#### `dashboard.show_token_analytics`

- **Type:** `bool`
- **Default value:** false

## `privacy`

- **Type:** `dict`
- **Default:** {1 keys: redact_pii}

#### `privacy.redact_pii`

- **Type:** `bool`
- **Default value:** false
