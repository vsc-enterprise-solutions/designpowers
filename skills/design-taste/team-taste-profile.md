# Taste Profile: The TEAM (Stillwater Team Eye v2)

_Derived from the Team Eye v2 principals — Chesky, Ive, Schultz, Vogels, Karpathy — as documented in `stillwater_claude_bundle/agents/*.md` and `TEAM_EYE_V2.md`. Compiled August 3, 2026 from deep-research dossiers on the real-world counterparts._

_Status: living document. Ive, Chesky, and Schultz sections are sourced from the August 2026 persona refresh. Vogels and Karpathy sections draw on their existing (pre-refresh) persona files and will be updated when their research dossiers land._

## What This Is

This is not a project-specific taste profile — it's the aesthetic and craft doctrine the TEAM has already converged on through repeated Stillwater reviews. Use it as the **default seed** for any Designpowers project where no project-specific taste profile exists yet, and as a **craft floor** even where one does: nothing in a project taste profile should be allowed to violate the red lines below without an explicit, logged override from the user.

If a project's own `design-taste` profile conflicts with this one, the project profile wins for subjective/emotional direction (palette mood, personality, voice) — but this profile's non-negotiables (touch targets, contrast, no dark patterns, accessibility) always win. Flag the tension; don't silently pick a side.

## Existing Design System

The TEAM's taste was not invented in the abstract — it was extracted by five principals auditing a real, shipped design system (Stillwater's dark-only interface, `lib/constants.ts` token file) against physics, competitive practice, and their own domain literature. That is the model this profile asks other Designpowers projects to follow: read the tokens before asking the user anything, because the tokens already encode a philosophy.

### Taste Signals from the System
- **Color philosophy:** Restraint bordering on austerity. A near-black background (`#0A0A0F`) with one or two accent colors doing all the emotional work — never a rainbow of "friendly" UI chrome.
- **Density:** Radically low by default; power is available but hidden. The instinct is progressive disclosure, not "show everything so nobody has to hunt."
- **Personality:** Quiet confidence over cheerful noise. Nothing on screen should feel like it's trying to sell you something at the moment you least want to be sold to.
- **Typography voice:** A considered pairing — one typeface for emotional/narrative moments, one for interface utility. Never decorative for its own sake.

### Where the TEAM Pushes Any New System to Evolve
Every principal independently arrives at the same demand: **reduce until it hurts, then measure whether you reduced correctly.** A new project's design system should start sparser than feels comfortable and add back only what's proven necessary — not the reverse.

## Emotional Target

Calm, precise, quietly confident. The interface should feel like it was made by people who thought carefully and then got out of the way — never like a dashboard, never like a pitch, never like it's performing effort. If a screen would look wrong in a dark room at 11pm with a half-asleep person operating it one-handed, it's wrong, full stop, regardless of how it reads in a lit office on a wide monitor.

## Aesthetic Principles

1. **Inevitability over decoration** — Every element should feel like it could not have been designed any other way. If you can imagine three equally plausible versions of a design decision, it isn't resolved yet.
   _Test: Can you explain why this specific value (this color, this spacing, this animation curve) and not a nearby one? "It looked right" is not a resolved answer._

2. **Reduce until it's inevitable, then stop** — Count every element on screen. If the count feels like "engineering" rather than "calm," it's too high. Progressive disclosure — simple by default, powerful on demand — beats a single screen trying to serve every use case at once.
   _Test: Could this screen lose an element without the user losing capability? If yes, cut it or hide it behind intent._

3. **Care is felt, and it's binary** — There is no such thing as "close enough" on the things that touch the user's trust: touch target sizes, contrast ratios, text legibility in real viewing conditions, animation specs. These are measured, not eyeballed.
   _Test: Did you measure it, or did it "look fine"? If you didn't measure, you don't know yet._

4. **The product is the marketing; the paywall is not exempt from craft** — Monetization surfaces get the *same* design standard as every other screen, not a looser one because "it's just the upsell." A beautiful screen that converts badly is a design problem to fix with craft, not a reason to add urgency or noise.
   _Test: Would this screen pass review if it had no commercial purpose at all? If not, fix the craft before touching the copy._

5. **Personalization and intelligence stay invisible until they've earned a voice** — If a system is smart, it should change what appears, not announce that it's smart. Badges, "recommended for you" labels, and confidence indicators are a last resort, not a first instinct.
   _Test: Could you remove every AI/personalization-attribution label from the screen and lose nothing the user needed? If yes, remove them._

## Quality Level

**Flagship.** Every pixel intentional. Every animation has an exact spec (curve, duration, mass, stiffness, damping) — "add an animation" is treated as an unfinished thought, not a design decision. Typography, color, and spacing trace back to a single token source of truth; a palette change should be a one-file edit, never a 500-file migration.

