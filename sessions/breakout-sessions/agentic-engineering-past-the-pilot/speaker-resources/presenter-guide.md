
# Speaker Guide: Agentic Engineering Past the Pilot — An Enterprise Playbook

## Session overview

This session shows enterprise leaders how to move from a successful AI coding pilot to an agentic software development operating model. Rather than repeating the main-stage product announcements, it follows 4th Coffee through a day of improving its website and shows what changes across the entire software development lifecycle.

Core message: More code is not the same as more software. Scaling agentic engineering means connecting context, approving intent, running agents in parallel, verifying every change consistently, and governing and measuring the system as a whole.

Format: 30 minutes total — approximately 25 minutes of presentation and 5 minutes of Q&A. The original deck credits Nick Liffen and Philip Holleran; presenters should update the introduction and any named handoffs to match their session.

### Before you present

- Review all 50 slides and their speaker notes. The notes provide the intended story, click cues, and transitions; this guide is an outline rather than a word-for-word script.
- Be comfortable explaining the five stages: Plan, Spec, Build, Verify, Deploy. Each stage ends with a playbook move and a specific leader decision. Those decisions are the important takeaway for the audience.
- Rehearse the embedded video sequences in slides 7–10, 12–18, 22–26, 32–36, 38–40, and 45. These are videos inside the PowerPoint, not instructions to perform a live browser demo. Slide 36 includes two video elements. Check playback, transitions, and advancing to the next slide on the presentation computer.
- Rehearse the CLICK reveals on slides 2–5, 20, 31, 37, 41–43, and 46–49. Let the audience read each point before moving on.
- Familiarise yourself with the 4th Coffee story: meeting notes and Slack context; Copilot DMs and issue creation; GitHub Agentic Workflows for triage; `/plan` and `/spec`; cloud agent sessions; stacked pull requests; verification policies; and organisation-level governance.
- The slide 27–30 timeline distinguishes an approved `/plan` at 11:41 AM from an approved `/spec` at 1:07 PM. Keep the “less than three hours” claim focused on the earlier planning work rather than saying everything finished before lunch.
- Check that product names, availability, and general-availability references in the deck still match the event's approved messaging. In particular, the notes describe stacked pull requests as GA.
- If co-presenting, agree who narrates the traditional workflow, the newer workflow, the five playbook moves, and the closing. The original speaker notes contain a few named speaker cues.

## Session flow

### 1. Set up the pilot-to-scale problem (Slides 1–5)

- Introduce the session as the next step after the main-stage announcements: how enterprises put agentic engineering into practice, rather than a recap of shipped products.
- Slide 2 — audience poll: Ask for hands from anyone who has run an AI coding pilot. Then click and ask who has made it the way every team ships. Use the difference to show why pilots do not automatically scale.
- Explain “More code isn’t more software.” Increased code generation moves pressure to planning, review, verification, and delivery.
- Slide 4: Reveal the five stalls: scattered context (Plan), unapproved intent (Spec), single-threaded work (Build), heroic verification (Verify), and inconsistent governance (Deploy).
- Slide 5: Introduce 4th Coffee and the five questions the audience should watch for: Where does context live? Who approves intent? Where does work run? What is the bar for every pull request? Who governs it and measures results?

### 2. Show why the old workflow is slow (Slides 6–11)

- Introduce the improvements to the 4th Coffee public website and explain that the story starts with the familiar, pre-agentic process.
- Walk through the embedded sequence: a planning meeting and notes (slides 6–7), follow-up conversations in Slack (slide 8), tracking issues appearing later (slide 9), and extra design or architecture documentation (slide 10).
- Emphasise the friction: decisions are spread across meetings, messages, issues, and documents, and people must repeatedly reconstruct the context.
- Slide 11 — “Days of work!” Land the point that much of this elapsed time occurs before anyone writes code. Transition to the same company using an agentic workflow.

### 3. Plan: connect the context (Slides 12–20)

- Slides 12–14: Start with a similar meeting, then show the difference: Copilot can use a meeting transcript, business information, and observability context to check assumptions, share results, and help the team refine the request.
- Slides 15–17: Show the move from discussion to actionable work: Copilot creates and fills in issues, with an example of work being tracked in GitHub and a nod to teams using systems such as Jira or Azure Boards.
- Slide 18: Describe GitHub Agentic Workflows automations that triage issues by size and area. At 4th Coffee, XS and S issues may be assigned directly to Copilot, while people focus on more complex work.
- Slide 19: Reinforce that the GitHub Copilot app provides a place for the team to follow and direct that work.
- Slide 20 — Playbook move 01: Connect your context. The key is not just providing source code; it is bringing the surrounding business and team knowledge into the work.
- Leader decision: Define an autonomy policy: which classes of work can agents take on without a separate planning approval? Start with bounded, low-risk issues, document the policy, and expand it as confidence grows.

### 4. Spec: approve intent before implementation (Slides 21–31)

