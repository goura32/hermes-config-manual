# セキュリティ・承認設定

セキュリティポリシー（プライベートURL許可、シークレットの削除、TIRITH認証）、
ツール呼び出しの前介入承認モード、コマンド許可リスト、シークレット管理（Bitwarden等）。

---

## `security`

- **Type:** `dict`
- **Default:** {9 keys: allow_private_urls, redact_secrets, tirith_enabled, tirith_path, tirith_timeout}

#### `security.allow_private_urls`

- **Type:** `bool`
- **Default value:** false

#### `security.redact_secrets`

- **Type:** `bool`
- **Default value:** true

#### `security.tirith_enabled`

- **Type:** `bool`
- **Default value:** true

#### `security.tirith_path`

- **Type:** `str`
- **Default value:** "tirith"

#### `security.tirith_timeout`

- **Type:** `int`
- **Default value:** 5

#### `security.tirith_fail_open`

- **Type:** `bool`
- **Default value:** true

#### `security.website_blocklist`

- **Type:** `dict`
- **Default value:** {3 keys: enabled, domains, shared_files}

### Sub-keys of `website_blocklist`

##### `security.website_blocklist.enabled`

- **Type:** `bool`
- **Default value:** false

##### `security.website_blocklist.domains`

- **Type:** `list`
- **Default value:** []

##### `security.website_blocklist.shared_files`

- **Type:** `list`
- **Default value:** []


#### `security.acked_advisories`

- **Type:** `list`
- **Default value:** []

#### `security.allow_lazy_installs`

- **Type:** `bool`
- **Default value:** true

## `approvals`

- **Type:** `dict`
- **Default:** {5 keys: mode, timeout, cron_mode, mcp_reload_confirm, destructive_slash_confirm}

#### `approvals.mode`

- **Type:** `str`
- **Default value:** "manual"

#### `approvals.timeout`

- **Type:** `int`
- **Default value:** 60

#### `approvals.cron_mode`

- **Type:** `str`
- **Default value:** "deny"

#### `approvals.mcp_reload_confirm`

- **Type:** `bool`
- **Default value:** true

#### `approvals.destructive_slash_confirm`

- **Type:** `bool`
- **Default value:** true

## `command_allowlist`

- **Type:** `list`
- **Default:** []

## `secrets`

- **Type:** `dict`
- **Default:** {1 keys: bitwarden}

#### `secrets.bitwarden`

- **Type:** `dict`
- **Default value:** {6 keys: enabled, access_token_env, project_id, cache_ttl_seconds, override_existing}

### Sub-keys of `bitwarden`

##### `secrets.bitwarden.enabled`

- **Type:** `bool`
- **Default value:** false

##### `secrets.bitwarden.access_token_env`

- **Type:** `str`
- **Default value:** "BWS_ACCESS_TOKEN"

##### `secrets.bitwarden.project_id`

- **Type:** `str`
- **Default value:** ""

##### `secrets.bitwarden.cache_ttl_seconds`

- **Type:** `int`
- **Default value:** 300

##### `secrets.bitwarden.override_existing`

- **Type:** `bool`
- **Default value:** true

##### `secrets.bitwarden.auto_install`

- **Type:** `bool`
- **Default value:** true

