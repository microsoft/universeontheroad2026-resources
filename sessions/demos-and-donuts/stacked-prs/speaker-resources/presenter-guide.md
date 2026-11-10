# Speaker Guide: Stop Waiting on Your Own Pull Requests — GitHub Stacked PRs in Practice

## Session overview

This session introduces GitHub Stacked Pull Requests and demonstrates how developers can break large changes into smaller, focused pull requests that are easier to review, manage, and merge.

**Core message:** As AI agents generate more code and developers work on multiple tasks in parallel, code review can become a bottleneck. GitHub Stacked PRs helps teams maintain development velocity by making changes easier to review without blocking dependent work.

### Before you present

- Review the presentation deck and speaker notes for detailed talking points.
- Familiarise yourself with stacked pull requests, dependent branches, and stack merging.
- Understand the GitHub Stacks CLI (`gh stack`) and its integration with GitHub Copilot and VS Code.
- Review and rehearse the demonstrations in the deck.
- Prepare an existing stack with pull requests in different review and CI states as a backup.

## Session flow

### 1. Introducing stacked pull requests (Slides 1–6)

- Start by asking the audience whether they've used stacked pull requests before.
- Explain how AI-driven development creates more parallel work, larger changes, and additional review pressure.
- Introduce stacked PRs as a way to break large changes into smaller, focused pull requests.
- Explain how each PR builds on the previous one, forming an ordered chain of dependent changes.
- Highlight the adoption and productivity benefits, and announce general availability.

### 2. Creating stacks with GitHub CLI and Copilot (Slides 7–9)

- Introduce the **GitHub Stacks CLI (`gh stack`)** for managing stacked branches and pull requests.
- Show how developers can use the Agent Skill to work with stacks through Copilot.
- Demonstrate how agents can work in parallel using worktrees and create separate layers of a stack.

### 3. Reviewing and navigating stacks (Slides 10–11)

- Show how GitHub identifies pull requests that belong to a stack.
- Demonstrate navigating between PRs and viewing the overall stack status.
- Explain how review approvals, CI checks, and merge requirements apply to dependent PRs.
- Introduce the dedicated stack page for viewing progress and sharing links.

### 4. Extending and merging a stack (Slides 12–18)

- Demonstrate checking out an existing stack locally.
- Add a new branch and commit changes to extend the stack.
- Use `gh stack submit` to create or update pull requests.
- Show how branch protection and required checks apply across the stack.
- Demonstrate merging the ready portion of a stack while leaving unfinished changes open.
- Introduce automatic merging once the selected PRs meet their requirements.

### 5. Managing stacks in VS Code (Slides 19–21)

- Introduce the GitHub Stacked PRs integration with VS Code.
- Demonstrate switching branches, reviewing stack status, and fixing CI issues.
- Show how to rebase a stack and resolve conflicts.
- Demonstrate how automatic merging completes the remaining PRs once checks pass.

### 6. Wrap-up (Slides 22–23)

- Reinforce how stacked PRs make large changes easier to review and manage.
- Highlight the flexibility of working with stacks through the CLI, Copilot, and VS Code.
- Encourage attendees to explore GitHub Stacked PRs at [gh.io/stacks](https://gh.io/stacks).

## Presenter checklist

- [ ] Review the deck and detailed speaker notes.
- [ ] Understand the relationship between stacked branches and pull requests.
- [ ] Rehearse the CLI, Copilot, and VS Code demonstrations.
- [ ] Confirm the demo stack has the required branches, PRs, and CI states.
- [ ] Prepare completed examples for merging, rebasing, and automatic merging.
- [ ] Verify product availability and announcements before presenting.

**Key takeaway:** Stacked pull requests help teams move faster by breaking large changes into smaller, independently reviewable pieces, allowing developers and agents to keep working without waiting for every pull request to merge.