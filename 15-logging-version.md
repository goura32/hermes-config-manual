# ロギング・バージョン管理

ログレベル、ローテートサイズ、バックアップ数、メモリモニターなどの設定。
,_config_version` は設定スキーマのバージョン番号。

---

## `logging`

- **Type:** `dict`
- **Default:** {4 keys: level, max_size_mb, backup_count, memory_monitor}

#### `logging.level`

- **Type:** `str`
- **Default value:** "INFO"

#### `logging.max_size_mb`

- **Type:** `int`
- **Default value:** 5

#### `logging.backup_count`

- **Type:** `int`
- **Default value:** 3

#### `logging.memory_monitor`

- **Type:** `dict`
- **Default value:** {2 keys: enabled, interval_seconds}

### Sub-keys of `memory_monitor`

##### `logging.memory_monitor.enabled`

- **Type:** `bool`
- **Default value:** true

##### `logging.memory_monitor.interval_seconds`

- **Type:** `int`
- **Default value:** 300


## `_config_version`

- **Type:** `int`
- **Default:** 23
