# The Continuity Stack

## How the Pieces Work Together

You've learned about Communication Guides, Session Summaries, and the four layers of context. Here's how they combine to create actual continuity.

## The Core Principle

**Claude has no memory. Continuity is entirely a function of what you load into context at the start of a session.**

You can't give Claude memory. But you can give Claude a filing system that reconstructs working state reliably.

## The Three-Layer Stack

### Layer 1: The Static Layer (How You Work Together)
**Communication Guide** handles this.

What it contains:
- How you think and communicate
- What works and what doesn't
- Context about you that doesn't change session to session

Why it matters: Without this, every session starts with Claude guessing how to calibrate. With it, Claude arrives already tuned to your frequency.

Where it lives: Personal Preferences (universal patterns) or Project Files (detailed guide)

### Layer 2: The Dynamic Layer (Where You Are)
**Session Summaries** handle this.

What they contain:
- Current state of work
- Decisions made and why
- What's in progress, what's blocked
- What will matter next session

Why it matters: Without this, you re-explain context every session. With it, Claude picks up where you left off.

Where they live: Project Files (most recent) or External Storage (archive)

### Layer 3: The Reference Layer (Resources and History)
**Project Files and External Storage** handle this.

What they contain:
- Historical decisions and rationale
- Templates and examples
- Domain-specific reference materials
- Long-term project documentation

Why it matters: This is the accumulated context that builds over time. Early sessions, it's thin. By month six, it's genuinely valuable.

Where it lives: Project Files (frequently consulted) or External Storage (on-demand)

## The Session Cycle

### Opening a Session
1. **Personal Preferences** load automatically (Layer 1: universal patterns)
2. **Project Instructions** load automatically (Layer 2: project context)
3. **Project Files** are present (Layer 3: recent summary, communication guide)
4. **External documents** get fetched as needed (Layer 4: historical context, specific references)

Claude arrives calibrated (Personal Preferences), knows what this project is (Project Instructions), and has immediate context about where you left off (recent summary in Project Files).

### During the Session
You work. Claude references the loaded context. If something from history matters, you or Claude fetches it from External Storage.

### Closing the Session
Claude generates a summary:
- What got decided
- What changed
- What's in progress
- What matters next time

You review it, fix anything Claude misweighted, and file it. The most recent summary might replace what's in Project Files. Older summaries archive to External Storage.

### Next Session Opens
The cycle repeats. But each time, there's slightly more accumulated context. The system gets cheaper to open and richer in usable history.

## The Compounding Effect

**Session 1:** Overhead. You're building the filing system.

**Session 5:** Marginal benefit. Claude remembers a few things without prompting.

**Session 20:** Real benefit. You're arriving at work 5 minutes faster every time.

**Session 50:** Compound benefit. The decision history and context archive are genuinely valuable reference material.

This only works if:
- You consistently create summaries
- You load them when relevant
- You curate what's in Project Files
- You maintain accurate information

Skipping sessions breaks the chain. Letting summaries pile up without reading them wastes the system.

## Why This Beats Long Conversations

Some people think: "Why not just keep one long ongoing conversation?"

Problems with that approach:
1. **Context degrades over very long windows** - earlier material gets less weight
2. **Can't work across instances** - each instance only knows its own thread
3. **Can't search or audit** - finding something from three weeks ago is impossible
4. **No portability** - if that instance resets, everything's gone

Structured summaries + loaded guides give you something more like a filing system than a memory - explicit, portable, auditable.

## Why This Beats Model Memory

Claude has a memory feature. Why not just use that?

Memory supplements this system, it doesn't replace it:
- Memory entries are generated automatically - you don't always know what got captured
- Memory can drift or misweight things over time
- Memory has no explicit structure - it's opaque
- Memory doesn't give you historical audit trail

The continuity stack gives you:
- **Explicit control** over what gets remembered
- **Auditability** - you can read summaries and see exactly what was captured
- **Portability** - documents travel across instances and model versions
- **History** - decision trail that compounds over time

Use memory for supplemental recall. Use the continuity stack for reliable state management.

## The Version Resilience Benefit

People who rely on model "feel" panic when versions change (Claude 3.5 → 4.0 → 4.5 → etc).

People who run this architecture don't notice much.

Why? **The architecture externalizes continuity.**

Communication Guide, Project Instructions, Session Summaries - they're all documents. They travel across model versions because they're portable text, not baked-in model behavior.

A new model reads the same guide and lands in roughly the same working relationship. The consistency is in the system, not the weights.

## Common Failure Modes

### Failure 1: Building Without Using
You create all the documents but never load them. Overhead without benefit.

### Failure 2: Using Without Maintaining
You load documents but never update them. Stale information compounds, system degrades.

### Failure 3: Overloading Context
You load everything every time. Context window fills with irrelevant material, attention dilutes.

### Failure 4: Underloading Context
You load nothing. Every session re-explains. The system provides no benefit.

**The balance:** Load what matters today, fetch history as needed, maintain what's loaded.

## For Newcomers: The Minimum Viable Stack

Don't build this all at once.

**Minimum to start:**
1. Personal Preferences (who you are, how you communicate)
2. One Communication Guide (even a rough one)
3. Basic session close habit (write down what happened, what's next)

That's enough to feel the difference.

Then grow:
- Project Instructions when you create a dedicated project
- Project Files when you're referencing the same documents most sessions
- External Storage when history accumulates enough to matter

Let the system earn its complexity through actual use.

## Next Steps

- See [Tam's System](../case-studies/tams-system.md) for this stack in practice
- Read [Cold-Start Management](../intermediate/cold-start-management.md) to optimize loading
- Check [Workflow](../implementation/workflow.md) for practical session patterns

---

**Key Insight:** The continuity stack isn't about giving Claude memory. It's about giving yourself a reliable way to reconstruct working state. Memory is a feature of the system, not the model.
