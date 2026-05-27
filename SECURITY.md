# Security Policy

## Supported Versions

| Version | Supported          |
|---------|--------------------|
| v1.x    | ✅ Active support   |

## Reporting a Vulnerability

If you discover a security vulnerability in Knowledge Diff, **please report it responsibly**.

### How to Report

1. **Do NOT open a public GitHub issue.** Security vulnerabilities should be reported privately.
2. **GitHub Private Vulnerability Reporting:** Go to the [Security tab](../../security) of this repository on GitHub and click **"Report a vulnerability"** to submit a private report directly to the maintainer.
3. **Include:**
   - A description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

### What to Expect

- **Acknowledgement** within 48 hours of your report.
- **Assessment** within 5 business days — we'll confirm whether it's a valid vulnerability.
- **Fix timeline** depends on severity:
  - **Critical / High:** Patch within 7 days
  - **Medium:** Patch within 30 days
  - **Low:** Addressed in the next release cycle

### Scope

The following are in scope for security reports:

- API key leakage or exposure in logs
- Injection attacks via LLM prompts (prompt injection)
- GitHub token misuse or privilege escalation
- Supply-chain vulnerabilities in dependencies
- Unauthorized repository access via the auto-patch feature

### Out of Scope

- LLM hallucinations or incorrect drift detection (these are accuracy issues, not security)
- Vulnerabilities in third-party LLM provider APIs (report to those providers directly)

## Security Best Practices for Users

1. **Use GitHub Secrets** for all API keys — never hardcode them in workflow files.
2. **Scope permissions** minimally: only grant `contents: write` if you use `auto-patch: true`.
3. **Review auto-generated patch PRs** before merging — AI-suggested changes should always be human-approved.
4. **Pin the action version** to a specific release tag (e.g., `@v1.0.0`) or commit SHA rather than a mutable tag.
