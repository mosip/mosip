# MOSIP Advisories

This directory hosts all official advisories published by MOSIP for adopters, system integrators and the community.

## Advisory types

| Type | Directory | Description |
|------|-----------|-------------|
| Security | [`security/`](security/README.md) | Vulnerabilities, security fixes and mitigations affecting MOSIP modules. |
| General | [`general/`](general/README.md) | Non-security advisories: critical bugs, deprecations, end-of-support notices, upgrade/migration guidance, dependency or infrastructure notices. |

## Naming convention

Every advisory has a unique ID that is also its file name:

```
MOSIP-<TYPE>-<SEVERITY>-<YEAR>-<SEQUENCE>.md
```

| Part | Values | Notes |
|------|--------|-------|
| `TYPE` | `SEC` (security), `GEN` (general) | Determines the directory the advisory lives in. |
| `SEVERITY` | `SEV1`, `SEV2`, `SEV3`, `SEV4` | See [Severity levels](#severity-levels). |
| `YEAR` | e.g. `2026` | Year the advisory was first published. |
| `SEQUENCE` | `001`, `002`, … | Three-digit running number per type per year. Resets each year. Independent of severity. |

Examples: `MOSIP-SEC-SEV1-2026-001`, `MOSIP-GEN-SEV2-2026-002`.

> The ID is permanent. If the severity of an advisory is later revised, keep the original ID and record the change in the advisory's **Revision history**.

## Severity levels

| Level | Meaning | Expected adopter action |
|-------|---------|-------------------------|
| **SEV1 – Critical** | Severe impact on security, data integrity or availability of production deployments; exploitation or failure is likely. | Act immediately. |
| **SEV2 – High** | Significant impact on a core function or a vulnerability with notable risk. | Act at the earliest planned window. |
| **SEV3 – Medium** | Limited impact, workaround available, or requires uncommon configuration. | Plan for the next regular upgrade. |
| **SEV4 – Low** | Minor impact or informational. | Act as convenient. |

For security advisories, the CVSS score (if assigned) should be stated in the advisory alongside the SEV level.

## Directory layout

```
advisories/
├── README.md                     # This file
├── security/                     # Security advisories (MOSIP-SEC-*)
├── general/                      # General advisories (MOSIP-GEN-*)
├── additionalfiles/<ADVISORY-ID>/  # Patches, scripts, configs, screenshots referenced by an advisory
└── templates/                    # Templates for new advisories
```

## Publishing a new advisory

1. Pick the next sequence number for the type and year from the index in [`security/README.md`](security/README.md) or [`general/README.md`](general/README.md).
2. Copy [`templates/general-advisory-template.md`](templates/general-advisory-template.md) into the right directory as `<ADVISORY-ID>.md` and fill in every section.
3. If the advisory needs supporting files, create `additionalfiles/<ADVISORY-ID>/` and link to the files using relative paths.
4. Add a row for the advisory to the index table in the type's `README.md`.
5. Raise a pull request for review.

> **Security issues must not be disclosed publicly before a fix or mitigation is available.** Do not open public issues or pull requests describing unpatched vulnerabilities. See [`security/README.md`](security/README.md) for how to report them.
