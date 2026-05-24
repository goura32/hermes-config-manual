# 全構成キー フラット一覧（全env-var, 全値）


## `_config_version`

- **Type:** `int`
- **Default:** 23

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

## `code_execution`

- **Type:** `dict`
- **Default:** {1 keys: mode}

#### `code_execution.mode`

- **Type:** `str`
- **Default value:** "project"

## `command_allowlist`

- **Type:** `list`
- **Default:** []

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

## `context`

- **Type:** `dict`
- **Default:** {1 keys: engine}

#### `context.engine`

- **Type:** `str`
- **Default value:** "compressor"

## `credential_pool_strategies`

- **Type:** `dict`
- **Default:** {0 keys: }

## `cron`

- **Type:** `dict`
- **Default:** {2 keys: wrap_response, max_parallel_jobs}

#### `cron.wrap_response`

- **Type:** `bool`
- **Default value:** true

#### `cron.max_parallel_jobs`

- **Type:** `NoneType`
- **Default value:** None

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


## `dashboard`

- **Type:** `dict`
- **Default:** {2 keys: theme, show_token_analytics}

#### `dashboard.theme`

- **Type:** `str`
- **Default value:** "default"

#### `dashboard.show_token_analytics`

- **Type:** `bool`
- **Default value:** false

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

## `discord`

- **Type:** `dict`
- **Default:** {13 keys: require_mention, free_response_channels, allowed_channels, auto_thread, thread_require_mention}

#### `discord.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `discord.free_response_channels`

- **Type:** `str`
- **Default value:** ""

#### `discord.allowed_channels`

- **Type:** `str`
- **Default value:** ""

#### `discord.auto_thread`

- **Type:** `bool`
- **Default value:** true

#### `discord.thread_require_mention`

- **Type:** `bool`
- **Default value:** false

#### `discord.history_backfill`

- **Type:** `bool`
- **Default value:** true

#### `discord.history_backfill_limit`

- **Type:** `int`
- **Default value:** 50

#### `discord.reactions`

- **Type:** `bool`
- **Default value:** true

#### `discord.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `discord.dm_role_auth_guild`

- **Type:** `str`
- **Default value:** ""

#### `discord.server_actions`

- **Type:** `str`
- **Default value:** ""

#### `discord.allow_any_attachment`

- **Type:** `bool`
- **Default value:** false

#### `discord.max_attachment_bytes`

- **Type:** `int`
- **Default value:** 33554432

## `display`

- **Type:** `dict`
- **Default:** {27 keys: compact, personality, resume_display, busy_input_mode, tui_auto_resume_recent}

#### `display.compact`

- **Type:** `bool`
- **Default value:** false

#### `display.personality`

- **Type:** `str`
- **Default value:** "kawaii"

#### `display.resume_display`

- **Type:** `str`
- **Default value:** "full"

#### `display.busy_input_mode`

- **Type:** `str`
- **Default value:** "interrupt"

#### `display.tui_auto_resume_recent`

- **Type:** `bool`
- **Default value:** false

#### `display.bell_on_complete`

- **Type:** `bool`
- **Default value:** false

#### `display.show_reasoning`

- **Type:** `bool`
- **Default value:** false

#### `display.streaming`

- **Type:** `bool`
- **Default value:** false

#### `display.timestamps`

- **Type:** `bool`
- **Default value:** false

#### `display.final_response_markdown`

- **Type:** `str`
- **Default value:** "strip"

#### `display.persistent_output`

- **Type:** `bool`
- **Default value:** true

#### `display.persistent_output_max_lines`

- **Type:** `int`
- **Default value:** 200

#### `display.inline_diffs`

- **Type:** `bool`
- **Default value:** true

#### `display.file_mutation_verifier`

- **Type:** `bool`
- **Default value:** true

#### `display.show_cost`

- **Type:** `bool`
- **Default value:** false

#### `display.skin`

- **Type:** `str`
- **Default value:** "default"

#### `display.language`

- **Type:** `str`
- **Default value:** "en"

#### `display.tui_status_indicator`

- **Type:** `str`
- **Default value:** "kaomoji"

#### `display.user_message_preview`

- **Type:** `dict`
- **Default value:** {2 keys: first_lines, last_lines}

### Sub-keys of `user_message_preview`

##### `display.user_message_preview.first_lines`

- **Type:** `int`
- **Default value:** 2

##### `display.user_message_preview.last_lines`

- **Type:** `int`
- **Default value:** 2


#### `display.interim_assistant_messages`

- **Type:** `bool`
- **Default value:** true

#### `display.tool_progress_command`

- **Type:** `bool`
- **Default value:** false

#### `display.tool_progress_overrides`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `display.tool_preview_length`

