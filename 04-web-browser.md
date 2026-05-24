# ウェブ検索・ブラウザ自動化設定

ウェブ検索バックエンドの選択と、ブラウザ統合ツールの動作設定。

---

## `web`

- **Type:** `dict`
- **Default:** {3 keys: backend, search_backend, extract_backend}

#### `web.backend`

- **Type:** `str`
- **Default value:** ""

#### `web.search_backend`

- **Type:** `str`
- **Default value:** ""

#### `web.extract_backend`

- **Type:** `str`
- **Default value:** ""

## `browser`

- **Type:** `dict`
- **Default:** {10 keys: inactivity_timeout, command_timeout, record_sessions, allow_private_urls, engine}

#### `browser.inactivity_timeout`

- **Type:** `int`
- **Default value:** 120

#### `browser.command_timeout`

- **Type:** `int`
- **Default value:** 30

#### `browser.record_sessions`

- **Type:** `bool`
- **Default value:** false

#### `browser.allow_private_urls`

- **Type:** `bool`
- **Default value:** false

#### `browser.engine`

- **Type:** `str`
- **Default value:** "auto"

#### `browser.auto_local_for_private_urls`

- **Type:** `bool`
- **Default value:** true

#### `browser.cdp_url`

- **Type:** `str`
- **Default value:** ""

#### `browser.dialog_policy`

- **Type:** `str`
- **Default value:** "must_respond"

#### `browser.dialog_timeout_s`

- **Type:** `int`
- **Default value:** 300

#### `browser.camofox`

- **Type:** `dict`
- **Default value:** {4 keys: managed_persistence, user_id, session_key, adopt_existing_tab}

### Sub-keys of `camofox`

##### `browser.camofox.managed_persistence`

- **Type:** `bool`
- **Default value:** false

##### `browser.camofox.user_id`

- **Type:** `str`
- **Default value:** ""

##### `browser.camofox.session_key`

- **Type:** `str`
- **Default value:** ""

##### `browser.camofox.adopt_existing_tab`

- **Type:** `bool`
- **Default value:** false

