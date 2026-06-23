---
layout: guide
title: 'Workflow: Session Open → Work → Close'
---

# Workflow: Session Open → Work → Close

## The Basic Pattern

Every session follows the same three-phase rhythm:

1. **Open:** Load context
2. **Work:** Do the actual thing
3. **Close:** Capture state for next time

## Phase 1: Session Open

### Automatic Loading (Happens Without You)

- Personal Preferences
- Project Instructions
- Project Files

These are already present when the session starts.

### Conditional Loading (You Decide)

Ask: What's today's focus?

**If continuing recent work:**

- Load most recent session summary (if not in Project Files already)
- "Get the summary from yesterday"

**If specific domain:**

- Load relevant references
- "Pull the Q3 financial snapshot"
- "Load the blog redesign decisions"

**If historical context matters:**

- Fetch older summaries or decisions
- "Get the decisions from March about architecture"

### The Greeting Pattern

You don't need to spend 5 messages on pleasantries and setup.

**Efficient open:**

```
"[load yesterday's summary]

Picking up where we left off - ready to finish the blog DNS configuration."
```

You've loaded context, stated intent, and you're at work in one message.

## Phase 2: Work

This is the actual session. You work, Claude helps, things get done.

### During Work: Fetch as Needed

If you reference something that's not loaded, fetch it then:

- "Pull the email draft we worked on last week"
- "Get the pricing research from April"

Don't pre-load "just in case." Fetch when it becomes relevant.

### If Claude Seems Lost

Sometimes Claude references wrong information or seems confused about context.

**Quick fixes:**

- Check what's loaded: "What summaries do you currently have?"
- Reload if needed: "Ignore that, here's the current state: [paste summary]"
- Clarify the discrepancy: "That decision was superseded. Current approach is X."

## Phase 3: Session Close

### Generate Summary

At the end of the session, have Claude create a summary:

**Prompt:** "Generate a session summary covering: what we accomplished, decisions made, current state, and what's next."

### Review Before Filing

Read the summary. Fix anything that:

- Misweights importance
- Gets framing wrong
- Misses critical context
- Over-explains minor details

Remember: This summary feeds future sessions. Get it right now.

### File with Timestamp

Save the summary:

```
YYYYMMDD-HHMM_session-summary.md
```

Put it in the appropriate folder:

- Instance-specific work → that instance's folder
- General/standing context → Standing folder

### Update Project Files (If Needed)

If this summary is more recent and relevant than what's currently in Project Files:

- Replace the old summary with this one
- Remove the old version (no multiple versions in Project Files)

## Frequency Patterns

### Every Session (Complex Work)

If working on something that spans multiple sessions with evolving state, close each session with a summary.

### Milestone-Based (Project Work)

If sessions are shorter or less connected, summarize when you hit natural breakpoints:

- "Finished X"
- "Decided Y"
- "Shipped Z"

### Significant State Changes

Anytime the working context shifts enough that the next session would need to know about it.

## Multi-Session Work Example

**Session 1 Close:**

```
Summary: Started blog redesign. Decided on Eleventy, researched themes.
Next: Implement base layout and configure deployment.
```

**Session 2 Open:**

```
[load Session 1 summary]
"Let's implement the base layout we planned."
```

**Session 2 Close:**

```
Summary: Implemented base layout, hit DNS configuration issues.
Blocked: Need to update Cloudflare records.
Next: Fix DNS, then deploy to production.
```

**Session 3 Open:**

```
[load Session 2 summary]
"DNS updated. Let's deploy."
```

Each session picks up exactly where the last one left off.

## Cross-Instance Handoff

If work needs to transfer from one instance to another:

**Instance 1 (Professional) Close:**
Create handoff note:

```
To: Personal instance
Context: Meetup documentation structure designed.
Action needed: Draft the announcement with creative framing.
Link: [pointer to relevant documents]
```

Save in Handoffs/To-Personal

**Instance 2 (Personal) Open:**

```
[load handoff note]
"Got the handoff from Professional instance. Let's draft the announcement."
```

## Time Management

**Good sessions:**

- 5 minutes: Open and load context
- 40-50 minutes: Actual work
- 5 minutes: Close and capture summary

**Bad sessions:**

- 15 minutes: Figuring out what context to load
- 30 minutes: Work, constantly explaining things Claude should know
- 0 minutes: No summary captured, next session starts cold again

The workflow exists to push time toward the middle category.

## When to Break the Pattern

### Quick Questions

"What's the syntax for X?" doesn't need a full open/close cycle. Ask, get answer, done.

### Rapid Iteration

If doing 5 short sessions in one day on the same thing, you might summarize once at the end of the day instead of after each session.

### Exploration/Brainstorming

Early exploratory work might not need session summaries until something concrete emerges.

**The test:** Would the next session benefit from knowing what happened this session? If yes, summarize. If no, skip it.

## Common Mistakes

### Mistake 1: Skipping the close

You finish work, close Claude, and forget to capture state. Next session starts cold.

### Mistake 2: Not loading summaries at open

You created summaries but never load them. Overhead without benefit.

### Mistake 3: Loading too much

You paste 5 summaries and 10 documents at session start. Context overload, attention dilution.

### Mistake 4: Never iterating on the process

The workflow should evolve based on what actually works for you. Don't cargo-cult it.

## Next Steps

- Set up [Google Drive](google-drive-setup.md) folder structure
- Use [Templates](templates.md) to start your first documents
- See [Tam's System](../case-studies/tams-system.md) for real workflow example

---

**Key Insight:** The workflow is a habit, not a ritual. Do it because it makes sessions cheaper and more effective, not because a guide said to.
