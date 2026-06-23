---
layout: guide
title: "Positive Framing: `Do This` vs `Don't` Do That"
---

# Positive Framing: "Do This" vs "Don't Do That"

## The Pattern

Instructions framed as "do this" outperform "don't do that" - and the reason is intuitive once you understand how language models work.

Claude is predicting what good output looks like. "Don't use bullet points" tells Claude what to avoid but leaves the target undefined. "Write in flowing prose" gives Claude something to aim at.

**The positive version is more information.**

## Why This Matters

When you write instructions negatively, Claude has to:

1. Understand the constraint (don't do X)
2. Infer what you want instead (probably Y? maybe Z?)
3. Hope it guessed right

When you write instructions positively, Claude:

1. Understands the target (do X)
2. Produces X

Less inference, fewer failure modes.

## Examples

### Formatting

❌ "Don't use bullet points"
✅ "Write in prose paragraphs"

❌ "Don't be too formal"
✅ "Use contractions and conversational tone"

### Interaction

❌ "Don't ask too many questions"
✅ "Ask one clarifying question per response, maximum"

❌ "Don't over-explain"
✅ "Lead with the answer, add context only if I ask"

### Content

❌ "Don't include unnecessary caveats"
✅ "State your position directly, flag uncertainty only when it changes the recommendation"

## The Combination Works Best

"Write in prose, not bullet points" gives both the target and the fence.

This is clearer than either alone:

- Positive only: "Write in prose" (but Claude might still use bullets for lists)
- Negative only: "Not bullet points" (but what format instead?)
- Combined: "Prose, not bullets" (target + constraint = clear instruction)

## When Negative Framing Is Useful

Sometimes the constraint is the point:

**"Never expose API keys in code examples"** - The violation is severe, the alternative is context-dependent. Leading with the prohibition is correct.

**"Don't mention this is from a Communication Guide"** - The thing to avoid is specific, the alternative is just "talk naturally."

But even here, you can often strengthen it:
**"Keep API keys in environment variables in code examples"** - Still prohibits the bad thing, but shows the right thing.

## Applying This to Your Communication Guide

Review your guide for negative instructions. Ask:

- What do I want instead?
- Can I say that directly?

Transform:

- ❌ "Don't be sycophantic"
- ✅ "Question my assumptions. Push back when you disagree. Be a peer, not a pet."

The second version gives Claude actual behavior to produce, not just behavior to avoid.

## The Specificity Layer

Positive framing combines with specificity:

- ❌ "Be direct" (vague positive)
- ✅ "Lead with the answer, then explain reasoning if needed" (specific positive)

- ❌ "Don't be indirect" (vague negative)
- ✅ Still worse than the specific positive version

**Positive + Specific = Most Effective**

## Common Mistake: Assuming "Obvious"

You might think: "Obviously if I say don't use bullets, Claude will use prose."

Maybe. Or maybe Claude will use:

- Numbered lists
- Definition lists
- Headers without content
- Something else entirely

Saying "use prose" removes the ambiguity.

## Practical Exercise

Take one negative instruction from your Communication Guide:

**"Don't \_\_\_\_"**

Rewrite it as:

**"Do \_\_\_\_"**

Then ask: Is the second version clearer to someone who doesn't share my context?

If yes, keep the positive version. If no, you might need the combination approach: "Do X, not Y."

## Next Steps

- Combine this with [Explicit Naming](explicit-naming.md) for even clearer instructions
- Apply it when writing [Communication Guides](../core-concepts/communication-guides.md)
- See [Tam's System](../case-studies/tams-system.md) for examples in practice

---

**Key Insight:** "Don't do X" makes Claude guess. "Do Y" tells Claude exactly what you want. Less inference = better results.
