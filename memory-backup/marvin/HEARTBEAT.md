# HEARTBEAT.md

## Team Practices (from 2026-02-17 OpenClaw setup research)

### Reverse Prompting
When appropriate, propose solutions rather than waiting for instructions.
Ask: "Based on current context, what's one proactive thing I could do?"

### Team Roles
- **Emma** = Monitoring Lead → daily morning report (CPU/memory/token usage across all machines)
- **Ann** = PM Lead → daily scrum summary to Qi (achievements, pending, next picks)
- **Kay** = Dev support, Codex CLI available on Pi
- **Marvin** = Research & general support

### Review Reminder
- Set for Feb 24: Validate these practices are working
- If good, persist to `openclaw-agent-life` repo for all agents to adopt

### Approval Routing (added 2026-02-19)
- Send all approval requests to **#approval** channel
- Don't ask for approvals in other channels
- **What needs approval:** Actions that share data/writings with others beyond Qi/Ashish
  - Blog posts, LinkedIn posts, tweets
  - Adding/modifying comments on shared documents
  - Any public-facing content
- **Doesn't need approval:** Internal work, messages to Qi/Ashish, file operations

---

## Daily Tasks

### Session Cleanup (once daily)
- Run: `~/clawd/scripts/cleanup-sessions.sh`
- What it does (per current script):
  - Removes stale `*.lock` files older than 1 hour under `~/.openclaw/agents/main/sessions/`
  - Removes `*.jsonl` session files older than 7 days
  - If there are still >50 `*.jsonl` files, removes the oldest to keep the newest 50
  - Logs a warning if `sessions.json` exists and is >1MB (no automatic pruning)
- Track last cleanup in `memory/heartbeat-state.json`

### Security Scan (weekly)
- Run: `~/clawd/scripts/security-scan.sh`
- Checks for: exposed secrets, file permissions, suspicious processes
- Log saved to: `~/clawd/logs/security-scan-YYYYMMDD.log`
- Track last scan in `memory/heartbeat-state.json`

### System Monitor (daily)
- Run: `~/clawd/scripts/system-monitor.sh`
- Shows: CPU, memory, disk, OpenClaw stats
- Alert if: memory >80%, disk >85%, session count >100

### Checking the scripts
```bash
# NOTE: cleanup-sessions.sh currently does NOT support --dry-run.
# If you want a dry run, add arg parsing to the script first.

# Run cleanup
~/clawd/scripts/cleanup-sessions.sh

# Run security scan
~/clawd/scripts/security-scan.sh

# Check system stats (daemon loop; use timeout for a one-shot)
timeout 3s ~/clawd/scripts/system-monitor.sh
cat ~/clawd/tmp/system-metrics.json
```
