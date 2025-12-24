# Life OS Setup Guide

Complete setup instructions for Life OS.

## Prerequisites

Before starting, ensure you have:

- [ ] macOS or Linux (Windows support coming)
- [ ] [Claude Code](https://claude.ai/code) installed and working
- [ ] [Logseq](https://logseq.com/) installed (desktop or mobile)
- [ ] A Google account (for Calendar integration)
- [ ] Node.js 18+ installed (`node --version`)

## Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/life-os.git
cd life-os
```

## Step 2: Set Up Logseq

### Option A: New Logseq Graph (Recommended for new users)

1. Open Logseq
2. Create a new graph called `LifeOS`
3. Note the graph location (e.g., `~/Documents/LifeOS/`)
4. Copy all template files:

```bash
# Replace ~/Documents/LifeOS with your actual graph path
cp logseq-templates/pages/* ~/Documents/LifeOS/pages/
```

### Option B: Existing Logseq Graph

1. Copy only the new pages you need:

```bash
GRAPH_PATH="~/Documents/YourGraph"  # Update this

# Core pages (required)
cp logseq-templates/pages/The\ Way.md "$GRAPH_PATH/pages/"
cp logseq-templates/pages/Habits.md "$GRAPH_PATH/pages/"
cp logseq-templates/pages/Prayer\ Times.md "$GRAPH_PATH/pages/"
cp logseq-templates/pages/Patterns.md "$GRAPH_PATH/pages/"
cp logseq-templates/pages/Important\ Contacts.md "$GRAPH_PATH/pages/"

# Optional (if you don't have equivalents)
cp logseq-templates/pages/Goals.md "$GRAPH_PATH/pages/"
cp logseq-templates/pages/Projects.md "$GRAPH_PATH/pages/"
cp logseq-templates/pages/Inbox.md "$GRAPH_PATH/pages/"
```

### Verify Logseq Setup

Open Logseq and check that you can see:
- [ ] The Way (your values and vision)
- [ ] Goals
- [ ] Projects
- [ ] Inbox
- [ ] Habits
- [ ] Prayer Times (update with your local times)

## Step 3: Install Claude Code Commands

Copy the slash commands to your Claude Code project:

```bash
# Navigate to your Claude Code project directory
cd ~/code/your-project  # Update this

# Create commands directory if it doesn't exist
mkdir -p .claude/commands

# Copy all commands
cp ~/code/life-os/.claude/commands/* .claude/commands/
```

### Verify Commands

```bash
ls .claude/commands/
# Should show: morning.md, triage.md, review.md, coach.md, evening.md, plan-week.md
```

## Step 4: Set Up Google Calendar Integration

### 4.1 Create Google Cloud Project

1. Go to [Google Cloud Console](https://console.cloud.google.com)
2. Click **Select a project** → **New Project**
3. Name: `Life OS`
4. Click **Create**

### 4.2 Enable APIs

1. Go to **APIs & Services** → **Library**
2. Search and enable:
   - **Google Calendar API**
   - **Gmail API** (for future use)

### 4.3 Configure OAuth Consent Screen

1. Go to **APIs & Services** → **OAuth consent screen** (or **Google Auth Platform**)
2. Click **Branding** in the left menu:
   - App name: `Life OS`
   - User support email: Your email
   - Developer contact: Your email
   - Click **Save**

3. Click **Audience**:
   - Select **External**
   - Click **Save**

4. Click **Data Access**:
   - Click **Add or remove scopes**
   - Add these scopes:
     - `https://www.googleapis.com/auth/calendar`
     - `https://www.googleapis.com/auth/calendar.events`
   - Click **Update**

### 4.4 Create OAuth Credentials

1. Go to **Clients** (left menu)
2. Click **+ Create Client**
3. Application type: **Desktop app**
4. Name: `Life OS Desktop`
5. Click **Create**
6. **Download JSON** file

### 4.5 Save Credentials

```bash
# Create config directory
mkdir -p ~/.config/life-os

# Move downloaded file (update filename as needed)
mv ~/Downloads/client_secret_*.json ~/.config/life-os/gcp-oauth.keys.json
```

### 4.6 Configure MCP Server

```bash
# Add Google Calendar MCP to Claude Code
claude mcp add-json google-calendar '{
  "type": "stdio",
  "command": "npx",
  "args": ["-y", "@cocal/google-calendar-mcp"],
  "env": {
    "GOOGLE_OAUTH_CREDENTIALS": "~/.config/life-os/gcp-oauth.keys.json"
  }
}'
```

### 4.7 Verify MCP Connection

```bash
claude mcp list
# Should show: google-calendar: ... - ✓ Connected
```

### 4.8 First-Time Authentication

1. Start Claude Code: `claude`
2. The first time you use calendar features, a browser window will open
3. Sign in with your Google account
4. Grant the requested permissions
5. Close the browser and return to Claude Code

## Step 5: Update Your Configuration

### 5.1 Update Prayer Times

Edit `pages/Prayer Times.md` in Logseq with your local prayer times.

Use [IslamicFinder](https://www.islamicfinder.org/) or your local mosque times.

### 5.2 Customize The Way

Edit `pages/The Way.md` in Logseq:

1. Update the 5-year vision to YOUR vision
2. Adjust the value hierarchy if needed
3. Add your guiding principles

### 5.3 Add Important Contacts

Edit `pages/Important Contacts.md`:

1. Add email addresses you want surfaced in morning briefings
2. Organize by category (Legal, Medical, Family, Work, etc.)

## Step 6: Update Command Paths

The slash commands reference a specific Logseq path. Update them for your setup:

```bash
# In each command file, find and replace the Logseq path
# Default: /Users/khasim/Library/Containers/nl.t-shaped.Sushitrain/Data/Documents/logseq-full/
# Replace with your Logseq graph path

# Example using sed (macOS):
LOGSEQ_PATH="/Users/yourname/Documents/LifeOS"  # Your path
cd .claude/commands

for file in *.md; do
  sed -i '' "s|/Users/khasim/Library/Containers/nl.t-shaped.Sushitrain/Data/Documents/logseq-full|$LOGSEQ_PATH|g" "$file"
done
```

Or manually edit each command file and update the paths.

## Step 7: Test the Setup

### Restart Claude Code

```bash
# Exit current session
exit

# Start fresh
claude
```

### Run Morning Briefing

```bash
> /morning
```

You should see:
- Prayer times for the day
- Calendar events (if any)
- ONE Thing suggestion
- Prioritized task list
- Coach note

### Test Other Commands

```bash
> /triage    # Process inbox items
> /coach     # Get coaching feedback
> /evening   # End of day wrap
```

## Troubleshooting

### "Command not found" error

- Ensure commands are in `.claude/commands/` directory
- Restart Claude Code after adding commands

### Google Calendar not connecting

- Check MCP configuration: `claude mcp list`
- Verify credentials file exists: `ls ~/.config/life-os/`
- Re-add MCP server if needed

### Logseq files not found

- Verify the path in command files matches your Logseq graph location
- Check file permissions

### OAuth errors

- Ensure you added yourself as a test user in Google Cloud Console
- Re-authenticate by deleting tokens: `rm ~/.config/google-calendar-mcp/tokens.json`

## Next Steps

1. Read [Daily Guide](DAILY-GUIDE.md) to learn the workflow
2. Customize [The Way](../logseq-templates/pages/The%20Way.md) with your values
3. Add your first tasks to Inbox
4. Run `/morning` tomorrow and start your first day!

---

## Quick Reference

### File Locations

| File | Purpose |
|------|---------|
| `~/.config/life-os/gcp-oauth.keys.json` | Google OAuth credentials |
| `.claude/commands/*.md` | Claude Code slash commands |
| `~/Documents/LifeOS/pages/` | Logseq pages (your graph) |

### Commands

| Command | When to Use |
|---------|-------------|
| `/morning` | Start of day |
| `/triage` | Process inbox (daily) |
| `/evening` | End of day |
| `/coach` | When stuck or overwhelmed |
| `/review` | Weekly (Sunday) |
| `/plan-week` | Weekly (Sunday/Monday) |
