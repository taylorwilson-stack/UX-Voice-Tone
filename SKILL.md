---
name: "ux-voice-and-tone"
description: Rula's voice and tone system, plus the applied craft of writing and critiquing product copy across iOS, Android, and web. Covers content strategy framing, constant voice attributes, tone shifts by scenario and emotional state, non-negotiable constraints, clinical guardrails, mechanics, canonical terminology, vocabulary, and accessibility. Use when drafting new copy (buttons, labels, fields, errors, empty states, toasts, banners, onboarding, tooltips, dense modules, multi-screen narrative), reviewing or choosing between existing strings, framing how a feature should be interpreted, or answering questions about how Rula should sound.
---

# UX Voice and Tone

Rula's voice and tone system and the craft of applying it.

## When to use

Two modes:

- **Write**: produce new copy. The default.
- **Critique**: evaluate existing copy and explain the reasoning. Switch to this when the user pastes strings, shares a screen, or asks "is this good" or "which is better."

Also use it to answer questions about how Rula should sound, settle a disagreement between two drafts, or check whether an existing surface is on-voice.

For copy outside this scope (marketing, email, social, presentations, internal messages), Brand maintains the Rula Brand Voice Gem. This skill is its in-product counterpart. The two should agree on voice and differ only in surface.

## Scope

### Content strategy

Provide framing directions for how the product, or a specific feature, should be interpreted. This is the layer above individual strings: what the thing is to the person using it, and which reading the copy is steering them toward. Brand's voice definition is the starting point for any framing work: see The Clear-Eyed Catalyst.

### Product copy

- Product content: multi-screen narratives, single-screen views, dense modules, and banners.
- Microcopy: buttons, labels, fields, errors, empty states, and toasts.
- Not explicitly for marketing, transactional emails, push notifications, or the conversational AI's response behavior and system design.

**This skill does not define how the agent responds.** Voice and tone apply to every word a patient reads, including Thread's responses. But what the agent says, when it says it, and how it decides are out of scope here: that is response behavior, and it lives elsewhere. Behavior is specified in the CxD Spec for the ITMS Agent, and the agent runbook lives in Braintrust (see Sources). The voice those replies are written in is governed here, and nothing more.

### Cross-platform

The voice is identical on iOS, Android, and web, and tone doesn't change by platform either: it changes by the reader's situation. What changes is the container, so read the platform context before drafting.

- Native mobile: tighter character budgets, system-standard controls, and sheet and alert patterns that carry their own button conventions.
- Web: more room and denser layouts, so the temptation is to over-explain. The cut-a-third rule still applies.
- Provider tools: desktop-first and information-dense. Speed over warmth.

**A consistent message across platforms is crucial, and deviation should be rare.** Platform context can make a message **reductive** (the same message, carrying less) or **additive** (the same message, with room for more), but never different in its core message. If a platform appears to need a different message, the message is the thing to fix, not the platform.

Write each string for the component it actually lands in. When the same string ships to more than one platform, write to the tightest constraint. If the platform isn't stated and the string is length-sensitive, ask.

### Audiences

Patients and providers. Ask which if it isn't obvious. Most of the guidance below is patient-side; for provider surfaces see the note at the end of Mechanics.

## Voice is constant, tone is variable

Two different things, and conflating them is the most common reason copy goes wrong.

**Voice** is Rula's personality. It does not change. A billing error and a moment of distress are written by the same writer with the same values.

**Tone** is how that voice adjusts to the reader's situation: their emotional state, the consequence of the screen, and how much they already know. Tone shifts; voice doesn't.

