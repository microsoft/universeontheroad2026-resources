# Speaker Guide: Agentic Security for Every Developer

**GitHub Universe on the Road 2026**

## Session overview

This session introduces GitHub's approach to agentic security, demonstrating how GitHub Advanced Security and Copilot help developers detect, prevent, and remediate security vulnerabilities throughout the software development lifecycle.

**Core message:** Security needs to keep pace with AI-driven development. GitHub is bringing security directly into developer workflows, using AI agents to identify and fix vulnerabilities earlier and at scale.

### Before you present

- Review the presentation deck and AI session summary for additional talking points.
- Familiarise yourself with GitHub Advanced Security, CodeQL, AI scanning, and Agentic Autofix.
- Confirm access to the demo environments and enabled features.
- Prepare completed scans and remediation pull requests as backups.
- Rehearse the guest demo handoff if delivering with a second presenter.

**Session timing:** Approximately 15 minutes of slides and 25 minutes of demonstrations.

## Session flow

### 1. Setting the scene (Slides 1–5)

- Security threats and vulnerability disclosures are increasing, while the time available to respond is shrinking.
- Introduce the GitHub Advanced Security pillars: **code security, code quality, supply chain security, and Copilot Autofix**.
- Explain why security must be integrated throughout the SDLC, not just when code reaches a pull request.
- Introduce GitHub's approach to securing every stage of agent-driven development.

### 2. Securing the agent loop (Slides 6–7)

- Explain how security checks are integrated into coding-agent workflows.
- Highlight code, dependency, and secret security checks.
- Demonstrate how agents identify and fix issues before code is committed.

### 3. Security in developer environments (Slides 8–9)

- Show how developers can request on-demand security reviews from the CLI.
- Highlight security findings alongside code in supported IDEs.
- Introduce the Copilot security extension and security canvas for reviewing, triaging, and fixing issues.

### 4. AI-powered security scanning (Slides 10–11)

- Explain how **CodeQL and AI scanning complement each other** to identify vulnerabilities.
- Introduce standard AI scanning and deeper repository-level analysis.
- Demonstrate security scanning on pull requests and across repositories.
- Highlight AI application scanning for risks such as prompt injection, sensitive information disclosure, and excessive agency.
- If using the original delivery format, hand over to the guest presenter for the AI application scanning demonstration, then return for repository scanning.

### 5. Agentic Autofix (Slides 12–13)

- Explain the challenge of large vulnerability backlogs and manual remediation.
- Introduce Agentic Autofix for addressing multiple security alerts.
- Demonstrate selecting alerts and assigning remediation to Copilot.
- Show how the agent investigates findings, proposes fixes, runs validation, and creates a pull request.
- Highlight how Copilot memories can help improve future remediation.

### 6. Wrap-up (Slides 14–15)

- Reinforce that security is becoming integrated into every stage of development.
- Summarise how developers can access security through agents, IDEs, the CLI, pull requests, and repositories.
- Highlight the available configuration options and next steps for enabling the capabilities.

## Presenter checklist

- [ ] Review the slides and AI session summary.
- [ ] Confirm all required security features are available in the demo environment.
- [ ] Rehearse each demonstration and prepare fallback examples.
- [ ] Coordinate the guest presenter handoff, if applicable.
- [ ] Verify feature availability, product claims, and links on the closing slide.

**Key takeaway:** Agentic security brings detection and remediation closer to where developers work, helping teams build and ship software securely without slowing down development.