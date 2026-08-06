# Security policy

Nexus Labs treats security reports as evidence-sensitive engineering work. Do
not disclose suspected vulnerabilities, credentials, personal data, or exploit
details in a public issue, discussion, or pull request.

## Supported versions

Unless an individual repository states otherwise, security fixes target:

- The current default branch.
- Releases explicitly marked as supported by that repository.

Development branches, archived repositories, prototypes, and historical tags
may not receive security updates.

## Reporting a vulnerability

Use the affected repository's private reporting channel:

1. Open the repository's **Security** tab.
2. Select **Advisories**.
3. Choose **Report a vulnerability** or create a private draft advisory.

If private vulnerability reporting is unavailable, open an issue in
[`nexuslabs-tech/.github`](https://github.com/nexuslabs-tech/.github/issues/new)
that contains no vulnerability details and requests a private reporting channel.

Include, when possible:

- The affected repository, component, branch, or release.
- A concise description of the impact.
- Reproduction steps or a minimal proof of concept.
- Relevant logs or traces with secrets and personal data removed.
- Known mitigations or environmental requirements.
- Whether the issue is already public or being actively exploited.

## What to expect

We will validate the report, assess severity and affected versions, and
coordinate remediation and disclosure based on the available evidence. Response
times depend on impact and project status; this policy does not promise a fixed
service-level agreement or bounty.

Please allow time for investigation before publishing details. We will credit
reporters when requested and when coordinated disclosure is appropriate.
