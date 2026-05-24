# 全設定キー一覧（構成ファイル v1.0+）


| # | キー | Type | Default | ファイル |
|---|-----|------|---------|--------|
| 1 | `_config_version` | `int` | 23 | []() |
| 2 | `agent` | `dict` | {12 keys: max_turns, gateway_timeout, restart_drain_timeout, api_max_retries, service_tier} | [02-agent-core.md](02-agent-core.md) |
| 3 | `approvals` | `dict` | {5 keys: mode, timeout, cron_mode, mcp_reload_confirm, destructive_slash_confirm} | []() |
| 4 | `auxiliary` | `dict` | {11 keys: vision, web_extract, compression, skills_hub, approval} | []() |
| 5 | `bedrock` | `dict` | {3 keys: region, discovery, guardrail} | []() |
| 6 | `browser` | `dict` | {10 keys: inactivity_timeout, command_timeout, record_sessions, allow_private_urls, engine} | []() |
| 7 | `checkpoints` | `dict` | {8 keys: enabled, max_snapshots, max_total_size_mb, max_file_size_mb, auto_prune} | []() |
| 8 | `code_execution` | `dict` | {1 keys: mode} | []() |
| 9 | `command_allowlist` | `list` | [] | []() |
| 10 | `compression` | `dict` | {7 keys: enabled, threshold, target_ratio, protect_last_n, hygiene_hard_message_limit} | []() |
| 11 | `context` | `dict` | {1 keys: engine} | []() |
| 12 | `credential_pool_strategies` | `dict` | {0 keys: } | []() |
| 13 | `cron` | `dict` | {2 keys: wrap_response, max_parallel_jobs} | [12-api-cron.md](12-api-cron.md) |
| 14 | `curator` | `dict` | {6 keys: enabled, interval_hours, min_idle_hours, stale_after_days, archive_after_days} | []() |
| 15 | `dashboard` | `dict` | {2 keys: theme, show_token_analytics} | []() |
| 16 | `delegation` | `dict` | {13 keys: model, provider, base_url, api_key, api_mode} | []() |
| 17 | `discord` | `dict` | {13 keys: require_mention, free_response_channels, allowed_channels, auto_thread, thread_require_mention} | []() |
| 18 | `display` | `dict` | {27 keys: compact, personality, resume_display, busy_input_mode, tui_auto_resume_recent} | [07-ui-display.md](07-ui-display.md) |
| 19 | `fallback_providers` | `list` | [] | []() |
| 20 | `file_read_max_chars` | `int` | 100000 | []() |
| 21 | `goals` | `dict` | {1 keys: max_turns} | []() |
| 22 | `honcho` | `dict` | {0 keys: } | []() |
| 23 | `hooks` | `dict` | {0 keys: } | [11-hooks-commands.md](11-hooks-commands.md) |
| 24 | `hooks_auto_accept` | `bool` | false | []() |
| 25 | `human_delay` | `dict` | {3 keys: mode, min_ms, max_ms} | [08-user-settings.md](08-user-settings.md) |
| 26 | `kanban` | `dict` | {10 keys: dispatch_in_gateway, dispatch_interval_seconds, failure_limit, worker_log_rotate_bytes, worker_log_backup_count} | [14-code-kanban.md](14-code-kanban.md) |
| 27 | `logging` | `dict` | {4 keys: level, max_size_mb, backup_count, memory_monitor} | [15-logging-version.md](15-logging-version.md) |
| 28 | `lsp` | `dict` | {5 keys: enabled, wait_mode, wait_timeout, install_strategy, servers} | []() |
| 29 | `matrix` | `dict` | {3 keys: require_mention, free_response_rooms, allowed_rooms} | []() |
| 30 | `mattermost` | `dict` | {4 keys: require_mention, free_response_channels, allowed_channels, channel_prompts} | []() |
| 31 | `memory` | `dict` | {5 keys: memory_enabled, user_profile_enabled, memory_char_limit, user_char_limit, provider} | [09-session-memory.md](09-session-memory.md) |
| 32 | `model` | `str` | "" | [01-model-providers.md](01-model-providers.md) |
| 33 | `model_catalog` | `dict` | {4 keys: enabled, url, ttl_hours, providers} | []() |
| 34 | `network` | `dict` | {1 keys: force_ipv4} | [13-network-updates.md](13-network-updates.md) |
| 35 | `onboarding` | `dict` | {1 keys: seen} | []() |
| 36 | `openrouter` | `dict` | {3 keys: response_cache, response_cache_ttl, min_coding_score} | []() |
| 37 | `personalities` | `dict` | {0 keys: } | []() |
| 38 | `prefill_messages_file` | `str` | "" | []() |
| 39 | `privacy` | `dict` | {1 keys: redact_pii} | []() |
| 40 | `prompt_caching` | `dict` | {1 keys: cache_ttl} | []() |
| 41 | `providers` | `dict` | {0 keys: } | []() |
| 42 | `quick_commands` | `dict` | {0 keys: } | []() |
| 43 | `secrets` | `dict` | {1 keys: bitwarden} | []() |
| 44 | `security` | `dict` | {9 keys: allow_private_urls, redact_secrets, tirith_enabled, tirith_path, tirith_timeout} | [10-security-approvals.md](10-security-approvals.md) |
| 45 | `sessions` | `dict` | {5 keys: auto_prune, retention_days, vacuum_after_prune, min_interval_hours, write_json_snapshots} | []() |
| 46 | `skills` | `dict` | {5 keys: external_dirs, template_vars, inline_shell, inline_shell_timeout, guard_agent_created} | []() |
| 47 | `slack` | `dict` | {4 keys: require_mention, free_response_channels, allowed_channels, channel_prompts} | [06-messaging.md](06-messaging.md) |
| 48 | `stt` | `dict` | {5 keys: enabled, provider, local, openai, mistral} | []() |
| 49 | `telegram` | `dict` | {3 keys: reactions, channel_prompts, allowed_chats} | []() |
| 50 | `terminal` | `dict` | {23 keys: backend, modal_mode, cwd, timeout, env_passthrough} | [03-terminal.md](03-terminal.md) |
| 51 | `timezone` | `str` | "" | []() |
| 52 | `tool_loop_guardrails` | `dict` | {4 keys: warnings_enabled, hard_stop_enabled, warn_after, hard_stop_after} | []() |
| 53 | `tool_output` | `dict` | {3 keys: max_bytes, max_lines, max_line_length} | [05-tool-lifecycle.md](05-tool-lifecycle.md) |
| 54 | `toolsets` | `list` | ["hermes-cli"] | []() |
| 55 | `tts` | `dict` | {8 keys: provider, edge, elevenlabs, openai, xai} | []() |
| 56 | `updates` | `dict` | {2 keys: pre_update_backup, backup_keep} | []() |
| 57 | `voice` | `dict` | {6 keys: record_key, max_recording_seconds, auto_tts, beep_enabled, silence_threshold} | []() |
| 58 | `web` | `dict` | {3 keys: backend, search_backend, extract_backend} | [04-web-browser.md](04-web-browser.md) |
| 59 | `whatsapp` | `dict` | {0 keys: } | []() |
| 60 | `x_search` | `dict` | {3 keys: model, timeout_seconds, retries} | []() |
