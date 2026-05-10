# Pass 3 — Visual Harmonisation

A family-wide design pass that brings the eight live Vinotheca leaves into
visual coherence: shared palette tokens, shared paper colour, shared raised-
panel treatment, and consistent token naming across static and React leaves.

This document is the canonical Pass 3 specification. Future execution sessions
work from it; PROJECT.md §6.3 links to it as the authoritative reference.

**Status**: ✅ **Pass 3 complete** as of 2026-05-10. Nine of nine
palette-bearing surfaces aligned. All six Phase 2 + Phase 3 decisions
resolved; all four deferred Questions answered. The Library family
is visually coherent.
**Origin**: PROJECT.md §6.3, unblocked by Body of Wine deploy (2026-05-09).
**Spec date**: 2026-05-09 (Phase 2). Updated 2026-05-09 with Tier 1+2
execution learnings; Decisions 5 and 6 from the hard-questions session;
Estate Atlas font follow-up; PDF naming convention; Wine Atlas Tier 3.
Updated 2026-05-10 with Tasterank Explorer Tier 3 (the final piece)
plus the Wine Atlas circular-reference fix and a lesson recorded for
future sed-substitution discipline.

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

Estate Atlas's font choice initially appeared to be an accidental rename
— "Cormorant" and "Cormorant Garamond" are two distinct Google Fonts.
However, the harvest performed during Tier 2 execution revealed 17
deliberate uses of "Cormorant" and zero of "Cormorant Garamond" in the
file, indicating a deliberate choice. The question of which display
font Estate Atlas should use is therefore promoted to Question D in
the deferred-decisions list (see end of spec).

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

### Decision 5 — Body fonts are artefact-class-distinguished

Different artefact classes get different body fonts to signal what
register of engagement the reader is encountering:

| Class | Body font | Members |
|---|---|---|
| Reading work (Library, atlases, reference) | EB Garamond | Vinotheca (parent), Estate Atlas, Wine Atlas (after migration), Region Affinities, Region Resonances |
| Study (research-paper register) | Source Sans 3 | Body of Wine, Soul of Wine |
| Tool (interactive instrument) | DM Sans | Tasterank Explorer |
| Personal Codex (Part II) | DM Sans | Codex Vini |

The pattern: when a reader walks from the parent (book serif) to a
Study (research sans) to Tasterank Explorer (interactive sans), the
visual shift signals *you're now in a different mode of engagement* —
even when the content domain is shared. Region Affinities and Region
Resonances are interactive but reference-style: you browse them like
atlases, so they sit on the Library side. Tasterank Explorer is the
only genuinely instrumental tool in the family — its force-directed
network visualization is its core experience — and DM Sans signals
that.

Codex Vini's DM Sans body is preserved as the typographic signature
of Part II, structurally distinct from Library / Study / Tool per §1.

**Concrete migration required**: Wine Atlas (currently DM Sans body)
→ EB Garamond. Part of Tier 3 work.

### Decision 6 — Display fonts unify the family

Cormorant Garamond is the canonical display font across the entire
family, including atlases and the Codex. Display fonts encode *family
identity*; body fonts encode *register*. Together they form a clean
two-axis system:

- **Display** (Cormorant Garamond, family-wide): you are inside Vinotheca
- **Body** (varies by class per Decision 5): this artefact's mode of engagement

Without a shared display font the family would visually fragment.
The shared display is the through-line that ties parent to atlases
to studies to Codex to tools.

**Concrete migrations required**:
- Estate Atlas's "Cormorant" → "Cormorant Garamond" (17 references plus
  the Google Fonts `<link>` tag). Estate Atlas's deliberate choice of
  the more austere "Cormorant" cut predates the family pattern; with
  Stance X locked in, alignment is the right call.
- Wine Atlas's DM Serif Display → Cormorant Garamond. Part of Tier 3.
- Tasterank Explorer's DM Serif Display → Cormorant Garamond. Part of
  Tier 3. Note: only the *display* font migrates; Tasterank Explorer's
  DM Sans body is preserved per Decision 5 as instrument-class signal.

---

## Execution change list

Mechanical edit list per leaf. Each row is one execution session's
worth of careful editing.

