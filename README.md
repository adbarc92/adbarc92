## Alex Barclay

Senior software engineer in Denver. By day: payments features for **GarminPay iOS**
(Swift/SwiftUI), where the edge cases carry financial consequences — before that, primary
engineer on a hardware-connected Android app streaming live GPS telemetry. Nights and
weekends: **agentic developer infrastructure**.

### What I'm building

- **[command-center](https://github.com/adbarc92/command-center)** — Rust control plane
  (tokio, axum, SQLite) supervising containerized coding agents: a reconcile loop over
  authoritative state, WebSocket streaming to thin renderers, durable recovery across
  restarts
- **[reqdrive](https://github.com/adbarc92/reqdrive)** — written spec → PRD →
  deterministic story-by-story implementation → draft PR unless the story set is
  complete and the test suite passes, with a validation checklist and verification
  table in the body
- **[appforge](https://github.com/adbarc92/appforge)** — multi-agent orchestration on
  the Model Context Protocol: an MCP state server, a six-phase dependency graph, and
  human approval gates
- **[mcp-browser-bridge](https://github.com/adbarc92/mcp-browser-bridge)** — MCP server
  giving AI coding assistants direct control of a real browser (navigate, click, fill
  forms, run JS, capture screenshots); published on npm
- **[halyard](https://github.com/adbarc92/halyard)** — event-driven release state
  machine for multi-platform launches; transitions, idempotence, and fail-safe paths
  under test

The common thread: agent systems where correctness is **enforced, not asserted** —
approval gates, fail-closed defaults, deterministic selection, verification tables.

### Elsewhere

**[tenzy.app](https://tenzy.app)** — a learning app built around matrix study guides
with FSRS scheduling (React Native + Expo).

📫 [linkedin.com/in/alex-barclay](https://linkedin.com/in/alex-barclay) ·
adb92.works@gmail.com
