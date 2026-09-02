# Security Policy

Report security vulnerabilities privately through the methods below.

See the [NautilusTrader security policies](https://nautilustrader.io/security/) for the complete
organization-wide policy set. The
[Responsible Disclosure Policy](https://nautilustrader.io/security/responsible-disclosure/)
provides the safe-harbor and privacy terms for reports covered here.

## Scope

This policy covers:

- NautilusTrader open-source software and official repositories.
- Nautech Systems websites (nautilustrader.io).

Third-party services, exchanges, and data providers are excluded.

## Reporting a vulnerability

**Preferred method:** [GitHub Security Advisories](https://github.com/nautechsystems/nautilus_agents/security/advisories/new)

This allows private disclosure and coordination before public release. You'll receive credit in the
security advisory and release notes.

**Alternative:** Email <security@nautechsystems.io>

For sensitive reports via email, you may request our PGP key for encrypted communication.

Please include: vulnerability description, reproduction steps, affected versions, and
suggested remediation if available.

## Response timeline

We commit to:

- **Initial response**: Within 48 hours of report submission.
- **Status update**: Within 7 days with initial assessment.
- **Fix timeline**: Critical vulnerabilities patched within 30 days; other issues within 90 days.
- **Coordinated disclosure**: We'll work with you to agree on a public disclosure date.

## Responsible disclosure

We encourage responsible disclosure of any security vulnerabilities you may discover. When reporting,
we ask that you:

- Do not publicly disclose the vulnerability before a fix is available.
- Only exploit the issue to the extent necessary to demonstrate it.
- Do not access unauthorized data or disrupt systems.
- Comply with all applicable laws.

We will acknowledge your contribution in our security advisories and release notes unless you
prefer to remain anonymous.

## Supported versions

We support only the latest released version of `nautilus-agents`. Older releases may lack fixes
available in a later release or in the repository.

## Bug bounty program

At this time, we do not have a formal bug bounty program. We appreciate any efforts to help us improve
the security of our platform and will do our best to properly recognize and credit your contributions.

## Security infrastructure

`nautilus-agents` uses multiple controls against supply-chain attacks and vulnerabilities:

- **Dependency auditing**: `cargo-audit` scans advisories, `cargo-deny` enforces dependency policy,
  and `cargo-vet` verifies supply-chain provenance.
- **Pre-commit security**: Gitleaks credential screening, private key detection, and
  Unicode control character detection.
- **License compliance**: `cargo-deny` enforces the repository's dependency license policy.
- **Source restrictions**: Rust packages sourced exclusively from crates.io; git dependencies and
  unknown registries are prohibited.

See the [Dependency and Supply Chain Security
Policy](https://nautilustrader.io/security/supply-chain/) for the organization-wide controls.
