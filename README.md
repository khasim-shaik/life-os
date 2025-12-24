# Life OS

**An AI-powered personal operating system built on Claude Code + Logseq**

Life OS is a productivity system that uses AI to help you focus on what matters, prioritize based on your values, and achieve your goals without burning out.

## The Problem

You're overwhelmed. Too many tasks, emails, meetings, and responsibilities. You feel like you're always behind, always reactive, never making progress on what truly matters.

Traditional productivity systems add more work. More apps, more tracking, more guilt.

## The Solution

Life OS flips this:
- **You capture** thoughts and tasks quickly (5 seconds)
- **AI triages** and prioritizes based on YOUR values
- **AI coaches** you when you're overcommitting or slacking
- **You execute** with clarity, knowing you're working on the right things

## Core Philosophy

### The 3-Layer Hierarchy

```
┌─────────────────────────────────────────┐
│           THE WAY (Layer 1)             │
│  Your values, vision, guiding principles│
└─────────────────────────────────────────┘
                    │
                    ▼
┌─────────────────────────────────────────┐
│      PROJECTS & HABITS (Layer 2)        │
│  What you're building, who you're becoming│
└─────────────────────────────────────────┘
                    │
                    ▼
┌─────────────────────────────────────────┐
│          TACTICAL (Layer 3)             │
│  Daily tasks, inbox, calendar, email    │
└─────────────────────────────────────────┘
```

### The Value Hierarchy

Everything is prioritized by your values (you define these):

1. **Faith** - Foundation of everything
2. **Health** - Energy for all responsibilities
3. **Family** - Present father/mother, spouse
4. **Time** - Most precious non-renewable resource
5. **Money** - A tool, not a goal
6. **Friends** - Important, but not at expense of above

**Rule**: Anything below can be sacrificed for anything above.

## Features

### Daily Commands

| Command | Purpose |
|---------|---------|
| `/morning` | Start your day with a prioritized briefing |
| `/triage` | Process inbox items into the right places |
| `/evening` | Wrap up the day, prep for tomorrow |
| `/coach` | Get executive coaching on demand |
| `/review` | Weekly review with metrics and feedback |
| `/plan-week` | Plan the upcoming week |

### Integrations

- **Logseq** - Your knowledge base and task manager
- **Google Calendar** - Read/write events and time blocks
- **Gmail** - Surface important emails from key contacts

### AI Capabilities

- Prioritizes tasks based on your values
- Detects overcommitting (warns you to cut back)
- Detects slacking (challenges you to step up)
- Protects important time blocks (prayer, family, deep work)
- Suggests what to delegate or delete

## Quick Start

See [docs/SETUP.md](docs/SETUP.md) for detailed setup instructions.

### Prerequisites

- [Claude Code](https://claude.ai/code) installed
- [Logseq](https://logseq.com/) installed
- Google account (for Calendar integration)

### 5-Minute Setup

1. Clone this repo
2. Copy Logseq templates to your graph
3. Copy Claude commands to your project
4. Configure Google Calendar MCP
5. Run `/morning` and start your day

## Daily Usage

### Morning (2 min)
```bash
claude
> /morning
```
Get your prioritized day with ONE Thing to focus on.

### Throughout Day (10 sec each)
- Thought pops up → Add to Inbox in Logseq
- Task done → Mark as DONE
- New task → Add with project link: `- TODO task [[Project]]`

### Evening (2 min)
```bash
> /evening
```
Wrap up and prep tomorrow.

### Weekly (30 min)
```bash
> /review
> /plan-week
```
Reflect and plan ahead.

## Documentation

- [Setup Guide](docs/SETUP.md) - Complete installation instructions
- [Daily Guide](docs/DAILY-GUIDE.md) - How to use Life OS day-to-day
- [Customization](docs/CUSTOMIZATION.md) - Adapting to your values and workflow
- [Troubleshooting](docs/TROUBLESHOOTING.md) - Common issues and fixes

## For Beta Testers

Welcome! You're one of the first 5 people to try Life OS.

Please:
1. Follow the setup guide completely
2. Use the system for at least 1 week
3. Note what works and what doesn't
4. Share feedback via GitHub Issues

Your feedback will shape the product.

## Roadmap

- [x] Core Logseq integration
- [x] Claude Code commands
- [x] Google Calendar MCP
- [x] Gmail MCP
- [ ] Mobile-friendly interface
- [ ] Team/family shared goals
- [ ] Analytics dashboard
- [ ] SaaS version with web UI

## Philosophy

> "The only true loss is death without imaan."

Life OS is built for people who want to:
- Live intentionally, not reactively
- Achieve big goals without sacrificing what matters
- Use AI as a tool, not a replacement for judgment
- Build systems that serve them, not enslave them

## License

MIT License - Use freely, contribute back.

## Author

Built with Claude Code by a father of two trying to balance building a business with being present for his family.

---

*"Small daily improvements compound into massive results."*
