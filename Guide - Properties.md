# Properties (Metadata)

Properties (formerly called "frontmatter") add structured metadata to your notes. They help with sorting, filtering, and organizing.

## What Are Properties?

Properties are key-value pairs at the top of a file:

```markdown
---
status: active
area: learning
target_date: 2026-12-31
tags: [language, spanish]
---

# Goal content here...
```

## Essential Properties for Goals

| Property | Values | Purpose |
|----------|--------|---------|
| `status` | `active`, `stalled`, `completed`, `developing` | Quick filtering |
| `area` | `health`, `finance`, `work`, `learning` | Categorization |
| `target_date` | `YYYY-MM-DD` | Deadline tracking |
| `start_date` | `YYYY-MM-DD` | When you started |
| `priority` | `high`, `medium`, `low` | What to focus on |
| `tags` | `[tag1, tag2]` | Alternative to inline tags |

## Example: Goal with Properties

```markdown
---
status: active
area: learning
start_date: 2026-01-01
target_date: 2026-12-31
priority: high
tags: [language, spanish, daily]
---

# Learn Spanish

Reach conversational fluency within 12 months.

Plan: [[Learn Spanish - Plan]]
```

## Properties by Folder

### 03_Goals/

```yaml
status: active
area: health | finance | work | learning
target_date: YYYY-MM-DD
priority: high | medium | low
```

### 02_Diary/

```yaml
date: YYYY-MM-DD
mood: good | okay | low
energy: high | medium | low
```

### 30_Weekly_Plans/

```yaml
week: WW
start_date: YYYY-MM-DD
end_date: YYYY-MM-DD
focus: [Brief description]
```

### 50_Reports/Daily/

```yaml
date: YYYY-MM-DD
type: daily_report
```

## Using Properties

### Adding Properties

1. Open a file in Obsidian
2. Click the "Add property" button at the top
3. Or type `---` at the top and press Enter

### Filtering by Properties

**Without plugins:**
- Search for a property value: `status:active`
- Use the file list and sort by property

**With Dataview plugin:**
```dataview
TABLE status, target_date, priority
FROM "03_Goals"
WHERE status = "active"
SORT priority DESC
```

### Property Types

| Type | Example | Usage |
|------|---------|-------|
| Text | `area: learning` | Words, phrases |
| Number | `hours: 30` | Quantities |
| Date | `target_date: 2026-12-31` | Dates for sorting |
| Checkbox | `completed: true` | Yes/no values |
| List | `tags: [work, urgent]` | Multiple values |
| Link | `related: [[Other Note]]` | Connections |

## Property Templates

### Goal Template

```yaml
---
status: active
area:
target_date:
priority: medium
tags: []
---
```

### Diary Entry Template

```yaml
---
date:
mood:
energy:
weather:
location:
---
```

### Project Template

```yaml
---
status: planning
start_date:
target_date:
budget:
tags: []
---
```

## Tips for Using Properties

1. **Be consistent** - Use the same values (e.g., always `active` not `Active` or `in progress`)
2. **Start simple** - Add properties as you need them, not all at once
3. **Use dates wisely** - Use `YYYY-MM-DD` format for proper sorting
4. **Link where helpful** - Use link properties to connect related notes
5. **Review regularly** - Update status properties during reviews

## Properties vs Tags

| Use Properties When | Use Tags When |
|---------------------|---------------|
| You need to sort by the value | You need flexible categorization |
| There are defined options (status, priority) | Content spans multiple topics |
| You want structured data | You want quick, informal labeling |
| Building queries or reports | Browsing and serendipitous discovery |

---

**Note**: Properties work best when you have a clear use case. Don't add properties just because you can - add them because they solve a problem (sorting, filtering, tracking).
