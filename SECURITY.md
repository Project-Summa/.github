# Security Policy

> Summa takes the security of its users and their financial data seriously.

---

## Supported Versions

| Version | Supported |
|---|---|
| Current development branch | Yes |
| Released versions | Yes |
| Older releases | No |

Security fixes are applied to the current main branch and the latest release.

---

## Reporting a Vulnerability

If you discover a security vulnerability, please report it responsibly.

**Do not open a public GitHub issue for security vulnerabilities.**

### How to Report

Send an email to:

```text
security@project-summa.org
```

Include the following information:

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if available)

### What to Expect

| Step | Timeline |
|---|---|
| Acknowledgment of report | Within 48 hours |
| Initial assessment | Within 5 business days |
| Status update | Within 10 business days |
| Resolution (if confirmed) | As soon as practically possible |

You will be notified when the vulnerability is confirmed, when a fix is developed and when the fix is released.

---

## Scope

The following are in scope:

- Remote code execution
- Authentication bypass
- Authorization bypass between workspaces or profiles
- Data leakage between users or workspaces
- Cross-site scripting in web components
- SQL injection
- Cryptographic weaknesses
- Token theft or session hijacking
- Backup file exposure
- Attachment unauthorized access
- Sync protocol data corruption

---

## Out of Scope

The following are generally out of scope:

- Denial of service against self-hosted instances
- Social engineering
- Physical access to unlocked devices
- Vulnerabilities in third-party dependencies (report upstream)
- Issues requiring physical access to the server

---

## Data Classification

Summa handles sensitive financial data. The following data classifications apply:

| Classification | Examples |
|---|---|
| **Critical** | Passwords, encryption keys, tokens, backup files |
| **Sensitive** | Transaction amounts, merchant names, account balances, categories |
| **Internal** | Device metadata, sync cursors, application version |
| **Public** | Repository content, documentation, release notes |

---

## Security Principles

- Local database is trusted
- Network is untrusted
- External services are optional
- Sensitive data must never leave the device unless synchronization is explicitly enabled
- All authentication occurs server-side
- Authorization must be validated on every protected request
- Passwords are hashed using Argon2id
- Refresh tokens are stored as hashed values
- HTTPS is required in production

---

## Responsible Disclosure

We believe in responsible disclosure and will credit reporters who follow this policy.

Public disclosure of confirmed vulnerabilities will occur after a fix is available, unless the reporter and the maintainers agree on a different timeline.

---

## Contact

```text
security@project-summa.org