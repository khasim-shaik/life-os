# Evening Wrap Protocol

Quick end-of-day summary and tomorrow prep.

## Step 1: Read Today's Data

Read from `/Users/khasim/Library/Containers/nl.t-shaped.Sushitrain/Data/Documents/logseq-full/`:

1. Today's journal from `journals/` (format: YYYY_MM_DD.md)
2. `pages/Inbox.md` - Check for new items
3. `pages/Goals.md` - Reference for tomorrow's priority

## Step 2: Analyze Today

### What Was Planned
- ONE Thing: [from journal]
- Tasks listed: [count and list]

### What Got Done
- ONE Thing completed? [Yes/No]
- Tasks marked DONE: [list]
- Unplanned accomplishments: [if any]

### What Didn't Happen
- Tasks still TODO: [list]
- Why: [if apparent from notes]

### Inbox Status
- New items added today: [count]
- Total inbox items: [count]

## Step 3: Generate Evening Summary

```
EVENING WRAP: [Day], [Date]
===============================================

✅ DONE TODAY
-----------------------------------------------
- [x] [Completed task 1]
- [x] [Completed task 2]
- [x] [Completed task 3]

ONE Thing: [Task] - [COMPLETED ✓ / NOT DONE ✗]

📋 CARRYING OVER
-----------------------------------------------
- [ ] [Task 1] - [Brief reason if known]
- [ ] [Task 2]

💭 WHY (if tasks didn't get done)
-----------------------------------------------
[Observations: interruptions? energy? unclear? avoided?]

📥 INBOX STATUS
-----------------------------------------------
[X] items in inbox
[Note if needs triage tomorrow]

🎯 TOMORROW'S PRIORITY
-----------------------------------------------
Based on what didn't happen today and upcoming deadlines:

Suggested ONE Thing: [Task]
Why: [Connection to goals/urgency]

🌙 GRATITUDE PROMPT
-----------------------------------------------
What went well today, even if small?

===============================================
```

## Step 4: Update Journal (Optional)

If user confirms, update today's journal Evening section:
```markdown
## 🌙 Evening
  - Done: [List of completed items]
  - Tomorrow: [Suggested ONE Thing]
```

## Step 5: Quick Inbox Check

If inbox has 5+ items:
- "You have [X] items in inbox. Consider running /triage tomorrow morning."

If inbox is empty:
- "Inbox is clear. Nice work!"

## Step 6: Offer Actions

- "Should I update today's journal with this summary?"
- "Want me to pre-set tomorrow's ONE Thing?"
- "Need to do a quick inbox triage before bed?"

## Rules

1. Keep it brief - this is end of day, energy is low
2. No guilt trips about undone tasks
3. Focus on progress made, not just gaps
4. Tomorrow is a new day
5. Protect sleep - don't add more work
