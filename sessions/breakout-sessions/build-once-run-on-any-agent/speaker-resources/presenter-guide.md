# Speaker Guide: Build Once, Run on Any Agent

## Session overview

This session demonstrates how developers can use **Agent Skills** to turn repetitive AI prompts into reusable instructions and workflows that can work across different coding agents.

Through two practical examples, attendees will see how skills can improve code verification and automate complex data engineering workflows.

**Core message:** Stop rebuilding the same prompts for every task or AI agent. Build reusable skills that capture knowledge, enforce standards, and work across different tools and environments.

### Before you present

- Review the [presentation deck](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/slides/talk.pdf) and [session summary](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/assets/session-summary.pdf).
- Familiarise yourself with Agent Skills and how `SKILL.md` defines reusable instructions.
- Review the [session repository](https://github.com/githubevents/build-once-run-on-any-agent) and both demo examples.
- Watch the demo recordings and confirm access to the required repositories.
- Prepare previously completed demo results as backups.

## Session flow

### 1. Setting the scene: From prompts to skills

- Explain the limitations of repeatedly prompting AI for the same tasks.
- Introduce Agent Skills as reusable instructions that capture workflows, expertise, and standards.
- Highlight how skills can be reused across compatible coding agents rather than recreated for each tool.

### 2. Demo 1: Independent verification with Proof Agent

- Introduce **Proof Agent**, a reusable skill for independently reviewing AI-generated code.
- Explain why the agent that writes code shouldn't be solely responsible for verifying its own work.
- Show how a separate verifier examines changes and provides evidence-based findings.
- Demonstrate the GitHub Actions integration and review results.

**Key message:** Reusable skills can make verification a consistent part of AI-assisted development.

**Resources:**
- [Proof Agent demo](https://github.com/githubevents/build-once-run-on-any-agent/tree/main/demos/proof-agent)
- [Narrated walkthrough](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/assets/recordings/proof-agent-narrated.mp4)

### 3. Demo 2: Building data pipelines with Dataforge

- Introduce **Dataforge**, which uses four reusable skills to build data pipelines.
- Explain how business-specific context is kept in a configuration manifest rather than embedded in the skills.
- Demonstrate how the skills take a GitHub issue through discovery, code generation, testing, and a pull request.
- Highlight engineering standards, verification, and human approval checkpoints.
- Show how the same skills can support different data platforms through configuration.

**Key message:** Skills can capture engineering expertise and make complex workflows repeatable without hardcoding business-specific knowledge.

**Resources:**
- [Dataforge demo](https://github.com/githubevents/build-once-run-on-any-agent/tree/main/demos/dataforge)
- [Step-by-step demo instructions](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/demos/dataforge/examples/support-desk/DEMO.md)
- [Demo recording](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/assets/recordings/Dataforge.mp4)

### 4. Wrap-up

- Agent Skills turn repeated prompts into reusable workflows.
- Skills help preserve engineering knowledge and enforce consistent practices.
- The same approach works for individual productivity and more complex team workflows.
- Developers can build skills once and reuse them across compatible agents.

## Presenter checklist

- [ ] Review the presentation and session summary.
- [ ] Understand the Agent Skills structure and `SKILL.md`.
- [ ] Watch and rehearse both demonstrations.
- [ ] Verify demo repositories, dependencies, and access.
- [ ] Prepare successful demo outputs as backups.
- [ ] Coordinate the handoff between demos if presenting with a co-speaker.

**Key takeaway:** Agent Skills allow developers to capture expertise once and reuse it across AI agents, making workflows more consistent, portable, and reliable.
</