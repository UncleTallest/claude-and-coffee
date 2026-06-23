---
layout: guide
title: 'Google Drive Setup'
---

# Google Drive Setup

## Why Google Drive

- Already where many people keep their stuff
- Sharing with collaborators (human or AI) is a single permission toggle
- Read and edit files from phone, tablet, computer
- No command line, no repository, no deployment
- If you can organize a folder for a project at work, you can run this system

## The Folder Structure

```
Claude System (root folder)/
├── Standing/
│   ├── Communication-Guide.md
│   ├── Current-State-Snapshot.md
│   └── [other always-relevant docs]
├── Instances/
│   ├── Professional/
│   │   ├── Session-Summaries/
│   │   ├── Working-Drafts/
│   │   └── Decisions/
│   ├── Personal/
│   │   ├── Session-Summaries/
│   │   └── Notes/
│   └── Creative/
│       ├── Session-Summaries/
│       └── Projects/
└── Handoffs/
    ├── To-Professional/
    └── To-Personal/
```

### Standing Folder

Documents that get loaded regularly:

- Communication Guide
- Financial snapshots
- Project status documents
- Anything stable and frequently referenced

### Instance Folders

Each Claude instance (Professional, Personal, Creative, etc.) gets its own folder for:

- Session summaries
- Drafts and in-progress work
- Instance-specific notes

Keeps each instance's work separate and organized.

### Handoffs Folder

When something needs to cross instances, drop it here:

- Personal Claude creates note → puts in Handoffs/To-Professional
- You copy-paste when convenient to Professional Claude

## File Naming Convention

**The one discipline that matters most:** Timestamp-based naming.

### Format

```
YYYYMMDD-HHMM_description.md
```

### Examples

```
20260514-1030_Session-Summary.md
20260514-1430_Blog-Draft.md
20260515-0900_Decision-Architecture.md
```

### Why This Works

- **Chronological order:** Files sort naturally by date
- **No ambiguity:** You know which version is newest
- **No overwrites:** Each session creates a new file
- **History intact:** You can see evolution over time

### What NOT to Do

❌ `Communication-Guide-v2.md`
❌ `Session-Summary-Final.md`
❌ `Notes-Updated.md`

Version numbers and labels like "final" create chaos. The timestamp is the version.

## Sharing with Claude

### Option 1: Google Drive MCP Server

If Claude has the Google Drive MCP server connected:

- Files are directly accessible via Claude's tools
- No manual copy-paste needed
- Claude can read and write to Drive

### Option 2: Manual Copy-Paste

If no MCP connection:

- Open the document in Drive
- Copy the content
- Paste into conversation with Claude
- Claude processes, generates output
- You save output back to Drive

Both work. MCP is more seamless, manual works everywhere.

## Access and Permissions

### For Your Eyes Only

Keep the root folder private. Only you can access.

### Sharing with Others

If collaborating, share specific subfolders:

- Share Instance/Professional with work collaborators
- Keep Instance/Personal private
- Share Standing/Communication-Guide with someone helping you set up

Granular sharing = better privacy control.

## The Trade-Off vs GitHub

### Google Drive Strengths

- No learning curve
- Works on all devices natively
- Familiar interface
- Easy sharing

### Google Drive Limitations

- No version control (can't easily diff two versions or roll back changes)
- No merge conflict resolution
- Limited collaboration features compared to Git

### The Substitute

Timestamp naming is the low-tech version control:

- Keep recent versions rather than overwriting
- History is visible from filenames
- Can roll back by loading an older timestamp

For most non-developers' use cases, this is perfectly adequate.

## Starting Simple

**Week 1:**

- Create root folder: "Claude System"
- Create "Standing" subfolder
- Create one Communication Guide document
- Start using timestamp naming

**Week 2-4:**

- Add "Session-Summaries" folder
- Start generating summaries at session close
- File them with timestamps

**Month 2:**

- Add instance folders if running multiple Claudes
- Add handoffs folder if you need cross-instance communication

**Month 3+:**

- Expand as needed based on actual friction
- Don't add structure you're not using

## Maintenance

### Weekly

- Check that recent files are in the right folders
- Skim Standing folder for anything outdated

### Monthly

- Archive old session summaries (keep last 3 months active, move older to Archive subfolder)
- Review Communication Guide for updates
- Clean out working drafts that are completed

### Quarterly

- Audit folder structure for unused sections
- Consider whether Standing documents are still relevant
- Archive anything historical that's not actively used

## Common Mistakes

### Mistake 1: Over-organizing too early

Don't build a complex 10-folder structure on day one. Start simple, expand as needed.

### Mistake 2: Not using timestamps

Files named "Summary1.md", "Summary2.md", "Summary-FINAL.md" create chaos. Use timestamps.

### Mistake 3: Never archiving

Session summaries from 2 years ago don't need to be in your active folder. Archive them.

### Mistake 4: Overwriting instead of versioning

When you update Communication Guide, save it as a new timestamped file. Keep the old version for at least a few weeks.

## Next Steps

- Set up the basic folder structure
- Review [Workflow](workflow.md) for how to actually use this system
- Get [Templates](templates.md) to start your first documents

---

**Key Insight:** Google Drive isn't fancy, but it works. The system doesn't need to be technically impressive - it needs to be maintainable by you, today, without requiring new skills.
