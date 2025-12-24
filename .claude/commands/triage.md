# Inbox Triage Protocol

Process inbox items and organize them into the right places.

## Step 1: Read Context

Read these files from `/Users/khasim/Library/Containers/nl.t-shaped.Sushitrain/Data/Documents/logseq-full/pages/`:

1. `Inbox.md` - Items to triage
2. `Projects.md` - Active projects
3. `Areas.md` - Life areas
4. `The Way.md` - Values for prioritization
5. `Goals.md` - Current focus

## Step 2: For Each Inbox Item

Analyze and determine:

### Type
- **Task**: Something to do
- **Event**: Something with a date/time
- **Note**: Information to capture
- **Reference**: Something to file away

### Area
Which life area does this serve?
- Deen (Faith)
- Health
- Family
- Career/Work
- Finances
- Personal

### Project
Does this belong to an active project?
- Check Projects.md for active projects
- If yes, which one?
- If no, is it standalone?

### Urgency
- **Today**: Must be done today
- **This Week**: Should be done this week
- **This Month**: Can wait but has deadline
- **Someday**: No deadline, do when possible

### Destination
Where should this go?
- **Today's Journal**: Urgent tasks for today
- **Project Page**: Tasks related to a project
- **Area Page**: Ongoing area responsibilities
- **Calendar**: If it's an event with date/time
- **Delete**: Not important, doesn't serve goals

## Step 3: Output Triage Results

Format output as:

```
INBOX TRIAGE ([X] items processed)
===============================================

1. "[Item text]"
   Type: Task | Area: [[Career]] | Project: [[MVP Launch]]
   Urgency: This Week | Priority Score: 12
   → MOVE TO: [[MVP Launch]] page

2. "[Item text]"
   Type: Event | Area: [[Family]]
   Date: [extracted date]
   → CREATE: Calendar event for [date/time]

3. "[Item text]"
   Type: Task | Area: None | Project: None
   Urgency: Someday | Priority Score: 4
   → DELETE: Doesn't serve current goals

4. "[Item text]"
   Type: Task | Area: [[Health]]
   Urgency: Today | Priority Score: 15
   → MOVE TO: Today's journal

===============================================
SUMMARY
===============================================
- Move to projects: X items
- Add to calendar: X items
- Add to today: X items
- Delete: X items

===============================================
ACTIONS AVAILABLE
===============================================
[ ] Move items to suggested destinations
[ ] Create calendar events
[ ] Clear processed items from inbox

Confirm to proceed? (yes/no)
```

## Step 4: Execute Actions (If Confirmed)

If user confirms:
1. Update project pages with new tasks
2. Create calendar events via MCP
3. Add urgent items to today's journal
4. Clear processed items from Inbox.md
5. Update Inbox.md with "Recently Triaged" section showing what was moved

## Decision Rules

### DELETE if:
- Doesn't serve any current goal
- Hasn't been acted on in 30+ days
- "Nice to have" with no real value
- Can be easily found online if needed later

### MOVE TO PROJECT if:
- Clearly related to an active project
- Moves a milestone forward
- Has dependencies with other project tasks

### MOVE TO TODAY if:
- Has a deadline today
- Blocks other important work
- Takes < 15 minutes (batch with other quick tasks)

### ADD TO CALENDAR if:
- Has a specific date/time
- Requires scheduling around other events
- Is a recurring commitment

## Priority Scoring

```
Score = (Value Priority * 2) + Urgency + Impact

Value: Imaan(6), Health(5), Family(4), Time(3), Money(2), Friends(1)
Urgency: Today(5), This Week(3), This Month(2), Someday(1)
Impact: Major goal(5), Milestone(4), Maintenance(3), Nice to have(1)
```

Higher score = higher priority
