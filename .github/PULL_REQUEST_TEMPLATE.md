## Summary

Describe the problem, the proposed change, and any user-visible effect.

## Validation

- [ ] Ran `bash -n` on all shell scripts
- [ ] Ran ShellCheck on all shell scripts
- [ ] Ran `git diff --check`
- [ ] Added or updated tests/documentation where appropriate

## Compatibility

- [ ] Clean installation still works, or installation is not affected
- [ ] Upgrade from the latest release still works, or upgrade is not affected
- [ ] Runtime installation path remains `/srv/GREX`
- [ ] Management command remains `grex`
- [ ] systemd service name remains `gre-tunnel`
- [ ] `/etc/gre-tunnel.conf` remains compatible and is preserved
- [ ] Default `grex` tunnel interface and `GREX-*` iptables chains are preserved
- [ ] Migration update fallback from `runovelhq/grex` to
      `AlirezaSayyari/GREX` remains functional

## Additional notes

Include logs with secrets and identifying information removed, rollout risks,
or follow-up work.
