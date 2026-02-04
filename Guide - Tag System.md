# Tag System

Tags help you categorize and find content across your vault. Use them consistently for best results.

## Core Tags

### Status Tags

| Tag | Meaning | Used On |
|-----|---------|---------|
| `#active` | Currently being worked on | Goals, projects |
| `#stalled` | Blocked or paused | Goals, projects |
| `#completed` | Finished | Goals, projects |
| `#developing` | Being explored | Goals in `03_Goals/Developing/` |

### Content Type Tags

| Tag | Meaning | Example |
|-----|---------|---------|
| `#idea` | A concept or possibility | "Maybe I should try..." |
| `#note` | General observation | "I noticed that..." |
| `#action` | Something to do | "Create a system for..." |
| `#review` | Request for feedback | "What do you think about..." |
| `#research` | Needs investigation | "Research best practices for..." |

### Area Tags

| Tag | Area | Example Files |
|-----|------|---------------|
| `#health` | Physical & mental health | Exercise goals, diet notes |
| `#finance` | Money, investing, business | Savings goals, income ideas |
| `#work` | Career, projects, skills | Work projects, learning |
| `#learning` | Skills, education, study | Language goals, courses |
| `#relationships` | Family, friends, community | Social goals, reflections |
| `#creative` | Writing, art, creative projects | Stories, designs, ideas |

## Tag Conventions

### Multi-word Tags

Use hyphens for multi-word concepts:
- `#deep-work` not `#deep work`
- `#time-blocking` not `#time blocking`

### Tag Hierarchy

Use `parent/child` structure for related concepts:
- `#goal/active` - Active goals
- `#goal/archived` - Archived goals
- `#project/creative` - Creative projects
- `#project/work` - Work projects

### When to Use Tags

**Use tags when:**
- Content spans multiple folders (cross-referencing)
- You want to see all items of a type in one place
- You need quick filtering (e.g., show all `#health` items)

**Use folders when:**
- Content has a clear home (diary, goals, reports)
- Structure matters more than flexible categorization
- Date-based organization makes sense

## Tag Workflows

### Inbox Processing

When processing `Inbox.md`, add appropriate tags:
- What type of content is it? (`#idea`, `#note`, `#action`)
- What area does it relate to? (`#health`, `#work`, `#learning`)
- Does it need follow-up? (`#review`, `#research`)

### Goal Tracking

Tag goals with status and area:
- `[[Learn Spanish]]` → `#active #learning`
- `[[Exercise regularly]]` → `#stalled #health`
- `[[Remote Work]]` → `#developing #work`

### Daily Reviews

When generating daily reports, tags help identify patterns:
- "Noticed three `#health` mentions this week - exercise habit forming?"
- "Many `#work` tasks stalled - blockers to investigate?"

## Finding Tags

### In Obsidian

1. **Tag pane** - Shows all tags with counts (enable in Settings → File & Links)
2. **Search** - Type `#tagname` in search to see all matching files
3. **Backlinks** - Hover over a tag to see files using it

### Quick Queries

Use Dataview plugin (optional) for tag queries:
```dataview
LIST
WHERE contains(tags, "#active")
SORT file.ctime DESC
```

## Recommended Tag Sets

### For Goals
- `#active`, `#stalled`, `#completed`, `#developing`
- Area tags: `#health`, `#finance`, `#work`, `#learning`

### For Diary
- Mood tags: `#mood/good`, `#mood/okay`, `#mood/low`
- Activity tags: `#deep-work`, `#social`, `#exercise`, `#rest`

### For Projects
- Status tags: `#planning`, `#in-progress`, `#on-hold`, `#done`
- Type tags: `#creative`, `#technical`, `#business`

---

**Tip**: Start simple. You can always refine your tag system as you use it. Better to have 5 useful tags than 50 unused ones.
