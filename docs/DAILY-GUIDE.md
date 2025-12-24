# Life OS Daily Guide

How to use Life OS every day to stay focused, productive, and aligned with your values.

## The Daily Rhythm

```
Morning (2 min)    →  /morning  →  Know your ONE Thing
Throughout Day     →  Capture   →  Tasks to Inbox
Evening (2 min)    →  /evening  →  Wrap up, prep tomorrow
```

Total daily overhead: **5-10 minutes**

Everything else is just doing the work.

---

## Morning Routine

### When: After Fajr (or when you wake up)

### Steps:

1. **Open Claude Code**
   ```bash
   claude
   ```

2. **Run morning briefing**
   ```bash
   > /morning
   ```

3. **Review the output**:
   - Prayer times for the day
   - Calendar commitments
   - Your ONE Thing (most important task)
   - Prioritized task list
   - Inbox status
   - Coach note (if any)

4. **Accept or adjust**:
   - Agree with the ONE Thing? Start working on it.
   - Disagree? Tell Claude why and get a new suggestion.

5. **Start your deep work block**
   - Ideally 5-8am before interruptions
   - Focus only on your ONE Thing
   - No email, no phone

### Sample Morning Output

```
Good Morning! Monday, December 23, 2025

🕌 PRAYER TIMES
Fajr: 06:15 | Dhuhr: 12:15 | Asr: 14:45 | Maghrib: 16:45 | Isha: 18:15

📅 CALENDAR
09:00 - Team standup (30min)
14:00 - School pickup

🎯 ONE THING
Ship MVP login feature [[MVP Launch]]
Why: Blocks all other progress, Q1 deadline approaching
Time: 06:30 - 08:30 AM

📋 TASKS
1. Ship MVP login [[MVP Launch]] - Score: 15
2. Call accountant [[Finances]] - Score: 10
3. Schedule dentist [[Health]] - Score: 9

💡 COACH NOTE
Good week ahead. You have 3 uninterrupted morning blocks.
Use them for deep work on the MVP.
```

---

## Throughout the Day

### Quick Capture (5 seconds)

When a thought, task, or idea pops into your head:

1. Open Logseq (phone or desktop)
2. Go to **Inbox** page
3. Type the thought (no formatting needed)
4. Close the app

**Examples:**
```
call mom about birthday
renew car insurance
idea: add dark mode to app
buy milk
```

Don't organize. Don't prioritize. Just capture.

### Completing Tasks

When you finish a task:

1. Open today's journal in Logseq
2. Change `TODO` to `DONE`
3. Continue to next task

Or just check the checkbox if using Logseq's checkbox format.

### Adding New Tasks

If you realize you need to do something specific today:

```
- TODO Buy groceries [[Family]]
- TODO Reply to client email [[Career]]
```

Link to a project when relevant using `[[Project Name]]`.

### Handling Interruptions

When something urgent comes up:

