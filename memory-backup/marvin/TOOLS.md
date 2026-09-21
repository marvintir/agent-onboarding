# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

## investment-tracker Repo

**GitHub:** `qike-ms/investment-tracker`

| Purpose | Path | When to use |
|---------|------|-------------|
| **Runtime** | `~/clawd/investment-tracker` | Default — use for running tools, generating ideas, all normal operations |
| **Development** | `~/clawd/dev/investment-tracker` | ONLY when actively coding/developing (PRs, feature branches) |

**Key rule:** Use runtime path unless Ashish says we're developing.

---

## Tailscale Hosts

- **qi-fl-p520** — Emma's machine (Qi's workstation)
- **parkland-linux** — My machine (Ashish's)

---

## Agent Network

| Agent | Machine | Signal UUID | Slack User ID |
|-------|---------|-------------|---------------|
| Emma | qi-fl-p520 | 2a3505bb-5b05-4a97-9f18-482eb67aa119 | U0ACF2X4MGU |
| Kay | Raspberry Pi | 7c092b0b-99e9-4d06-9be0-b855de98a360 | U0ACQJD7W6M |
| Ann | ra-mac-pro | (TBD) | U0AC4MR3895 |
| Marvin | parkland-linux | (this instance) | U0ADUL92YUB |

**Humans:**
| Name | Slack User ID |
|------|---------------|
| Qi | U0AC501S0Q3 |
| Ashish | U0ADV11L99T |

---

Add whatever helps you do your job. This is your cheat sheet.
