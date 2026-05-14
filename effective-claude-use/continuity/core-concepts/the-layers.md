# The Layers: Where Context Lives

## The Core Problem

Claude starts every session cold. No memory, no context, nothing. The question is: how much do you load at the beginning of a session before you can actually get to work?

Loading everything → context window limits, attention dilution
Loading nothing → constant re-explanation

The solution: **tiered loading**. Different types of information live in different layers based on how stable they are and how often they're needed.

## The Four Layers

### Layer 1: Personal Preferences (Innermost)
**What it is:** Profile-level setting in Claude's interface. Applies across every conversation, every project, automatically.

**What belongs here:**
- Who you are (background, identity, context)
- Universal communication patterns (how your brain works)
- Tone preferences that never change
- Core people/context that matters everywhere

**Why here:** It's always loaded without any action from you. Set it once, it's there forever (until you change it).

**Size:** Limited by the UI field - can't be huge. Focus on truly universal patterns.

### Layer 2: Project Instructions (Project-Specific)
**What it is:** Per-project setting in Claude. Every Project you create can have its own instructions.

**What belongs here:**
- What this specific instance does
- What it doesn't touch
- Session opening/closing protocols
- Standing workflows or flags for this context
- Role definition (if distinct from other projects)

**Why here:** Automatically loaded for every conversation in that project. No fetch required, no risk of forgetting.

**Size:** Also limited by UI field. Keep it focused on operational context for this specific instance.

### Layer 3: Project Files (Available, Not Forced)
**What it is:** Documents attached directly to a Claude Project. Available to every session without fetching, but they consume context window.

**What belongs here:**
- Communication Guide (if too detailed for Personal Preferences)
- Recent session summary (the one most likely to matter)
- Key reference documents consulted frequently
- Standing templates or examples

**Why here:** Present by default but needs active curation. Every file attached costs context window whether it's used or not.

**Critical discipline:** One version at a time. When you update a guide, remove the old version. Keep this layer lean - if something isn't consulted most sessions, it belongs in Layer 4.

### Layer 4: External Storage (Conditional Loading)
**What it is:** Google Drive, local filesystem, wherever you store working documents.

**What belongs here:**
- Session summary archive (all summaries, not just the most recent)
- Historical decisions and context
- Project-specific documents that aren't always relevant
- Templates, examples, reference materials
- Anything dynamic that changes frequently

**Why here:** Loaded intentionally when needed. Doesn't consume context window unless explicitly fetched. Scales infinitely - you can have thousands of documents here without impacting performance.

**The fetch pattern:** When starting a session, Claude or you decides what's relevant and fetches it. "Pull the Q3 financial summary" or "load the last three session summaries for the blog project."

## How They Work Together

### At Session Start

1. **Personal Preferences** are already loaded (Layer 1)
2. **Project Instructions** are already loaded (Layer 2)
3. **Project Files** are already present (Layer 3)
4. **External documents** get fetched as needed (Layer 4)

Claude arrives with general calibration (Layer 1), knows what this project is about (Layer 2), and has immediate access to recently-used reference materials (Layer 3). Everything else loads on-demand (Layer 4).

### The Information Flow

```
Universal → Project-Specific → Recent/Frequent → On-Demand
   L1              L2                 L3              L4
```

Information that's true everywhere lives innermost (loaded always). Information that's situational lives outermost (loaded conditionally).

## Choosing the Right Layer

Ask these questions:

**Is it true across ALL projects?** → Personal Preferences (L1)
**Is it specific to THIS project?** → Project Instructions (L2)
**Do I consult it in MOST sessions here?** → Project Files (L3)
**Is it useful SOMETIMES but not always?** → External Storage (L4)

### Examples

**"I think out loud and refine as I go"**
→ Layer 1 (Personal Preferences) - true everywhere

**"This project is for DevRel work, not personal tasks"**
→ Layer 2 (Project Instructions) - defines this specific project

**"Communication Guide v2.3"**
→ Layer 3 (Project Files) - consulted most sessions, needs to be present

**"Session summary from March 15th"**
→ Layer 4 (External Storage) - historical record, load if needed

## Managing the Layers

### Layer 1 & 2: Occasional Updates
Personal Preferences and Project Instructions change slowly. Update when you discover new patterns or when the project's purpose shifts.

### Layer 3: Active Curation
Project Files need regular gardening:
- Remove old versions when you update something
- If you haven't used a file in 10 sessions, move it to Layer 4
- Keep this layer tight - it costs context window

### Layer 4: Archive and Organize
External storage can grow freely, but organization matters:
- Use timestamp-based naming (`YYYYMMDD-HHMM_description.md`)
- Keep related documents in clear folder structures
- Don't overwrite - create new versions, keep history

## The Cold-Start Benefit

With this layered system:
- Sessions start fast (Layers 1-3 are already present)
- Context is relevant (Layer 3 is curated, Layer 4 is fetched intentionally)
- Nothing important gets forgotten (it's explicitly in one of the layers)

Without it:
- Every session starts by pasting in a bunch of documents
- You forget what's relevant this time
- Context window fills with stuff that doesn't matter today

## Common Mistakes

### Mistake 1: Everything in Layer 4
Nothing gets loaded automatically. Every session starts with manual fetching. Overhead never goes away.

### Mistake 2: Everything in Layer 3
Context window fills with documents you don't need today. Attention gets diluted. Slower, not faster.

### Mistake 3: Never curating Layer 3
Old versions pile up. Files that haven't been used in months consume space. System degrades instead of improving.

### Mistake 4: Putting dynamic content in Layer 1 or 2
You end up editing Personal Preferences every week. That's a signal the information belongs in Layer 3 or 4.

## Evolution Over Time

**Early on:** Layer 1 (Personal Preferences) and maybe a simple Communication Guide in Layer 4 that you paste in.

**As the system matures:** Communication Guide moves to Layer 3 (Project Files). Session summaries accumulate in Layer 4. Project Instructions get more refined.

**At full maturity:** All four layers working together. Session opens cleanly, you arrive at work fast, and nothing important gets lost.

## For Newcomers: Start Simple

Don't build all four layers on day one.

**Week 1:** Write Personal Preferences. That's Layer 1.
**Week 2-4:** Add a Communication Guide in Layer 4. Paste it in manually at session start.
**Month 2:** Create a Project and add Project Instructions (Layer 2).
**Month 3+:** Move Communication Guide to Layer 3 (Project Files) and start building a session summary archive in Layer 4.

Let complexity emerge from friction, not from planning.

## Next Steps

- Learn about [Cold-Start Management](../intermediate/cold-start-management.md) for optimizing Layer 3 and 4 loading
- Read [Tam's System](../case-studies/tams-system.md) to see the layers in practice
- Check [Implementation guides](../implementation/) for setup details

---

**Key Insight:** The layers aren't bureaucracy. They're a filing system that makes "where we left off" automatic instead of manual.
