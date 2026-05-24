# モデル・プロバイダー設定

Hermes Agent が使用するAIモデル、APIプロバイダー、フォールバック構成。
`,model_catalog` は外部のモデルリストAPIと連携し、`,credential_pool_strategies` 
はクレデンシャル管理（vault等）の設定を担う。

---

## `model`

- **Type:** `str`
- **Default:** ""

## `providers`

- **Type:** `dict`
- **Default:** {0 keys: }

## `fallback_providers`

- **Type:** `list`
- **Default:** []

## `delegation`

- **Type:** `dict`
- **Default:** {13 keys: model, provider, base_url, api_key, api_mode}

#### `delegation.model`

- **Type:** `str`
- **Default value:** ""

#### `delegation.provider`

- **Type:** `str`
- **Default value:** ""

#### `delegation.base_url`

- **Type:** `str`
- **Default value:** ""

#### `delegation.api_key`

- **Type:** `str`
- **Default value:** ""

#### `delegation.api_mode`

- **Type:** `str`
- **Default value:** ""

#### `delegation.inherit_mcp_toolsets`

- **Type:** `bool`
- **Default value:** true

#### `delegation.max_iterations`

- **Type:** `int`
- **Default value:** 50

#### `delegation.child_timeout_seconds`

- **Type:** `int`
- **Default value:** 600

#### `delegation.reasoning_effort`

- **Type:** `str`
- **Default value:** ""

#### `delegation.max_concurrent_children`

- **Type:** `int`
- **Default value:** 3

#### `delegation.max_spawn_depth`

- **Type:** `int`
- **Default value:** 1

#### `delegation.orchestrator_enabled`

- **Type:** `bool`
- **Default value:** true

#### `delegation.subagent_auto_approve`

- **Type:** `bool`
- **Default value:** false

## `toolsets`

- **Type:** `list`
- **Default:** ["hermes-cli"]

## `credential_pool_strategies`

- **Type:** `dict`
- **Default:** {0 keys: }

## `model_catalog`

- **Type:** `dict`
- **Default:** {4 keys: enabled, url, ttl_hours, providers}

#### `model_catalog.enabled`

- **Type:** `bool`
- **Default value:** true

#### `model_catalog.url`

- **Type:** `str`
- **Default value:** "https://hermes-agent.nousresearch.com/docs/api/model-catalog.json"

#### `model_catalog.ttl_hours`

- **Type:** `int`
- **Default value:** 24

#### `model_catalog.providers`

- **Type:** `dict`
- **Default value:** {0 keys: }

## `openrouter`

- **Type:** `dict`
- **Default:** {3 keys: response_cache, response_cache_ttl, min_coding_score}

#### `openrouter.response_cache`

- **Type:** `bool`
- **Default value:** true

#### `openrouter.response_cache_ttl`

- **Type:** `int`
- **Default value:** 300

#### `openrouter.min_coding_score`

- **Type:** `float`
- **Default value:** 0.65

## `bedrock`

- **Type:** `dict`
- **Default:** {3 keys: region, discovery, guardrail}

#### `bedrock.region`

- **Type:** `str`
- **Default value:** ""

#### `bedrock.discovery`

- **Type:** `dict`
- **Default value:** {3 keys: enabled, provider_filter, refresh_interval}

### Sub-keys of `discovery`

##### `bedrock.discovery.enabled`

- **Type:** `bool`
- **Default value:** true

##### `bedrock.discovery.provider_filter`

- **Type:** `list`
- **Default value:** []

##### `bedrock.discovery.refresh_interval`

- **Type:** `int`
- **Default value:** 3600


#### `bedrock.guardrail`

- **Type:** `dict`
- **Default value:** {4 keys: guardrail_identifier, guardrail_version, stream_processing_mode, trace}

### Sub-keys of `guardrail`

##### `bedrock.guardrail.guardrail_identifier`

- **Type:** `str`
- **Default value:** ""

##### `bedrock.guardrail.guardrail_version`

- **Type:** `str`
- **Default value:** ""

##### `bedrock.guardrail.stream_processing_mode`

- **Type:** `str`
- **Default value:** "async"

##### `bedrock.guardrail.trace`

- **Type:** `str`
- **Default value:** "disabled"


## `auxiliary`

- **Type:** `dict`
- **Default:** {11 keys: vision, web_extract, compression, skills_hub, approval}

#### `auxiliary.vision`

- **Type:** `dict`
- **Default value:** {7 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `vision`

##### `auxiliary.vision.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.vision.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.vision.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.vision.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.vision.timeout`

- **Type:** `int`
- **Default value:** 120

##### `auxiliary.vision.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }

##### `auxiliary.vision.download_timeout`

- **Type:** `int`
- **Default value:** 30


#### `auxiliary.web_extract`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `web_extract`

##### `auxiliary.web_extract.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.web_extract.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.web_extract.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.web_extract.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.web_extract.timeout`

- **Type:** `int`
- **Default value:** 360

##### `auxiliary.web_extract.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.compression`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `compression`

##### `auxiliary.compression.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.compression.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.compression.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.compression.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.compression.timeout`

- **Type:** `int`
- **Default value:** 120

##### `auxiliary.compression.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.skills_hub`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `skills_hub`

##### `auxiliary.skills_hub.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.skills_hub.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.skills_hub.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.skills_hub.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.skills_hub.timeout`

- **Type:** `int`
- **Default value:** 30

##### `auxiliary.skills_hub.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.approval`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `approval`

##### `auxiliary.approval.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.approval.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.approval.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.approval.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.approval.timeout`

- **Type:** `int`
- **Default value:** 30

##### `auxiliary.approval.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.mcp`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `mcp`

##### `auxiliary.mcp.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.mcp.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.mcp.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.mcp.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.mcp.timeout`

- **Type:** `int`
- **Default value:** 30

##### `auxiliary.mcp.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.title_generation`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `title_generation`

##### `auxiliary.title_generation.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.title_generation.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.title_generation.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.title_generation.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.title_generation.timeout`

- **Type:** `int`
- **Default value:** 30

##### `auxiliary.title_generation.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.triage_specifier`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `triage_specifier`

##### `auxiliary.triage_specifier.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.triage_specifier.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.triage_specifier.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.triage_specifier.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.triage_specifier.timeout`

- **Type:** `int`
- **Default value:** 120

##### `auxiliary.triage_specifier.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.kanban_decomposer`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `kanban_decomposer`

##### `auxiliary.kanban_decomposer.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.kanban_decomposer.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.kanban_decomposer.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.kanban_decomposer.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.kanban_decomposer.timeout`

- **Type:** `int`
- **Default value:** 180

##### `auxiliary.kanban_decomposer.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.profile_describer`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `profile_describer`

##### `auxiliary.profile_describer.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.profile_describer.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.profile_describer.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.profile_describer.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.profile_describer.timeout`

- **Type:** `int`
- **Default value:** 60

##### `auxiliary.profile_describer.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }


#### `auxiliary.curator`

- **Type:** `dict`
- **Default value:** {6 keys: provider, model, base_url, api_key, timeout}

### Sub-keys of `curator`

##### `auxiliary.curator.provider`

- **Type:** `str`
- **Default value:** "auto"

##### `auxiliary.curator.model`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.curator.base_url`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.curator.api_key`

- **Type:** `str`
- **Default value:** ""

##### `auxiliary.curator.timeout`

- **Type:** `int`
- **Default value:** 600

##### `auxiliary.curator.extra_body`

- **Type:** `dict`
- **Default value:** {0 keys: }

