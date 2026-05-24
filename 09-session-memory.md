# セッション・メモリ管理設定

長期メモリ（OpenViking統合）、セッションの自動整理、
キュレーターによる自動メンテナンス、スキル設定など。

---

## `memory`

- **Type:** `dict`
- **Default:** {5 keys: memory_enabled, user_profile_enabled, memory_char_limit, user_char_limit, provider}

#### `memory.memory_enabled`

- **Type:** `bool`
- **Default value:** true

#### `memory.user_profile_enabled`

- **Type:** `bool`
- **Default value:** true

#### `memory.memory_char_limit`

- **Type:** `int`
- **Default value:** 2200

#### `memory.user_char_limit`

- **Type:** `int`
- **Default value:** 1375

#### `memory.provider`

- **Type:** `str`
- **Default value:** ""

## `sessions`

- **Type:** `dict`
- **Default:** {5 keys: auto_prune, retention_days, vacuum_after_prune, min_interval_hours, write_json_snapshots}

#### `sessions.auto_prune`

- **Type:** `bool`
- **Default value:** false

#### `sessions.retention_days`

- **Type:** `int`
- **Default value:** 90

#### `sessions.vacuum_after_prune`

- **Type:** `bool`
- **Default value:** true

#### `sessions.min_interval_hours`

- **Type:** `int`
- **Default value:** 24

#### `sessions.write_json_snapshots`

- **Type:** `bool`
- **Default value:** false

## `curator`

- **Type:** `dict`
- **Default:** {6 keys: enabled, interval_hours, min_idle_hours, stale_after_days, archive_after_days}

#### `curator.enabled`

- **Type:** `bool`
- **Default value:** true

#### `curator.interval_hours`

- **Type:** `int`
- **Default value:** 168

#### `curator.min_idle_hours`

- **Type:** `int`
- **Default value:** 2

#### `curator.stale_after_days`

- **Type:** `int`
- **Default value:** 30

#### `curator.archive_after_days`

- **Type:** `int`
- **Default value:** 90

#### `curator.backup`

- **Type:** `dict`
- **Default value:** {2 keys: enabled, keep}

### Sub-keys of `backup`

##### `curator.backup.enabled`

- **Type:** `bool`
- **Default value:** true

##### `curator.backup.keep`

- **Type:** `int`
- **Default value:** 5


## `honcho`

- **Type:** `dict`
- **Default:** {0 keys: }

## `goals`

- **Type:** `dict`
- **Default:** {1 keys: max_turns}

#### `goals.max_turns`

- **Type:** `int`
- **Default value:** 20

## `skills`

- **Type:** `dict`
- **Default:** {5 keys: external_dirs, template_vars, inline_shell, inline_shell_timeout, guard_agent_created}

#### `skills.external_dirs`

- **Type:** `list`
- **Default value:** []

#### `skills.template_vars`

- **Type:** `bool`
- **Default value:** true

#### `skills.inline_shell`

- **Type:** `bool`
- **Default value:** false

#### `skills.inline_shell_timeout`

- **Type:** `int`
- **Default value:** 10

#### `skills.guard_agent_created`

- **Type:** `bool`
- **Default value:** false

## `prefill_messages_file`

- **Type:** `str`
- **Default:** ""