| # | Leaf | Tier | File(s) | Edit |
|---|---|---|---|---|
| 1 | Body of Wine | 1 | `body-of-wine/index.html` | ✅ Shipped (`f8e23b0`). `:root`: rename `--cream: #FAF6F1` → `--paper: #FAF6F1`. Add `--paper-raised: #FFFDF8`. Global find-replace: `var(--cream)` → `var(--paper)`. Replace `#fff` raised-panel uses with `var(--paper-raised)`. |
| 2 | Soul of Wine | 1 | `soul of wine/soul-of-wine/index.html` | ✅ Shipped (`c578109`). Identical to #1; the two Studies stay byte-identical. |
| 3 | Codex Vini | 1 | `codex vini/index.html` | ✅ Shipped (`cbcd2d8`). `:root`: change `--paper: #FAF6EF` → `#FAF6F1`. (No change to `--bordeaux` or `--paper-raised` — both already correct.) |
| 4 | Vinotheca | 2 | `vinotheca/index.html` | ✅ Shipped (Tier 2). `:root`: rename and revalue `--accent`/`--accent-soft` per Decision 4. Add `--wine-dark: #5A1F1A`. Change `--paper: #f6f1e8` → `#FAF6F1`. Add `--paper-raised: #FFFDF8`. Global find-replace: `var(--accent)` → `var(--wine)` (25 uses), `var(--accent-soft)` → `var(--wine-light)` (4 uses). |
| 5 | Estate Atlas | 2 | `estate-atlas/index.html` | ✅ Shipped (Tier 2). `:root`: change `--wine: #6e1f2a` → `#7B2D26`. Change `--paper: #f5efe6` → `#FAF6F1`. Add `--wine-dark: #5A1F1A`, `--paper-raised: #FFFDF8`. **Correction from original spec**: Estate Atlas had `--wine-soft: #8a3a44` (not noted in original spec), renamed to `--wine-light: #A04038` with same-step value change; `var(--wine-soft)` → `var(--wine-light)` global find-replace (3 uses). Also updated `--pin-shadow: rgba(110, 31, 42, 0.35)` → `rgba(123, 45, 38, 0.35)` to track the new wine value. **Display font deferred**: 17 deliberate uses of "Cormorant" preserved for Question D (see deferred decisions). |
| 6 | Region Affinities | (React) | `region-affinities/tailwind.config.js` | ✅ Shipped 2026-05-09. `parchment.DEFAULT: '#FAF7F2'` → `'#FAF6F1'`. Added `parchment.raised: '#FFFDF8'`. Wine palette unchanged (already canonical). Build pipeline: GitHub Actions Vite build, ~1–3 min deploy. |
| 7 | Region Resonances | (React) | `region-resonances/app/tailwind.config.js` | ✅ Shipped 2026-05-09. Identical changes to #6; the two Region tools stay byte-identical per the existing in-file comment that the file tracks region-affinities. |
| 8 | Wine Atlas | 3 | `wine atlas/grand-cru-atlas/index.html` | ✅ Shipped (`2617c76`). Tier 3 — full token system introduced from scratch; canonical 10-token `:root`. Hard-coded values replaced with `var()` references; `#FAF8F5` paper drift revalued to canonical `#FAF6F1`. Typography migration per Decisions 5 and 6: DM Serif Display → Cormorant Garamond (3 uses), DM Sans → EB Garamond (7 uses). Google Fonts `<link>` tag updated. Grape category colours and local one-off decorative colours preserved unchanged. The largest single visual change of Pass 3. |
| 9 | Tasterank Explorer | 3 | `tasterank-explorer/index.html` | ✅ Shipped (`8c4f0ce`). Tier 3 — token system introduced from scratch with canonical 10-token `:root`; 15 wine + 9 paper + 8 border + 6 raised-panel `#fff` references replaced with `var()`; 3 high-contrast `#fff` preserved (button hover text, SVG node stroke, JS fallback). Display font DM Serif Display → Cormorant Garamond (7 uses) per Decision 6. **DM Sans body preserved** (12 uses) per Decision 5 — Tasterank Explorer is the family's only instrument-class Tool, and the Cormorant Garamond + DM Sans combination is its register signal: visibly within the family, register distinct. Google Fonts `<link>` tag updated. |
| 10 | Estate Atlas (font follow-up) | 2 | `estate-atlas/index.html` | ✅ Shipped 2026-05-09 (`d855598`). Per Decision 6 (Question D resolved): "Cormorant" → "Cormorant Garamond" across 16 font-family references in CSS plus the Google Fonts `<link>` tag URL parameter. |

**Tier 1+2 execution = 5 leaves, ~75–90 minutes total spread across two
sessions.** **React execution = 2 leaves, ~30 minutes.** **Tier 3 = 2 leaves,
likely 2 dedicated sessions.**

---

## Recommended session sequence

1. ✅ **Tier 1 execution** — Body of Wine, Soul of Wine, Codex Vini.
   Shipped 2026-05-09 (`f8e23b0`, `c578109`, `cbcd2d8`).
