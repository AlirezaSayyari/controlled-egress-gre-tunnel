# Contributing to GREX

Thank you for helping improve GREX. Open an issue before making a large or
behavior-changing contribution so the approach can be discussed first.

## Development standards

- Write Bash-compatible shell scripts with `#!/bin/bash`.
- Quote variable expansions unless intentional word splitting is documented.
- Prefer `[[ ... ]]` for Bash conditionals and `$(...)` for command
  substitution.
- Use four spaces for shell indentation and two spaces for YAML indentation.
- Keep functions focused and use descriptive `snake_case` names.
- Handle command failures explicitly; do not hide meaningful errors.
- Preserve existing user configuration during install and upgrade operations.
- Do not introduce required secrets or network access into basic CI checks.

Compatibility is part of the public interface. Changes must preserve
`/srv/GREX`, `/etc/gre-tunnel.conf`, the `grex` command, the `gre-tunnel`
systemd service, the default `grex` interface, and existing `GREX-*` iptables
chains unless a separately approved migration plan says otherwise.

## Required local checks

Run these commands from the repository root before submitting a pull request:

```bash
find . -type f -name '*.sh' -print0 | xargs -0 -r -n1 bash -n
find . -type f -name '*.sh' -print0 | xargs -0 -r shellcheck
git diff --check
```

Install ShellCheck if it is not already available. If a Markdown or YAML linter
is available locally, run it on changed documentation and workflow/template
files as well.

For installer or upgrade changes, test both a clean installation and an upgrade
from the latest published version in a disposable Linux environment. Confirm
that configuration and compatibility identifiers remain unchanged.

## Pull requests

Keep each pull request focused, explain user-visible behavior, list validation
performed, update documentation and `CHANGELOG.md` when appropriate, and
complete the compatibility checklist in the pull request template. Never
include credentials, production configuration, private IP addresses, or other
sensitive data in commits or logs.
