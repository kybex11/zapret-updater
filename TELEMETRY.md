# zapret-stats

Anonymous opt-in telemetry from Zapret clients (strategy wins from Find best).

## Setup

1. Create a **fine-grained PAT** with `Issues: Write` on this repo only.
2. When building the client:

```bat
set ZAPRET_TELEMETRY_TOKEN=github_pat_...
cargo build --release
```

Or drop the token into the installed app as `utils/telemetry.token` (one line).

3. Create label `telemetry` on this repo (optional; API may auto-create if allowed).

Clients never send IPs, hostnames, or lists — only `{v, os, strategy, event}`.
