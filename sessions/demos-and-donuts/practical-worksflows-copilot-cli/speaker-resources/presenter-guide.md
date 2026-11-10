# Speaker Guide: Rediscover the Command Line


**Session duration:** 15 minutes

## Session overview

This session explores how GitHub Copilot CLI and traditional command-line tools can work together to automate everyday developer workflows more efficiently.

Through a practical comparison, attendees will see how existing CLI tools, custom extensions, and Copilot can reduce execution time, token usage, and repetitive work.

**Core message:** Not every problem needs a new AI capability. Sometimes the most efficient solution is to combine AI with the mature, composable tools already available in the terminal.

### Before you present

- Review the presentation deck and speaker notes for detailed talking points.
- Familiarise yourself with GitHub CLI (`gh`), Copilot CLI, and GitHub CLI extensions.
- Understand the three approaches compared in the session: computer use, Copilot using CLI commands, and Copilot with a custom extension.
- Review the `gh-notifs` example, including its terminal UI, custom status line, and hooks.
- Rehearse the demonstrations and transitions in the deck.

## Session flow

### 1. Setting the scene (Slides 1–3)

- Introduce the challenge of repetitive developer tasks, using GitHub notifications as an example.
- Explain how Copilot Computer Use can automate graphical applications, including those without APIs.
- Introduce the idea that traditional CLI tools may offer a more efficient alternative when programmatic access exists.

### 2. Three agents, one task (Slides 4–6)

- Introduce the challenge: identifying which issues and pull requests in a GitHub inbox are still open.
- Compare three approaches:
  - **Computer Use:** Navigates the GitHub website.
  - **Copilot CLI:** Figures out the required commands and API calls.
  - **Copilot with `gh-notifs`:** Uses a purpose-built CLI extension.
- Highlight the results: approximately 4 minutes 21 seconds, 37 seconds, and 13 seconds respectively.
- Explain how choosing the right tool can significantly reduce execution time and token consumption.

### 3. Why the terminal still matters (Slides 7–10)

- Introduce GitHub CLI as a powerful interface to GitHub's APIs.
- Explain the Unix philosophy of small tools that each do one thing well.
- Highlight how commands can be combined to build more complex workflows.
- Show how Copilot can use existing tools or generate scripts to accomplish a task.

### 4. Building reusable tools with `gh-notifs` (Slides 11–14)

- Introduce `gh-notifs`, a GitHub CLI extension for managing notifications.
- Demonstrate its terminal interface for filtering, viewing, and managing notifications.
- Show how custom commands can be integrated into the Copilot CLI status line.
- Explain how Copilot CLI hooks can execute scripts automatically during a session.

### 5. Wrap-up (Slides 15–17)

- Reinforce the progression from **prompt → skill → script → extension**.
- Highlight how reusable tools can save time and tokens compared with repeatedly generating the