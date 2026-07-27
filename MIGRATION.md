# Repository migration

GREX is moving from `AlirezaSayyari/GREX` to `runovelhq/grex`. New installs
and update checks use `runovelhq/grex` as their primary source. The previous
repository remains an update fallback during the migration period.

## Impact on existing users

Existing installations remain compatible. The migration changes where GREX is
downloaded from; it does not rename installed paths, commands, configuration,
or services.

## Recommended upgrade path

Run the normal upgrade command:

```bash
sudo grex upgrade
```

The manager checks `runovelhq/grex` first and falls back to
`AlirezaSayyari/GREX` if the new repository is unavailable or has no usable
release or tag.

## Recovery if upgrade fails

For an older or broken installation, rerun the bootstrap installer from the new
repository:

```bash
curl -fsSL https://raw.githubusercontent.com/runovelhq/grex/main/bootstrap.sh | sudo bash
```

## What does not change

- Runtime installation path: `/srv/GREX`
- Configuration file: `/etc/gre-tunnel.conf`
- Management command: `sudo grex`
- systemd service name: `gre-tunnel`

## What changes

- The primary source repository for installation and updates becomes
  `runovelhq/grex`.

## Post-upgrade checklist

```bash
sudo grex version
sudo grex health
sudo grex check
```
