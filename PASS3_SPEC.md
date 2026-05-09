# Pass 3 — Visual Harmonisation

A family-wide design pass that brings the eight live Vinotheca leaves into
visual coherence: shared palette tokens, shared paper colour, shared raised-
panel treatment, and consistent token naming across static and React leaves.

This document is the canonical Pass 3 specification. Future execution sessions
work from it; PROJECT.md §6.3 links to it as the authoritative reference.

**Status**: spec written, execution pending.
**Origin**: PROJECT.md §6.3, unblocked by Body of Wine deploy (2026-05-09).
**Spec date**: 2026-05-09.

---

## Why this exists

Per §4.7 of PROJECT.md, the family was built leaf by leaf over time, with
design decisions made in isolation as each leaf was created. This produced
small inconsistencies that are visible only when leaves are walked together:
slightly different wine reds, slightly different paper creams, divergent
token names for the same conceptual values, and a mix of font choices.

Pass 3 was deferred until at least two Studies existed, so the study-class
template could be designed against a real pair rather than a template-of-one.
With Body of Wine deployed alongside Soul of Wine on 2026-05-09, the
precondition is met. The harvest documented in this spec was performed the
same day.

---

## What was harvested

A complete inventory of the nine palette-bearing surfaces in the family
(eight leaves plus the parent Vinotheca):

### Wine red

| Leaf | Value | Token | Status |
|---|---|---|---|
| Body of Wine | `#7B2D26` | `--wine` | canonical |
| Soul of Wine | `#7B2D26` | `--wine` | canonical |
| Wine Atlas (Grand Cru) | `#7B2D26` | hard-coded | canonical |
| Tasterank Explorer | `#7B2D26` | hard-coded | canonical |
| Region Affinities | `#7B2D26` | Tailwind `wine.DEFAULT` | canonical |
| Region Resonances | `#7B2D26` | Tailwind `wine.DEFAULT` | canonical |
| Codex Vini | `#5B1A2D` | `--bordeaux` | intentional differentiation (Personal Codex per §1) |
| Vinotheca (parent) | `#6a2430` | `--accent` | drift |
| Estate Atlas | `#6e1f2a` | `--wine` | drift |

Six leaves already use `#7B2D26`. Two diverge slightly (drift). Codex Vini
diverges meaningfully and intentionally — it sits in Part II of the
architecture, separated from the Library proper.

### Paper cream

| Leaf | Value | Token | Status |
|---|---|---|---|
| Body of Wine | `#FAF6F1` | `--cream` | within tight cluster |
| Soul of Wine | `#FAF6F1` | `--cream` | within tight cluster |
| Region Affinities | `#FAF7F2` | `parchment.DEFAULT` | within tight cluster |
| Region Resonances | `#FAF7F2` | `parchment.DEFAULT` | within tight cluster |
| Codex Vini | `#FAF6EF` | `--paper` | within tight cluster |
| Wine Atlas | `#faf8f5` | hard-coded | within tight cluster |
| Tasterank Explorer | `#faf8f5` | hard-coded | within tight cluster |
| Vinotheca (parent) | `#f6f1e8` | `--paper` | meaningfully warmer (drift) |
| Estate Atlas | `#f5efe6` | `--paper` | meaningfully warmer (drift) |

Seven leaves cluster within ~2 hex units of each other (visually
indistinguishable). Two are meaningfully warmer.

### Raised panel surfaces

Codex Vini uniquely defines a `--paper-raised: #FFFDF8` token, used for
raised cards and elevated panels (warmer than pure white, harmonious with
the cream paper). Other leaves use `#fff` or pure white directly, which
reads as harsh against warm cream backgrounds.

### Body fonts

| Leaf | Body font |
|---|---|
| Vinotheca (parent), Estate Atlas, Region Affinities, Region Resonances | EB Garamond |
| Body of Wine, Soul of Wine | Source Sans 3 |
| Codex Vini, Wine Atlas, Tasterank Explorer | DM Sans |

Three different body-font families across nine leaves. Deciding the
canonical here is one of the *deferred* hard questions (see end of spec) —
not part of this Phase 2 spec.

### Display fonts

| Leaf | Display font |
|---|---|
| Vinotheca, Body of Wine, Soul of Wine, Codex Vini | Cormorant Garamond |
| Estate Atlas | Cormorant *(without "Garamond")* |
| Wine Atlas, Tasterank Explorer | DM Serif Display |

Estate Atlas's font is almost certainly an accidental rename — "Cormorant"
and "Cormorant Garamond" are two distinct Google Fonts. Worth fixing in
execution, regardless of larger font decisions.

---

## Structural tiers

The leaves fall into three tiers based on their token-system maturity:

**Tier 1 — Fully tokenised, modern**
- Body of Wine, Soul of Wine, Codex Vini
- `:root` block with named tokens; clean structure
- Pass 3 work: minor value normalisation and small token renames

