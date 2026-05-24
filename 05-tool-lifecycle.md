# ツール出力・圧縮・チェックポイント設定

ツール呼び出しの出力制限、コンテキスト圧縮の閾値とターゲット比率、
チェックポイントスナップショットの管理に関する設定。

---

## `checkpoints`

- **Type:** `dict`
- **Default:** {8 keys: enabled, max_snapshots, max_total_size_mb, max_file_size_mb, auto_prune}

#### `checkpoints.enabled`

- **Type:** `bool`
- **Default value:** false

#### `checkpoints.max_snapshots`

- **Type:** `int`
- **Default value:** 20

#### `checkpoints.max_total_size_mb`

- **Type:** `int`
- **Default value:** 500

#### `checkpoints.max_file_size_mb`

- **Type:** `int`
- **Default value:** 10

#### `checkpoints.auto_prune`

- **Type:** `bool`
- **Default value:** true

#### `checkpoints.retention_days`

- **Type:** `int`
- **Default value:** 7

#### `checkpoints.delete_orphans`

- **Type:** `bool`
- **Default value:** true

#### `checkpoints.min_interval_hours`

- **Type:** `int`
- **Default value:** 24

## `file_read_max_chars`

- **Type:** `int`
- **Default:** 100000

## `tool_output`

- **Type:** `dict`
- **Default:** {3 keys: max_bytes, max_lines, max_line_length}

#### `tool_output.max_bytes`

- **Type:** `int`
- **Default value:** 50000

#### `tool_output.max_lines`

- **Type:** `int`
- **Default value:** 2000

#### `tool_output.max_line_length`

- **Type:** `int`
- **Default value:** 2000

## `tool_loop_guardrails`

- **Type:** `dict`
- **Default:** {4 keys: warnings_enabled, hard_stop_enabled, warn_after, hard_stop_after}

#### `tool_loop_guardrails.warnings_enabled`

- **Type:** `bool`
- **Default value:** true

#### `tool_loop_guardrails.hard_stop_enabled`

- **Type:** `bool`
- **Default value:** false

#### `tool_loop_guardrails.warn_after`

- **Type:** `dict`
- **Default value:** {3 keys: exact_failure, same_tool_failure, idempotent_no_progress}

### Sub-keys of `warn_after`

##### `tool_loop_guardrails.warn_after.exact_failure`

- **Type:** `int`
- **Default value:** 2

##### `tool_loop_guardrails.warn_after.same_tool_failure`

- **Type:** `int`
- **Default value:** 3

##### `tool_loop_guardrails.warn_after.idempotent_no_progress`

- **Type:** `int`
- **Default value:** 2


#### `tool_loop_guardrails.hard_stop_after`

- **Type:** `dict`
- **Default value:** {3 keys: exact_failure, same_tool_failure, idempotent_no_progress}

### Sub-keys of `hard_stop_after`

##### `tool_loop_guardrails.hard_stop_after.exact_failure`

- **Type:** `int`
- **Default value:** 5

##### `tool_loop_guardrails.hard_stop_after.same_tool_failure`

- **Type:** `int`
- **Default value:** 8

##### `tool_loop_guardrails.hard_stop_after.idempotent_no_progress`

- **Type:** `int`
- **Default value:** 5


## `compression`

- **Type:** `dict`
- **Default:** {7 keys: enabled, threshold, target_ratio, protect_last_n, hygiene_hard_message_limit}

#### `compression.enabled`

- **Type:** `bool`
- **Default value:** true

#### `compression.threshold`

- **Type:** `float`
- **Default value:** 0.5

#### `compression.target_ratio`

- **Type:** `float`
- **Default value:** 0.2

#### `compression.protect_last_n`

- **Type:** `int`
- **Default value:** 20

#### `compression.hygiene_hard_message_limit`

- **Type:** `int`
- **Default value:** 400

#### `compression.protect_first_n`

- **Type:** `int`
- **Default value:** 3

#### `compression.abort_on_summary_failure`

- **Type:** `bool`
- **Default value:** false

## `prompt_caching`

- **Type:** `dict`
- **Default:** {1 keys: cache_ttl}

#### `prompt_caching.cache_ttl`

- **Type:** `str`
- **Default value:** "5m"

## `context`

- **Type:** `dict`
- **Default:** {1 keys: engine}

#### `context.engine`

- **Type:** `str`
- **Default value:** "compressor"
