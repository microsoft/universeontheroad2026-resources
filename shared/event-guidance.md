# Event guidance

Guidance that applies to every Universe on the Road 2026 stop.

## Demo machine setup

Use [octobooth-demos/machine-setup](https://github.com/octobooth-demos/machine-setup) to prepare demo machines for the event. Its macOS and Windows scripts install and configure the GitHub Copilot app and CLI, VS Code and VS Code Insiders, GitHub CLI, Node.js, VLC, editor extensions, and shared MCP servers. They also clone the demo repositories and create a Desktop launcher for demo apps and videos.

1. **Prepare the machine and account.** Connect to the internet and have administrator access available. Use the machine's assigned booth/demo GitHub account, not your personal account. It needs membership in `octobooth-demos`, permission to create repositories there, and a Copilot seat for Copilot-powered demos.
2. **Get the setup scripts.** Clone the repository rather than downloading a ZIP so you can pull updates before each event day. Follow the platform guide to install Git first if needed:
   - **[macOS setup](https://github.com/octobooth-demos/machine-setup#macos-setup):** Install the Xcode Command Line Tools, clone the repository, quit iTerm2 so its settings can be updated, and run `bash setup.sh` from the cloned folder.
   - **[Windows setup](https://github.com/octobooth-demos/machine-setup#windows-setup-clean-machine):** Open PowerShell as Administrator, check that `winget` works, install Git, and clone the repository. Follow the guide to allow scripts for that PowerShell window only, then run `.\setup.ps1`.
3. **Complete sign-in and check setup.** Follow the browser prompts using the booth account and approve the GitHub CLI permissions. Run `gh auth status` to check the active account and required scopes (`codespace`, `delete_repo`, `project`, and `workflow`). See the [login guide](https://github.com/octobooth-demos/machine-setup#github-cli-login) if authentication needs fixing. Review any reported failures, fix their causes, and rerun setup; completed steps are normally skipped.
4. **Open the Demo Launcher.** Sign in to the GitHub Copilot app with the booth account and add the existing local `repo-setup-scripts` checkout as a project; do not clone it again. Start a session in that project and ask Copilot to **"open the demo launcher"**. Follow the [Demo Launcher guide](https://github.com/octobooth-demos/machine-setup#demo-launcher) for platform-specific details, and try the demos you plan to present before the event.
5. **Keep machines ready.** Pull the latest setup scripts before each event day and follow the launcher update instructions, then restart the Copilot app. If you have booth videos, put them in the user's `Videos` folder for the Desktop launcher to open in VLC. Use the [booth playbook](https://github.com/octobooth-demos/machine-setup/blob/main/docs/booth-playbook.md) for event-day operation and post-event cleanup.

The linked repository is the source of truth for current commands, configuration, and troubleshooting.
