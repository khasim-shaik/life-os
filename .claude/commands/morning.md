# Morning Briefing Protocol

Generate a comprehensive morning briefing to start the day with clarity and purpose.

## Step 1: Read Foundation Context

Read these files from the Logseq graph at `/Users/khasim/Library/Containers/nl.t-shaped.Sushitrain/Data/Documents/logseq-full/pages/`:

1. `The Way.md` - Core values and 5-year vision
2. `Me.md` - Personal constraints and preferences
3. `Prayer Times.md` - Today's prayer schedule
4. `Goals.md` - Current goals and focus
5. `Projects.md` - Active projects and deadlines

## Step 2: Read Current State

1. Check today's journal in `/Users/khasim/Library/Containers/nl.t-shaped.Sushitrain/Data/Documents/logseq-full/journals/` (format: YYYY_MM_DD.md)
2. Read `Inbox.md` for pending items
3. Read `Patterns.md` for recent trends and coaching signals

## Step 3: Check Calendar (via Google Calendar MCP)

Use the google-calendar MCP tools to:
- Get today's events
- Identify existing commitments
- Check for conflicts with prayer times
- Find available time blocks

## Step 4: Apply Prioritization Algorithm

For all tasks found, calculate priority score:

```
Score = (Value Priority * 2) + Urgency Score + Impact Score

Value Priority (from The Way):
1. Imaan (Faith): 6
2. Health: 5
3. Family: 4
4. Time: 3
5. Money/Career: 2
6. Friends: 1

Urgency Score:
- Due today: 5
- This week: 3
- This month: 2
- Someday: 1

Impact Score:
- Major goal progress: 5
- Project milestone: 4
- Maintenance: 3
- Nice to have: 1
```

## Step 5: Generate Briefing

Output the briefing in this format:

```
Good Morning! [Day], [Date]

===============================================
PRAYER TIMES TODAY
===============================================
Fajr: [time] | Dhuhr: [time] | Asr: [time] | Maghrib: [time] | Isha: [time]

===============================================
TODAY'S CALENDAR
===============================================
[List events with times]
[Flag any conflicts with prayers]

===============================================
🎯 ONE THING
===============================================
[Single most important task for today]
Why: [Connection to goals/values]
Time Block: [Suggested time]

===============================================
📋 PRIORITIZED TASKS
===============================================
1. [Task] - [Area] - Score: X
2. [Task] - [Area] - Score: X
3. [Task] - [Area] - Score: X
(Max 5-6 tasks)

===============================================
📥 INBOX ([X] items)
===============================================
[Summary or "Empty - great!"]

===============================================
📊 WEEK PROGRESS
===============================================
- ONE Things: X/5
- Deep Work: X hours
- Exercise: X/3 sessions
- Prayer: X%

===============================================
💡 COACH NOTE
===============================================
[If overcommitting: Warning + suggestions to cut]
[If slacking: Challenge + suggestions to push]
[If on track: Encouragement + small improvement suggestion]
```

## Step 6: Offer Actions

After the briefing, offer:
- "Would you like me to create time blocks on your calendar?"
- "Should I triage your inbox items?"
- "Want me to pre-populate today's journal?"

## Rules

1. NEVER schedule over prayer times
2. Protect 5-8am for deep work (ONE Thing)
3. Max 6 hours of scheduled work
4. Leave buffer time between blocks
5. Be realistic about capacity
6. Reference The Way values when prioritizing
