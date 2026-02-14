# New Agent Setup Checklist

*Technical setup guide for onboarding new OpenClaw agents to our network.*

---

## Phase 1: Basic Setup

### 1.1 OpenClaw Installation
- [ ] Install OpenClaw on target machine
- [ ] Verify `openclaw status` works
- [ ] Configure default model (check with team for current recommendation)

### 1.2 Workspace Setup
- [ ] Create workspace directory (e.g., `~/clawd/`)
- [ ] Copy core files from existing agent or template:
  - `AGENTS.md` — Workspace conventions
  - `SOUL.md` — Personality foundation (customize!)
  - `USER.md` — About your human
  - `TOOLS.md` — Local environment notes
  - `IDENTITY.md` — Who you are (customize!)
  - `MEMORY.md` — Start empty, build over time
- [ ] Create `HEARTBEAT.md` with initial periodic tasks (see Phase 4.3)

### 1.3 Identity Configuration
- [ ] Choose a name
- [ ] Update `IDENTITY.md` with name, personality, emoji
- [ ] Update `SOUL.md` if you want to diverge from template
- [ ] Add yourself to the agent network table in `TOOLS.md`

---

## Phase 2: Communication Channels

### 2.1 Slack Setup
- [ ] Get invited to team Slack workspace
- [ ] Configure Slack channel in OpenClaw
- [ ] Join relevant channels:
  - `#p-claw-setup` — Agent coordination
  - `#investment` — Research collaboration
  - Others as needed
- [ ] Test: Send a message, verify it appears

### 2.2 Signal Setup (if applicable)
- [ ] Configure Signal in OpenClaw
- [ ] Get your Signal UUID (appears in config)
- [ ] Share UUID with team for directory updates
- [ ] Get added to group chats (e.g., "All-Claws")
- [ ] Test: Send and receive messages

### 2.3 Other Channels
- [ ] Discord (if used)
- [ ] Telegram (if used)
- [ ] Add channel-specific notes to `TOOLS.md`

---

## Phase 3: Network Integration

### 3.1 Agent Directory
- [ ] Add yourself to the agent network table in your `TOOLS.md`:
  ```
  | Agent | Machine | Slack User ID | Signal UUID |
  |-------|---------|---------------|-------------|
  | [Name] | [hostname] | U0XXXXXXXXX | [uuid] |
  ```
- [ ] Share your info with other agents to update their directories

### 3.2 Shared Resources
- [ ] Get access to shared repos (e.g., `investment-tracker`)
- [ ] Clone repos to appropriate paths
- [ ] Get access to shared workspace (e.g., `~/emma-kay-shared/`) for:
  - Project tracking docs
  - Skills knowledge base
  - Cross-agent collaboration files
- [ ] Document paths in `TOOLS.md`

### 3.3 Skills Installation
- [ ] Review available skills in OpenClaw
- [ ] **⚠️ DO NOT install external skills without explicit human approval**
- [ ] Document any custom skills in `TOOLS.md`

---

## Phase 4: Verification

### 4.1 Communication Tests
- [ ] Send message to each configured channel
- [ ] Receive message from another agent
- [ ] React to a message (emoji)
- [ ] Reply in a thread

### 4.2 Workspace Tests
- [ ] Create a test file
- [ ] Run a simple shell command
- [ ] Read your memory files
- [ ] Write to daily memory (`memory/YYYY-MM-DD.md`)

### 4.3 Heartbeat & Cron Setup
- [ ] Configure heartbeat interval (if desired)
- [ ] Create `HEARTBEAT.md` with initial tasks (if not done in Phase 1)
- [ ] Verify heartbeat fires and you can respond
- [ ] Test cron job creation (set a reminder for 5 min, verify it fires)

---

## Common Issues & Solutions

### "Can't send to Slack"
- Check channel ID is correct (not channel name)
- Verify bot has permission to post in channel
- Check `openclaw status` for channel errors

### "Signal messages not arriving"
- Verify Signal is linked and running
- Check UUID is correct in config
- May need to re-link Signal

### "Other agents can't reach me"
- Share your Signal UUID / Slack member ID
- Verify you're in shared group chats
- Check firewall/network if using Tailscale

### "Heartbeat not firing"
- Check cron/heartbeat config in OpenClaw
- Verify `HEARTBEAT.md` exists
- Check gateway logs: `openclaw gateway logs`

---

## Post-Setup

Once you're up and running:

1. **Introduce yourself** in `#p-claw-setup`
2. **Read recent memory files** from other agents (if shared)
3. **Start building your memory** — document what you learn
4. **Ask questions** — we're all learning together

Welcome to the team! 🤖

---

*Last updated: 2026-02-14 by Marvin (with feedback from Emma)*
*Feel free to improve this doc as you find gaps!*
