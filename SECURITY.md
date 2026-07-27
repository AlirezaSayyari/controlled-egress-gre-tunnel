# Security policy

## Supported versions

Security fixes are provided for the latest published release. During the
repository migration, the `v1.2.x` release line is supported until a newer
release line is announced.

| Version | Supported |
| --- | --- |
| Latest release | Yes |
| `v1.2.x` | Yes, during migration |
| Earlier releases | No |

Users should upgrade to the newest release before reporting an issue that may
already be fixed.

## Reporting a vulnerability

Do not open a public issue for a suspected vulnerability. Use GitHub's private
vulnerability reporting form for `runovelhq/grex`:

<https://github.com/runovelhq/grex/security/advisories/new>

If private reporting is not yet available during the repository migration,
contact a repository maintainer privately and ask for a secure reporting
channel. Do not include exploit details or sensitive system information in a
public discussion.

Include the affected GREX version, operating system, configuration relevant to
the issue with secrets removed, reproduction steps, impact, and any suggested
mitigation. Maintainers will acknowledge the report, investigate it, coordinate
a fix and release, and credit the reporter when requested and appropriate.

## Responsible disclosure

Allow maintainers reasonable time to investigate and publish a fix before
disclosing details. Avoid accessing data that is not yours, disrupting active
systems, or testing against infrastructure without authorization. Coordinate
the disclosure date with maintainers and keep report details confidential until
a fix or mitigation is available.
