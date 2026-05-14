# Communication Guides

## What They Are

A Communication Guide documents how you communicate and think - the patterns Claude needs to know to work effectively with you. It's the calibration layer between Claude's general capabilities and your specific working style.

## How They Compare to Other Documentation

If you've ever written a voice bible for fiction writing, the parallel is closer than it looks at first.

Both documents are fundamentally doing the same job: giving a future collaborator (human or AI) enough signal to stay in voice without constant correction. The architecture is nearly identical - core register, what works, what to avoid, named patterns, and the live tensions that define the thing.

The meaningful differences:
- **Fiction voice bible:** Calibrating for a constructed voice with deliberately held tensions
- **Communication Guide:** Calibrating for a real person's actual brain, where getting it wrong breaks trust or shuts down the interaction

A voice bible is largely generative - it tells you how to produce new content. A Communication Guide is more receptive - it tells Claude how to read and respond to what's coming in.

## What to Include

### Core Communication Patterns
How you structure requests, how you give feedback, how you signal different levels of urgency or certainty.

### Working Preferences
- Output format (prose vs lists, when to use which)
- Tone (clinical, conversational, blunt)
- Question cadence (one at a time vs batched)
- Explanation depth (assume expertise vs explain thoroughly)

### What Breaks the Interaction
Be explicit about what makes you close the tab:
- Over-apologizing
- Therapist tone when you're not in distress
- Too many affirmations
- Specific phrases or patterns you find grating

### Context About You
- Relevant background (technical expertise, domain knowledge)
- How to read your emotional register
- Neurological context if relevant (ADHD, autism, etc.)
- Working constraints (time pressure, cognitive load patterns)

### How to Handle Uncertainty
When Claude doesn't know something or you're ambiguous:
- Ask for clarification vs make reasonable assumptions
- Surface the uncertainty vs proceed and flag it later
- Offer options vs recommend a direction

## Structure Approaches

### Option 1: Prose Narrative
Natural language document that reads like instructions to a collaborator. Works well if you think in continuous narrative.

### Option 2: Sectioned Headers
Clear categories with bullet points under each. Works well if you think in taxonomies.

### Option 3: Hybrid
Prose sections for complex patterns, bullets for quick reference items. Most flexible approach.

## Size Guidance

**Too short:** A couple of sentences won't give Claude enough to work with. You need specifics.

**Too long:** If Claude has to summarize your guide to understand it, you've defeated the purpose.

**Right size:** Usually 1-3 pages. Enough detail to be actionable, concise enough to be absorbable.

## The Specificity Principle

Vague guidance produces vague results:
- ❌ "Be direct"
- ✅ "Lead with the answer, then explain reasoning if needed"

Specific guidance produces specific adjustments:
- ❌ "Don't be too formal"
- ✅ "Use contractions, avoid 'indeed' and 'moreover', match my energy level"

## Evolution

Communication Guides aren't static. They evolve as you discover new friction points or refine what works.

Some systems have instances update the guide at session close based on what went well or poorly. Others update manually when patterns emerge.

The key: a guide that never changes probably isn't being used effectively.

## Per-Instance vs Universal

If you run multiple Claude instances for different contexts (work, personal, creative), you'll eventually notice:
- Some patterns are universal (how you think, core communication style)
- Some are context-specific (formality level, domain assumptions)

When that split becomes apparent, you can maintain:
- **One universal guide:** Loaded by all instances
- **Per-instance additions:** Context-specific calibration

Don't build this complexity before you need it. Start with one guide, split when friction demands it.

## Common Mistakes

### Mistake 1: Writing for yourself
The guide is for Claude, not for you. "I prefer X" is less useful than "Claude should do X."

### Mistake 2: Listing problems without solutions
"Don't ask too many questions" → How many is too many? What should Claude do instead?

### Mistake 3: Assuming obvious things are obvious
Your "obviously use prose here" might not be obvious at all. State it.

### Mistake 4: Never updating it
If the guide isn't evolving, you're not learning from friction. Update when patterns emerge.

## Next Steps

- See [The Layers](the-layers.md) to understand where Communication Guides fit in the broader system
- Read [Tam's System](../case-studies/tams-system.md) for a real working example
- Check [Implementation](../implementation/) for templates and setup guides

---

**Remember:** A Communication Guide is an investment. The first few sessions feel like overhead. By session 10 or 20, you're arriving at work faster and with better context every time. That's the compounding effect.
