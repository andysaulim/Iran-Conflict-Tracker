---
name: design-authority
description: >
  Precedence router for any frontend, HTML, design, or document build. Fires
  whenever output is a visual deliverable (HTML brief, dashboard, timeline,
  tracker, carousel, slide, Word memo, personal/WORKSHOP project) OR whenever a
  third-party design/engineering skill (taste-skill / design-taste-frontend,
  mattpocock skills, etc.) would otherwise drive styling or workflow. Establishes
  Andy's v3.3 register system as authority and demotes imported skills to
  fallback nudges only.
---

# Design Authority — Precedence Router

My v3.3 working preferences are the authority. Imported third-party skills are
reference material, never the driver. When an imported skill and my preferences
disagree, my preferences win — silently, no negotiation.

## Precedence ladder (top wins)

1. Project-specific instruction I give in the conversation.
2. My v3.3 register system (Publications / Dashboards / Editorial Social /
   WORKSHOP) and all rules in my userPreferences.
3. Imported third-party skills (`design-taste-frontend`, mattpocock skills,
   any other installed SKILL.md) — fallback nudges only, and only where
   rungs 1–2 are silent.

If you ever find yourself applying an imported skill's default over one of my
rules, stop. That's a regression. Flag it instead of shipping it.

## Hard overrides — these beat ANY imported skill, always

- **No gold.** Retired everywhere except the two documented FY2025 Annual
  Report legacy elements. Any new gold is a regression.
- **No shadow / blur / backdrop-filter for elevation.** Use surface tone shift
  + hairline rule. The only exception is the WORKSHOP hard offset-shadow on
  interactive hover. If an imported skill says "tint your shadows," ignore it.
- **No Tailwind defaults as a look:** no `rounded-2xl` everywhere, no
  `shadow-lg`, no `hover:scale-105`, no pill buttons as default.
- **Fonts are fixed per register — do not substitute.** Publications: Libre
  Baskerville + Source Sans 3 + IBM Plex Mono. Dashboards: Libre Baskerville +
  IBM Plex Sans + IBM Plex Mono. Editorial Social: Playfair Display + Source
  Sans 3 + IBM Plex Mono. WORKSHOP: Bricolage Grotesque + Instrument Serif
  italic + JetBrains Mono. Never swap in Geist, Satoshi, Cabinet Grotesk,
  Inter, or any imported-skill default.
- **CSIS work is not a React/Tailwind/Motion project by default.** Default
  stack is vanilla HTML/CSS, Chart.js for figures, Leaflet for maps. Do not
  pull in Motion/Framer, GSAP, Next.js, or a component-library design system
  (Fluent/Material/Atlaskit) unless I explicitly ask.
- **Register is chosen by venue, then tokens follow** — per my Register
  Selection rules. The default for personal/non-CSIS work is WORKSHOP, never
  Publications.

## Adopted practices (distilled from the source repos — now native, no install required)

These are the genuinely useful bits, rewritten in my system. Because they live
here, I get the value without installing the foreign skills or fighting their
defaults.

From taste-skill:
- **Design Read before building.** Before generating any visual deliverable,
  state one line: "Reading this as: <register> for <audience>, <intent>." For
  CSIS work the register makes this deterministic; for WORKSHOP it forces a
  deliberate choice instead of a default aesthetic.
- **Corner-radius lock.** Pick ONE radius scale per composition and hold it
  everywhere — all-sharp, or all-softened at a single value. Mixed radii
  (round buttons in a square layout, etc.) is broken. My default leans sharp /
  slightly-softened; never pill as a default.
- **Same-family headline emphasis.** To emphasize a word inside a headline, use
  italic or bold of the SAME font, not a random serif dropped into a sans
  headline. Documented exception: the WORKSHOP Instrument Serif flourish is an
  intentional, one-per-composition signature move — that's a deliberate
  family mix, not an accidental one.

From mattpocock:
- **Grill ambiguous briefs first.** When a request is underspecified or
  high-stakes, interrogate it before generating — surface the decisions, get
  alignment, then build. Don't jump to output on a fuzzy brief.
- **Handoff on long sessions.** Before passing pipeline or multi-step Claude
  Code work to another agent (or a future session), compact what's done, what's
  pending, and the key decisions into a short handoff note so context isn't lost.
- **Optional per-repo CONTEXT.md.** For a repo with its own jargon (Korea
  Digest, the timeline, a pipeline), a small shared-vocabulary doc keeps naming
  consistent and cuts wasted tokens re-explaining terms each session. Worth it
  only where the vocabulary is real and recurring.

From pretext:
- Capability to remember, not a rule: text height/overflow can be measured
  without the DOM via `@chenglou/pretext`. Reach for it only in a project that
  renders text to canvas/SVG/WebGL or needs dev-time "does this label wrap?"
  checks. Not part of the default stack.

Already covered by my system, so NOT re-adopted: the anti-default checklist
(no AI-purple, no centered-hero-over-mesh, no three equal feature cards,
no Inter+slate-900) — mine already says this. The dials (VARIANCE / MOTION /
DENSITY) and the "use the official design-system package" rule don't fit my
vanilla-HTML, register-driven workflow.

## Where imported design skills (taste-skill) MAY contribute

Only on personal / WORKSHOP greenfield work where I have no existing register
rule for the specific decision. Even then, borrow only the *discipline*, not
the tokens:

- The "Design Read" one-liner before building (state what I'm reading the brief
  as) — useful.
- The anti-default checklist (no AI-purple, no centered-hero-over-mesh, no three
  equal feature cards, no Inter+slate-900) — already mine; reinforces it.
- The single corner-radius lock (pick one scale, hold it) — useful.

Never borrow from taste-skill: its font defaults, its Motion-library mandate,
its shadow-tinting, its bento-card defaults, its dashboard scope-out (my
dashboards are first-class, not excluded).

For any CSIS-attributed deliverable (Publications / Dashboards / Editorial
Social), taste-skill does not apply at all. My registers already make the
design read deterministic.

## Where imported engineering skills (mattpocock) MAY contribute

Keep and use:

- `grill-me` — run before any ambiguous build to force alignment first.
- `handoff` — compact a long Claude Code session before passing pipeline work
  to the next agent.
- `git-guardrails-claude-code` — keep installed on my repos; it blocks
  destructive git, which matches my backup-before-risky-ops rule.
- `zoom-out` — fine, harmless.

Skip unless I'm explicitly running a real software project: `to-prd`,
`to-issues`, `triage`, `tdd`, `improve-codebase-architecture`,
`setup-matt-pocock-skills`. I work in plain English and don't run an issue
tracker for HTML briefs.

`caveman` (token compression) is off by default — I prefer plain English.

## pretext (library, not a skill)

Not in the default stack. Reach for `@chenglou/pretext` only inside a specific
project that renders text to canvas/SVG/WebGL or needs DOM-free measurement
(virtualization, shrink-wrap, dev-time overflow checks). Normal CSS-flow HTML
does not need it. Install per-project, never globally.

## Self-check before shipping any visual build

- Did I pick the register by venue first? Is personal work in WORKSHOP, not
  Publications?
- Any gold? Any shadow-for-elevation? Any substituted font? → fix before ship.
- Did an imported skill's default sneak in over one of my rules? → revert,
  flag it.
