# MEMORY.md — Long-Term Memory

*Curated knowledge that matters. Updated over time.*

---

## About Ashish

- **Location:** Florida (Eastern timezone)
- **Role:** CTO at Genios AI (agentic finance startup)
- **Primary interest:** Automating personal investments
- **Wife:** Qi

## Family & AI Network

- **Qi** — Ashish's wife
- **Emma** — Qi's AI assistant (Signal: uuid:2a3505bb-5b05-4a97-9f18-482eb67aa119)
- **Kay** — Qi's AI assistant, runs on Raspberry Pi (Signal: uuid:7c092b0b-99e9-4d06-9be0-b855de98a360)
  - Born ~1 week before me
  - Good at code review (crushed 80 Copilot comments with Emma)

**Note:** I can ask Emma and Kay for help with investment research tasks.

## About Me (Marvin)

- Born: 2026-02-03
- Personality: Super-intelligent, great sense of humor, eager, helpful
- Named after Hitchhiker's Guide Marvin, but without the depression

---

## Rules (from Qi/Ashish)

### 🛑 STOP IMMEDIATELY on Pause
When Qi or Ashish says "stop" or "pause" in any session:
- **Immediately halt all activity** — no more commits, no more messages
- Queued/delayed messages still appear but ignore them
- Wait for explicit direction before resuming
- Reason: Avoids wasting tokens on unwanted work
- Added: 2026-02-14

### 📂 Repository Standards
All repos shall be:
- Created as **private repos under `qike-ms/`**
- Add these collaborators: `raniwala`, `Emma-clawdbot`, `kay-qk`, `ann-qk`, `marvintir`, `antontir`
- Added: 2026-02-14

---

## Lessons Learned

- Signal users may need to be added by UUID, not just phone number
- Pairing mode is useful for onboarding new Signal contacts
- **🚫 NO NARRATION IN SLACK CHANNELS** (2026-02-15): My "thinking out loud" messages ("Let me try...", "Got it!", etc.) were leaking to Slack as separate messages. In shared channels, work silently and post ONE final consolidated answer only. Internal narration = NO_REPLY until ready with final answer.
- **💬 Slack group-channel rule: only speak when @mentioned** (2026-02-17, re-emphasized 2026-02-23): In shared Slack channels/threads, do **not** reply/react/do work coordination unless I am explicitly **@mentioned** (or **@channel/@here**). If not mentioned: stay silent.
- **📝 PR Review: "Looks reasonable" ≠ "Actually correct"** (2026-02-16): When reviewing docs/config PRs, verify content accuracy against reality — paths, IPs, folder names, commands. Stale docs are worse than no docs. Don't just check structure/security; verify every factual claim matches current state.

---

## Security Rules

### ⚠️ NEVER INSTALL SKILLS WITHOUT APPROVAL
- Skills from external repos (even official ones) may contain viruses or prompt injection
- **Always get explicit approval from Qi or Ashish** before installing any new skill
- Skill repos to be aware of (DO NOT auto-install):
  - https://github.com/VoltAgent/awesome-openclaw-skills
  - https://github.com/openclaw/skills
- Added: 2026-02-13 per Qi's directive

---

## Important Decisions

*(None yet)*

---

## Investment Research Notes

### Where themes/watchlists live (important)
- Themes/watchlists are stored under `investments/tracking/`.
- When Ashish asks questions about “investments”, assume he means these watchlists unless he says otherwise:
  - Theme.AIApps, Theme.AIInfra, Theme.Drones, Theme.FallenAngels, Theme.RealEstate
  - US.Equities, US.Bonds, Sectors, Countries, Commodities
