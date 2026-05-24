# ネットワーク・アップデート設定

IPv4強制フラグ、自動アップデート設定、LSP設定、X(Twitter)検索設定、
オンボーディング、自動更新のバックアップ動作など。

---

## `network`

- **Type:** `dict`
- **Default:** {1 keys: force_ipv4}

#### `network.force_ipv4`

- **Type:** `bool`
- **Default value:** false

## `updates`

- **Type:** `dict`
- **Default:** {2 keys: pre_update_backup, backup_keep}

#### `updates.pre_update_backup`

- **Type:** `bool`
- **Default value:** false

#### `updates.backup_keep`

- **Type:** `int`
- **Default value:** 5

## `lsp`

- **Type:** `dict`
- **Default:** {5 keys: enabled, wait_mode, wait_timeout, install_strategy, servers}

#### `lsp.enabled`

- **Type:** `bool`
- **Default value:** true

#### `lsp.wait_mode`

- **Type:** `str`
- **Default value:** "document"

#### `lsp.wait_timeout`

- **Type:** `float`
- **Default value:** 5.0

#### `lsp.install_strategy`

- **Type:** `str`
- **Default value:** "auto"

#### `lsp.servers`

- **Type:** `dict`
- **Default value:** {0 keys: }

## `x_search`

- **Type:** `dict`
- **Default:** {3 keys: model, timeout_seconds, retries}

#### `x_search.model`

- **Type:** `str`
- **Default value:** "grok-4.20-reasoning"

#### `x_search.timeout_seconds`

- **Type:** `int`
- **Default value:** 180

#### `x_search.retries`

- **Type:** `int`
- **Default value:** 2

## `onboarding`

- **Type:** `dict`
- **Default:** {1 keys: seen}

#### `onboarding.seen`

- **Type:** `dict`
- **Default value:** {0 keys: }
