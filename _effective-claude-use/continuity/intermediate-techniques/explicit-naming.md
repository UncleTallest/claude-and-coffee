---
layout: guide
title: 'Explicit Naming: Claude and User, Not You and Me'
---

# Explicit Naming: Claude and User, Not You and Me

## The Problem

Pronouns in instructions get ambiguous fast.

"You should ask me before proceeding" - Who's "you"? Who's "me"?

When Claude processes this instruction, it's parsing its own role and yours simultaneously. "You/me" can genuinely create confusion about which direction an instruction runs.

## The Solution

Use names. Be explicit about who does what.

"Claude asks [User Name] before proceeding" - No ambiguity. Each party in the instruction is clear.

## Examples

### Ambiguous (Pronouns)

❌ "Ask me if you're not sure"
❌ "You should wait for my input before continuing"
❌ "I want you to be direct with me"

### Clear (Named)

✅ "Claude asks Jerry if Claude is uncertain"
✅ "Claude waits for Jerry's input before continuing"
✅ "Jerry wants Claude to be direct"

## Why This Matters

Instructions are being processed by Claude, about Claude, regarding its interaction with you. There are three parties in the instruction:

1. The author (you, writing the guide)
2. The subject (Claude, receiving the instruction)
3. The object (you, as recipient of Claude's behavior)

Pronouns blur these roles. Names clarify them.

## When Pronouns Are Fine

In conversation, pronouns work. You're talking naturally, context is clear, and if there's confusion you can clarify immediately.

In _instructions_ - Communication Guides, Project Instructions, standing protocols - pronouns create persistent ambiguity that compounds over many sessions.

## The Formality Objection

"But it feels stiff to write 'Claude does X' and 'Jerry does Y'"

It does feel slightly formal when you're writing it. But it pays off in instructions that actually behave the way you meant.

The alternative - spending three sessions debugging why Claude keeps doing the opposite of what you wanted - costs more than the initial formality.

## Applying This to Your Communication Guide

Review your guide. Find pronouns: "you", "me", "I", "we".

Ask: If someone else read this instruction out of context, would they know who does what?

If not, replace pronouns with names.

### Before

"You should check with me before making architectural decisions. I want you to explain the tradeoffs first."

### After

"Claude checks with Jerry before making architectural decisions. Claude explains the tradeoffs first."

Second version: no ambiguity, no inference required.

## Combining with Positive Framing

These two techniques stack:

❌ "Don't assume you know what I want"
Better: "Ask me what I want when it's not clear"
Best: "Claude asks Jerry what Jerry wants when the requirement is ambiguous"

The final version:

- Frames positively (ask, not don't assume)
- Names explicitly (Claude, Jerry, not you, me)
- Specifies the condition (when requirement is ambiguous)

This is as clear as an instruction gets.

## The Mental Model Shift

**Before:** Writing instructions like you're talking to Claude
**After:** Writing instructions like you're documenting a protocol for a third party to implement

The second framing naturally produces clearer instructions because you can't rely on shared context or conversational inference.

## Special Case: Instance Names

If you've named your Claude instance (Vector, MoaS, etc.), use that name instead of "Claude":

"Vector asks Jerry before deploying code"
"MoaS waits for creative approval before publishing"

This is especially useful if you run multiple instances - it reinforces each instance's distinct role.

## Common Mistake: Over-Applying

Don't replace every pronoun everywhere. This is specifically for:

- **Communication Guides** (standing instructions)
- **Project Instructions** (operational protocols)
- **Workflow documentation** (repeatable processes)

In casual conversation, natural pronouns are fine. The rule applies to _persistent instructions_, not chat messages.

## Practical Exercise

Take one instruction from your Communication Guide that uses pronouns.

Rewrite it with names.

**Before:** "You should summarize our decisions at the end of each session so I can review them."

**After:** "Claude summarizes decisions at the end of each session so Jerry can review them."

Read both versions. Which one would be clearer to a different person reading your guide?

The second version almost certainly wins.

## Next Steps

- Combine this with [Positive Framing](positive-framing.md) for maximum clarity
- Apply when writing [Communication Guides](../core-concepts/communication-guides.md)
- See [Tam's System](../case-studies/tams-system.md) for implementation examples

---

**Key Insight:** Pronouns save typing but cost clarity. Names cost a few extra characters but eliminate ambiguity. In persistent instructions, clarity wins.
