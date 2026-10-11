# Security Policy

This policy explains how to report security vulnerabilities or sensitive-information exposures related to this repository. It is intended to support responsible reporting while protecting students, faculty, staff, maintainers, institutional systems, and the broader GitHub community.

Do not report security vulnerabilities, exposed credentials, or sensitive information through a public issue, discussion, pull request, commit, or comment.

## Table of Contents <!-- omit from toc -->

1. [Supported Versions](#supported-versions)
2. [Security Issues Covered by This Policy](#security-issues-covered-by-this-policy)
3. [Issues Not Covered by This Policy](#issues-not-covered-by-this-policy)
4. [Reporting a Vulnerability](#reporting-a-vulnerability)
5. [Information to Include](#information-to-include)
6. [Handling of Reports](#handling-of-reports)
7. [Responsible Testing](#responsible-testing)
8. [Exposed Credentials and Sensitive Information](#exposed-credentials-and-sensitive-information)
9. [Coordinated Disclosure](#coordinated-disclosure)
10. [Academic and Institutional Requirements](#academic-and-institutional-requirements)
11. [Provisional Status](#provisional-status)
12. [References](#references)

## Supported Versions

Security corrections are generally applied only to the current version of the authoritative repository.

| Repository version | Support status |
| ------------------ | -------------- |
| Default branch and current release | Supported |
| Earlier releases or inactive branches | Best effort |
| Archived versions | Not supported |
| Forks, student repositories, and personal copies | Not directly supported by the upstream maintainers |

If a vulnerability found in a copy or fork originated in the authoritative repository, report it to the maintainers of the authoritative repository.

## Security Issues Covered by This Policy

Examples of appropriate security reports include:

* Exposed passwords, access tokens, private keys, or other credentials
* Vulnerable repository scripts, applications, or configuration files
* GitHub Actions workflows with unsafe permissions or injection risks
* Dependencies with a vulnerability that affects repository functionality
* Instructions or automation that could expose personal, academic, or institutional information
* Unauthorized access to protected files, systems, or repository functions
* Unintended disclosure of nonpublic course, assessment, or student information
* Code that permits unintended command execution, privilege escalation, or data access
* Security controls that can be bypassed in a manner that creates a meaningful risk

A security weakness in an assignment, assessment, or automated test should be reported privately if public disclosure could expose answers, undermine an assessment, or enable academic misconduct.

## Issues Not Covered by This Policy

Use the repository’s ordinary support channels for:

* General questions about a course, assignment, or repository
* Installation, configuration, or troubleshooting assistance
* Broken links, typographical errors, or ordinary software defects
* Feature requests or suggested improvements
* Academic-integrity or conduct concerns
* Problems limited to a separately maintained third-party product or service

Repository support options are described in [SUPPORT.md](SUPPORT.md). Conduct concerns are addressed in [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

Vulnerabilities in GitHub itself should be reported through GitHub’s designated security-reporting process rather than to this repository.

## Reporting a Vulnerability

### Preferred Method

If private vulnerability reporting is enabled for this repository:

1. Open the repository’s **Security** or **Security and quality** area.
2. Select **Advisories**.
3. Select **Report a vulnerability**.
4. Complete the private report.

This method creates a private communication space where the reporter and repository maintainers can discuss the issue without exposing it publicly.

### Alternative Method

If private vulnerability reporting is unavailable, use an approved private institutional communication channel. Appropriate options may include:

* Privately contacting the course instructor through the learning management system
* Contacting a repository administrator through an established institutional channel
* Using the applicable institutional information-security or service-desk reporting process

Do not place vulnerability details in a public GitHub issue or discussion. Do not include working credentials, actual student records, or other sensitive data in a report.

## Information to Include

Provide enough information for maintainers to understand and reproduce the issue safely:

* A concise description of the vulnerability
* The affected file, component, workflow, version, branch, or release
* The potential security or privacy impact
* The conditions required to reproduce the issue
* Clear reproduction steps using synthetic or non-sensitive data
* A minimal proof of concept, when necessary and safe
* Relevant operating system, software, or environment information
* Any temporary mitigation or proposed correction
* Whether the issue has been disclosed to anyone else
* A safe method for maintainers to request additional information

Remove credentials, student information, private communications, and unrelated personal information before submitting the report.

## Handling of Reports

Repository maintainers will make a reasonable effort to:

1. Review the report.
2. Determine whether the issue is reproducible and within scope.
3. Assess its potential impact.
4. Identify an appropriate correction or mitigation.
5. Coordinate necessary communication with institutional or platform personnel.
6. Notify the reporter when the issue has been resolved or otherwise addressed, when practical.

Response and remediation times depend on the issue’s severity, complexity, available resources, academic calendar, and any required institutional review. This policy does not establish a guaranteed response time or service-level agreement.

Reports may be closed without remediation when an issue cannot be reproduced, is outside the repository’s control, presents no meaningful security impact, or concerns an unsupported version.

This repository does not offer a vulnerability-reward or bug-bounty program unless a separate written program explicitly states otherwise.

## Responsible Testing

This policy does not authorize security testing against GitHub, institutional systems, course platforms, third-party services, other users’ repositories, or devices that you do not own or have explicit permission to test.

Unless separately authorized in writing, do not:

* Access, modify, retain, or disclose another person’s data
* Use real credentials or attempt to determine whether exposed credentials remain valid
* Conduct automated scanning against institutional or third-party systems
* Perform denial-of-service, load, or resource-exhaustion testing
* Use social engineering, phishing, or impersonation
* Bypass authentication or access controls
* Introduce malware or persistent access
* Disrupt instruction, assessment, repository availability, or other services
* Test using student records, grades, or other regulated information

When possible, perform analysis in a local copy using synthetic data and an environment you control.

If you encounter sensitive information unintentionally, stop testing, avoid additional access, preserve only the minimum information needed to report the issue, and submit a private report promptly.

## Exposed Credentials and Sensitive Information

If you discover an exposed credential:

1. Do not use or test it.
2. Report it privately and promptly.
3. Identify its location without reproducing the complete secret.
4. If the credential belongs to you, revoke or rotate it immediately.
5. Follow applicable institutional incident-reporting requirements.

Deleting a secret from the current version of a file may not remove it from Git history, cached content, forks, logs, or prior workflow output. Revocation or rotation is therefore normally required.

## Coordinated Disclosure

Please allow repository maintainers a reasonable opportunity to investigate and address a reported vulnerability before disclosing it publicly.

The reporter and maintainers should coordinate:

* Whether public disclosure is appropriate
* What technical details can be shared safely
* When disclosure should occur
* Whether a security advisory or release note is needed
* How contributors should be credited

Do not publish details that expose credentials, personal information, student information, assessment content, or an uncorrected vulnerability without authorization.

## Academic and Institutional Requirements

Security reporting does not replace applicable course instructions, academic-integrity requirements, acceptable-use policies, privacy requirements, or institutional incident-reporting procedures.

Discovering a vulnerability does not authorize a person to exploit it, access restricted information, disrupt a course or service, or exceed the scope of an assignment. Any academic or disciplinary consequences will be determined through the applicable institutional processes.

## Provisional Status

Formal institutional review and approval of this Security Policy are pending. This interim document may be revised or replaced after that review is complete.

This policy does not create a safe-harbor agreement, authorize security testing, establish a contractual response obligation, or replace applicable institutional policies, course requirements, contractual obligations, laws, or platform terms. If a conflict exists, the controlling institutional policy, course requirement, law, contract, or platform term takes precedence.

## References

This document uses original, academic-context wording informed by the following sources:

* [Adding a security policy to your repository](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/configure-vulnerability-reporting/add-security-policy), which describes GitHub’s requirements for communicating supported versions and reporting procedures.
* [Privately reporting a security vulnerability](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/report-privately), which explains how to submit a private vulnerability report when the repository has this feature enabled.
* [Coordinated disclosure of security vulnerabilities](https://docs.github.com/en/code-security/concepts/vulnerability-reporting-and-management/coordinated-disclosure), which describes private collaboration and coordinated publication through repository security advisories.
* [GitHub Community Guidelines](https://docs.github.com/en/site-policy/github-terms/github-community-guidelines), which establishes expectations for safe, respectful, and responsible participation on GitHub.
* [GitHub Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service), which governs access to and use of GitHub.
* Applicable institutional information-security, privacy, acceptable-use, academic-integrity, records-management, and incident-response policies.