**Tier 2 — Tokenised but with non-canonical names**
- Vinotheca (parent), Estate Atlas
- Have `:root`, but tokens diverge from family pattern (`--accent` instead of `--wine`)
- Pass 3 work: token renaming + value normalisation

**Tier 3 — Hard-coded values, no token system**
- Wine Atlas (Grand Cru), Tasterank Explorer
- Hex values scattered throughout the stylesheet, no `:root` declarations
- Pass 3 work: introduce token system, then values fall into place
- Largest scope; deferred to dedicated sessions

The two React leaves (Region Affinities, Region Resonances) are
structurally distinct again — palette lives in `tailwind.config.js`, not
in CSS variables. They are byte-identical to each other by design (per the
deliberate comment in `region-resonances/app/tailwind.config.js`).

---

## Phase 2 decisions (this document)

Three decisions are locked in by this spec. Two further questions are
explicitly deferred.

### Decision 1 — Canonical wine red

**Value**: `#7B2D26`
**Token name (static)**: `--wine`
**Token variants**: `--wine-dark` (`#5A1F1A`), `--wine-light` (`#A04038`)
**Token name (React)**: Tailwind `wine.DEFAULT` (already in place)

**Codex Vini is exempted**: it keeps `--bordeaux: #5B1A2D` as deliberate
visual differentiation per §1 (Codex sits in Part II of the architecture).

### Decision 2 — Canonical paper cream

**Value**: `#FAF6F1`
**Token name (static)**: `--paper`
**Token name (React)**: Tailwind `parchment.DEFAULT` (kept; already
embedded in components like `bg-parchment-warm`)

Both resolve to the same hex value across the family.

The Studies' current token name `--cream` is renamed to `--paper` to align
with the dominant family pattern (Vinotheca, Estate Atlas, Codex Vini all
use `--paper`). The `parchment` family in the React leaves stays — its
naming is too embedded in component classes to rename without substantial
collateral edits.

### Decision 3 — Universal `--paper-raised` token

**Value**: `#FFFDF8`
**Token name (static)**: `--paper-raised`
**Token name (React)**: To be added to Tailwind palette as
`paper.raised` or `parchment.raised` — finalised at React execution time.

Replaces `#fff`, `#ffffff`, and `var(--white)` for raised card and panel
backgrounds throughout the family. Pure white remains available for
true-white needs (high-contrast button text on dark backgrounds, etc.).

### Decision 4 — Vinotheca's `--accent` rename

The parent Vinotheca's token names diverge from the family pattern
(`--accent`, `--accent-soft`). Decision 4 brings them into alignment:

- `--accent` (`#6a2430`) → `--wine` (`#7B2D26`)
- `--accent-soft` (`#8a3240`) → `--wine-light` (`#A04038`)
- New: `--wine-dark: #5A1F1A` (for forward consistency)

Plus a global find-replace within `vinotheca/index.html`:
- `var(--accent)` → `var(--wine)`
- `var(--accent-soft)` → `var(--wine-light)`

---

## Execution change list

Mechanical edit list per leaf. Each row is one execution session's
worth of careful editing.

| # | Leaf | Tier | File(s) | Edit |
|---|---|---|---|---|
| 1 | Body of Wine | 1 | `body-of-wine/index.html` | `:root`: rename `--cream: #FAF6F1` → `--paper: #FAF6F1`. Add `--paper-raised: #FFFDF8`. Global find-replace: `var(--cream)` → `var(--paper)`. Replace `#fff` raised-panel uses with `var(--paper-raised)`. |
| 2 | Soul of Wine | 1 | `soul of wine/soul-of-wine/index.html` | Identical to #1; the two Studies stay byte-identical. |
| 3 | Codex Vini | 1 | `codex vini/index.html` | `:root`: change `--paper: #FAF6EF` → `#FAF6F1`. (No change to `--bordeaux` or `--paper-raised` — both already correct.) |
| 4 | Vinotheca | 2 | `vinotheca/index.html` | `:root`: rename and revalue `--accent`/`--accent-soft` per Decision 4. Add `--wine-dark: #5A1F1A`. Change `--paper: #f6f1e8` → `#FAF6F1`. Add `--paper-raised: #FFFDF8`. Global find-replace: `var(--accent)` → `var(--wine)`, `var(--accent-soft)` → `var(--wine-light)`. |
| 5 | Estate Atlas | 2 | `estate-atlas/index.html` | `:root`: change `--wine: #6e1f2a` → `#7B2D26`. Add `--wine-dark: #5A1F1A`, `--wine-light: #A04038`. Change `--paper: #f5efe6` → `#FAF6F1`. Add `--paper-raised: #FFFDF8`. Fix display-font reference: `Cormorant` → `Cormorant Garamond`. |
| 6 | Region Affinities | (React) | `region-affinities/tailwind.config.js` | `parchment.DEFAULT: '#FAF7F2'` → `'#FAF6F1'`. Add a `paper.raised` (or `parchment.raised`) value of `#FFFDF8`. (Wine palette already canonical.) |
| 7 | Region Resonances | (React) | `region-resonances/app/tailwind.config.js` | Identical to #6; the two Region tools stay byte-identical per the existing in-file comment. |
| 8 | Wine Atlas | 3 | `wine atlas/index.html` | Defer to dedicated Tier 3 session. Introduce `:root` with canonical tokens, replace hard-coded values throughout. |
| 9 | Tasterank Explorer | 3 | `tasterank-explorer/index.html` | Same as #8. Defer to dedicated Tier 3 session. |