- **Type:** `int`
- **Default value:** 0

#### `display.ephemeral_system_ttl`

- **Type:** `int`
- **Default value:** 0

#### `display.platforms`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `display.runtime_footer`

- **Type:** `dict`
- **Default value:** {2 keys: enabled, fields}

### Sub-keys of `runtime_footer`

##### `display.runtime_footer.enabled`

- **Type:** `bool`
- **Default value:** false

##### `display.runtime_footer.fields`

- **Type:** `list`
- **Default value:** ["model", "context_pct", "cwd"]


#### `display.copy_shortcut`

- **Type:** `str`
- **Default value:** "auto"

## `fallback_providers`

- **Type:** `list`
- **Default:** []

## `file_read_max_chars`

- **Type:** `int`
- **Default:** 100000

## `goals`

- **Type:** `dict`
- **Default:** {1 keys: max_turns}

#### `goals.max_turns`

- **Type:** `int`
- **Default value:** 20

## `honcho`

- **Type:** `dict`
- **Default:** {0 keys: }

## `hooks`

- **Type:** `dict`
- **Default:** {0 keys: }

## `hooks_auto_accept`

- **Type:** `bool`
- **Default:** false

## `human_delay`

- **Type:** `dict`
- **Default:** {3 keys: mode, min_ms, max_ms}

#### `human_delay.mode`

- **Type:** `str`
- **Default value:** "off"

#### `human_delay.min_ms`

- **Type:** `int`
- **Default value:** 800

#### `human_delay.max_ms`

- **Type:** `int`
- **Default value:** 2500

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

## `matrix`

- **Type:** `dict`
- **Default:** {3 keys: require_mention, free_response_rooms, allowed_rooms}

#### `matrix.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `matrix.free_response_rooms`

- **Type:** `str`
- **Default value:** ""

#### `matrix.allowed_rooms`

- **Type:** `str`
- **Default value:** ""

## `mattermost`

- **Type:** `dict`
- **Default:** {4 keys: require_mention, free_response_channels, allowed_channels, channel_prompts}

#### `mattermost.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `mattermost.free_response_channels`

- **Type:** `str`
- **Default value:** ""

#### `mattermost.allowed_channels`

- **Type:** `str`
- **Default value:** ""

#### `mattermost.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

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

## `model`

- **Type:** `str`
- **Default:** ""

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

## `network`

- **Type:** `dict`
- **Default:** {1 keys: force_ipv4}

#### `network.force_ipv4`

- **Type:** `bool`
- **Default value:** false

## `onboarding`

- **Type:** `dict`
- **Default:** {1 keys: seen}

#### `onboarding.seen`

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

## `personalities`

- **Type:** `dict`
- **Default:** {0 keys: }

## `prefill_messages_file`

- **Type:** `str`
- **Default:** ""

## `privacy`

- **Type:** `dict`
- **Default:** {1 keys: redact_pii}

#### `privacy.redact_pii`

- **Type:** `bool`
- **Default value:** false

## `prompt_caching`

- **Type:** `dict`
- **Default:** {1 keys: cache_ttl}

#### `prompt_caching.cache_ttl`

- **Type:** `str`
- **Default value:** "5m"

## `providers`

- **Type:** `dict`
- **Default:** {0 keys: }

## `quick_commands`

- **Type:** `dict`
- **Default:** {0 keys: }

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

## `slack`

- **Type:** `dict`
- **Default:** {4 keys: require_mention, free_response_channels, allowed_channels, channel_prompts}

#### `slack.require_mention`

- **Type:** `bool`
- **Default value:** true

#### `slack.free_response_channels`

- **Type:** `str`
- **Default value:** ""

#### `slack.allowed_channels`

- **Type:** `str`
- **Default value:** ""

#### `slack.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

## `stt`

- **Type:** `dict`
- **Default:** {5 keys: enabled, provider, local, openai, mistral}

#### `stt.enabled`

- **Type:** `bool`
- **Default value:** true

#### `stt.provider`

- **Type:** `str`
- **Default value:** "local"

#### `stt.local`

- **Type:** `dict`
- **Default value:** {2 keys: model, language}

### Sub-keys of `local`

##### `stt.local.model`

- **Type:** `str`
- **Default value:** "base"

##### `stt.local.language`

- **Type:** `str`
- **Default value:** ""


#### `stt.openai`

- **Type:** `dict`
- **Default value:** {1 keys: model}

### Sub-keys of `openai`

##### `stt.openai.model`

- **Type:** `str`
- **Default value:** "whisper-1"


#### `stt.mistral`

- **Type:** `dict`
- **Default value:** {1 keys: model}

### Sub-keys of `mistral`

