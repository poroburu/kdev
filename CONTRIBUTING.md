# Contributing

Write-path for parser work is [`kparser2`](kparser2/). Write-path for live capture is [`kpacket2`](kpacket2/).

- **GitHub Issues** on the child that owns the change = open work and decisions. Close when decided.
- **Git** = facts that would otherwise lie (architecture, runbooks, evidence). One canonical file; pointers elsewhere.
- **PRs** preferred for decoder, wire-contract, and plugin runtime changes. Direct push to `main` is allowed on first-party children when you own them.

After changing a submodule, bump the parent pin ([docs/pin-bump.md](docs/pin-bump.md)).

## Tracking

GitHub Issues on the child that owns the change hold open work and decisions.

- Before starting, pull with submodules, then read the issue, its comments, and its board status. In Progress means claimed; pick another unless the user says otherwise.
- On start and when you finish or pause an issue, comment and set status. Close an issue with a commit keyword only when the commit finishes it. Standing contracts stay open. Close when decided; pausing does not close an issue.
- Continue through dependency-ready, unclaimed issues within the user's authorized scope without asking again after each completion. Completing one issue is a checkpoint, not a turn boundary. Keep one actively claimed issue per harness at a time; commit, verify, report evidence, and bump applicable pins before switching. Do not expand into unrelated backlog work.
- If an issue is blocked, record the blocker and committed handoff, then continue independent authorized work when available. Stop when the requested scope is complete, the user asks to stop, an actual blocker prevents all further authorized progress, or an execution/usage limit requires a handoff. When the same step fails twice, stop repeating it unchanged: diagnose, change approach, or move to independent authorized work.
- Use durable checkpoints to manage usage limits rather than an issue-count limit. Before a limit or interruption, commit pending work without falsely closing the issue and record commits, verification, remaining steps, ownership, and blockers. Do not leave a paused issue's edits uncommitted.
- If board fields cannot be accessed, say so and do not claim a status update. Check issue comments for ownership; a fresh issue or clear unclaimed comments may establish safe ownership. Do not take an issue whose claim is uncertain merely because the board is unavailable.
