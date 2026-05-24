# エージェントコア設定

エージェントの動作制約（ターン数, タイムアウト, トークン制限）と
ツールの強制処理に関する設定。

---

## `agent`

- **Type:** `dict`
- **Default:** {12 keys: max_turns, gateway_timeout, restart_drain_timeout, api_max_retries, service_tier}

#### `agent.max_turns`

- **Type:** `int`
- **Default value:** 90

#### `agent.gateway_timeout`

- **Type:** `int`
- **Default value:** 1800

#### `agent.restart_drain_timeout`

- **Type:** `int`
- **Default value:** 180

#### `agent.api_max_retries`

- **Type:** `int`
- **Default value:** 3

#### `agent.service_tier`

- **Type:** `str`
- **Default value:** ""

#### `agent.tool_use_enforcement`

- **Type:** `str`
- **Default value:** "auto"

#### `agent.gateway_timeout_warning`

- **Type:** `int`
- **Default value:** 900

#### `agent.clarify_timeout`

- **Type:** `int`
- **Default value:** 600

#### `agent.gateway_notify_interval`

- **Type:** `int`
- **Default value:** 180

#### `agent.gateway_auto_continue_freshness`

- **Type:** `int`
- **Default value:** 3600

#### `agent.image_input_mode`

- **Type:** `str`
- **Default value:** "auto"

#### `agent.disabled_toolsets`

- **Type:** `list`
- **Default value:** []