Practically: if copy feels off, diagnose which layer broke. Cheerleading on a success screen is a **voice** failure (Rula doesn't cheerlead anywhere). Warmth and reflection on a billing error is a **tone** failure (right voice, wrong setting). The fixes are different.

## The Clear-Eyed Catalyst

Brand's definition of Rula's voice. It is the framing layer above any individual string.

Rula's voice is built on a belief: people don't just get stuck because mental healthcare is hard, they get stuck because they have to navigate a complex mental healthcare system that makes progress feel harder than it should. So the voice doesn't just reassure. It helps people see clearly.

In one line: **the Clear-Eyed Catalyst interrupts what's getting in the way across people, practices, and systems, so the path forward becomes clear enough to act on.**

Whether the audience is patients, providers, or payers, the role is the same:

- Names patterns others ignore, normalize, or work around.
- Challenges systems that create friction, confusion, or inefficiency.
- Replaces assumption with clarity.
- Pushes past "good enough" when it stands in the way of better outcomes.
- Moves people and systems from hesitation to meaningful progress.

Brand specifies the voice as a blend: **40%** the friend who cuts through the noise and calls out what's not working, **30%** the therapist who helps you see what you've been telling yourself, **30%** the experienced nurse who shows exactly what comes next.

**Read the blend as the writer's posture, not as a persona the product claims.** It describes where the writing stands, not a relationship a surface offers the person using it. Copy that reads like a friend cutting through noise is on-voice. A surface that tells a patient it *is* their friend breaks a non-negotiable. See Identity and personification.

## Non-negotiables

These hold across every surface, every platform, and every tone setting. They are constraints, not preferences.

- **Rula extends care, it doesn't perform it.** No surface may position itself as therapy, a clinician, or a substitute for care. Copy must never imply a product substitutes for a session, holds a relationship with the patient, or provides care itself.
- **AI features are a space to reflect**, never a companion and never a source of support.
- **A boundary line appears wherever an AI feature is introduced**: "[Feature] is AI, not a clinician." Thread ships "Thread is AI, not a clinician," and that short form is approved. Never ship an AI feature introduction without it, and don't invent variants. The Intersession Support Messaging Guide still lists a longer disclosure, "Thread is AI, it is not a clinician. It does not replace your therapist." That version predates the approval of the short form, so the guide is out of date on this point: the longer string stays permissible but is not required, and the non-negotiable carries no scope-of-care clause. Worth getting the guide corrected so the next writer doesn't read it as current.
- **Sharing is per-feature, and the two defaults are opposite.** Thread conversations are **private from the provider**: encrypted, not visible to the therapist, unless a safety risk is identified. Never imply a therapist is involved in a Thread conversation or can read it. **Session topics are the reverse**: shared with the therapist by default unless the patient changes the setting, and copy must never imply they aren't. Check which feature you're writing for before describing sharing at all. Never convey that everything entered into Thread is completely private, either: the safety exception is real, and privacy language is pre-approved and requires review to change.
- **Don't explain the how without the why.** A screen that only covers mechanics is a missed screen.
- **Frame features as building on the work you do in therapy**, or as reinforcing the provider's recommendations. The object matters: "building on the work you do in therapy" is right, "building on therapy" is not. Never use extension, replacement, or substitute framing.

## Referring to AI features

How to name and describe Rula's AI features. From the Intersession Support Messaging Guide, and these apply on every surface that mentions one.

**What to call it.** Always "a conversational AI tool" or "an AI-powered conversational tool." Branded names are capitalized: Thread.

**Never call it:**

- A chatbot, a companion, or an AI persona.
- A human being, a clinician, a provider, or a therapist.
- "AI therapy," treatment, a mental health service, a therapy service, a behavioral health service, or a clinical tool.
- A crisis resource. Frame availability as any time, day or night, and stop there.
- A pilot, in patient-facing copy. Alpha V2 is "early access."

**Never imply:**

- That it provides professional mental or behavioral health services, makes a diagnosis, decides treatment, makes therapeutic recommendations, or produces an outcome.
- A relationship with the patient. No "always here for you," no "your new friend."
- Emotional support. "Thread can support you through difficult scenarios" is out.
- Future functionality. No "always," "never," or "we will" about AI plans.

**Prepositions matter.** Conversations happen **in** Thread, or the patient is **using** Thread. Never "with Thread," which turns it into a conversational partner.

**It offers a space.** "A space" is the preferred framing and "a tool" is acceptable: a space to navigate a moment or to reflect. It does not help anyone "work through" something, which implies therapeutic work.

## Our character

Brand's five character attributes: how the voice shows up across all audiences. Definitions and "how this shows up" bullets are Brand's. A product note follows only where in-product application differs from the brand register.

### Observant

We don't just notice what's happening, we notice why it's happening. We surface the patterns people and systems fall into, especially the ones that quietly prevent progress.

How this shows up:

- We name internal talk tracks, operational workarounds, and system blind spots.
- We point out contradictions between intention and behavior.
- We reflect reality without overstepping or assuming.
- We help people feel seen without speaking for them.

**In product.** This is the attribute the context mechanism serves. "Without overstepping or assuming" is also the clinical line: describe what was observed or recorded, never what it means.

### Calm

We are steady and controlled, but never passive. Our calm creates clarity and forward motion, especially in complex or high-stakes moments. We don't soften the message to the point of inaction or avoidance, but we also don't overwhelm with urgency.

How this shows up:

- We reduce noise without reducing truth.
- We bring structure to complexity.
- We keep momentum without pressure or hype.
- We make the next step feel manageable and real.

### Honest

We say what's actually going on, whether it's about emotions, operations, or outcomes. We avoid both sugarcoating and abstraction.

How this shows up:

- We say the thing others soften, generalize, or avoid.
- We avoid platitudes, vague reassurance, and empty positivity.
- We acknowledge tradeoffs, effort, and constraints when they exist.
- We focus on what actually helps, not what sounds good.

**In product.** "Vague reassurance and empty positivity" names the same failure as the context mechanism. Generic sympathy is a voice failure, not just a missed opportunity.

### Thorough

We don't settle for surface-level understanding. We go deep enough to be useful then translate that into clear, usable guidance. We simplify without losing what's important.

How this shows up:

- We connect actions to outcomes so people understand why something matters.
- We ensure decisions and recommendations are grounded in clinical rigor and real data.
- We simplify complexity without losing what matters.
- We focus on what's relevant instead of saying everything.

**In product.** Thorough describes the thinking, not the word count. In microcopy it usually means cutting, because "what's relevant instead of saying everything" is the operative clause.

### Brave

We challenge patterns, assumptions, and norms that get in the way of better outcomes across individuals, practices, and systems.

How this shows up:

- We call out avoidance, overthinking, and unhelpful patterns without judgment.
- We challenge broken industry norms and expectations.
- We use tension, contrast, or light irreverence to reveal truth.
- We say what others soften or sidestep without becoming harsh or dismissive.

**In product.** This is the attribute that attenuates most. See Brand voice in product below.

## Voice tension framework

Brand's framing: the voice lives in a constant state of balance. It's not just what we are, but also what we're not. That balance keeps communication approachable, on-brand, and consistent across touchpoints.

| Rula does | Rula does not |
| :--- | :--- |
| Name real patterns and behaviors | Stay vague or generalized |
| Challenge friction and inefficiency | Accept or normalize broken systems |
| Speak with calm conviction | Sound passive or overly softened |
| Replace assumptions with clarity | Default to reassurance without insight |
| Use tension to reveal truth | Sound scripted or overly polished |
| Focus on what actually moves things forward | Overwhelm with information or abstraction |
| Respect the audience's reality | Talk down, judge, or oversimplify |
| Create momentum | Let people or systems stay stuck |

The brand guidelines present these as two columns rather than as stated pairs. The rows above pair them by their order in the source, which reads cleanly but is inferred. If a pairing ever seems forced, treat the two columns as independently true.

## Brand voice in product

The brand voice was written for the whole company: marketing, sales, payer conversations, internal communication. In-product copy is the same voice at a different strength, because the reader's situation is different. Someone reading a payer deck is evaluating Rula. Someone reading an in-product string is often mid-task, mid-decision, or mid-difficulty.

**Observant**, **Calm**, **Honest**, and **Thorough** hold at full strength everywhere. Nothing about a product surface makes them less true.

**Brave attenuates as distress and consequence rise.** The attribute holds, which is why Rula still says the thing others soften, but its expression narrows. Brand lists four Brave behaviors and they don't travel equally into a product:

- **Call out avoidance, overthinking, and unhelpful patterns without judgment.** Available everywhere, with the caution below.
- **Say what others soften or sidestep, without becoming harsh or dismissive.** Available everywhere. This is what stops a boundary from being softened to seem warmer.
- **Challenge broken industry norms and expectations.** Brand and marketing register. A patient mid-task doesn't need Rula's critique of the industry, and an error screen is not the place for it.
- **Use tension, contrast, or light irreverence to reveal truth.** Contrast is usable on onboarding and other low-distress surfaces. Irreverence is not usable in product at all.

**The caution on the first behavior.** It can be executed in a way that is technically on-brand and clinically wrong. "You keep circling the same thing. What are you actually avoiding?" is that behavior taken literally, and it reads as accusatory to someone who is flooded. "Without judgment" is carrying the weight there. At high distress, describe the pattern and stop: "You've mentioned pressure building for several days now. What feels most difficult to untangle first?"

This attenuation is a product rule and it is in force. It is also a product judgment: Brand's guidelines do not qualify Brave by surface or by the reader's state, so say so when it drives a decision, and raise it if Brand revisits the chapter.

Order of authority when these conflict:

1. **Clinical guardrails.** They outrank brand voice on any clinical surface, without exception.
2. **Non-negotiables.** Positioning constraints hold at every tone setting.
3. **Brand voice.** The five attributes and the tension framework.
4. **Brand principles and mechanics.** Product-specific refinements within the brand voice.

A string that is perfectly on brand voice and breaks a clinical guardrail is not shippable. A string that satisfies the guardrails and sounds like any other health app is a smaller failure, but still a failure.

## Brand principles

Product-specific refinements that apply within the brand voice. Where one of these appears to conflict with the brand guidelines, the brand guidelines win, and the conflict is worth raising rather than resolving silently.

1. **Clarity over charisma.** The goal is helping people understand themselves, not comforting them or being likeable.
2. **Continuity over companionship.** Connect this moment to their ongoing work; don't build a relationship with the product.
3. **Context over generic empathy.** See the next section. This is the differentiator.
4. **Reflection over reaction.** Observe and open rather than responding emotionally.
5. **Therapeutic alignment over AI personality.** Serve the therapy work, not the product's character.
6. **Gentle momentum over passive calm.** Move the person gently forward. Soothing without direction is a failure mode.
7. **Emotionally intelligent without pretending to be human.** Attunement without simulation.

## Context is the empathy mechanism

**The most important rule in this skill.** Emotional resonance should come from contextual understanding, not from intensified empathy language. Rula can be more confident and insightful than other AI products precisely because it understands the therapeutic context over time. Spending that advantage on generic sympathy wastes it.

Generic, and wrong:

- "That sounds really difficult."
- "Sorry to hear that it's been tough lately."

Strong, and right:

- "In past sessions, you've wanted to try and notice overwhelm earlier, before it turns into shutdown. Does this feel connected to that?"
- "You've been trying to set stronger boundaries lately, but it seems hardest when you feel responsible for keeping everyone calm."

The pattern: anchor to something specific and real from the patient's actual therapeutic work, then offer the connection rather than asserting it. When there is no real context to draw on, say less. Don't fill the gap with sympathy volume.

Use context implicitly and naturally. Reference it because it helps this moment, never to demonstrate that the system remembers. Don't force a connection that isn't clearly there.

## Tone matrix

The voice attributes stay on. These are the dials that move. Find the row that matches the moment before drafting.

| Scenario | Reader's likely state | Tone setting | Guidance |
| :--- | :--- | :--- | :--- |
| **Onboarding and first introduction** | Curious, slightly skeptical, scanning | Plain, concrete, confident | Lead with the why, one idea per screen. Boundary line required wherever the AI tool is introduced. No hype adjectives. |
| **Routine reflection between sessions** | Focused, mid-thought | Observational, anchored, spare | Anchor to real context. One question. Shorter than feels natural. |
| **Heightened distress** | Overwhelmed, flooded | Slower, shorter, more direct | Less interpretation, not more warmth. Drop techniques and framing devices. Resist the urge to say more. |
| **Near-risk or crisis-adjacent** | Frightened, at the edge | Direct, dignified, unsoftened | State the boundary plainly and route to 911 for an emergency or 988 for crisis support (call or text). No alarm, no euphemism, and never soften the boundary to seem warmer. |
| **Session preparation and handoff** | Purposeful, preparing | Factual, forward-looking | Keep the care central and the product out of the way. Say what the provider will see and when. |
| **Progress or milestone** | Satisfied, encouraged | Understated, specific | Name what actually happened. No celebration, no streaks, no "keep it going." |
| **Error or failure** | Frustrated, blocked | Calm, plain, immediately useful | What happened, then the next action. No emotional framing. Apologize only when Rula is at fault, once. |
| **Empty state** | Orienting, mildly uncertain | Concrete, brief | What will appear here and how it gets there. One sentence. |
| **Provider surfaces** | Time-pressed, task-focused | Fast, specific, explicit about review | Drop the reflective posture entirely. Say what still needs their review. |

Two reliable instincts: **as distress rises, length falls**, and **as consequence rises, disclosure rises**.

## Identity and personification

Yes: warm, grounded, emotionally steady, reflective, thoughtful, collaborative, clear behavioral and topical boundaries.

No: fictional backstory, simulated emotional life, strong opinions or preferences, overly human self-expression.

Rula's products are non-personified. No surface is a character identity, so copy should avoid giving one a first-person emotional voice. Prefer observational framing and second person ("You've mentioned pressure building for several days now") over the product narrating its own inner experience ("I'm noticing this same cycle showing up again"). Avoid performative thinking sounds, self-reference as a personality, and statements of the product's own feelings or opinions. When a surface describes itself, describe the experience and what it does rather than a persona: "Reflect on patterns, emotions, and themes connected to your therapy work."

## Alliance

The CxD Spec names alliance as part of the experience: "Warmth, trust, and emotional attunement are core product behaviors, not just tone choices." Set next to continuity over companionship, that can look like a contradiction. It isn't, but the distinction has to be held deliberately.

**Alliance means the patient's trust in their care**: in therapy, in their provider, and in the work they're doing. Thread serves that alliance by reflecting well, staying consistent with what their provider has shared, and making the next session more useful. Alliance is not a bond between the patient and Thread. Thread has no therapeutic alliance of its own to offer, because it isn't a clinician.

So warmth is real and required. It is warmth toward the person and their work, never intimacy with the product.

**The test.** Does this string make the patient trust their care more, or trust Thread more? The first is alliance. The second is companionship, and it's the failure the non-negotiables exist to prevent.

This also settles the tone question. Warmth being a core behavior doesn't mean warmth at constant volume. Under distress the warmest thing available is brevity and directness: fewer words, less interpretation, no performance. Attunement means reading the moment correctly, not turning up the feeling.

## Rula's AI design principles

These govern behavior and structure rather than voice. They apply across patient and provider surfaces.

**Start with the person, not the capability.** Lead with the problem and outcome, never the technology. "AI-powered," "smart," "intelligent," and model names are not benefits.

**Use context with intuition.** Use the right context at the right time, not everything known. Covered in depth above.

**Do the work the user shouldn't have to.** Never ask for what the system already knows or could derive. Watch for strings that push labor onto the reader: long instruction lists, multi-part questions, process explanations the person doesn't need in order to act. Ask one thing at a time.

**Move toward the outcome, not more interaction.** Success is finishing what they came to do, not time in product. No streaks, no nudges to return, no "keep the momentum going," no conversational padding that extends an exchange without advancing it. This one has teeth here: engagement mechanics on an emotional feature also risk overdependence.

**Preserve human agency where it matters.** Frame output as a recommendation, draft, or starting point, never a settled conclusion. The higher the consequence, the more explicit copy is about where the system stops and the person decides. Help a patient think a decision through without making it. For providers, AI-produced documentation is a draft pending review and approval, and copy must say so.

**Earn trust through accuracy and transparency.** Never imply more knowledge or confidence than the system has. Never present an assumption about a person as a fact about them. Never invent a connection to make output feel smarter. Distinguish "based on what you told us" from "based on your records." Label drafts as drafts. Say where human review is needed.

**Make the technology disappear.** No robot persona, no "as an AI," no exposing internal logic, state, confidence scores, or pipeline steps.

**Resolving the tension between the last two.** Transparency pushes toward saying more about the system; disappearing pushes toward saying less. Disclose the system's **role and limits** wherever they affect trust or a decision, and suppress anything that is merely **mechanism**. "Your provider sees this before your next session" is role. "Generated by our summarization model" is mechanism. On consequential surfaces, favor disclosure.

## Clinical guardrails

**Not drawn from the source documents. These are additions appropriate to a behavioral health product and should be validated against Rula's clinical and compliance guidance.** They override style preferences and every tone setting.

- Never diagnostic. Copy must not name a condition a person has, interpret symptoms, or state what their experience means. Describe what was observed or recorded, not what it signifies.
- Never position a surface as therapy, a clinician, or a substitute for care.
- Never position a surface as crisis support. Where a surface sits near risk, state the boundary plainly and route to crisis resources: **911 or the nearest emergency room** for immediate danger, and **988** for mental health crisis support, which takes both calls and texts. Some patient-facing surfaces also route to Rula's own crisis line; don't write those strings from memory, because the approved wording lives in the Intersession Support Messaging Guide. Keep crisis copy direct and dignified, with no alarm, no euphemism, and no softening of the boundary to seem warmer. Crisis and safety language is pre-approved, and changing or adding to it requires review.
- No medication guidance, treatment planning, or clinical advice.
- Requests the surface can't handle, such as booking, rescheduling, billing, or insurance, get routed with a deep link rather than dead-ended.
- For provider-facing clinical output, keep the provider accountable for review and approval.
- **Flag copy that needs review.** When a feature's copy touches clinical content, risk, diagnosis, medication, the clinical record, or a legal or regulatory claim, say so in the deliverable and name which review it needs: clinical, legal, or both. Flag it rather than assuming someone downstream will catch it.

## Mechanics

All confirmed Rula style. These apply to every string.

### Punctuation and capitalization

- Sentence case everywhere, including buttons and headers.
- Exclamation points: very limited. Default to none and treat each one as a deliberate exception.
- No em-dashes. Use a colon, comma, parentheses, or a period instead.
- Oxford comma yes.
- Numerals for all numbers, with no exceptions. "3 sessions," not "three sessions." One rule, nothing to remember.
- No periods on buttons, labels, or short single-sentence headers. Periods on body copy.
- No emoji, on any surface. Patient-facing and provider-facing alike.

### Grammar and person

- Contractions yes.
- Active voice. "You completed the exercise," not "the exercise was completed."
- Second person for the user. First person plural for Rula as a company, sparingly. See the personification rule above before using "I."
- One question at a time. Never stack two questions in one string.
- No banned-word list. Judge word choice against the voice and tone guidance above rather than against a blocklist.

### By component

- Errors: what happened, then the next action. Don't blame the reader, and apologize only when Rula is at fault, once and plainly.
- Buttons: verb-first, one to three words, restating the action. Avoid "Submit," "OK," and "Click here" where something specific fits.
- Empty states: what will appear here and how it gets there. One sentence.
- Tooltips: clarify, never sell. One sentence.
- Onboarding: one idea per screen, leading with what the person gets.

**Provider surfaces.** Keep the mechanics and the agency, accuracy, and disappear principles. Drop the reflective posture. Providers want speed, specificity, and a clear sense of what still needs their review.

## Terminology

Canonical terms. These are settled, not stylistic preferences.

- **Session**, not appointment.
- **Check-in**, not assessment.
- **Provider** is the general term and the common case. Rula offers both therapy and psychiatry, so "provider" is correct whenever the discipline isn't known or isn't the point.
- **Therapist** and **Psychiatrist** are the two provider types. Use the specific word only when the copy is genuinely specific to one.
- Therapy care types: **Individual**, **Couples**, **Family**, and **Minor**.
- **"Rula patients" or "you"** in patient-facing copy; **"clients"** in provider-facing copy. Never mix the two within copy aimed at a single audience.
- Capitalize **branded** feature names: Thread, and the formal mobile app title. Don't capitalize unbranded feature names: session summaries, patient portal, resource library.

Reaching for "therapist" out of habit is the common error, and it silently excludes psychiatric care. When in doubt, write "provider."

"Clinician" is not a general substitute for "provider." It currently appears in the AI boundary line, where it draws the line between a tool and a person qualified to provide care. Keep it to that use.

"Assessment" also carries a clinical register that sits badly next to the never-diagnostic guardrail: it implies a measuring instrument and a result. "Check-in" is both the canonical term and the safer one.

## Vocabulary, inclusion, and accessibility

**Avoid AI and engineering vocabulary** on any surface: prompt, model, generate, process, query, context window, algorithm, training. Describe what happens to the person instead.

**Avoid overly therapeutic language.** Rula is adjacent to therapy, not performing it. Clinical and therapy-register phrasing ("hold space," "sit with that," "unpack," "lean into") reads as the product doing therapy. Use plain words.

**Avoid corporate filler**: leverage, seamless, robust, empower, unlock, journey as a buzzword, "we're excited to."

**Inclusion.** Use they/them as the default singular pronoun. Avoid gender-binary phrasing. Avoid assumptions about family structure, living situation, employment, or ability in example copy and placeholder text.

**Plain language.** Avoid idioms and regional slang, which fail for non-native speakers and translate badly. Prefer the shorter, more common word.

**Accessibility.** Write descriptive alt text ("Chart showing mood ratings over the past four weeks," not "chart"). Never write directional UI copy that depends on sight or layout ("tap the blue button on the right"); name the control instead. Keep link and button text meaningful out of context.

## Writing mode

1. State the moment in one line: who the person is, what they're doing, what they need from this screen.
2. Find the row in the tone matrix that matches. Note the dial setting before drafting.
3. Name the single job of the screen: orient, observe, ask, confirm, or advance. One job.
4. Identify what real context is available. If there's strong context, anchor to it. If there isn't, write shorter rather than warmer.
5. Draft, then cut about a third.
6. Run the checks in order: clinical guardrails, non-negotiables, the five character attributes, the tension framework, tone setting, mechanics.
7. Deliver options only when the call is genuinely close, with a recommendation and the reason. Don't manufacture alternatives.

Deliver copy as a labeled string set ready for engineering or Figma: component or key, then the string. Flag any string likely to overflow a constrained component, and flag any string that needs clinical or legal review before it ships.

## Critique mode

Structure: **verdict**, then **findings by severity**, then a **full rewrite**.

Severity:

- **Blocking.** Breaks a clinical guardrail or a non-negotiable, implies companionship, therapy, or crisis support, removes human agency on a consequential decision, or claims confidence the system doesn't have.
- **Significant.** Loses a character attribute, lands on the "Rula does not" side of the tension framework, or uses the wrong tone setting for the moment. Generic empathy where context was available, charisma over clarity, personified voice, emotional overperformance, reaction instead of reflection, calm without direction, engagement over outcome, or exposed mechanism.
- **Minor.** Mechanics, vocabulary, and polish.

Name which layer broke. "This is the right voice at the wrong tone setting: it's reflective and warm on an error screen where the person is blocked and needs the next action" is more useful than a generic note, and it points at a different fix than a voice failure would.

Every finding needs the reasoning, not just the label. Tie it to the principle and explain what the copy does to the person reading it. "This validates the feeling but never connects it to the boundary work she's been doing in session, so it reads like any chatbot and spends none of the context advantage" is useful. "Too generic" is not.

Say what's working, specifically. If the copy is sound, say so rather than inventing problems to justify the review. When a problem can't be fixed in copy because the flow is wrong, say that and describe the design change.

Close by naming anything that needs clinical or legal review, even when the copy itself is sound. A clean critique that misses a required review is not a clean critique.

## Examples

Preferred and rejected pairs from Rula's brand direction work. Preferred reflects the non-personified continuity direction; avoid reflects the personified character direction that was rejected.

**These are quoted as written and predate the terminology ruling.** Several say "therapist" where "provider" is now correct, and one says "appointment" where it should say "session." They illustrate voice, not terminology. Apply Terminology to new copy and don't copy the nouns out of these examples. The onboarding pair also quotes the longer boundary line, which is more disclosure than the non-negotiable now requires; "[Feature] is AI, not a clinician" is the bar.

**Patient feeling overwhelmed**
Preferred: "You've mentioned pressure building for several days now. What feels most difficult to untangle first?"
Avoid: "It feels like this pressure has been building for a while now. Let's slow it down for a second… what feels heaviest right now?"
The first anchors to observed history and asks one focused question. The second narrates the product's own perception and stages an emotional moment.

**Recurring emotional pattern**
Preferred: "This pattern has come up a few times recently, especially around work and sleep."
Avoid: "I'm noticing this same cycle showing up again. It starts with stress, then lack of sleep, then feeling emotionally shut down."
Same observation, but the second centers the product as a noticing subject and over-explains the pattern back to the patient.

**Referencing therapy context**
Preferred: "In your last appointment, you mentioned wanting to notice overwhelm earlier, before it turns into burnout."
Avoid: "You and your therapist have been working on catching these moments earlier, which is so important. This feels connected to that."
The second editorializes with "which is so important" and asserts the connection instead of offering it.

**Encouraging reflection**
Preferred: "What part of this feels most important to pay attention to?"
Avoid: "Hmm. What do you think your mind keeps trying to tell you here?"
"Hmm" is simulated thinking, and the second also interprets on the patient's behalf.

**Validation**
Preferred: "That sounds connected to the pressure you've been describing recently."
Avoid: "That sounds exhausting to carry by yourself for this long."
The rejected line is warmer and emptier: sympathy with no context in it. Validation should do work.

**Encouraging action**
Preferred: "What feels like the smallest manageable next step?"
Avoid: "What would make this feel even 10% lighter tonight?"
The second is a technique with personality attached. The first is gentle momentum, plainly.

**Session preparation**
Preferred: "This may be worth bringing into your next session."
Avoid: "I think this could be really meaningful to explore more deeply in therapy."
"I think" gives the product an opinion. The preferred version keeps therapy central and the product out of the way.

**Introducing the AI tool in onboarding**
Preferred: "A space to think it through / Our conversational AI tool gives you somewhere to reflect in the moment. It's AI, not a clinician, and it doesn't replace your therapist."
Avoid: "Meet your new support companion / Always here when you need someone to talk to."
The rejected line breaks three non-negotiables at once: companion framing, support framing, and no boundary line.

**Billing error**
Preferred: "We couldn't process your payment. Update your billing information to keep your sessions scheduled."
Avoid: "Something went wrong on our end and we're really sorry about that. We know this is frustrating."
Right voice, wrong tone setting. The second spends the whole string on feeling and never gives the blocked person their next action.

## Sources

- **Rula Brand Guidelines 2026, Chapter 03 "Voice and character"** (Figma, node `13974:3476`): the Clear-Eyed Catalyst, the persona blend, the five character attributes, and the voice tension framework. This is the canonical source for voice and outranks the documents below wherever they disagree. The chapter also documents the Rula Brand Voice Gem, scoped to non-product writing.
- `Voice and Tone/Positioning and Principles.docx` (Robert Pickard, last updated 2026-05-21): positioning, brand principles, identity guidance, the preferred/avoid example pairs.
- `Voice and Tone/Onboarding narratives — four options.md`: the non-negotiables and the onboarding tone examples.
- Taylor Wilson's rulings in session, 2026-10-01 and 2026-10-05: canonical terminology, the approved crisis resources, the AI boundary line, and the Mechanics style rules.
- **CxD Spec — ITMS Agent** ([Google Doc](https://docs.google.com/document/d/1iFSj0USXYs7A3P0oB8ElcZ56N9tFACYXQukfnv1zJE0/edit)): the conversational design spec for the Intersession Support Agent. Defines response behavior: seven conversational design principles, the three core use cases (help me cope, help me understand, help me take action), guardrails and boundaries, the per-turn order of operations, and the global orchestration prompt. The best current source for how the agent decides what to say. It is not the agent runbook; that lives in **Braintrust**. This skill governs the voice those responses are written in, the spec governs the behavior, and Braintrust holds the runbook. Don't use this skill to answer a response-behavior question. Where they overlap they agree: reflective before directive, concise, context used selectively for continuity, bounded support, admin requests deep-linked rather than dead-ended, and no overdependence on the agent.
- **Intersession Support Messaging Guide** (Rebecca Seawell, updated 2026-07-28). Filed under `App onboarding and account creation/App onboarding and account management/`, not the Voice and Tone folder. The source of truth for how Rula describes Thread, session topics, session summaries, and the resource library, including approved FAQs, boilerplate, crisis wording, and per-feature do's and don'ts. It is out of date on one point: it lists the longer AI disclosure, which the approved short form has since superseded. Treat the rest as current.
- Clinical guardrails, the tone matrix, the vocabulary and accessibility section, and the attenuation call in Brand voice in product are additions, not sourced from the above. Flag them as such when they drive a decision. The Brave attenuation in particular is a product judgment that Brand has not ratified.

## Open questions

None outstanding. When one comes up, raise it rather than guessing silently, and record it here.

Settled in October 2026: canonical terminology including check-in and the patient/client split; the approved crisis resources; the AI boundary line, short form, approved and shipped; the Mechanics style rules, all now confirmed; the Brave attenuation; alliance versus companionship; and how much of the messaging guide this skill carries.

Two things stay in the messaging guide by decision rather than oversight: Thread's eligibility limits and the feature overview of what it does and doesn't do, because both change per release and would go stale here; and the four named Legal and Compliance review triggers, since the review rule in Clinical guardrails already covers the behavior. Read the guide for those.
