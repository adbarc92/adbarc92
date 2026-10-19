## Alex Barclay

**Autonomous systems are easy to build and hard to trust. I work on the second problem.**

I build the layer that supervises, coordinates, and verifies systems that run unattended —
control planes that hold authoritative state, reconcile loops that correct drift, and gates
that fail closed rather than ship.

Most of my professional work has been where software meets hardware in the field. I was
primary engineer on the operator-facing Android client for a **handheld-and-collar GPS
system** — the console a handler actually watches — ingesting and rendering **11M+ data
points of live telemetry** from distributed devices over intermittent links, with a
production Mapbox integration putting live positions on an interactive map. I'm now on
**GarminPay iOS** (Swift/SwiftUI), where the edge cases carry financial consequences.

Senior software engineer in Denver. Nights and weekends: **fleet and verification
infrastructure**.

### Supervision & fleet state

- **[command-center](https://github.com/adbarc92/command-center)** — a Rust control plane
  (tokio, axum, SQLite) that holds authoritative state over a fleet of containerized agents and
  drives them toward it through a reconcile loop. The reconciler is tested for restraint as hard
  as for reach: strays reaped, stranded units halted, healthy live work provably untouched. The
  event log cannot be double-written no matter how often a write retries, and in-flight work
  rehydrates after a restart.

- **[appforge](https://github.com/adbarc92/appforge)** — multi-agent orchestration on the Model
  Context Protocol: an MCP state server, a six-phase dependency graph, independent worker
  processes that claim work without collision, human approval gates, and automatic budget control.

### Verification & enforcement

- **[reqdrive](https://github.com/adbarc92/reqdrive)** — a requirements-to-PR pipeline that
  refuses to bluff. Story selection is deterministic by construction — a pure function of the PRD,
  not an agent decision. Pull requests arrive as drafts unless every piece of positive evidence is
  in hand. A frozen test oracle catches any attempt to weaken or drop a test, and a CI self-test
  proves, against a planted violation, that the gate still fires. Requirement text is treated as
  hostile until screened.

- **[halyard](https://github.com/adbarc92/halyard)** — multi-platform releases modeled as a
  durable, event-driven state machine: idempotent transitions, gates that end a release instead of
  deploying it, and recovery from failed transitions under test.

- **[mcp-browser-bridge](https://github.com/adbarc92/mcp-browser-bridge)** — an MCP server giving
  AI assistants control of a real Chrome browser through a deliberately narrow doorway: exactly
  eleven tools, counted and closed, defended by a test that fails the moment a twelfth appears.

### How I work

Claims exist only when a command proves them. Every project above states what it has shown and
what it has not — readiness is a rung you earn, not a label you apply. No agent both sets the bar
and clears it: oracle, builder, and reviewer stay in separate contexts, because tests are the only
objective signal and review adds confidence rather than truth.

The common thread is correctness **enforced, not asserted** — approval gates, fail-closed
defaults, deterministic selection, reconcile loops that converge.

**Currently studying:** UL 4600, ISO 21448 (SOTIF), and IEC 62443 — the standards vocabulary of
assurance for autonomous and operational-technology systems.

📫 [linkedin.com/in/alex-barclay](https://linkedin.com/in/alex-barclay) ·
[alexanderdbarclay.com](https://alexanderdbarclay.com) · adb92.works@gmail.com
