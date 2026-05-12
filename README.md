# EverMe CLI

[![npm](https://img.shields.io/npm/v/@everme/cli?label=npm)](https://www.npmjs.com/package/@everme/cli)
[![GitHub release](https://img.shields.io/github/v/release/alwaysday1/everme?include_prereleases)](https://github.com/alwaysday1/everme/releases)

**EverMe CLI** (`evercli`) — cloud-memory CLI for AI Agents such as Claude Code and OpenClaw. Installs the EverMe MCP plugin across AI Agents and orchestrates cold-start memory imports.

## Install

### Via npm (recommended)

```bash
npm install -g @everme/cli@beta
```

The npm wrapper downloads the platform-native `evercli` binary on first use and verifies its SHA-256 checksum.

### Manual download

Download the archive for your platform from [Releases](https://github.com/alwaysday1/everme/releases), verify against `sha256sums.txt`, unpack, and place `evercli` somewhere on your `PATH`.

| Platform | Asset |
|---|---|
| macOS (Apple Silicon) | `evercli_darwin_arm64.tar.gz` |
| macOS (Intel) | `evercli_darwin_amd64.tar.gz` |
| Linux (x86_64) | `evercli_linux_amd64.tar.gz` |
| Linux (ARM64) | `evercli_linux_arm64.tar.gz` |
| Windows (x86_64) | `evercli_windows_amd64.zip` |
| Windows (ARM64) | `evercli_windows_arm64.zip` |

## Quickstart

```bash
evercli auth login                  # log in via Device Flow
evercli plugin install claude-code  # or `openclaw`
evercli import run                  # optional: cold-start memory upload
evercli doctor                      # health check
evercli --version                   # build identity
```

## Command surface

| Command | Purpose |
|---|---|
| `auth` | login / logout / status / me |
| `plugin` | list / install (Claude Code, OpenClaw) |
| `import` | scan / run (cold-start memory upload) |
| `doctor` | connectivity + credential health check |

For AI-Agent / CI invocations pass `--no-prompt --format json` to get structured envelopes instead of interactive prompts.

## Release channels

- **`@everme/cli@beta`** — pre-release builds
- **`@everme/cli@latest`** — stable releases

Tagged as `cli/v<MAJOR>.<MINOR>.<PATCH>[-prerelease]`.

## Support

- Website: <https://everme.ai>
- Issues / bug reports: <https://github.com/alwaysday1/everme/issues>

## License

Distributed under the [Apache License 2.0](LICENSE).