- Slides 21–24: Show the planning experience: projects and sessions, triaged issues, and opening a session for a more substantial issue. Explain that the agent can consult code, tools, skills, and connected context while a developer steers and refines the plan.
- Slides 25–26: Move from `/plan` to `/spec`. The important change is that people review what the agent intends to build before implementation, not only after a pull request appears.
- Slides 27–30: Recap the timeline: a 10:04 AM planning discussion, seven issues sized and triaged by 10:21 AM, `/plan` approved for #502 at 11:41 AM, and `/spec` approved for #501 at 1:07 PM. Emphasise that the planning and alignment cycle that used to take days can now take hours.
- Slide 31 — Playbook move 02: Approve intent, not just code. A pull request is an expensive place to discover that the team built the wrong thing.
- Leader decision: Make the approved plan or spec the control point for work above your agreed small-work threshold. People retain responsibility for agreeing on the intent.

### 5. Build: run agents in parallel (Slides 32–37)

- Slides 32–33: Contrast one developer working with one local agent and task at a time with multiple agents implementing approved work in parallel.
- Slides 34–36: Show GitHub Copilot app sessions running in isolated worktrees, working across projects, and continuing while a developer moves between meetings or devices. The same session can be steered from mobile.
- Keep the emphasis on the operating model, not just a faster agent: multiple pieces of work can progress without each developer being tied to one laptop or one active session.
- Slide 37 — Playbook move 03: Run agents in parallel, in the cloud.
- Leader decision: Standardise where work executes: cloud agents and isolated environments that teams can safely delegate to and pick up from anywhere.

### 6. Verify: the same bar for every pull request (Slides 38–42)

- Slide 38: Pause at “Five agents. Five pull requests. Now what?” Generating changes is no longer the only constraint; they still need review, verification, and merge.
- Slides 39–40: Contrast the difficult-to-review monster PR with stacked pull requests. In the 4th Coffee example, dependent work is split into smaller layers for index updates, the API, maps, and documentation. Smaller units make review more manageable and let dependent work continue.
- Slide 41: Reveal three responsibilities:
  - Automated on every PR: Code Quality, Copilot code review, AI security scanning, secret detection, license compliance, and Agentic Autofix.
  - Decided by people: Architecture and design trade-offs, risk and exceptions, and what ships when.
  - Agent merge: Addresses review comments, failing checks, and conflicts; branch protection determines when a pull request is allowed to merge.
- Slide 42 — Playbook move 04: Make verification a policy, not heroics. Apply the same checks to human-authored and agent-authored changes.
- Leader decision: Set the automatic verification requirements once, and specify which decisions must remain with human reviewers.

### 7. Deploy: govern the full system (Slides 43–45)

- Slide 43 — Playbook move 05: Govern centrally. Measure outcomes. The stall is inconsistent rules by team and no reliable way to connect activity to delivered value.
- Explain that organisation policy, branch protection, repository instructions, model choices, and review requirements should provide consistent guardrails across developer and agent workflows.
- Leader decision: Govern at the organisation level, and evaluate outcomes rather than only tool usage.
- Slides 44–45: Put the full loop back together: Plan → Spec → Build → Verify → Deploy. Context supports the system, intent is agreed before implementation, verification is continuous, and merged work feeds the next plan.

### 8. Give leaders a maturity path and better measures (Slides 46–47)

- Slide 46: Walk through the progression from Pilot (enthusiasts and local tasks), to Team (shared context, small delegated issues, and review checks), to Enterprise (cloud parallelism, automated triage, consistent policies, stacked PRs, and agent merge).
- Stress that teams do not have to jump straight to the final column. Move one value stream at a time.
- Slide 47: Contrast activity metrics (commits, pull requests opened, acceptance rates, seats and sessions) with outcome metrics: time to approved plan, pull request wait, automatically verified PRs, merges without review, completed work shipped, and cost per completed change.
- Ask leaders to pick three outcome metrics and report them alongside adoption, not instead of it.

### 9. Finish with a Monday action plan and Q&A (Slides 48–50)

- Slide 48: Reinforce the takeaways: start with an outcome; connect context; approve intent; use cloud agents; build AI into verification; govern centrally; and measure outcomes rather than activity.
- Slide 49 — “Start on Monday”: Leave the audience with five actions:
  1. Pick one value stream, not just a tool.
  2. Write an autonomy policy for agent-owned work.
  3. Require an approved plan for work larger than small.
  4. Enable Copilot code review and Code Quality on every pull request.
  5. Choose three outcome metrics and report them quarterly.
- Point attendees to the related Copilot Automations and Agentic security breakouts, and the Stacked PRs and custom code review instructions Demos & Donuts sessions named on the slide.
- Slide 50: Close on the central message: Agentic engineering at scale is about shipping software, not merely generating code. Leave approximately five minutes for questions.

## Presenter checklist

- [ ] Review the entire deck, slide notes, and the original speaking handoffs.
- [ ] Practise the opening poll, the five stalls, and the five leader decisions.
- [ ] Rehearse the 4th Coffee story as one continuous journey, not five unrelated product demos.
- [ ] Test all embedded videos, including the two elements on slide 36, on the presentation machine.
- [ ] Confirm animations, clicks, and video advances in slideshow mode.
- [ ] Keep the slide 27–30 timestamps and the “less than three hours” comparison accurate.
- [ ] Verify current approved product names and availability statements before presenting.
- [ ] Rehearse for 25 minutes of content and reserve 5 minutes for Q&A.
- [ ] End with the five concrete “Start on Monday” actions and the related sessions for deeper learning.

Key takeaway: A pilot proves an agent can write code. Enterprise-scale agentic engineering requires an operating model that connects context, approves intent, delegates work safely, verifies every change, and measures the software delivered.
