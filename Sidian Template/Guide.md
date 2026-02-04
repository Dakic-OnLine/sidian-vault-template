
## Folder Organization

```
 01_ThinkingLines/     # Long-form thinking and conceptual notes
02_Diary/             # Daily journal entries (YYYY-MM-DD.md)
03_Goals/             # Long-term goals and their plans
  └─ Archive/         # Inactive/paused goals (excluded from reviews)
30_Weekly_Plans/      # Weekly execution plans (links to goals)
31_Monthly_Reviews/   # Monthly reviews and goal adjustments
32_Quarterly_Strategy/ # Quarterly strategy and new goal creation
50_Reports/           # Reports organized by type
  ├─ Daily/           # Daily reports (YYYY-MM-DD Report.md)
  ├─ Research/        # Research reports (Research - Topic.md)
  └─ Review/          # Review reports (Review - Topic.md)
92_Longer_writes/     # Extended writing pieces
99_Assets/            # Templates and scripts
  └─ templates/       # All interval templates (daily, weekly, monthly, quarterly)
```

## Planning System

### Time Hierarchy

| Level | Folder | Purpose | File Naming |
|-------|--------|---------|-------------|
| Quarterly | `32_Quarterly_Strategy/` | High-level strategy, new goals | `YYYY-Q#.md` |
| Monthly | `31_Monthly_Reviews/` | Review progress, adjust goals | `YYYY-MM.md` |
| Weekly | `30_Weekly_Plans/` | Execute on goals, daily breakdown | `YYYY-W##.md` |
| Goals | `03_Goals/` | Long-term goals and plans | `Goal Name.md` |
| Daily | `02_Diary/` | Journal entries | `YYYY-MM-DD.md` |

### How They Connect

1. **Quarterly Strategy** (`32_Quarterly_Strategy/`):
   - Defines 3 core focus areas for the quarter
   - Creates new goals in `03_Goals/`
   - Breaks down into monthly priorities

2. **Monthly Reviews** (`31_Monthly_Reviews/`):
   - Review progress on all goals
   - Adjust priorities based on what's working
   - Link back to goals in `03_Goals/`

3. **Weekly Plans** (`30_Weekly_Plans/`):
   - Link to specific goals being worked on
   - Daily task breakdown
   - End-of-week review for learning

4. **Goals** (`03_Goals/`):
   - Remain the source of truth for what you want to achieve
   - Paired with `Goal Name - Plan.md` for next steps

### Example Workflow

```
32_Quarterly_Strategy/2025-Q1.md
├── Creates → [[KDP notebooks]] in 03_Goals/
│
31_Monthly_Reviews/2025-01.md
├── Reviews → [[KDP notebooks]] progress
│
30_Weekly_Plans/2025-W01.md
├── Links to → [[KDP notebooks]]
└── Daily tasks from → [[KDP notebooks - Plan]]
│
03_Goals/KDP notebooks.md
└── Contains plan link → [[KDP notebooks - Plan]]
```

---

# Report Generation Instructions

Create a concise daily report that observes patterns, tracks goals, and provides encouragement.