2. ✅ **Tier 2 execution** — Vinotheca, Estate Atlas. Shipped 2026-05-09.
3. ✅ **React execution** — Region Affinities, Region Resonances.
   Shipped 2026-05-09.
4. ✅ **Hard-questions session** — Decisions 5 and 6 resolved 2026-05-09.
   No code changes from the session itself; Decisions 5 and 6 ripple
   into the remaining execution work below.
5. ✅ **Estate Atlas font follow-up** — shipped 2026-05-09 (`d855598`):
   "Cormorant" → "Cormorant Garamond" across 17 font-family references
   plus the Google Fonts `<link>` tag.
6. ✅ **PDF naming convention** — shipped 2026-05-09. Tasterank
   Explorer's five PDFs renamed to `lowercase-with-hyphens.pdf` form,
   matching Soul of Wine's existing convention. Coordinated commits
   across `tasterank-explorer` and `body-of-wine` (cross-repo links
   updated). Tasterank Explorer's README also gained the previously-
   missing Methods Primer entry in its Files table.
7. ✅ **Tier 3 execution (Wine Atlas)** — shipped 2026-05-09 (`2617c76`).
   Full token system introduced from scratch; typography migrated to
   family canonical per Decisions 5 and 6.
8. ✅ **Tier 3 execution (Tasterank Explorer)** — shipped 2026-05-10
   (`8c4f0ce`). Token system introduced from scratch; display font
   migrated DM Serif Display → Cormorant Garamond; DM Sans body
   preserved per Decision 5. Plus immediate follow-up: LICENSE
   attribution corrected to "Grape Affinities" to match display name.

After step 8, **Pass 3 is complete and §6.3 closes**.

### Bug found and fixed during this sequence

Yesterday's Wine Atlas Tier 3 commit (`2617c76`) shipped with two
circular references in `:root`: `--wine: var(--wine);` and `--border:
var(--border);`. Caused by an over-eager sed substitution that
caught the values inside the `:root` declaration as well as their
references in the body of the file. The bug silently broke wine-red
and border rendering — every `var(--wine)` reference fell through to
inherited values; every `var(--border)` to currentColor. Caught the
next morning during Tasterank Explorer prep when the same sed pattern
produced the same bug in working memory; visual inspection of the
`:root` block caught both. Wine Atlas fix shipped as commit `64e839e`.
Lesson: post-edit visual verification of the `:root` block via
`awk '/:root/,/}/'` is mandatory after any sed substitution that
might touch token-definition values; counting hex occurrences is not
sufficient — counts of zero look like success when they actually mean
the tokens themselves got substituted into self-references.

---

## Deferred questions — resolved 2026-05-09

The four deferred hard questions were resolved in a dedicated session
after Tier 1, Tier 2, and React execution had shipped. Each question's
resolution is captured below for the historical record.

### Question A — Body font canonical

**Resolved**: Decision 5. Body fonts are artefact-class-distinguished.
- Reading work (Library, atlases, reference): EB Garamond
- Study: Source Sans 3
- Tool (interactive instrument): DM Sans
- Personal Codex (Part II): DM Sans

Three sub-questions resolved within Decision 5:
- A.1 Region pair: keeps EB Garamond (atlas-style tools)
- A.2 Wine Atlas: migrates DM Sans → EB Garamond
- A.3 Tasterank Explorer: keeps DM Sans (instrument register)

### Question B — Atlas distinctness policy

**Resolved**: Decision 6. Stance X — display fonts unify the family,
body fonts distinguish classes. Atlases share Cormorant Garamond display
with the rest of the Library. Wine Atlas's DM Serif Display migrates
to Cormorant Garamond. Atlas-class signal is encoded in body font
(EB Garamond, Reading-work register) rather than display font.

### Question C — Codex Vini differentiation depth

**Resolved**: Stance X (Decision 6) preserves Codex's existing
distinctness — `--bordeaux`, slightly cooler paper, `--rule-soft`,
`--gold`, DM Sans body — as deliberate Codex signature. The display
font (already Cormorant Garamond) keeps Codex within the family's
visual through-line. Codex emerges as *visually distinct from but
visibly within* the family, which is what Part II of the architecture
should be.

No code changes needed for Codex; its current state already implements
Stance X correctly. Codex's font choices weren't drift — they were
correct, just unexamined until now.

### Question D — Estate Atlas display font

**Resolved**: Decision 6 (Stance X). Estate Atlas's "Cormorant"
migrates to "Cormorant Garamond". The "Cormorant" choice was deliberate
but predates the family pattern; with Stance X locked in, alignment is
the right call.

---

## Open ambiguities (smaller)

A few smaller things noticed during the harvest that aren't full
"questions" but should be resolved during execution:

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