**Tier 1+2 execution = 5 leaves, ~75–90 minutes total spread across two
sessions.** **React execution = 2 leaves, ~30 minutes.** **Tier 3 = 2 leaves,
likely 2 dedicated sessions.**

---

## Recommended session sequence

1. **Tier 1 execution** — Body of Wine, Soul of Wine, Codex Vini. Three
   leaves, all already correct in value or close to it. Likely the
   simplest session.
2. **Tier 2 execution** — Vinotheca, Estate Atlas. Token renames plus value
   swaps. More careful work because of global find-replace.
3. **React execution** — Region Affinities, Region Resonances. Tailwind
   config edits plus verification that components still render correctly
   in the live React build pipeline (1–3 min deploy each, then visual
   walk-through).
4. **Hard-questions session** — body font, atlas distinctness, Codex
   differentiation depth. *No code changes; outcome is decisions added
   to this spec as Decisions 5–7.*
5. **Tier 3 execution (Wine Atlas)** — introduce token system, replace
   hard-coded values, verify deployment.
6. **Tier 3 execution (Tasterank Explorer)** — same approach as Wine Atlas.
7. **PDF naming convention** — settle the divergent naming (Soul of Wine
   uses `lowercase-with-hyphens.pdf`; Tasterank Explorer uses
   `TasteRank_Title_Case_With_Underscores.pdf`). Tiny session.

After step 7, Pass 3 is complete and §6.3 closes.

---

## Deferred questions (Phase 3 — hard decisions)

These are explicitly NOT settled by this spec. They will become
Decisions 5–7 once the project is ready to address them.

### Question A — Body font canonical

EB Garamond (5 leaves: Vinotheca, Estate Atlas, Region Affinities, Region
Resonances, plus implicit on the parent's prose) vs. Source Sans 3 (2
leaves: Body of Wine, Soul of Wine) vs. preserve distinction by
artefact-class (atlases use DM, studies use Source Sans 3, library uses
EB Garamond).

The choice has the largest visual consequence of any Pass 3 decision.
Probably best made in a session where leaves are walked side by side and
the experiential difference between font choices is felt rather than
specified.

### Question B — Atlas distinctness policy

Wine Atlas uses DM Serif Display + DM Sans, distinguishing it visually
from the Library family. Two readings:

- *Preserve* — atlases are a different *kind* of artefact (map-class)
  and visual distinction encodes that classification.
- *Align* — Pass 3's purpose is family unity; Wine Atlas should adopt
  the canonical fonts.

Same question applies to Tasterank Explorer (uses the same DM fonts as
Wine Atlas), though Tasterank Explorer is a Tool, not an atlas — so the
question there is whether tools-with-heavy-visualisation should look
different from prose-heavy tools.

### Question C — Codex Vini differentiation depth

Decision 1 already preserves Codex's `--bordeaux` wine value. Decision 2
brings Codex's paper closer to canonical (one hex unit). The remaining
question: how *much* visual distinctness should Part II maintain from
Part I (the Library)? Possible positions:

- Maximal differentiation: keep all current Codex tokens, including
  `--rule-soft`, `--gold`, distinctive font stack
- Minimal differentiation: only `--bordeaux` differs; everything else
  aligns
- Calibrated differentiation: pick which tokens differentiate
  meaningfully vs. which are accidental drift

Worth a deliberate decision rather than a default.

---

## Open ambiguities (smaller)

A few smaller things noticed during the harvest that aren't full
"questions" but should be resolved during execution:

- **Estate Atlas's "Cormorant" font reference** is probably a typo; the
  family pattern is "Cormorant Garamond". Easy fix during Tier 2.
- **Region pair's `parchment.warm` and `parchment.edge` Tailwind
  values** are not yet harvested in this spec — they may need their own
  canonical decisions if other leaves use similar warm/edge variants.
- **Codex Vini's `--rule-soft` and `--gold` tokens** are unique to it;
  decide during Question C whether they propagate or stay Codex-only.
- **The static leaves use `--ink`, `--ink-soft`, `--ink-faint` (plus
  `--ink-light`, `--ink-muted` in Studies); the React leaves use
  `ink.DEFAULT`, `ink.muted`, `ink.subtle`.** Three different naming
  patterns for what should be one set of values. Likely a small
  Decision 8 in the future.

---

*The Vinotheca family is built leaf by leaf, but it is read as a whole.
Pass 3 is the work of making the whole legible.*
