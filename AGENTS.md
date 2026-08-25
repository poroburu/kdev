# Agent notes

Follow [CONTRIBUTING.md](CONTRIBUTING.md).

- GitHub Issues on the owning child hold open work and decisions. Close the issue when decided.
- Git holds facts. Do not spray a verdict across parent README and child docs.
- Parent `kdev` mostly pins submodules. Edit the child that owns the fact, then bump the pin.
- PRs preferred for runtime and wire-contract changes. Direct push to `main` is allowed on first-party children.
- Native win32 has no agent filesystem sandbox. Request unsandboxed Shell (`required_permissions: ["all"]`) and continue; do not abort or move this stack to Remote-WSL. See `.cursor/rules/windows-shell.mdc`.