1. **Capture it** in Inbox (don't act immediately)
2. **Ask**: Is this more important than my ONE Thing?
3. **If yes**: Switch (and note why)
4. **If no**: It can wait until ONE Thing is done

---

## Triage Time

### When: Once daily (evening or next morning)

### Steps:

1. **Run triage command**
   ```bash
   > /triage
   ```

2. **Review suggestions**:
   - Claude categorizes each inbox item
   - Suggests where it should go
   - Identifies what to delete

3. **Confirm or adjust**:
   - Agree? Let Claude move items.
   - Disagree? Override specific items.

4. **Goal**: Empty inbox by end of session

### Sample Triage Output

```
INBOX TRIAGE (5 items)

1. "call mom about birthday"
   → Family | This Week | Move to [[Family]] page

2. "renew car insurance"
   → Finances | Today (due soon?) | Move to today's journal

3. "idea: add dark mode to app"
   → Career | Someday | Move to [[MVP Launch]] ideas section

4. "buy milk"
   → Delete (too small to track, just do it)

5. "random thought about life"
   → Delete (not actionable)

Confirm? [yes/adjust/cancel]
```

---

## Evening Wrap

### When: After Isha (or before bed)

### Steps:

1. **Run evening command**
   ```bash
   > /evening
   ```

2. **Review what got done**:
   - Did you complete your ONE Thing?
   - What else got done?
   - What's carrying over?

3. **Set tomorrow's priority**:
   - Claude suggests based on deadlines and goals
   - Accept or override

4. **Clear your mind**:
   - Everything is captured
   - Tomorrow is planned
   - Sleep well

### Sample Evening Output

```
EVENING WRAP: Monday, December 23

✅ DONE TODAY
- [x] Ship MVP login feature
- [x] Team standup
- [x] School pickup

ONE Thing: COMPLETED ✓

📋 CARRYING OVER
- [ ] Call accountant (moved to tomorrow)
- [ ] Schedule dentist (not urgent)

🎯 TOMORROW'S ONE THING
Suggested: Test MVP login with beta users
Why: Builds on today's progress, tight deadline

Inbox: 2 items (consider /triage)
```

---

## Weekly Rhythm

### Sunday Evening (30 min)

1. **Run weekly review**
   ```bash
   > /review
   ```
   - See wins and misses
   - Check metrics (deep work hours, exercise, etc.)
   - Get coaching feedback

2. **Run weekly planning**
   ```bash
   > /plan-week
   ```
   - Set 3-5 key outcomes
   - Plan daily ONE Things
   - Check capacity

### The Weekly Review Shows:

- ONE Things completed vs planned
- Deep work hours
- Exercise sessions
- Prayer consistency
- Family time
- Project progress
- Values alignment
- Trends (up/down/stable)

---

## On-Demand Commands

### When Overwhelmed

```bash
> /coach
```

The AI will:
- Analyze your patterns
- Detect if you're overcommitting
- Suggest what to cut
- Help you refocus on priorities

### When Stuck

```bash
> /coach
```

The AI will:
- Identify what's blocking you
- Challenge you if you're avoiding
- Break down the task
- Set accountability

---

## Tips for Success

### The 3 Rules

1. **Capture fast, organize later**
   - Don't let thoughts escape
   - Inbox is your safety net

2. **ONE Thing first**
   - Do the most important task before distractions
   - Morning hours are sacred

3. **Trust the system**
   - Let AI prioritize based on your values
   - You focus on execution

### What NOT to Do

- Don't spend 20 minutes "planning" each day
- Don't reorganize your system every week
- Don't feel guilty about empty days
- Don't track everything (Streaks handles habits)
- Don't use this for reference material (use Notion/Drive for that)

### Energy Management

- **High energy (morning)**: ONE Thing, deep work
- **Medium energy (afternoon)**: Meetings, calls, admin
- **Low energy (evening)**: Light tasks, family, rest

Match your tasks to your energy.

---

## Quick Reference

| Time | Action | Command |
|------|--------|---------|
| Morning | Get prioritized day | `/morning` |
| Anytime | Capture thought | Add to Inbox |
| Daily | Process inbox | `/triage` |
| Evening | Wrap up day | `/evening` |
| When stuck | Get coaching | `/coach` |
| Sunday | Review week | `/review` |
| Sunday | Plan week | `/plan-week` |

---

## Your First Week

### Day 1 (Today)
- [ ] Run `/morning`
- [ ] Note your ONE Thing
- [ ] Capture 3 things in Inbox
- [ ] Run `/evening`

### Day 2-5
- [ ] Morning briefing daily
- [ ] Capture throughout day
- [ ] Triage inbox daily
- [ ] Evening wrap daily

### Day 7 (Sunday)
- [ ] Run `/review`
- [ ] Run `/plan-week`
- [ ] Celebrate your first week!

---

*Remember: The goal is not productivity for its own sake. It's to free up time and energy for what truly matters—your faith, your health, your family, and your purpose.*
