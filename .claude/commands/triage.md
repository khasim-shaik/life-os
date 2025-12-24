# Inbox Triage Protocol

Process inbox items and organize them into the right places.

## The Project Decision Framework

### Quick Decision Tree

```
Is this item actionable?
    │
    ├─ NO → Delete or file as reference/insight
    │
    └─ YES → Does it take < 2 minutes?
              │
              ├─ YES → Mark as "Just do it" (don't track, delete after)
              │
              └─ NO → Is it a single action?
                       │
                       ├─ YES → One-time task (add to journal or area page)
                       │
                       └─ NO → Does it fit an EXISTING project?
                                │
                                ├─ YES → Add to that project
                                │
                                └─ NO → Does it need 3+ tasks to complete?
                                         │
                                         ├─ YES → CREATE NEW PROJECT
                                         │
                                         └─ NO → One-time task
```

### The "3+ Tasks" Rule for New Projects

**CREATE a new project when ALL of these are true:**
- Requires 3 or more separate actions to complete
- Spans multiple days or weeks
- Has a clear outcome or deliverable
- Doesn't fit any existing active project

**Examples that NEED projects:**
- "Renew passport" → photos, forms, appointment, payment, pickup
- "Plan birthday party" → venue, invites, cake, decorations, food
- "Launch website" → design, build, content, domain, deploy
- "Get US visa" → documents, DS-160, fees, interview, pickup

**KEEP as one-time task when:**
- Single action (one phone call, one purchase, one conversation)
- Takes less than 30 minutes total
- No dependencies on other tasks
- Won't generate follow-up tasks

**Examples that are ONE-TIME tasks:**
- "Call dentist" → single call
- "Buy groceries" → single errand
- "Reply to email" → single action
- "Downgrade car insurance" → single phone call

### Handling Insights & Ideas

Some inbox items aren't tasks at all:
- **Insights/Principles** → Move to The Way.md
- **Ideas for later** → Move to relevant project's "Ideas" section or Someday list
- **Reference info** → File in appropriate area page or delete
- **Random thoughts** → Usually delete (if important, it will come back)

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
INBOX TRIAGE ([X] items)
===============================================

🗑️ JUST DO IT / DELETE (< 2 min or not actionable)
-----------------------------------------------
1. "[Item]" → Do now then delete / Just delete
2. "[Item]" → Do now then delete

💡 INSIGHTS & IDEAS (not tasks)
-----------------------------------------------
3. "[Item]" → Move to [[The Way]] (principle)
4. "[Item]" → Move to [[Project]] ideas section

✅ ONE-TIME TASKS (single actions)
-----------------------------------------------
5. "[Item]"
   Area: [[Finances]] | Urgency: This Week | Score: 9
   → Add to today's journal or area page

6. "[Item]"
   Area: [[Family]] | Urgency: Today | Score: 12
   → Add to today's journal

📁 ADD TO EXISTING PROJECT
-----------------------------------------------
7. "[Item]"
   Project: [[MVP Launch]] | Urgency: This Week | Score: 14
   → Add as task to [[MVP Launch]]

🆕 CREATE NEW PROJECT (3+ tasks needed)
-----------------------------------------------
8. "[Item]" → Needs new project: [[Project Name]]
   Why: Requires multiple steps over several days
   Suggested tasks:
   - Task 1
   - Task 2
   - Task 3

📅 CALENDAR EVENTS
-----------------------------------------------
9. "[Item]" → Create event: [Date/Time]

===============================================
SUMMARY
===============================================
- Just do it / Delete: X items
- Insights to file: X items
- One-time tasks: X items
- Add to projects: X items
- New projects: X items
- Calendar events: X items

===============================================
Confirm to proceed? (yes/adjust/cancel)
```

## Step 4: Execute Actions (If Confirmed)

If user confirms:

### For New Projects:
1. Create new project page with template:
   ```markdown
   - ## [Project Name]
     status:: active
     area:: [[Area]]
     created:: [date]
     why:: [Connection to goals/values]

   - ## Tasks
     - TODO [Task 1]
     - TODO [Task 2]
     - TODO [Task 3]

   - ## Ideas
     - (future ideas go here)

   - ## Notes
     - (reference info goes here)
   ```
2. Add project to Projects.md under "Active Projects"

### For Existing Items:
1. Update project pages with new tasks
2. Create calendar events via MCP
3. Add urgent items to today's journal
4. Move insights to The Way.md or area pages
5. Clear processed items from Inbox.md

### Always:
Update Inbox.md with "Recently Triaged" section:
```markdown
## Recently Triaged ([date])
- "[item]" → [[Destination]]
- "[item]" → Deleted
- "[item]" → Created [[New Project]]
```

## Decision Rules

### 🗑️ JUST DO IT / DELETE if:
- Takes less than 2 minutes → do it now, don't track
- Doesn't serve any current goal → delete
- "Nice to have" with no real value → delete
- Random thought that isn't actionable → delete
- Can be easily found online if needed → delete

### 💡 FILE AS INSIGHT if:
- It's a principle or lesson learned → The Way.md
- It's an idea for a project → that project's Ideas section
- It's reference information → relevant area page

### ✅ ONE-TIME TASK if:
- Single action (one call, one email, one purchase)
- Takes less than 30 minutes total
- No dependencies, no follow-up tasks expected
- Add to today's journal if urgent, otherwise area page

### 📁 ADD TO EXISTING PROJECT if:
- Clearly related to an active project
- Moves a milestone forward
- Has dependencies with other project tasks
- Check Projects.md to find the right project

### 🆕 CREATE NEW PROJECT if (ALL must be true):
- Requires 3+ separate actions to complete
- Spans multiple days or weeks
- Has a clear outcome or deliverable
- Doesn't fit any existing active project
- When creating, also suggest initial tasks

### 📅 ADD TO CALENDAR if:
- Has a specific date/time
- Requires scheduling around other events
- Is a meeting or appointment
- Is a recurring commitment

## Priority Scoring

```
Score = (Value Priority * 2) + Urgency + Impact

Value: Imaan(6), Health(5), Family(4), Time(3), Money(2), Friends(1)
Urgency: Today(5), This Week(3), This Month(2), Someday(1)
Impact: Major goal(5), Milestone(4), Maintenance(3), Nice to have(1)
```

Higher score = higher priority
