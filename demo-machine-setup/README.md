# Demo Machine Setup

Use [octobooth-demos/machine-setup](https://github.com/octobooth-demos/machine-setup) to prepare demo machines for the event. Its macOS and Windows scripts install and configure the GitHub Copilot app and CLI, VS Code and VS Code Insiders, GitHub CLI, Node.js, VLC, editor extensions, and shared MCP servers. They also clone the demo repositories and create a Desktop launcher for demo apps and videos.

## Before you start: Octobooth accounts and 1Password access

- **Each city is allocated its own Octobooth accounts.** Every demo machine must use one of these Octobooth accounts, never a personal GitHub account.
- **The person setting up the demo machines needs 1Password access.** The Octobooth account credentials are stored in 1Password and are needed to authenticate each account during setup.
- **No 1Password access? Request it ahead of time in entitlements.** Approval can take time, so request access well before setup day.

## Set up each machine

Run the setup script on **every** demo machine, and make sure every sign-in on the machine (GitHub Copilot app, GitHub CLI, browser, and VS Code) uses the **Octobooth** account.

1. **Prepare the machine and account.** Connect to the internet and have administrator access available. Use the machine's assigned Octobooth account, not your personal account. It needs membership in `octobooth-demos`, permission to create repositories there, and a Copilot seat for Copilot-powered demos.
2. **Get the setup scripts.** Clone the repository rather than downloading a ZIP so you can pull updates before each event day. Follow the platform guide to install Git first if needed:
   - **[macOS setup](https://github.com/octobooth-demos/machine-setup#macos-setup):** Install the Xcode Command Line Tools, clone the repository, quit iTerm2 so its settings can be updated, and run `bash setup.sh` from the cloned folder.
   - **[Windows setup](https://github.com/octobooth-demos/machine-setup#windows-setup-clean-machine):** Open PowerShell as Administrator, check that `winget` works, install Git, and clone the repository. Follow the guide to allow scripts for that PowerShell window only, then run `.\setup.ps1`.
3. **Complete sign-in and check setup.** Follow the browser prompts using the Octobooth account (credentials are in 1Password) and approve the GitHub CLI permissions. Run `gh auth status` to confirm the active account is the Octobooth account and has the required scopes (`codespace`, `delete_repo`, `project`, and `workflow`). See the [login guide](https://github.com/octobooth-demos/machine-setup#github-cli-login) if authentication needs fixing. Review any reported failures, fix their causes, and rerun setup; completed steps are normally skipped.
4. **Keep machines ready.** Pull the latest setup scripts before each event day and follow the launcher update instructions, then restart the Copilot app. If you have booth videos, put them in the user's `Videos` folder for the Desktop launcher to open in VLC. Use the [booth playbook](https://github.com/octobooth-demos/machine-setup/blob/main/docs/booth-playbook.md) for event-day operation and post-event cleanup.

## Run the demos

1. Open the **GitHub Copilot app** and confirm you are signed in as the **Octobooth** account.
2. Open the existing local `repo-setup-scripts` checkout as a project (do not clone it again) and start a session in it.
3. Type **`open launcher`** (or "open the demo launcher"). The Demo Launcher opens in a canvas, where you can pick a demo to run.

See the [Demo Launcher guide](https://github.com/octobooth-demos/machine-setup#demo-launcher) for platform-specific details.

### Which demos to run

The two fastest demos are ready to show right away:

| Demo | What it shows |
| --- | --- |
| **Ctrl Slash** | Displays a Fruit Ninja-style ninja game on GitHub Pages. |
| **Booth Bingo** | Demonstrates stacked pull requests. |

The other demos take longer to build. Either build them before the event kicks off, or stick to **Ctrl Slash** and **Booth Bingo** during the event. Try every demo you plan to present before attendees arrive.

The linked repository is the source of truth for current commands, configuration, and troubleshooting.
