---
layout: guide
title: 'Auditing: Trust, But Verify'
---

# Auditing: Trust, But Verify

## The Core Principle

Claude generates plausible-sounding output. **Plausible and correct are not the same thing.**

The user is always the last line of verification. This isn't a limitation to work around - it's how responsible use of the tool works.

## What Needs Auditing

### 1. Claude's Memory (If Enabled)

Claude's memory system generates its own entries based on conversations. That means you don't always know what got captured, how it got framed, or whether it's still accurate.

**Problems that accumulate:**

- Facts that were true six months ago but have been superseded
- Framing that's subtly off (something you said in passing during a frustrated vent gets encoded as more significant than it was)
- Conflicts with other sources (memory says X, Project Instructions say Y)

**The habit:** Skim memory every few weeks. Look for:

- Anything outdated
- Anything framed in a way that doesn't sit right
- Anything that's been superseded by more recent developments

### 2. Session Summaries

Claude generates these, but Claude is also summarizing and interpreting, not transcribing.

**What goes wrong:**

- A session summary might capture the facts of what happened while quietly characterizing your state, your reasoning, or a decision in a way you'd push back on if you caught it
- Over time, if those summaries feed future sessions, a slightly off framing compounds
- Important details get dropped, minor details get over-weighted

**The habit:** Read summaries before they go into the filing system. If something's off, fix it now - not after it's influenced three more sessions.

### 3. Communication Guide Updates

If you have instances updating Communication Guides based on sessions, those updates need review.

**What goes wrong:**

- An update might drift from what you actually meant
- A pattern gets codified that was specific to one frustrating session, not universal
- An edge case gets elevated to a rule

**The habit:** Review guide updates before they're committed. A Communication Guide is supposed to represent you accurately - a drifted guide is worse than no guide.

### 4. Professional Outputs

**Non-negotiable rule:** Anything going to a client, an employer, a legal context, a medical context - read it fully, verify the claims, take ownership before it leaves your hands.

**Why this matters:**

- Claude can produce something that looks authoritative, reads well, and is subtly wrong in ways that matter
- A confident tone is not a quality signal
- "Claude wrote it" is not a defense and not a workflow

**The habit:** Professional outputs get human review, always. No exceptions.

### 5. Math and Calculations

Claude is genuinely bad at math in ways that aren't obvious.

**What happens:**

- Claude doesn't calculate - it predicts what a calculation's output should look like
- It can get arithmetic right, especially simple arithmetic
- It can also get it wrong with total confidence and no visible indication that anything went sideways

**The rule:** Any numbers that matter get verified independently. Calculator, spreadsheet, your own head - anything but trusting the output.

**Famous example:** "How many R's in Strawberry?" - Claude confidently counts wrong. If that can happen with letter counting, it can happen with your quarterly projections.

## Auditing Project Files

Every few weeks, review what's in Project Files:

- **Is each document still relevant?** (If you haven't used it in 10 sessions, archive it)
- **Is there more than one version?** (Keep only the current version)
- **Is anything stale?** (Outdated information needs updating or removal)

Project Files cost context window whether they're used or not. Keep this layer clean.

## Auditing Communication Guides

Beyond just reviewing updates, periodically check if the guide still matches reality:

- **Have your preferences changed?** (What annoyed you six months ago might not matter now)
- **Are instructions still actionable?** (Vague guidance that felt clear then might need specificity now)
- **Do any sections conflict?** (You added something new that contradicts something old)

A guide that never changes probably isn't being used. A guide that changes too often is probably unstable. Find the middle.

## The Overconfidence Problem

Claude doesn't flag uncertainty well. It produces output with the same confident tone regardless of whether it's:

- Drawing from training data
- Inferring from context
- Making an educated guess
- Completely confabulating

**Your job:** Don't rely on tone as a quality signal. Verify independently when stakes are high.

## The Compounding Error Problem

A small error in a summary becomes context for the next session. That session's summary might build on the error. Three sessions later, a minor misframing has become established fact in your documentation.

**The solution:** Catch errors early. Audit outputs when they're created, not after they've propagated.

## What You Can Trust

**Claude is generally reliable for:**

- Explaining concepts (within training data)
- Structuring information
- Drafting and revising text
- Generating code (with testing)
- Brainstorming and exploration

**Claude is unreliable for:**

- Math and numerical calculations
- Current events (without search)
- Legal or medical advice (not qualified)
- Remembering things across sessions (without your system)
- Knowing whether it's right or wrong (overconfidence is default)

## Building the Audit Habit

### Weekly

- Skim Claude's memory (if enabled) for anything obviously stale or wrong

### After Each Session

- Read the session summary before filing
- Review any Communication Guide updates

### Before Release

- Read all professional outputs fully
- Verify all numbers independently
- Check all references and citations

### Monthly

- Audit Project Files for staleness
- Review Communication Guide for accuracy
- Clean out outdated documents from storage

## The Trust Gradient

**Low-stakes, exploratory:** Trust more, verify less. You're brainstorming.

**Medium-stakes, operational:** Trust but verify. Read summaries, check key facts.

**High-stakes, public/professional:** Verify everything. Claude is a drafting tool, not a publisher.

Calibrate your verification effort to the stakes.

## Common Mistakes

### Mistake 1: Never verifying

"Claude is usually right, so I'll just trust it" - Until it's catastrophically wrong in a way you don't catch until it's shipped.

### Mistake 2: Over-verifying

Spending 30 minutes fact-checking a casual email - calibration is off, overhead is too high.

### Mistake 3: Verifying tone instead of content

"It sounds confident, so it must be right" - No. Verify the actual claims.

### Mistake 4: Letting errors accumulate

Small drifts in summaries or memory compound. Catch them early.

## The Responsibility Principle

**You are responsible for what Claude produces under your name.**

Not Claude. Not Anthropic. You.

That responsibility includes:

- Reading before publishing
- Verifying before claiming
- Correcting before it propagates
- Auditing systems before they drift

This isn't paranoia. It's hygiene.

## Next Steps

- Apply this to [Session Summaries](../core-concepts/session-summaries.md) review
- Check your [Communication Guide](../core-concepts/communication-guides.md) accuracy
- Read [Tam's System](../case-studies/tams-system.md) for practical workflow

---

**Key Insight:** Claude produces plausible output, not verified output. The gap between plausible and correct is your responsibility to close.
