# Contributing

## Evidence-first contributions

Qnty holds its own work to a falsification-first standard. Contributions should be evidence-first:

- Claims must be proportionate to evidence.
- Provide artifacts, receipts, or reproducible steps.
- State uncertainty honestly when evidence is incomplete.

## No alpha or profitability claims without artifacts

Do not claim a strategy is profitable, has edge, or is ready for deployment without:

- Clear backtest or validation artifacts
- Explicit caveats and limitations
- Acknowledgment of what remains unknown

## No live trading additions in normal PRs

Live trading integrations, exchange connectors, or capital-deployment features are out of scope for normal pull requests. Discuss in an issue first if you believe there is a strong research reason.

## Tests and smoke checks

- Include or update tests for code changes.
- Ensure `./scripts/release_smoke.sh` passes before opening a PR.
- Prefer deterministic tests that can be reproduced by others.

## Keep Qnty separate from Franken / THT0

- Qnty's target durable role is the downstream acceptance, deterministic
  replay, accounting, execution-realism, paper-control, and shadow-control side
  of the Qnty ecosystem.
- Qnty's current implementation also contains research and falsification
  machinery. It is preserved as active, defensive, transitional, and/or
  legacy-compatible capability until separately classified or migrated, and its
  presence does not make Qnty the durable owner of upstream research.
- Franken is a separate paper-flow / reconciliation shell.
- THT0 is a separate strategy stack.

Do not blur these boundaries in documentation or code comments. Do not describe
Qnty as already implementing downstream handoff acceptance, and do not describe
it as a live-execution system. See
[docs/PROJECT_BOUNDARIES.md](docs/PROJECT_BOUNDARIES.md) for the full ownership
and overlap classification.
