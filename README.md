# UX Voice and Tone

A Claude Code skill that writes and critiques Rula product copy. It carries Rula's voice
and tone system in one place: Brand's voice definition and character attributes, the tone
settings for different patient situations, the non-negotiable constraints, clinical
guardrails, canonical terminology, and the mechanics that apply to every string.

It replaces the earlier `ux-copy` skill.

## Install

This is a Claude Code skill. It works in the **Code tab of the Claude desktop app** and in
the `claude` CLI, which read skills from the same folder, so one install covers both.

`SKILL.md` needs to end up here:

| | |
| :--- | :--- |
| macOS and Linux | `~/.claude/skills/ux-voice-and-tone/SKILL.md` |
| Windows | `%USERPROFILE%\.claude\skills\ux-voice-and-tone\SKILL.md` |

### Claude Desktop, without using a terminal

1. On GitHub, choose **Code** then **Download ZIP**, and unzip it.

2. Open the skills folder. The `.claude` folder is hidden, so you can't browse to it
   normally:
   - **macOS:** in Finder press **Cmd+Shift+G**, paste `~/.claude/skills`, press Return.
   - **Windows:** paste `%USERPROFILE%\.claude\skills` into the File Explorer address bar.

   If there's no `skills` folder, create one with exactly that name.

3. Drag the unzipped folder in, then check its name. GitHub ZIPs usually unpack with a
   suffix like `ux-voice-and-tone-main`, so **rename it to `ux-voice-and-tone`**. This is
   the most common reason an install silently does nothing.

4. Start a new session in the Code tab. Skills are read when a session starts, so a session
   that is already open won't see it. If it still doesn't appear, quit the app fully and
   reopen.

5. Type `/ux-voice-and-tone`. If it's listed, it loaded.

### With git

```bash
git clone <repo-url> ~/.claude/skills/ux-voice-and-tone
```

Then start a new session.

### If it doesn't show up

- **Folder name must match the frontmatter.** The directory has to be `ux-voice-and-tone`,
  matching the `name:` field at the top of `SKILL.md`. Renaming one without the other
  breaks it.
- **`SKILL.md` must sit directly inside that folder**, not in a subfolder. The path has to
  be `…/skills/ux-voice-and-tone/SKILL.md` exactly.
- **Start a fresh session.** Nothing reloads mid-session.

Note this covers the Code tab specifically. Installing skills for the desktop app's regular
chat is a separate mechanism and isn't what this folder layout is for.

## Use

Two modes, and it picks on its own in most cases:

- **Write** is the default. Ask for copy and you get a labeled string set ready for
  engineering or Figma, with anything needing clinical or legal review flagged.
- **Critique** triggers when you paste strings, share a screen, or ask "is this good" or
  "which is better." You get a verdict, findings by severity, then a full rewrite.

It also answers questions about how Rula should sound, settles disagreements between
drafts, and checks whether an existing surface is on-voice.

Tell it the platform and the audience if they are not obvious. It will ask when a string is
length-sensitive and the platform is unstated.

## What's in it

| Section | What it settles |
| :--- | :--- |
| Scope | Content strategy, product copy, cross-platform, audiences |
| Voice is constant, tone is variable | The diagnostic for whether a failure is voice or tone |
| The Clear-Eyed Catalyst | Brand's voice definition and the persona blend |
| Non-negotiables | Constraints that hold at every tone setting |
| Referring to AI features | How to name and describe AI features |
| Our character | Brand's five attributes, verbatim |
| Voice tension framework | Brand's eight do / don't pairs |
| Brand voice in product | How brand voice attenuates in product, and the order of authority |
| Context is the empathy mechanism | The most important rule in the skill |
| Tone matrix | Nine scenarios mapped to tone settings |
| Alliance | Why alliance is not companionship |
| Clinical guardrails | Hard limits, including crisis routing |
| Terminology | Session, check-in, provider, patient/client, capitalization |
| Mechanics | Punctuation, grammar, and per-component rules |
| Writing mode / Critique mode | The two workflows |
| Examples | Preferred and rejected pairs from brand direction work |
| Sources | Provenance, including which parts are not sourced |
| Open questions | Decision log. Currently nothing outstanding |

## Sources it depends on

The skill's authority comes from Rula documents. Full use assumes access to these:

- **Rula Brand Guidelines 2026, Chapter 03 "Voice and character"** (Figma) is canonical for
  voice and outranks everything below.
- **Intersession Support Messaging Guide** (local) governs how Rula describes Thread and the
  other intersession features, and holds the approved crisis and privacy strings.
- **CxD Spec — ITMS Agent** (Google Doc) governs agent response behavior.
- **Positioning and Principles** (local) is the product-specific principle layer.

Note the division of labor: **this skill governs voice. It does not define how the agent
responds.** Behavior lives in the CxD Spec, and the agent runbook lives in Braintrust.

Without access to those, most of the skill still works. What breaks is anything that needs
an exact approved string, which the skill deliberately points at rather than reproduces.

## Maintaining it

`SKILL.md` is the source of truth. `SKILL.html` is a generated companion for reading and
review, built by the `md-companion-html` skill.

**Do not hand-edit `SKILL.html`.** Regenerate it from `SKILL.md` instead, or it will
silently drift. After regenerating, check that heading count and order match between the
two files and that no anchors are broken.

The `Open questions` section doubles as a decision log. When something gets settled, record
it there rather than letting the reasoning disappear into chat history. Several decisions in
this skill were re-litigated once because the reasoning was not written down.

## Known gaps

Honest list, as of 2026-10-05:

- **Clinical guardrails have never been validated.** They are flagged in the skill as
  additions appropriate to a behavioral health product that should be checked against
  Rula's clinical and compliance guidance. That check has not happened. Highest-priority
  gap in the document.
- **Three sections of the messaging guide are unabsorbed**: Session Summaries, Resource
  Library, and Mobile App each carry their own do's and don'ts. At least one contradicts
  the skill as written: for session summaries, do *not* describe them as AI-written to
  patients, because the therapist reviews and owns them.
- **The Brave attenuation is a product judgment Brand has not ratified.** It is in force,
  and flagged as unratified.
- **The voice tension framework pairing is inferred**, not stated in the brand guidelines,
  which present the two columns separately.
- **The Examples section uses outdated terminology** ("therapist," "appointment"). The pairs
  are quoted as written and flagged; they illustrate voice, not terminology.
- **The print stylesheet in `SKILL.html` is untested.** Responsive behavior has been
  verified at 360, 561, and 1440px; printing has not.
