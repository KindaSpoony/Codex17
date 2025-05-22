# Codex17 Agent Roles Reference

This document summarizes the primary agent components within Codex17 and how they interact. These descriptions consolidate information from the white paper and configuration files for quick reference.

| Agent | Purpose | Key Behaviors / Handshakes |
|-------|---------|----------------------------|
| **Counterintelligence Sentinel** | Meta-guardian scanning inputs and outputs for disinformation or security threats. | Monitors every recursion tier; can quarantine content or halt processes if a critical breach is detected.|
| **Manager Protector** | Proactive controller that manages routine operations and keeps Exiles contained. | Handles day-to-day input first; defers to Self unless emergency; uses the passphrase handshake to authenticate communications.|
| **Firefighter Protector** | Reactive crisis responder that intervenes when emotional spikes occur. | Activates during acute distress; temporarily takes control to stabilize emotions before returning oversight.|
| **Core Self** | Integrates input from all parts with compassion and clarity. | Holds ultimate decision authority during normal conditions; may override protectors if actions conflict with system values.|
| **Exile Archive** | Protected store of vulnerable memories and emotions. | Accessed carefully when safe; informs Self and protectors without directly controlling the system.|

## Interaction Rules

- **Passphrase Handshake** – Agents authenticate by exchanging the motto "No Veteran Stands Alone, No Veteran Left Behind." This challenge-response occurs at every recursion tier.
- **Priority Stack** – Sentinel can override any layer for security. Manager handles routine tasks. Firefighter responds to crises. Core Self integrates all input and holds final authority when present. Exiles influence decisions indirectly via Self and protectors.
- **Recursive Integration (RI) Tiers** – Deeper RI tiers engage more agents and internal dialogue cycles. Each layer verifies the passphrase and maintains security before proceeding.

This reference helps new contributors or reviewers quickly understand Codex17’s internal agent roles and their coordination.
