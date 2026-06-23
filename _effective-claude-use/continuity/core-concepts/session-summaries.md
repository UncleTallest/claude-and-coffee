---
layout: guide
title: 'Session Summaries'
---

# Session Summaries

## The Problem They Solve

Claude has no persistent memory. Every session starts completely cold. A Session Summary is how you capture "where we left off" so the next session can pick up without re-explaining everything.

## What Goes in a Summary

### State Capture

Where things stand right now:

- What got decided
- What's in progress
- What's blocked and why
- What changed since last session

### Context That Matters

Not everything needs to be in the summary. Include:

- Decisions with rationale (why, not just what)
- Unresolved questions or tensions
- Things that will matter next session
- Anything you'd have to re-explain otherwise

### What to Leave Out

Temporary scaffolding that served its purpose:

- Brainstorming that led to a decision (capture the decision, not the 20 ideas you rejected)
- Troubleshooting steps that worked (capture "fixed the bug" not "tried these 15 things")
- General conversation that didn't change state

## Structure

### Minimal Version

<br />

```markdown
## Session Summary - 2026-05-14

**Decided:** Using Eleventy for blog, custom domain configured
**In Progress:** Meetup documentation structure
**Next:** Build out markdown files for docs site
**Blockers:** None
```

<br />

---

<br />

### Expanded Version

<br />

```markdown
## Session Summary - 2026-05-14 10:30 AM

### What We Accomplished

- Configured custom domains for three sites (continuity-bridge, blog, claude-and-coffee)
- Fixed Eleventy pathPrefix issue in blog deployment
- Started documentation structure for meetup resources

### Decisions Made

- Meetup docs in uncletallest-infra org (DevRel with everyman approach)
- Start with Markdown, migrate to Eleventy later
- Documentation structure: getting-started, core-concepts, intermediate, implementation, case-studies, resources

### Current State

- All three domains live and serving correctly
- Blog rendering properly with updated paths
- Skeleton structure designed, files being created

### Next Session

- Finish building out markdown file stubs
- User fleshes out content from Tam/MuChao conversations
- Consider Luma setup for broader meetup reach

### Open Questions

- None currently

### Context for Future

- User (Jerry) runs Claude and Coffee Austin meetup, 121 members
- Teaching continuity concepts to non-technical users
- "A non-coder's system" is primary case study
```

<br />

---

<br />

## Frequency

### Every Session

If you're working on something complex that spans multiple sessions, summarize at the end of each one.

### Milestone-Based

If sessions are shorter or less connected, summarize when you hit natural breakpoints: "finished X", "decided Y", "shipped Z".

### When State Changes Significantly

Anytime the working context shifts enough that the next session would need to know about it.

## Storage and Naming

### File Naming Convention

Use timestamps to maintain order and prevent chaos:

<br />

```bash
20260514-1030_session-summary.md
20260514-1430_session-summary.md
20260515-0900_session-summary.md

Format: `YYYYMMDD-HHMM_session-summary.md`
```

<br />

No "v2", no "final", no "updated". The timestamp tells you the order. Never overwrite a previous summary - always create a new one.

<br />
### Where to Store

- **Google Drive:** In a dedicated folder for that instance or project
- **Project Files:** Recent summary can be attached to Claude Project for automatic loading
- **Local filesystem:** If you're using a file-based system

The key: put summaries somewhere both you and Claude can access them when starting the next session.

## Using Summaries at Session Start

### Loading the Summary

At the start of a new session, either:

- Have Claude fetch it from Drive/storage
- Paste it into the conversation
- Have it attached as a Project File

### What Claude Does With It

The summary re-establishes working state. Claude can pick up where you left off without:

- Re-explaining what you're working on
- Repeating decisions already made
- Asking questions already answered

### When to Load Multiple Summaries

- If continuing a thread from several sessions back
- If there are dependencies across different workstreams
- If context has been building over many sessions

But: don't load everything by default. Load what's relevant to _this_ session.

## Common Mistakes

### Mistake 1: Too much detail

Summaries aren't transcripts. Capture decisions and state, not every step taken.

### Mistake 2: Too little context

"We fixed the bug" → Which bug? How? What was the root cause? Will this matter later?

### Mistake 3: Never reading them back

Summaries are only useful if they're loaded. Build the habit of starting sessions by reviewing the last summary.

### Mistake 4: Letting Claude write them unchecked

Claude generates summaries. You should read them before filing. Sometimes Claude misweights things or misses context. Fix it before it becomes the record.

## Combining with Communication Guides

Communication Guides handle the static layer: how you work together.
Session Summaries handle the dynamic layer: where you are right now.

Together they create continuity:

- The guide tells Claude _how_ to work with you
- The summary tells Claude _what_ you're working on

Without both, you're either re-establishing process every session, or re-explaining context every session, or both.

## The Compounding Effect

The first summary feels like overhead. By session 10, you're saving 5-10 minutes at the start of every session by not re-explaining. By session 50, the accumulated context and decision history is genuinely valuable reference material.

This only works if summaries are:

- Actually created consistently
- Stored where they can be found
- Loaded when relevant
- Maintained with accurate information

## Next Steps

- See [The Layers](the-layers.md) for where summaries fit in the overall system
- Check [Workflow](../implementation/workflow.md) for session open/close patterns
- Read [Tam's System](../case-studies/tams-system.md) for how summaries work in practice

---

**Key Insight:** Session Summaries aren't documentation for its own sake. They're the mechanism that makes tomorrow's session cheaper than today's.
