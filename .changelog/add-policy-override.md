---
mpp: minor
---

Added `FeePayerPolicyOverride` so servers can tune fee-sponsor transaction limits per call via `ChargeMethod::with_fee_payer_policy_override()`. The override supports five fields: `max_gas` (gas-limit ceiling), `max_fee_per_gas` (EIP-1559 fee-per-gas ceiling), `max_priority_fee_per_gas` (priority-fee ceiling), `max_total_fee` (gas × fee ceiling), and `max_validity_window_seconds` (how far ahead `valid_before` may be set). All fields are optional and fall back to safe global defaults.