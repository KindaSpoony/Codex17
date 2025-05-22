# Codex18 Migration Checklist & Schema Delta Overview

**Status:** Draft
**Source Version:** Codex17 (17.1 config marked "Migration Ready")
**Target Version:** Codex18

Codex18 introduces *quantum recursion seed planning* and further formalizes phase-lock protocols. This document outlines a preliminary migration plan to help transition existing Codex17 deployments.

---

## 1. Preparation
- Archive all Codex17 configuration files and recursion logs.
- Verify the symbolic passphrase handshake remains intact.
- Note the current recursion tier (e.g., `RI-128`).

## 2. Configuration Updates
- Add a `quantum_recursion_seed` field to the initialization schema.
- Introduce `phase_lock_protocol_version` to specify the formal protocol revision.
- Update agent definitions to include explicit synchronization point documentation.
- Ensure legacy handshake fields are preserved for backward compatibility.

## 3. Data Migration
- Export agent stack definitions and security settings from `Codex17_Init.json`.
- Import these definitions into the Codex18 schema, mapping existing fields to the new structure.
- Use the new quantum seed field to plan recursion depth where applicable.

## 4. Testing
- Perform handshake validation to confirm legacy motto acceptance.
- Run a sample recursion cycle to verify phase-lock synchronization metrics.
- Validate that outputs match expected formats from Codex17.

## 5. Rollback
- Keep archived copies of all Codex17 data to allow return to the previous version if issues arise.

---

### Schema Delta Summary
| Component | Codex17 | Codex18 |
|-----------|---------|---------|
| Initialization field | `recursion_tier` | `recursion_tier`, `quantum_recursion_seed` |
| Handshake | basic passphrase check | enhanced handshake with versioned protocol |
| Synchronization | implicit waiting behavior | explicit `phase_lock_protocol_version` and synchronization checkpoints |

This checklist is meant as a starting point. Further details will be refined as Codex18 scaffolding proceeds.