##### `stt.mistral.model`

- **Type:** `str`
- **Default value:** "voxtral-mini-latest"


## `telegram`

- **Type:** `dict`
- **Default:** {3 keys: reactions, channel_prompts, allowed_chats}

#### `telegram.reactions`

- **Type:** `bool`
- **Default value:** false

#### `telegram.channel_prompts`

- **Type:** `dict`
- **Default value:** {0 keys: }

#### `telegram.allowed_chats`

- **Type:** `str`
- **Default value:** ""

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

## `timezone`

- **Type:** `str`
- **Default:** ""

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

## `toolsets`

- **Type:** `list`
- **Default:** ["hermes-cli"]

## `tts`

- **Type:** `dict`
- **Default:** {8 keys: provider, edge, elevenlabs, openai, xai}

#### `tts.provider`

- **Type:** `str`
- **Default value:** "edge"

#### `tts.edge`

- **Type:** `dict`
- **Default value:** {1 keys: voice}

### Sub-keys of `edge`

##### `tts.edge.voice`

- **Type:** `str`
- **Default value:** "en-US-AriaNeural"


#### `tts.elevenlabs`

- **Type:** `dict`
- **Default value:** {2 keys: voice_id, model_id}

### Sub-keys of `elevenlabs`

##### `tts.elevenlabs.voice_id`

- **Type:** `str`
- **Default value:** "pNInz6obpgDQGcFmaJgB"

##### `tts.elevenlabs.model_id`

- **Type:** `str`
- **Default value:** "eleven_multilingual_v2"


#### `tts.openai`

- **Type:** `dict`
- **Default value:** {2 keys: model, voice}

### Sub-keys of `openai`

##### `tts.openai.model`

- **Type:** `str`
- **Default value:** "gpt-4o-mini-tts"

##### `tts.openai.voice`

- **Type:** `str`
- **Default value:** "alloy"


#### `tts.xai`

- **Type:** `dict`
- **Default value:** {4 keys: voice_id, language, sample_rate, bit_rate}

### Sub-keys of `xai`

##### `tts.xai.voice_id`

- **Type:** `str`
- **Default value:** "eve"

##### `tts.xai.language`

- **Type:** `str`
- **Default value:** "en"

##### `tts.xai.sample_rate`

- **Type:** `int`
- **Default value:** 24000

##### `tts.xai.bit_rate`

- **Type:** `int`
- **Default value:** 128000


#### `tts.mistral`

- **Type:** `dict`
- **Default value:** {2 keys: model, voice_id}

### Sub-keys of `mistral`

##### `tts.mistral.model`

- **Type:** `str`
- **Default value:** "voxtral-mini-tts-2603"

##### `tts.mistral.voice_id`

- **Type:** `str`
- **Default value:** "c69964a6-ab8b-4f8a-9465-ec0925096ec8"


#### `tts.neutts`

- **Type:** `dict`
- **Default value:** {4 keys: ref_audio, ref_text, model, device}

### Sub-keys of `neutts`

##### `tts.neutts.ref_audio`

- **Type:** `str`
- **Default value:** ""

##### `tts.neutts.ref_text`

- **Type:** `str`
- **Default value:** ""

##### `tts.neutts.model`

- **Type:** `str`
- **Default value:** "neuphonic/neutts-air-q4-gguf"

##### `tts.neutts.device`

- **Type:** `str`
- **Default value:** "cpu"


#### `tts.piper`

- **Type:** `dict`
- **Default value:** {1 keys: voice}

### Sub-keys of `piper`

##### `tts.piper.voice`

- **Type:** `str`
- **Default value:** "en_US-lessac-medium"


## `updates`

- **Type:** `dict`
- **Default:** {2 keys: pre_update_backup, backup_keep}

#### `updates.pre_update_backup`

- **Type:** `bool`
- **Default value:** false

#### `updates.backup_keep`

- **Type:** `int`
- **Default value:** 5

## `voice`

- **Type:** `dict`
- **Default:** {6 keys: record_key, max_recording_seconds, auto_tts, beep_enabled, silence_threshold}

#### `voice.record_key`

- **Type:** `str`
- **Default value:** "ctrl+b"

#### `voice.max_recording_seconds`

- **Type:** `int`
- **Default value:** 120

#### `voice.auto_tts`

- **Type:** `bool`
- **Default value:** false

#### `voice.beep_enabled`

- **Type:** `bool`
- **Default value:** true

#### `voice.silence_threshold`

- **Type:** `int`
- **Default value:** 200

#### `voice.silence_duration`

- **Type:** `float`
- **Default value:** 3.0

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

## `whatsapp`

- **Type:** `dict`
- **Default:** {0 keys: }

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
