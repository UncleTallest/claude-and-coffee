---
layout: guide
title: 'Templates: Starter Documents'
---

# Templates: Starter Documents

## Communication Guide Template

```markdown
# Communication Guide - [Your Name]

## About Me

[Brief background - what Claude should know about you]

## How I Communicate

- [Do you think out loud or arrive with formed requests?]
- [Do you prefer prose or bullets?]
- [How do you use punctuation/emphasis?]
- [Formal or casual tone?]

## What Works

- [Specific patterns that land well]
- [Example: "Show me a draft rather than describing what one could say"]
- [Example: "Give me options when I'm stuck"]

## What Doesn't Work

- [Things that make you want to close the tab]
- [Example: "No affirmations before answers"]
- [Example: "One question at a time, maximum"]

## How to Read My State

- [How to distinguish venting from distress]
- [How to recognize when you're tired/rushed/focused]
- [What emotional cues mean what]

## Context That Matters

- [Relevant expertise or background]
- [Neurological context if applicable (ADHD, autism, etc.)]
- [Working constraints or patterns]

## Special Instructions

[Any specific protocols or preferences not covered above]

---

Last Updated: [DATE]
```

## Session Summary Template

```markdown
# Session Summary - [YYYYMMDD-HHMM]

## What We Accomplished

- [Key outcomes from this session]
- [Things that got finished]
- [Progress made on ongoing work]

## Decisions Made

- [Decision]: [Rationale]
- [Decision]: [Rationale]

## Current State

- [What's in progress]
- [What's working]
- [What's blocked]

## Next Session

- [Immediate next steps]
- [What to pick up]
- [What needs attention]

## Open Questions

- [Unresolved items]
- [Things to think about]

## Context for Future

[Anything that will matter later but isn't immediate]

---

Created: [TIMESTAMP]
Instance: [Which Claude instance if running multiple]
```

## Minimal Session Summary Template

```markdown
# Session Summary - [YYYYMMDD-HHMM]

**Decided:** [Key decisions]
**Done:** [Completed work]
**In Progress:** [Current state]
**Next:** [Next steps]
**Blockers:** [If any]

---

[TIMESTAMP] - [Instance Name]
```

## Project Instructions Template

```markdown
# Project Instructions - [Project Name]

## What This Instance Does

[Primary purpose and scope]

## What This Instance Doesn't Touch

[Boundaries - what stays in other projects]

## Session Opening Protocol

- [What to load automatically]
- [What context to check]

## Session Closing Protocol

- [Summary requirements]
- [Where to file documents]
- [Any updates needed]

## Standing Workflows

[Repeated patterns or processes]

## Key People/Context

[Relevant names, relationships, or context for this project]

## Communication Preferences

[Project-specific tone or approach]

---

Last Updated: [DATE]
```

## Handoff Note Template

```markdown
# Handoff: [From Instance] → [To Instance]

**Date:** [YYYYMMDD-HHMM]

## Context

[What happened that requires handoff]

## Action Needed

[What the receiving instance should do]

## Relevant Documents

- [Link or path to relevant files]
- [Any background the receiving instance needs]

## Priority

[Urgent / Normal / Low]

## Status

- [ ] Created
- [ ] Handed off
- [ ] Completed

---

Created by: [From Instance]
```

## Decision Record Template

```markdown
# Decision: [Brief Title]

**Date:** [YYYYMMDD]
**Status:** Decided / Under Review / Superseded
**Instance:** [Which instance made this decision]

## Context

[What situation prompted this decision]

## Options Considered

1. [Option A] - [Pro/Con]
2. [Option B] - [Pro/Con]
3. [Option C] - [Pro/Con]

## Decision

[What was decided and why]

## Rationale

[Reasoning behind the choice]

## Implications

[What this means for future work]

## Supersedes

[If this replaces an older decision, note it]

---

[TIMESTAMP]
```

## Using These Templates

### Getting Started

1. Copy the template
2. Fill in the bracketed sections
3. Remove any sections that don't apply
4. Save with timestamp naming: `YYYYMMDD-HHMM_description.md`

### Adapting Them

These are starting points, not rules. Adjust to fit your actual needs:

- Add sections that matter to you
- Remove sections you never use
- Change the format to match your thinking style

### The Test

If you're filling in a section just because the template has it, remove that section. If you keep wishing a section existed, add it.

Templates serve you, not the other way around.

## Starter Folder Structure

```
/Claude-System/
├── Standing/
│   └── 20260514-1200_Communication-Guide.md
├── Instances/
│   └── Main/
│       └── Session-Summaries/
│           └── 20260514-1430_Session-Summary.md
└── Templates/
    ├── Communication-Guide-Template.md
    ├── Session-Summary-Template.md
    └── Handoff-Template.md
```

Copy these templates into a Templates folder. When you need one, duplicate it and fill it in.

## Next Steps

- Set up your [Google Drive](google-drive-setup.md) folders
- Copy these templates to your Templates folder
- Create your first Communication Guide
- Read [Workflow](workflow.md) for how to use them in practice

---

**Key Insight:** Templates give you structure to start, but they should evolve into forms that actually match how you work.