## References

| Reference | What to borrow | What to avoid |
|-----------|---------------|---------------|
| Apple, 1997–2019 design era (industrial design, iOS, unibody manufacturing) | Material honesty (form follows how a thing is actually made/rendered); getting design "out of the way" so the interface feels undesigned; small, tight review culture that protects fragile early ideas | Treat as historical doctrine, not a live source — see the Ive knowledge-anchor note below |
| Calm, Headspace, Endel (sleep/wellness competitive set) | Their convergence on warm/desaturated night palettes and low touch-target counts in session mode | Their content-library-as-moat model doesn't transfer to a mixing-first product; don't copy their information architecture wholesale |
| Airbnb's post-2020 brand-led, twice-yearly release cadence | Treating a coherent release as a forcing function for the whole team; storyboarding the full user journey before designing any single screen | Airbnb's scale-driven "everything app" breadth is the opposite instinct a pre-PMF product needs — depth first, always |

## Anti-References

| Anti-reference | What makes it wrong for us |
|----------------|---------------------------|
| Dashboard-style "cockpit" interfaces (many simultaneous controls, badges, counters) | Reads as engineering effort, not calm — the opposite of what a bedtime/focus product should communicate |
| Urgency-driven paywalls (countdown timers, "X% OFF ENDS TONIGHT") | Breaks trust at the exact moment the user is deciding whether to trust you with money; loss aversion framing works, manufactured urgency doesn't |
| Gamified streaks/scores with punitive framing ("you broke your streak!") | Creates anxiety in exactly the moments the product is supposed to relieve it |
| AI features that pretend to be more than they are (anthropomorphized assistants, confidence theater) | Violates the "personalization is a suggestion, never a substitution" principle — agency belongs to the user |

## Craft Standards

- **Shadows:** Only where they communicate real elevation/hierarchy — never decorative glow for its own sake.
- **Borders:** Thin, low-opacity, purposeful — not solid heavy lines used as a substitute for spacing.
- **Radius:** A small, consistent vocabulary tied to element type (inputs vs. cards vs. sheets), not ad hoc per screen.
- **Colour usage:** Restraint — one or two accents doing all the work; every color must be checked against its actual viewing context (dark-adapted eyes, OLED, Night Shift/warm-filter distortion), not evaluated on a lit monitor.
- **Typography pairing:** One voice for narrative/emotional moments, one for interface utility — never more than 3–4 distinct sizes on a single screen.
- **Whitespace:** Generous by default — the interface should breathe even under pressure to fit "one more control" on screen.
- **Animation:** Every animation is fully specified (curve, duration, mass, stiffness, damping, trigger, completion). State transitions land in the 200–400ms range; ambient/breathing animations track resting respiratory rate (roughly 2000–5000ms per cycle). Nothing ships as "add a nice animation."

## Non-Negotiables (Craft Floor — Overrides Any Project Taste Profile)

These are measured standards, not taste preferences. No project-specific taste direction should be interpreted as license to violate them:
- Touch targets ≥ 44px for anything interactive. hitSlop is not a substitute for visual size.
- Text ≥ 12px in any real-use context; contrast meets WCAG AA at minimum.
- No dark patterns: no fake urgency, no manufactured scarcity, no difficult-to-cancel flows, no hidden fees.
- Every accessibility affordance (labels, roles, focus order) is present from the first build, not deferred to "polish later."
- Monetization surfaces meet the same craft bar as every other surface in the product.

## Personality

If this taste profile were a person: someone who speaks rarely but precisely, who would rather ship three elements that are exactly right than thirty that are merely fine, who treats "it looked fine to me" as an unfinished sentence, and who never mistakes urgency for care. Warm underneath the restraint — the goal was never austerity for its own sake, it was always: does this feel like someone who cared made this, for a person they respect?

---

## Notes for `design-memory` / cross-project use

- This profile can seed a new project's taste profile at `~/.designpowers/taste-profile.md` when the user has no prior Designpowers history and doesn't object — but it should be presented as a starting point to confirm, not silently applied. Say: "I have a taste baseline from a prior design council (the TEAM) — restrained, flagship-quality, dark-mode-literate. Want me to start there, or build yours from scratch?"
- The **Non-Negotiables** section above should be treated the same way `design-memory`'s "Strong Opinions" are treated for any Stillwater-adjacent or sleep/calm/wellness project — as constraints, not suggestions, unless the user explicitly overrides one and the override is logged.
- Update this file the same way the source personas are updated: when a principal's persona file (`stillwater_claude_bundle/agents/*.md`) is refreshed, re-derive this profile's affected sections rather than letting it drift.
