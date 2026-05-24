# カンバン・コード実行設定

カンバンタスク管理（ゲートウェイ経由、インターバル、障害限界、再開戦略）と、
コード実行モード（project/vm）の設定。

---

## `kanban`

- **Type:** `dict`
- **Default:** {10 keys: dispatch_in_gateway, dispatch_interval_seconds, failure_limit, worker_log_rotate_bytes, worker_log_backup_count}

#### `kanban.dispatch_in_gateway`

- **Type:** `bool`
- **Default value:** true

#### `kanban.dispatch_interval_seconds`

- **Type:** `int`
- **Default value:** 60

#### `kanban.failure_limit`

- **Type:** `int`
- **Default value:** 2

#### `kanban.worker_log_rotate_bytes`

- **Type:** `int`
- **Default value:** 2097152

#### `kanban.worker_log_backup_count`

- **Type:** `int`
- **Default value:** 1

#### `kanban.orchestrator_profile`

- **Type:** `str`
- **Default value:** ""

#### `kanban.default_assignee`

- **Type:** `str`
- **Default value:** ""

#### `kanban.auto_decompose`

- **Type:** `bool`
- **Default value:** true

#### `kanban.auto_decompose_per_tick`

- **Type:** `int`
- **Default value:** 3

#### `kanban.dispatch_stale_timeout_seconds`

- **Type:** `int`
- **Default value:** 14400

## `code_execution`

- **Type:** `dict`
- **Default:** {1 keys: mode}

#### `code_execution.mode`

- **Type:** `str`
- **Default value:** "project"
