# Contributing

Thank you for helping improve the Universe on the Road 2026 resource center.

We welcome corrections, working resource links, and session recordings, code, and demos that you have permission to share.

## Propose a change

For missing resources, broken links, or suggestions, open an issue describing the session and the requested change. For security concerns, follow [security.md](security.md) instead of opening a public issue.

## Submit a pull request

1. Fork the repository and create a branch for your change.
2. Make focused edits in the appropriate session folder or in `shared/`.
3. Update the root [README.md](README.md) when adding, renaming, or moving a session.
4. Check Markdown formatting and confirm that all changed links lead to the intended resources.
5. Open a pull request explaining what changed and which session it affects. Link any related issue.

## Resource organization

Each session has its own folder under `sessions/`, named `session-NN-name` with a two-digit number and a lowercase, hyphenated name. Each session folder contains:

- `README.md`: Presentation resources table and the **Before presenting** checklist.
- `deck/presentation.pptx`: Latest approved slides.
- `speaker-guide.md`: Narrative, talking points, and timing.
- `transcript.md`: Full AI-generated reference transcript.
- `demo-prep.md`: Demo setup, validation, and fallback.

Guidance that applies across sessions belongs in `shared/`: `event-guidance.md` for event-wide guidance and `city-notes.md` for city-specific changes. The root `SPEAKER-GUIDE.md` explains how speakers use these resources.

Replace "Coming soon." with content or descriptive links as resources become available, and leave unavailable entries clearly marked.

Use relative links for files in this repository. Encode spaces and special characters in Markdown link destinations.

## Sharing guidelines

Only submit content you own or have permission to publish. Do not include credentials, personal information, confidential customer material, or internal-only links. Keep discussions respectful and focused on improving the resources.
