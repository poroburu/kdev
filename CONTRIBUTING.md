# Contributing

Write-path for parser work is [`kparser2`](kparser2/). Write-path for live capture is [`kpacket2`](kpacket2/).

- **GitHub Issues** on the child that owns the change = open work and decisions. Close when decided.
- **Git** = facts that would otherwise lie (architecture, runbooks, evidence). One canonical file; pointers elsewhere.
- **PRs** preferred for decoder, wire-contract, and plugin runtime changes. Direct push to `main` is allowed on first-party children when you own them.

After changing a submodule, bump the parent pin ([docs/pin-bump.md](docs/pin-bump.md)).
