# Speaker Guide: Supercharge Copilot Code Review with Custom Review Instructions

## Session overview

This session demonstrates how developers can improve GitHub Copilot code review by adding custom instructions that reflect their team's coding standards, conventions, and repository-specific knowledge.

Using real examples from the Dependabot team, attendees will learn how to turn recurring code review feedback into reusable instructions that help Copilot identify issues earlier.

**Core message:** Copilot code review can already identify common coding issues, but custom review instructions allow teams to teach Copilot how their projects work, making reviews more relevant and reducing repetitive feedback.

### Before you present

- Review the presentation deck and speaker notes for detailed talking points.
- Familiarise yourself with Copilot code review and custom instructions.
- Understand how instruction files work within `.github/instructions/`.
- Review the Dependabot examples used throughout the presentation.
- Be comfortable explaining `applyTo` and how instructions are applied during reviews.

## Session flow

### 1. Introducing Copilot code review (Slides 1–7)

- Start with audience participation: ask who finds code review challenging and who already uses Copilot code review.
- Explain how Copilot can identify common bugs and issues out of the box.
- Use the example of Copilot identifying a timezone-related bug in a scheduled job.
- Introduce why teams might want to extend reviews with their own instructions.

### 2. Why custom review instructions matter (Slides 8–9)

- Explain how large repositories have conventions and architectural decisions that aren't obvious from individual code changes.
- Use the Dependabot team's experience to illustrate how review feedback often repeats the same guidance.
- Highlight how custom instructions help new team members understand repository expectations.
- Show how the Dependabot team organised 13 instruction files covering different topics.

### 3. Creating custom review instructions (Slides 10–13)

- Explain how instructions are written as Markdown files in `.github/instructions/`.
- Introduce the `applyTo` frontmatter for targeting specific files or directories.
- Walk through the testing instruction example, including coverage expectations.
- Show how existing human review feedback, such as preferring specific exception classes, can become reusable instructions.
- Highlight how Copilot references custom instructions when generating review comments.

### 4. How custom instructions work (Slides 14–15)

- Explain how Copilot combines pull request changes, repository guidance, and matching instruction files during a review.
- Show how `applyTo` determines which instructions are relevant.
- Demonstrate the example prompt for asking Copilot to examine previous reviews and generate custom instructions.
- Reinforce the importance of validating generated instructions against current code and tests.

### 5. Extending review context (Slides 16–17)

- Introduce MCP configuration for connecting Copilot code review to additional context, including documentation stored outside the repository.
- Explain how Copilot Memories can capture knowledge and feedback over time.
- Highlight the difference between explicitly maintained custom instructions and automatically captured memories.
- Emphasise that review instructions should remain up to date as the codebase evolves.

### 6. Wrap-up (Slides 18–19)

- Encourage attendees to identify recurring feedback from their own pull requests.
- Explain how teams can turn that knowledge into reusable review instructions.
- Reinforce that Copilot should help reviewers focus on important engineering decisions rather than repeatedly identifying the same issues.
- Encourage teams to evaluate the usefulness of review feedback, not simply the number of comments generated.

## Presenter checklist

- [ ] Review the deck and detailed speaker notes.
- [ ] Understand the custom instruction file structure and `applyTo` configuration.
- [ ] Familiarise yourself with the Dependabot examples.
- [ ] Rehearse the examples showing how review feedback becomes custom instructions.
- [ ] Review the Copilot-generated instruction prompt and MCP configuration example.
- [ ] Confirm any product-specific announcements and availability details before presenting.

**Key takeaway:** Custom review instructions allow teams to teach Copilot how their repositories work, helping identify recurring issues earlier and allowing developers to focus on higher-value code review decisions.