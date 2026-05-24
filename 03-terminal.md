# ターミナル (バックエンド) 設定

ターミナルバックエンド（local / docker / modal / daytona / singularity / container）の
実行環境に関する設定。Docker イメージ、環境変数継承、CPU/メモリ制約などを設定できる。

---

## `terminal`

- **Type:** `dict`
- **Default:** {23 keys: backend, modal_mode, cwd, timeout, env_passthrough}

#### `terminal.backend`

- **Type:** `str`
- **Default value:** "local"

#### `terminal.modal_mode`

- **Type:** `str`
- **Default value:** "auto"

#### `terminal.cwd`

- **Type:** `str`
- **Default value:** "."

#### `terminal.timeout`

- **Type:** `int`
- **Default value:** 180

#### `terminal.env_passthrough`

- **Type:** `list`
- **Default value:** []

#### `terminal.shell_init_files`

- **Type:** `list`
- **Default value:** []

#### `terminal.auto_source_bashrc`

- **Type:** `bool`
- **Default value:** true

#### `terminal.docker_image`

- **Type:** `str`
- **Default value:** "nikolaik/python-nodejs:python3.11-nodejs20"

#### `terminal.docker_forward_env`

- **Type:** `list`
- **Default value:** []

#### `terminal.docker_env`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `terminal.singularity_image`

- **Type:** `str`
- **Default value:** "docker://nikolaik/python-nodejs:python3.11-nodejs20"

#### `terminal.modal_image`

- **Type:** `str`
- **Default value:** "nikolaik/python-nodejs:python3.11-nodejs20"

#### `terminal.daytona_image`

- **Type:** `str`
- **Default value:** "nikolaik/python-nodejs:python3.11-nodejs20"

#### `terminal.vercel_runtime`

- **Type:** `str`
- **Default value:** "node24"

#### `terminal.container_cpu`

- **Type:** `int`
- **Default value:** 1

#### `terminal.container_memory`

- **Type:** `int`
- **Default value:** 5120

#### `terminal.container_disk`

- **Type:** `int`
- **Default value:** 51200

#### `terminal.container_persistent`

- **Type:** `bool`
- **Default value:** true

#### `terminal.docker_volumes`

- **Type:** `list`
- **Default value:** []

#### `terminal.docker_mount_cwd_to_workspace`

- **Type:** `bool`
- **Default value:** false

#### `terminal.docker_extra_args`

- **Type:** `list`
- **Default value:** []

#### `terminal.docker_run_as_host_user`

- **Type:** `bool`
- **Default value:** false

#### `terminal.persistent_shell`

- **Type:** `bool`
- **Default value:** true
