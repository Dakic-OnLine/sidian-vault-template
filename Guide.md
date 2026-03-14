# Guide

## Contents

- [Folder Organization](#folder-organization)
- [Planning System](#planning-system)
- [Report Generation](#report-generation-instructions)
- [Goal Management](#updating-goals-from-daily-journals)
- [Tag System](#tag-system)
- [Review & Research](#review--research-tag-processing)
- [Daily Review Process](#daily-review--inbox-processing)
- [Weekly Planning](#weekly-plan-creation)

---

## Folder Organization

```
00_Inbox/            # Quick capture for thoughts, ideas, assignments
01_Journal/          # Daily journal entries (YYYY-MM-DD.md)
02_MindSpace/        # Conceptual notes and thinking pieces
  └─ _LongWriting/   # Extended writing pieces and essays
03_Goals/            # Aspirations and long-term direction
  ├─ Archive/        # Inactive/paused goals (excluded from reviews)
  └─ Developing/     # Goals still being formed or explored
04_Planning/         # Weekly, Monthly, Quarterly plans
  ├─ 1_Weekly/       # Weekly execution plans (YYYY-W##.md)
  ├─ 2_Monthly/      # Monthly reviews (YYYY-MM.md)
  └─ 3_Quarterly/    # Quarterly strategy (YYYY-Q#.md)
05_Projects/         # Active projects (concrete work)
  ├─ Backlog/        # Planned but not started
  └─ Archive/        # Completed or paused
50_Reports/          # Reports organized by type
  ├─ Daily/          # Daily reports (YYYY-MM-DD Report.md)
  ├─ Research/       # Research reports (Research - Topic.md)
  └─ Review/         # Review reports (Review - Topic.md)
99_Assets/           # Templates
  └─ templates/      # All interval templates (daily, weekly, monthly, quarterly)
```

## Planning System

### Time Hierarchy

| Level | Folder | Purpose | File Naming |
|-------|--------|---------|-------------|
| Quarterly | `04_Planning/3_Quarterly/` | High-level strategy, new goals | `YYYY-Q#.md` |
| Monthly | `04_Planning/2_Monthly/` | Review progress, adjust goals | `YYYY-MM.md` |
| Weekly | `04_Planning/1_Weekly/` | Execute on goals, daily breakdown | `YYYY-W##.md` |
| Goals | `03_Goals/` | Long-term aspirations and direction | `Goal Name.md` |
| Projects | `05_Projects/` | Concrete work with deliverables | `Project Name.md` |
| Daily | `01_Journal/` | Journal entries | `YYYY-MM-DD.md` |

### How They Connect

1. **Quarterly Strategy** (`04_Planning/3_Quarterly/`):
   - Defines 3 core focus areas for the quarter
   - Creates new goals in `03_Goals/`
   - Breaks down into monthly priorities

2. **Monthly Reviews** (`04_Planning/2_Monthly/`):
   - Review progress on all goals
   - Adjust priorities based on what's working
   - Link back to goals in `03_Goals/`

3. **Weekly Plans** (`04_Planning/1_Weekly/`):
   - Link to specific goals being worked on
   - Daily task breakdown
   - End-of-week review for learning

4. **Goals** (`03_Goals/`):
   - Remain the source of truth for what you want to achieve
   - Paired with `Goal Name - Plan.md` for next steps

### Example Workflow

```
04_Planning/3_Quarterly/2025-Q1.md
├── Creates → [[Launch online store]] in 03_Goals/
│
04_Planning/2_Monthly/2025-01.md
├── Reviews → [[Launch online store]] progress
│
04_Planning/1_Weekly/2025-W01.md
├── Links to → [[Launch online store]]
└── Daily tasks from → [[Launch online store - Plan]]
│
03_Goals/Launch online store.md
└── Contains plan link → [[Launch online store - Plan]]
```
04_Planning/3_Quarterly/2025-Q1.md
├── Creates → [[Launch online store]] in 03_Goals/
│
04_Planning/2_Monthly/2025-01.md
├── Reviews → [[Launch online store]] progress
│
04_Planning/1_Weekly/2025-W01.md
├── Links to → [[Launch online store]]
└── Daily tasks from → [[Launch online store - Plan]]
│
03_Goals/Launch online store.md
└── Contains plan link → [[Launch online store - Plan]]
```

---

# Goals vs Projects

## The Difference

| Goals | Projects |
|-------|----------|
| **Aspirations** - what you want to become | **Work** - what you're building |
| Long-term direction | Specific deliverable |
| May never fully "complete" | Has a clear finish line |
| Inspires and motivates | Executes and ships |
| Lives in `03_Goals/` | Lives in `05_Projects/` |

## Examples

| Goal (Aspiration) | Project (Concrete) |
|-------------------|---------------------|
| Become a published author | Write my first novel |
| Get fit and healthy | Complete 12-week fitness program |
| Learn to code | Build a personal website |
| Build passive income | Launch an online course |
| Master photography | Complete 365 photo challenge |

## How They Work Together

1. **Goals give direction** - They answer "Why am I doing this?"
2. **Projects are the vehicle** - They answer "What am I building?"
3. **Plans connect them** - A goal's plan often includes specific projects

### Workflow

```
Goal: "Become a published author"
│
├── Project: "Write first novel" (Active)
│   └── Plan: Outline → Draft → Edit → Submit
│
└── Project: "Build author platform" (Backlog)
    └── Plan: Website → Social media → Newsletter
```

## When to Create a Project

Create a project when:
- There's a specific deliverable (a thing that will exist when done)
- You can define "done" clearly
- It supports one or more of your goals
- It requires multiple steps over time

## Project Lifecycle

1. **Backlog** (`05_Projects/Backlog/`) - Ideas you want to do but haven't started
2. **Active** (`05_Projects/` root) - Currently working on (limit to 2-3)
3. **Archived** (`05_Projects/Archive/`) - Completed, paused, or cancelled

---

# Report Generation Instructions

Create a concise daily report that observes patterns, tracks goals, and provides encouragement.

## Report Format
- **Format**: Markdown (.md)
- **Location**: `50_Reports/Daily/` folder
- **Filename**: `YYYY-MM-DD Report.md` (today's date)
- **Always overwrite** existing reports

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
- Read **latest entry** from `01_Journal/` (find by date-sorted filename)
- One-line summary capturing the essence
- Translate to your primary language if needed
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
- Review **active** files in `03_Goals/` (exclude `Archive/` and `Developing/` subfolders)
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

# Updating Goals from Daily Journals

## When Writing Daily Entries

As you write in your daily diary (`01_Journal/YYYY-MM-DD.md`), make it a habit to link and update your goals.

### What to Link

Look for mentions of:
- **Projects** (business ideas, creative work, app ideas)
- **Habits** (exercise, meditation, reading)
- **Learning topics** (languages, skills, technologies)
- **Health goals** (diet, fasting, medical checkups)
- **Financial goals** (saving, investing, business ventures)

### 1. Link to Goals When You Mention Them

When you write about working on a project, habit, or goal, add a Wikilink:

```markdown
Today I worked on my publishing project. Installed the software and created first pages. [[Publish notebooks]]
```

This creates a connection between your daily thoughts and your formal goals.

### 2. Update Goal Plans When You Complete Tasks

When you complete a task that was in your goal's plan, open the plan file and check it off:

1. Navigate to `03_Goals/Goal Name - Plan.md`
2. Find the completed task
3. Change `- [ ]` to `- [x]`

Example:
```markdown
## Publish notebooks - Plan

- [x] Install publishing software  ← Completed!
- [ ] Create test layouts
- [ ] Publish first book
```

### 3. Add Progress Notes to Goal Files

When you make significant progress on a goal, add a note to the main goal file:

```markdown
## My goal
Create and publish notebooks for online marketplace...

## Progress Log
### 2026-01-02
Installed publishing software and created first layouts. Ready to format.
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

# Goal Development

## What is Developing?

The `03_Goals/Developing/` folder is for goals that are still being formed or explored.

## When to Use Developing

Put goals in `Developing/` when:
- You're exploring an idea but not ready to commit
- The goal is still vague and needs definition
- You're testing whether it's worth pursuing
- You want to experiment before full commitment

## How to Move to Active

When the goal is clear and you're ready to commit:
1. Create proper goal file in `03_Goals/`
2. Create corresponding plan file
3. Delete from `Developing/` folder

## Difference from Archive

| Folder | Purpose | Included in Reviews? |
|--------|---------|---------------------|
| `Developing/` | Goals being explored | Yes, as "exploring" |
| `Archive/` | Inactive/paused goals | No |

---

# Maintaining Home.md

`Home.md` is your personal dashboard - the first thing you see when opening your vault. Keep it updated to reflect your current priorities.

## What to Update

### Current Focus Section

Update when:
- You **start** a new goal - add it to the list
- You **complete** a goal - remove it from the list
- You **archive** a goal - move it from Current Focus
- You **promote** a goal from Developing - add it here

### Developing Ideas Section

Update when:
- You move a goal to `03_Goals/Developing/` - add it here
- A developing goal becomes active - remove from here
- You abandon an exploration - delete from here

### Recent Activity Section

Update when:
- You create a new diary entry - link the latest one
- You create a weekly plan - link the current week
- You complete a monthly review - link the latest month

### Active Goals Overview Table

Update when:
- Goals change status (On Track → Stalled or vice versa)
- Next actions change
- Goals are added or removed

## How Often to Update

| Frequency | What to Update |
|-----------|----------------|
| **Daily** | Recent Activity links |
| **Weekly** | Active Goals Overview table, Current Focus |
| **Monthly** | Full review of all sections, remove completed items |

## Quick Update Checklist

During your weekly review:
- [ ] Are Current Focus goals still active?
- [ ] Any developing goals ready to promote?
- [ ] Are Recent Activity links current?
- [ ] Does the Goals Overview table reflect latest status?

## Automation Tips

If you use AI to generate reports, ask it to:
1. Suggest updates to Home.md based on recent activity
2. Identify goals that should be added or removed
3. Update the Active Goals Overview table with latest statuses

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

### For #research
1. **Scan for #research**: Search all notes for `#research` tag
2. **Read the note**: Understand what topic needs research
3. **Launch parallel subagents**:
   - Use independent subagents for each research topic
   - Launch multiple research agents in parallel when multiple `#research` tags exist
   - Each subagent handles web search, source reading, and synthesis independently
4. **Create research report** in `50_Reports/Research/` folder (subagent will do this)
5. **Replace tag**: `#research` → `[[Research - Topic Name]]`

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

The daily review process captures random thoughts from `00_Inbox/Inbox.md`, tags them, and distributes them to appropriate locations.

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

### Step 1: Process @00_Inbox/Inbox.md

For each paragraph (blank-line separated) in `00_Inbox/Inbox.md`:

1. **Read the note**
2. **Tag it**: `#idea` | `#note` | `#action` | `#review` | `#research`
3. **For #action and #note**: Move to diary by appending to `01_Journal/YYYY-MM-DD.md`
4. **For #review**: CREATE THE REVIEW immediately in `50_Reports/Review/`, then replace tag with link
5. **For #research**: CREATE THE RESEARCH immediately in `50_Reports/Research/`, then replace tag with link
6. **Add to daily report** (if `#action` or significant `#idea`): Add to `50_Reports/Daily/YYYY-MM-DD Report.md`
7. **Remove from Inbox**: Delete processed note

### Step 2: Complete Daily Report

Follow the report format above, including any new items from the inbox. Create in `50_Reports/Daily/YYYY-MM-DD Report.md`.

## Automation

When AI processes inbox:

1. **For #action and #note**: Append to today's diary with tag
2. **For #review**: Create review report immediately, link from diary
3. **For #research**: Launch research subagent immediately, link from diary when complete
4. **Clear 00_Inbox/Inbox.md** when all items processed

## Template

See `99_Assets/templates/tm_daily_review.md` for the full daily review template.

---

# Weekly Plan Creation

## Overview

Create a weekly plan based on recent daily notes, active goals, and their plans. This bridges the gap between daily reflections and long-term goals.

## Process

### Step 1: Review Recent Diary Entries

Read the latest entries from `01_Journal/` (past 3-7 days) to understand:
- What you've been working on
- Patterns and themes
- Blocks or challenges
- Ideas mentioned

### Step 2: Review Active Goals

Read **active** files in `03_Goals/` (exclude `Archive/` and `Developing/` subfolders):
- Main goal files (e.g., `Goal Name.md`)
- Plan files (e.g., `Goal Name - Plan.md`)
- Extract next actions from plan checklists

### Step 3: Determine Week Focus

Based on diary and goals, identify 1-2 main focuses for the week.

### Step 4: Create Daily Breakdown

Using the template (`99_Assets/templates/tm_weekly_plan.md`), create:
- File: `04_Planning/1_Weekly/YYYY-W##.md`
- Link to goals being worked on
- Break down goal tasks into daily actionable items
- Include habits (morning routine, exercise, etc.)

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
- [ ] Habit item (morning routine, exercise, etc.)

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

**From Diary:**
```
Today is Monday, start of the week...
Need to get the publishing project to the point where I can publish a book.
Need the app to accept user registration and payments.
```

**From Goals:**
```
Publish notebooks - Plan: Install software, create test pages
SaaS MVP - Plan: Enable registration, payment, create course
```

**Creates Weekly Plan:**
```markdown
## Focus
Launch two income streams: publish notebooks and SaaS user acquisition.

## Goals to Work On
- [[Publish notebooks]]
- [[SaaS MVP]]

### Monday - YYYY-MM-DD
- [ ] Download and install publishing software
- [ ] Fix login issue in app
- [ ] Morning: meditation
```
