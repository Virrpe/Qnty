# Project Boundaries

## Target durable role

Qnty is the intended downstream consumer and acceptance boundary for an earned
immutable handoff or promotion-candidate artifact. Its durable target role is:

- downstream acceptance / rejection
- deterministic replay
- accounting
- execution realism
- paper controls
- shadow controls
- live or external-effect controls only when separately authorized

`QNTY_HANDOFF_CREATED` is not `QNTY_HANDOFF_ACCEPTED`. Qnty's acceptance
decision is independent, immutable, and does not rewrite QntyLab's research
history or source artifact.

## Current implementation and overlap classification

The existing research, replay, and falsification machinery is preserved. This
architecture alignment does not delete, rename, or refactor it. Based on the
current code and contracts, the overlap is classified as:

- `STILL_ACTIVE_ARCHITECTURE` — deterministic replay, accounting, execution
  realism, paper controls, and shadow controls already present in Qnty.
- `INTENTIONAL_DEFENSE_IN_DEPTH` — downstream checks that independently replay
  or falsify an incoming artifact before accepting it.
- `TRANSITIONAL_RESPONSIBILITY` — upstream-style research and falsification
  workflows that remain co-located until a separately authorized migration or
  ownership decision.
- `LEGACY_COMPATIBILITY` — historical integration and protocol surfaces kept
  for compatibility and evidence continuity.

These labels describe current implementation versus target ownership; they do
not authorize a migration, acceptance, execution, or runtime transition.

## What does NOT belong to Qnty

- QntyLab's upstream hypothesis registration, scientific contract ownership,
  research ledger, Jigsaw evidence ownership, survivor qualification, or
  promotion-candidate construction.
- **Franken** is a separate paper-flow / reconciliation shell.
- **THT0** is a separate strategy stack.

## Franken references in this repo

You will see `Franken` mentioned in:

- `quantbot/experiment/calibration.py` — data structures for importing Franken reconciliation records
- `quantbot/experiment/index.py` — promotion contract logic that references external Franken calibration data
- Tests that verify Franken calibration ingestion
- Historical verdicts and plans that mention Franken as a separate system

These are **legacy / integration-boundary artifacts**. They exist to define the interface between Qnty and Franken, but they are not claims that Franken is part of Qnty or that Qnty requires Franken to function.

## THT0 references in this repo

You will see `THT0` mentioned in:

- Historical plans and verdicts that evaluated THT0 strategy variants
- Comments noting where THT0 adapters were excluded

These are historical research artifacts. THT0 is a separate strategy stack and is not part of the public Qnty v0.1 research preview.