## Report Format
- **Format**: Markdown (.md)
- **Location**: `50_Reports/Daily/` folder
- **Filename**: `YYYY-MM-DD Report.md` (today's date)
- **Always overwrite** existing reports

## After Creating Report
- **Send email**: From parent folder, run `bun run send-daily-report` to email the report
- The script reads today's report and sends it via the Resend email service

## Report Structure

```markdown
# Daily Report - YYYY-MM-DD

## Diary Snapshot: [[YYYY-MM-DD]]

[One-line summary of the day's mood/theme]

### Thinking Patterns
[Observation of recurring thought patterns, cognitive loops, or mental habits noticed in recent entries]

### Journal Feedback
[Constructive feedback on journaling quality, honesty, self-awareness, or areas to explore deeper]

---

## Goals & Next Steps

| Goal | Status | Next Action |
|------|--------|-------------|
| [[Goal - Name]] | On Track/Stalled | [First unchecked item] |
| [[Plan - Name]] | Orphaned | [First unchecked item] |

---

## Goal Clarification Questions

[Questions about goals that need clarification or could be improved]

### [[Goal Name]]
- Question that would help clarify this goal
- Suggestion for improvement

---

## Today's Reviews & Research (if any)

- [[Review - Topic Name]] - [Brief description]
- [[Research - Topic Name]] - [Brief description]

---

## Summary & Encouragement

[1-2 sentences of honest reflection + 1 encouraging sentence + 1 concrete suggestion for today]
```

## Content Guidelines

### Diary Snapshot
- Read **latest entry** from `02_Diary/` (find by date-sorted filename)
- One-line summary capturing the essence
- Translate Serbian to English if needed
- Use Wikilink: `[[YYYY-MM-DD]]`

### Thinking Patterns
- Look across **recent entries** for patterns (rumination, avoidance, optimism loops, etc.)
- Note connections between mood and productivity
- Keep it brief (2-3 bullets max)

### Journal Feedback
- Comment on journaling quality (depth, honesty, consistency)
- Gently point out avoided topics
- Celebrate self-awareness when present

### Goals & Next Steps
- Review **active** files in `03_Goals/` (exclude `Archive/` subfolder)
- Goals are named `Goal Name.md` and link to their plan with `Plan: [[Goal Name - Plan]]`
- Plans are named `Goal Name - Plan.md` and link back with `Goal: [[Goal Name]]`
- For goals with plans: read plan, extract first unchecked item
- Mark orphaned plans (plans with "Status: Orphaned" in file)
- Use **table format** for brevity
- Use Wikilinks: `[[filename]]`

### Goal Clarification Questions
- Review each goal for clarity, specificity, and actionability
- Identify vague areas that could benefit from more detail
- Ask questions that help clarify:
  - Success criteria (how will you know when it's done?)
  - Timeline (when do you want to achieve this?)
  - Metrics (how will you measure progress?)
  - Dependencies (what else needs to happen first?)
- Note goals without plans - suggest creating one
- **User action**: Add answers either:
  - Directly in the goal file (edit `03_Goals/Goal Name.md`)
  - Via `Inbox.md` (add note, it will be processed next daily review)
- Only include this section when there are actual questions to ask

### Summary & Encouragement
- Honest: acknowledge struggles without judgment
- Encouraging: remind of progress or capability
- Actionable: one specific thing to do today
- Total: 2-3 sentences max

---

# Goal Linking

## Implicit Goal Mentions

Daily diary entries often mention goals indirectly without linking to them. When generating reports, identify these mentions and add proper Wikilinks.

## How to Identify

Look for mentions of:
- **Projects** (KDP, RPG game, app ideas, etc.)
- **Habits** (exercise, meditation, reading, etc.)
- **Learning topics** (languages, skills, technologies)
- **Health goals** (diet, fasting, medical checkups)
- **Financial goals** (saving, investing, business ventures)

## Linking Process

When you find an implicit goal mention in a diary entry:

1. **Check if goal exists**: Look in `03_Goals/` for matching goal
2. **If goal exists**: Add Wikilink in diary entry
3. **If no goal exists**: Consider noting it in "Suggestions" as a potential goal to formalize

## Examples

### Before (Diary Entry)
```markdown
Danas sam razmišljao o Sudoku knjigama. Treba da instaliram KDP software.
```
(Translation: Today I was thinking about Sudoku books. I need to install KDP software.)

### After (With Link)
```markdown
Danas sam razmišljao o Sudoku knjigama. Treba da instaliram KDP software. [[Create KDP notebooks]]
```

### Before (Diary Entry)
```markdown
Finally started working out again. Going to try to keep it up this time.
```

### After (With Link)
```markdown
Finally started working out again. Going to try to keep it up this time. [[Exercise regularly]]
```

## Report Integration

When generating daily reports:
- **Diary Snapshot**: If the entry mentions an existing goal, include the link
- **Goals Table**: Cross-reference - if diary worked on a goal, note it in the status column
- **Suggestions**: If you notice recurring mentions of a topic that has no goal file, suggest creating one

## Length Target
- **Entire report**: ~40-60 lines
- **Each section**: concise, scannable
- **Avoid repetition**: don't restate same points across sections

---

# Updating Goals from Daily Journals

## When Writing Daily Entries

As you write in your daily diary (`02_Diary/YYYY-MM-DD.md`), make it a habit to:

### 1. Link to Goals When You Mention Them

When you write about working on a project, habit, or goal, add a Wikilink:

```markdown
Danas sam radio na KDP knjigama. Instalirao sam software i napravio prve strane. [[KDP notebooks]]
```

This creates a connection between your daily thoughts and your formal goals.

### 2. Update Goal Plans When You Complete Tasks

When you complete a task that was in your goal's plan, open the plan file and check it off:

1. Navigate to `03_Goals/Goal Name - Plan.md`
2. Find the completed task
3. Change `- [ ]` to `- [x]`

Example:
```markdown
## KDP notebooks - Plan

- [x] Install KDP software  ← Completed!
- [ ] Create test layouts
- [ ] Publish first book
```

### 3. Add Progress Notes to Goal Files

When you make significant progress on a goal, add a note to the main goal file:

```markdown
## My goal
Create write on notebooks for Amazon KDP...

## Progress Log
### 2026-01-02
Installed KDP software and created first Sudoku layouts. Ready to format.
```

### 4. Create Goals for Recurring Themes

If you notice yourself writing about the same topic repeatedly (3+ times), consider creating a formal goal:

1. Create new file in `03_Goals/Goal Name.md`
2. Create corresponding plan: `Goal Name - Plan.md`
3. Link from future diary entries using `[[Goal Name]]`

## Daily Workflow Checklist

When journaling:
- [ ] Did I mention any goals? → Add Wikilink: `[[Goal Name]]`
- [ ] Did I complete any planned tasks? → Check off in `Goal Name - Plan.md`
- [ ] Did I make progress? → Add note to `Goal Name.md`
- [ ] Any new recurring themes? → Consider creating a new goal

## Benefits

- **Traceability**: See what you worked on each day
- **Progress tracking**: Goals automatically document your journey
- **Motivation**: Checked items show progress over time
- **Connections**: Diary entries become searchable by goal

---

# Goal Archiving

## What to Archive

Move goals to `03_Goals/Archive/` when:
- Project is paused or cancelled
- Goal is no longer relevant
- You want to focus on other priorities
- Goal is completed (for historical reference)

## How to Archive

1. Move goal file(s) to `03_Goals/Archive/`
   - Main goal: `Goal Name.md`
   - Plan: `Goal Name - Plan.md` (if exists)

2. Archived goals are **automatically excluded** from:
   - Daily reports (goals table)
   - Weekly plans (goal selection)
   - Monthly reviews (progress tracking)

## Reactivating Archived Goals

To bring back an archived goal:
1. Move files from `Archive/` back to `03_Goals/`
2. Goal will appear in next review cycle

---

# Review & Research Tag Processing

## Two Types of Requests

| Tag | Purpose | Output |
|-----|---------|--------|
| `#review` | Feedback, analysis, perspective on your question | `Review - Topic.md` (shorter, opinion/analysis) |
| `#research` | Deep research with web search, sources, findings | `Research - Topic.md` (longer, research-heavy) |

## Process

### For #review
1. **Scan for #review**: Search all notes for `#review` tag
2. **Read the note**: Understand what question needs feedback
3. **Provide analysis**: Give thoughtful feedback, perspective, or answer based on knowledge
4. **Create review** in `50_Reports/Review/` folder
5. **Replace tag**: `#review` → `[[Review - Topic Name]]`
6. **Send email** with the review: From parent folder, run `bun run send-report Svastara/50_Reports/Review/Review-Topic.md`

### For #research
1. **Scan for #research**: Search all notes for `#research` tag
2. **Read the note**: Understand what topic needs research
3. **Launch parallel subagents**:
   - Use independent subagents for each research topic
   - Launch multiple research agents in parallel when multiple `#research` tags exist
   - Each subagent handles web search, source reading, and synthesis independently
4. **Create research report** in `50_Reports/Research/` folder (subagent will do this)
5. **Replace tag**: `#research` → `[[Research - Topic Name]]`
6. **Send email** with the research: From parent folder, run `bun run send-report Svastara/50_Reports/Research/Research-Topic.md`

**Why use parallel subagents:**
- Multiple research tasks can run simultaneously without blocking each other
- Each research topic gets dedicated attention and context
- Faster completion - no waiting for one research task to finish before starting another

## Formats

### Review Format (#review)

```markdown
# Review: [Topic Name]

**Source:** [[Original Note]]

**Date:** YYYY-MM-DD

## Feedback
[Your analysis, perspective, or answer to the question - 3-5 sentences]

## Key Points
- [Point 1]
- [Point 2]

## Recommendation
[1-2 sentences of actionable advice]
```

### Research Format (#research)

```markdown
# Research: [Topic Name]

**Source:** [[Original Note]]

**Date:** YYYY-MM-DD

## Summary
[2-3 sentence overview of findings]

## Key Findings
- [Finding 1]
- [Finding 2]
- [Finding 3]

## Sources
- [Source 1](URL)
- [Source 2](URL)

## Notes
[Additional context, quotes, or relevant details]
```

## File Naming

Both go in `50_Reports/` subfolders:
- `#review` → `Review/[Topic Name].md` (creates `Review - Topic Name.md`)
- `#research` → `Research/[Topic Name].md` (creates `Research - Topic Name.md`)

## Examples

### #review Example

Before:
```markdown
Should I quit my job and start a business? #review
```

After:
```markdown
Should I quit my job and start a business? [[Review - Career Change Risk]]
```

Review gives thoughtful analysis based on context, no web search needed.

### #research Example

Before:
```markdown
What are the latest trends in AI agents for 2025? #research
```

After:
```markdown
What are the latest trends in AI agents for 2025? [[Research - AI Agent Trends 2025]]
```

Research includes web search, sources, and synthesized findings.

## Daily Report Integration

When generating daily reports, check if the diary entry contains `#review` or `#research` tags:

1. **If found**: Launch parallel subagents to create all review/research reports simultaneously
2. **Then**: In the daily report, add a section linking to them:

```markdown
---

## Today's Reviews & Research

- [[Review - Topic Name]] - [Brief description]
- [[Research - Topic Name]] - [Brief description]

---
```

**Note:** Use the Task tool with subagent_type='general-purpose' to launch independent research agents for each `#research` topic. Launch them in parallel (same message with multiple Task tool calls) for maximum efficiency.

---

# Daily Review & Inbox Processing

## Overview

The daily review process captures random thoughts from `Inbox.md`, tags them, and distributes them to appropriate locations.

## Tag Types

| Tag | Meaning | Typical Content |
|-----|---------|-----------------|
| `#idea` | A concept, possibility, or future consideration | "Maybe I should...", "What if...", "Could try..." |
| `#note` | General observation, reflection, or record | "I noticed that...", "Today was...", "Feeling like..." |
| `#action` | Something to implement or do | "Create a system for...", "Build...", "Set up..." |
| `#review` | Request for feedback/analysis on a question | "What do you think about...", "Review this idea..." |
| `#research` | Request for deep research with sources | "Research pricing for...", "Find best practices for..." |

**IMPORTANT:** When Inbox contains `#review` or `#research` tags, **CREATE THE ACTUAL REPORT**, not a todo about creating it. Execute the review/research immediately during inbox processing.

## Process

### Step 1: Process @Inbox.md

For each paragraph (blank-line separated) in `Inbox.md`:

1. **Read the note**
2. **Tag it**: `#idea` | `#note` | `#action` | `#review` | `#research`
3. **For #action and #note**: Move to diary by appending to `02_Diary/YYYY-MM-DD.md`
4. **For #review**: CREATE THE REVIEW immediately in `50_Reports/Review/`, then replace tag with link, then send email
5. **For #research**: CREATE THE RESEARCH immediately in `50_Reports/Research/`, then replace tag with link, then send email
6. **Add to daily report** (if `#action` or significant `#idea`): Add to `50_Reports/Daily/YYYY-MM-DD Report.md`
7. **Remove from Inbox**: Delete processed note

### Step 2: Complete Daily Report

Follow the report format above, including any new items from the inbox. Create in `50_Reports/Daily/YYYY-MM-DD Report.md`.

## Automation

When AI processes inbox:

1. **For #action and #note**: Append to today's diary with tag
2. **For #review**: Create review report immediately, link from diary, send via email
3. **For #research**: Launch research subagent immediately, link from diary when complete, send via email
4. **Clear Inbox.md** when all items processed

The manual script (if used):

```bash
../scripts/daily_review.sh
```

The script will:
- Read each note from `Inbox.md`
- Ask you to choose a tag (1=#idea, 2=#note, 3=#action, 4=#review, 5=#research)
- Append to today's diary
- For #review/#research: create the report immediately and ask to send via email
- Optionally add to the daily report
- At end: ask to send daily report via email
- Clear `Inbox.md` when done

## Template

See `99_Assets/tm_daily_review.md` for the full daily review template.

---

# Weekly Plan Creation

## Overview

Create a weekly plan based on recent daily notes, active goals, and their plans. This bridges the gap between daily reflections and long-term goals.

## Process

### Step 1: Review Recent Diary Entries

Read the latest entries from `02_Diary/` (past 3-7 days) to understand:
- What you've been working on
- Patterns and themes
- Blocks or challenges
- Ideas mentioned

### Step 2: Review Active Goals

Read **active** files in `03_Goals/` (exclude `Archive/` subfolder):
- Main goal files (e.g., `Goal Name.md`)
- Plan files (e.g., `Goal Name - Plan.md`)
- Extract next actions from plan checklists

### Step 3: Determine Week Focus

Based on diary and goals, identify 1-2 main focuses for the week.

### Step 4: Create Daily Breakdown

Using the template (`99_Assets/templates/tm_weekly_plan.md`), create:
- File: `30_Weekly_Plans/YYYY-W##.md`
- Link to goals being worked on
- Break down goal tasks into daily actionable items
- Include habits (Gateway meditation, exercise, etc.)

### Step 5: Complete Weekly Review

At end of week, fill out the review section:
- Wins: What went well
- Challenges: What was difficult
- Lessons learned: What you discovered
- Next week adjustments: What to change

## Weekly Plan Format

```markdown
# Week ## (YYYY-MM-DD to YYYY-MM-DD)

## Focus
[1-2 sentence main focus for the week]

## Goals to Work On
- [[Goal Name 1]]
- [[Goal Name 2]]
- [[Goal Name 3]]

## Daily Plan

### Monday - YYYY-MM-DD
- [ ] Task from Goal 1 plan
- [ ] Task from Goal 2 plan
- [ ] Habit item (Gateway, exercise, etc.)

### Tuesday - YYYY-MM-DD
- [ ] Task from Goal 1 plan
- [ ] Task from Goal 2 plan
- [ ] Habit item

[... continue for each day ...]

### Weekend - YYYY-MM-DD to YYYY-MM-DD
- [ ] Weekly review
- [ ] Rest and reflection
- [ ] Plan next week

## Notes
- Patterns identified
- Health/finance targets
- Blockers or dependencies

## Weekly Review (fill out at end of week)
**Wins:**
- [Win 1]
- [Win 2]

**Challenges:**
- [Challenge 1]
- [Challenge 2]

**Lessons learned:**
- [Lesson 1]
- [Lesson 2]

**Next week adjustments:**
- [Adjustment 1]
- [Adjustment 2]
```

## Automation

Run the weekly plan creation:
```bash
ask AI: "Create weekly plan based on my daily notes"
```

The AI will:
1. Read recent diary entries
2. Review active goals and plans
3. Create a new weekly plan file
4. Include daily tasks based on goal next steps
5. Note patterns and targets from diary

## Example

**From Diary (2025-12-29):**
```
Danas je ponedeljak, pocetak nedelje...
Da KDP projekat dovedem dotle da mogu da objavim knjigu.
Da Hypr moze da se prijavi korisnik, da moze da plati.
```

**From Goals:**
```
KDP notebooks - Plan: Install software, create test pages
HyprCreate MVP - Plan: Enable registration, payment, create course
```

**Creates Weekly Plan (2025-W01):**
```markdown
## Focus
Launch two income streams: KDP notebooks and HyprCreate user acquisition.

## Goals to Work On
- [[KDP notebooks]]
- [[HyprCreate MVP]]

### Monday - 2024-12-30
- [ ] Download and install KDP software
- [ ] Fix Google login issue in HyprCreate
- [ ] Morning: Gateway meditation
```



## Example

**Before (@Inbox.md):**
```markdown
I want to split day into intervals, intervals and make sure that I do one thing during each interval.

I also want to create an inbox node that I will just record my random thoughts there and based on what I'm saying it will be distributed to other nodes.
```

**After (02_Diary/2025-12-27.md):**
```markdown
---

#idea Day intervals: Split day into focused blocks
- Morning interval: till 11am
- Noon interval: 11am - 2pm
...

#action Inbox node system: Create capture point for random thoughts that get distributed to relevant nodes/plans

```

**After (50_Reports/2025-12-27 Report.md):**
```markdown
## New Ideas & Actions

- **Day intervals system** (#idea): Split day into focused time blocks for single-tasking
- **Inbox node system** (#action): Create capture point for random thoughts that auto-distribute
```

