# Speaker Guide: Disrupting Supply Chain Attacks — A Threat Framework for GitHub Actions

## Session overview

This session explores how software supply chain attacks exploit trust relationships across repositories, CI/CD workflows, and dependencies.

Through a practical GitHub Actions attack scenario, attendees will learn how attackers move from an initial vulnerability to downstream compromise, and how GitHub's security improvements help disrupt the attack chain.

**Core message:** Supply chain attacks require multiple steps to succeed. By introducing security controls at each stage, organisations can break the attack chain and protect their software development workflows.

### Before you present

- Review the presentation deck and speaker notes for detailed talking points.
- Familiarise yourself with GitHub Actions security, workflow permissions, caching, and dependency management.
- Understand the five-stage attack scenario and the corresponding security protections.
- Review and rehearse the demonstrations involving producer and consumer repositories.
- Prepare completed workflow runs and configuration examples as backups.
- Confirm current product availability and preview requirements.

## Session flow

### 1. Understanding software supply chain attacks (Slides 1–7)

- Explain how software supply chain attacks exploit trust between software producers and consumers.
- Demonstrate how a compromised producer can distribute malicious code through trusted dependencies.
- Highlight how compromised consumers can become new sources of attacks.
- Introduce real-world incidents including Shai-Hulud, tj-actions, and other GitHub Actions ecosystem compromises.
- Emphasise how attacks can propagate across multiple organisations and repositories.

### 2. Anatomy of a GitHub Actions supply chain attack (Slides 8–17)

- Introduce the five-stage attack scenario involving producer and consumer repositories.
- Explain the roles of `lint.yml`, `release.yml`, and `comment.yml`.
- Walk through the attack stages:
  1. **Untrusted execution:** A malicious contribution executes through an unsafe workflow configuration.
  2. **Cache poisoning:** A lower-privilege workflow modifies shared state consumed by a privileged workflow.
  3. **Privilege escalation:** The compromised release workflow gains access to publishing permissions.
  4. **Compromised dependencies:** A malicious release tag distributes altered Action code to consumers.
  5. **Downstream compromise:** Consumers execute malicious code with access to their own credentials and resources.
- Highlight the trust boundaries crossed during the attack.

### 3. Breaking the attack chain (Slides 18–21)

- Challenge the traditional assumption that defenders must prevent every possible mistake.
- Explain how disrupting any required stage can prevent an attack from succeeding.
- Introduce GitHub's approach to improving Actions security through safer defaults and additional controls.
- Highlight the importance of collaboration between security researchers, maintainers, and GitHub's product teams.

### 4. Demonstration setup (Slides 22–26)

- Introduce the producer and consumer repositories used in the demonstrations.
- Review the three workflows and their responsibilities.
- Explain how the attack chain connects contribution checks, release processes, and downstream Action consumers.
- Establish how each upcoming security control addresses a specific attack stage.

### 5. Demonstrating GitHub Actions security protections (Slides 27–42)

- **Stage 1 — Safer checkout defaults:** Demonstrate how checkout protections help prevent unsafe execution of untrusted pull request code.
- **Stage 2 — Read-only Actions cache:** Show how restricted cache write access helps mitigate cache poisoning.
- **Stage 3 — Cache mode and execution policies:** Demonstrate how `cache-mode: none` isolates privileged workflows from shared cache state, while workflow execution policies restrict who can initiate sensitive workflows.
- **Stage 4 — Actions lockfiles:** Introduce `gh actions-lock` and demonstrate how lockfiles record dependency identities and commits to protect against moved Action references.
- **Stage 5 — Actions egress firewall:** Demonstrate how outbound network restrictions help prevent malicious code from reaching unauthorised destinations.

Emphasise that these protections are complementary and that no single control addresses every supply chain risk.

### 6. Future direction and wrap-up (Slides 43–47)

- Highlight GitHub's direction for strengthening the Actions ecosystem through immutable releases, enhanced lockfiles, and expanded policy controls.
- Explain the importance of understanding existing security defaults and deliberately configuring additional protections.
- Reinforce the need to review workflow triggers, permissions, dependencies, caching, and network access.
- Close by returning to the original attack scenario and showing how multiple protections provide opportunities to interrupt it.

## Presenter checklist

- [ ] Review the deck and detailed speaker notes.
- [ ] Understand the five attack stages and their corresponding protections.
- [ ] Rehearse the security demonstrations and workflow examples.
- [ ] Verify the availability and rollout status of the security features discussed.

**Key takeaway:** Attackers need a complete path through the software supply chain. Defenders can disrupt that path at multiple points by combining secure defaults, workflow policies, dependency protections, and network controls.