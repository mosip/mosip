# MOSIP Advisories

## 1\. Overview

MOSIP publishes advisories to inform adopters, system integrators, partners, and the broader community about important security concerns, product-related issues, operational risks, and other developments that may require attention or action.

Advisories provide information on affected components or versions, potential impact, recommended actions, available fixes, and workarounds, where applicable.

This directory serves as the **central repository for official MOSIP advisories**, providing a consistent and accessible reference for stakeholders to stay informed and take appropriate action.

## 2\. Advisory Types
MOSIP publishes two categories of advisories:

| Type | Directory | Description |
|------|-----------|-------------|
| Security | [`security/`](security/README.md) | Security vulnerabilities, risks, affected product versions, fixes, mitigations, and other security-related concerns requiring attention or action. |
| General | [`general/`](general/README.md) | Important non-security updates, critical functional issues, compatibility concerns, configuration changes, deprecations, end-of-support notices, and operational or migration guidance. |

### Security Advisories

Security advisories are published through GitHub's [Security](https://github.com/mosip/mosip/security) → [Advisories](https://github.com/mosip/mosip/security/advisories) functionality, using the standard GitHub Security Advisory format.
Each published security advisory is also referenced in the [MOSIP Security Advisory Index](https://github.com/mosip/mosip/blob/master/advisories/security/README.md), which links to the original GitHub Security Advisory as the authoritative source of information.

### General Advisories

General advisories are published as dedicated pages in the [MOSIP General Advisory Index](https://github.com/mosip/mosip/blob/master/advisories/general/README.md), following a standard advisory format.
Advisories are published as and when required, based on the nature, impact, and relevance of the concern.

## 3\. Directory Structure

MOSIP advisories are organised into the following directories for easy access and reference:

```text
advisories/
├── README.md            # Overview and advisory index
├── security/            # Published security advisory references
├── general/             # Published general advisories
├── additionalfiles/     # Supporting files referenced by advisories
└── templates/           # Standard advisory templates
```

Security advisories link to the original GitHub Security Advisory, which serves as the authoritative source of information.

General advisories are published as dedicated Markdown pages within the `general/` directory.

## 4\. Advisory Severity Levels

MOSIP classifies advisories based on their severity and potential impact on affected deployments.

| Level | Description | Recommended Adopter Action |
| --- | --- | --- |
| **SEV1 – Critical** | Severe impact on security, data integrity, or availability of production deployments. | Take immediate action. |
| **SEV2 – High** | Significant impact on core functionality or a security concern presenting notable risk. | Prioritise remediation at the earliest. |
| **SEV3 – Medium** | Limited or moderate impact, potentially with available workarounds or specific conditions for occurrence. | Plan remediation as part of the regular maintenance or upgrade cycle, considering deployment-specific risks. |
| **SEV4 – Low** | Minor impact or informational guidance requiring limited action. | Review and act as applicable. |

For security advisories, CVSS scores may also be provided, where applicable.
The severity classification and recommended actions for each advisory should be considered alongside the specific risks and operational context of the affected deployment.

## 5\. Advisory Identification and Naming Convention

Each MOSIP advisory is assigned a unique reference identifier to support identification, tracking, and future reference.
The standard naming convention is: `MOSIP-<TYPE>-<SEVERITY>-<YEAR>-<SEQUENCE>`

| Component | Description |
| --- | --- |
| **TYPE** | `SEC` – Security Advisory; `GEN` – General Advisory |
| **SEVERITY** | `SEV1`, `SEV2`, `SEV3`, or `SEV4`, based on the severity classification |
| **YEAR** | Calendar year in which the advisory is first published |
| **SEQUENCE** | Three-digit sequence number, starting from `001` |

Examples:

-   `MOSIP-SEC-SEV1-2026-001`
-   `MOSIP-GEN-SEV2-2026-001`

**Note:** Advisory sequence numbers reset at the beginning of each calendar year, with separate sequences maintained for each advisory type and severity level.

Once assigned, an advisory ID remains unchanged, even if the severity classification is subsequently revised. Any significant changes will be reflected in the advisory's revision history, where applicable.
Security advisories may additionally have GitHub-generated GHSA identifiers and CVE identifiers, where applicable.

## 6\. Accessing Advisories and Staying Informed

All published MOSIP advisories can be accessed through the following resources:

| Resource | Purpose |
| --- | --- |
| [Security Advisory Index](https://github.com/mosip/mosip/blob/master/advisories/security/README.md) | Browse published MOSIP security advisories. |
| [General Advisory Index](https://github.com/mosip/mosip/blob/master/advisories/general/README.md) | Browse published MOSIP general advisories. |
| [GitHub Security Advisories](https://github.com/mosip/mosip/security/advisories) | Access detailed security advisories published through GitHub. |
| [MOSIP Community Forum](https://community.mosip.io/) | Follow community announcements and relevant updates. |

Adopters and partners are encouraged to review published advisories periodically and assess their applicability to their respective MOSIP deployments.
To receive notifications of new security advisories, users may subscribe to the relevant repository's GitHub security advisory notifications.

## 7\. Advisory Updates and Maintenance

MOSIP may update published advisories as additional information, fixes, mitigations, or recommendations become available.
Where applicable, advisories will include relevant references, affected versions, recommended actions, and revision details.
Stakeholders are encouraged to refer to the latest published version of an advisory before taking action.
For security advisories, the original GitHub Security Advisory remains the authoritative source of information.

## 8\. Reporting a Security Vulnerability

MOSIP welcomes responsible reporting of potential security vulnerabilities from community members, security researchers, adopters, and partners.
If you identify a potential security vulnerability in MOSIP, please report it confidentially through GitHub's private vulnerability reporting mechanism by following the steps below, or email us at security-team@mosip.io.

1.  Navigate to the [MOSIP GitHub repository](https://github.com/mosip/mosip).
2.  Open [Security and quality](https://github.com/mosip/mosip/security) → [Advisories](https://github.com/mosip/mosip/security/advisories).
3.  Select [Report a vulnerability](https://github.com/mosip/mosip/security/advisories/new).
4.  Submit the details of the potential vulnerability through GitHub's private reporting mechanism.

Reports may include the affected components or versions, a description of the issue, potential impact, and steps to reproduce it, where available.

MOSIP will assess reported vulnerabilities and determine the appropriate course of action. **Not every reported vulnerability will result in a published security advisory.** Where warranted, MOSIP may publish an advisory following its security assessment and coordinated disclosure process.

**Important:** Please do not disclose potential security vulnerabilities through public GitHub issues, pull requests, or discussion forums before they have been appropriately assessed.

For detailed reporting instructions, scope, and disclosure practices, refer to the [**MOSIP Security Vulnerability Disclosure Policy - To be published shortly**](LINK-TO-BE-PUBLISHED-SECURITY-POLICY).

* * *

**MOSIP is committed to supporting secure, reliable, and sustainable deployments through timely communication of important advisories and responsible handling of reported security vulnerabilities.**

* * *
