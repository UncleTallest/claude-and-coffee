---
layout: guide
title: 'Cold-Start Context Management'
---

# Cold-Start Context Management

## The Problem

Every session with Claude starts completely cold. No memory, no context, nothing.

The "cold start" problem: how much do you load at the beginning of a session before you can actually get to work?

## The Naive Approaches (Both Fail)

### Approach 1: Load Everything

All your standing documents, every recent summary, the full history.

**Fails because:**

- Context windows have limits
- Claude's attention isn't equally distributed - earlier material carries less weight than recent material
- You spend 5 minutes loading before you can work
- Most of what you loaded isn't relevant today

### Approach 2: Load Nothing

Start fresh, paste in context as needed during the session.

**Fails because:**

- You spend the first 10 minutes of every session re-explaining
- You forget what context matters
- No continuity across sessions
- Everything is manual overhead

## The Smart Approach: Tiered Loading

Some things load every session without question. Other things load conditionally. Everything else stays in storage until it's actually needed.

### Always-Load Tier

**Small, stable, always relevant:**

- Personal Preferences (automatic)
- Project Instructions (automatic)
- Communication Guide (if in Project Files)
- Most recent session summary (if in Project Files)

These are small, stable, and always provide value. Load them every time.

### Conditional-Load Tier

**Relevant today, not always:**

- Finance snapshot (only if money is on the agenda)
- Specific project summary (only if continuing that thread)
- Technical documentation (only if working on that system)
- Reference materials (only if needed for today's task)

Check: is this actually relevant to today's session? If yes, fetch it. If no, leave it in storage.

### Archive Tier

**Historical, rarely needed:**

- Old session summaries (unless reviewing history)
- Deprecated decisions (unless understanding evolution)
- Completed project documentation (unless referencing it)

These live in storage. Fetch only when explicitly needed.

## The Decision Framework

Ask this about each document: **"If I loaded nothing but this document, would this session still work?"**

- **Yes** → Candidate for always-loading (add to Project Files)
- **Depends on the topic** → Conditional loading (fetch when relevant)
- **No / Rarely** → Archive tier (storage only)

## Attention Distribution

Even within loaded context, Claude doesn't weight everything equally:

- **Recent content gets more attention** than early content
- **Explicit references get more attention** than background material
- **Structured content gets more attention** than unformatted dumps

This means:

- Put the most important thing last (right before you start talking)
- Reference specific documents explicitly when they matter
- Keep loaded documents clean and well-structured

## Size vs Relevance Trade-Off

A smaller, highly relevant document beats a larger, partially relevant one:

**Option 1:** Load entire 50-page project history
**Option 2:** Load 2-page summary of decisions that matter today

Option 2 wins. More signal, less noise, less context window consumed.

## Managing Project Files (Layer 3)

This is where cold-start optimization lives.

**Discipline required:**

- **One version at a time** - when you update a document, remove the old version
- **Audit regularly** - every few weeks, check what's in Project Files
- **Remove stale content** - if you haven't referenced it in 10 sessions, move it to storage
- **Keep it tight** - the goal is the smallest set that gets Claude to fully functional working state

Every document in Project Files costs context window whether you use it or not. Make each one earn its place.

## The Session Rhythm

### Opening

1. Automatic layer already present (Personal Preferences, Project Instructions, Project Files)
2. Check: what's today's focus?
3. Fetch conditionally: "Get the Q3 summary" or "Load the blog redesign decisions"
4. Start work

### During

If you reference something that's not loaded, fetch it then. Don't pre-load "just in case."

### Closing

Update the summary. File it. If it's the most recent and most likely to matter next time, maybe replace what's in Project Files.

## Warning Signs You're Doing It Wrong

### Sign 1: Sessions open slowly

If you're spending 5+ minutes loading context every time, you're overloading or fetching manually instead of pre-positioning.

### Sign 2: You're re-explaining constantly

If you're repeating the same context every session, you're underloading or not maintaining summaries.

### Sign 3: Claude references wrong information

If Claude is pulling from stale documents in Project Files, you're not curating that layer.

### Sign 4: Context feels scattered

If Claude seems confused about what's relevant, you're either loading too much (signal/noise problem) or not structuring what's loaded (attention distribution problem).

## The Compounding Benefit

Early sessions, cold-start management feels like overhead. By session 20, you're arriving at work 5 minutes faster every time because the right context is already present.

By session 50, the context archive is valuable reference material and you know exactly what to load for any given task.

This only works if you:

- Actually maintain the layers
- Curate what's in Project Files
- Archive what's not needed
- Fetch conditionally based on today's needs

## Practical Exercise

Look at what's currently in your Project Files.

For each document, ask:

- **Have I referenced this in the last 5 sessions?**
- **Will I reference it in the next 5 sessions?**

If "no" to both, move it to external storage. You can always fetch it later if needed.

## Next Steps

- Understand [The Layers](../core-concepts/the-layers.md) to see where this fits
- Read [Tam's System](../case-studies/tams-system.md) for practical implementation
- Check [Workflow](../implementation/workflow.md) for session patterns

---

**Key Insight:** The goal is to arrive at actual work as fast as possible with the minimum context necessary to do it well. Not maximum context. Minimum effective context.
