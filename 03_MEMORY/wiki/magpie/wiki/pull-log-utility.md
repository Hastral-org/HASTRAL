---
type: wiki
sourcecode: projects/MAGPIE_Server/scripts/pull_log.ps1
version: 2026 07 02
description: Remote log pulling and cleanup utility for MAGPIE GCP VM.
---

# Remote Log Pull Utility

The `pull_log.ps1` utility is a PowerShell script designed to automate the retrieval, filtering, and optional cleanup of remote log files from the MAGPIE GCP virtual machine.

## Overview

The tool allows developers to pull specific logs based on level and date, and optionally delete them from the remote server once they have been successfully retrieved locally.

## Key Features

- **IAP Tunnel Optimization**: Specifically configured with `-n` and `-o BatchMode=yes` to prevent hangs during SSH/SCP operations over Google Cloud's Identity-Aware Proxy.
- **Flexible Filtering**: Supports filtering by log level (`-Lvl`) and date ranges (`-From`, `-To`).
- **Remote Cleanup**: The `-Del` switch enables the deletion of successfully pulled logs from the remote server.
- **Dry Run Mode**: The `-DryRun` switch allows for remote-only cleanup by marking files as "pulled" without actually transferring them.

## Documentation

For detailed usage instructions, parameter descriptions, and command examples, refer to the official readme:
[projects/MAGPIE_Server/scripts/pull_log_readme.md](projects/MAGPIE_Server/scripts/pull_log_readme.md)

## Technical Details

- **Language**: PowerShell
- **Remote Target**: `magpie-gcp`
- **Local Storage**: `tmp/MAGPIE_Server/logs`
- **Regex Pattern**: `^([a-zA-Z_]+)(\d{8})?\.log$`
