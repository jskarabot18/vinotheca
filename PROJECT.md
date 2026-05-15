# Vinotheca — Project State

> **Canonical source of truth for the Vinotheca family of sites.**
> When working on any site in the family — adding a leaf, changing a design
> rule, planning a redesign — read this file first. If anything proposed
> contradicts this file, this file wins until the file is updated.
>
> **Maintenance rule.** When a decision is made, a leaf is added or removed,
> or a design rule changes — update this file in the same commit, or the
> next commit. Append an entry to §8 (Document changelog) so the change
> is recorded.

Last meaningful update: 2026-05-14 (see §8 for full history)

---

## 1. Architecture

Vinotheca is a library of wine works. The parent page (`vinotheca/index.html`)
is the catalogue and the home; each "leaf" is a separate site that lives at
its own GitHub Pages URL.

The architecture is organised by **operational purpose** — what the visitor
is *doing* when they arrive at a section — rather than by what the artefact
technically is. Five sections, each a distinct mode of engagement:

| Section | Operational verb | What the visitor is doing |
|---------|------------------|---------------------------|
| **Maps** | Locate | Finding where wine is in the world |
| **Works** | Understand | Navigating the structure of wine and reading its argument |
| **Correspondence** | Converse | Speaking to a tool, receiving a response |
| **Reference** | Ground | Reaching the conceptual foundations beneath the wine work |
| **Personal Codex** | Record | Keeping a personal accumulating record |

**Part I — The Library** holds the first four sections (Maps, Works,
Correspondence, Reference). Reference works, tools, studies, and the
foundational documents that ground the methodology.

**Part II — The Personal Codex** holds the fifth (Codex Vini, and
forthcoming Codex Vinitorum). The instruments and works in Part I
look at wine in general; the Codex is different in kind — it looks
at one person's experience of wine.

Everything in Vinotheca is connected; the section structure expresses
operational mode, not isolation.

---

## 2. The "Work" — paired tool + study

A **Work** is a single artefact with **two faces**:

- A **Tool face** — the interactive instrument, on its own page
- A **Study face** — the intellectual companion, on its own page, in
  the same documentation format as Soul of Wine (question, findings,
  why it matters, documents, method)

The two faces share the same set of supporting PDFs (Summary, Technical
Appendix, Methods Primer, Data Appendix, optionally a domain Reference).
The PDFs are linked from both faces. The Tool face surfaces them in its
Documentation dropdown; the Study face weaves them into the narrative.

A tool without its paired study is **incomplete** — the Work is half-built.
A tool can launch ahead of its study (this is the current state of Grape
Affinities) but the goal is paired completion.

The parent Vinotheca page presents each Work as a single entry showing
both faces, not as separate Tool and Study cards.

---

## 3. Leaves — current state

| Section | Site | Repo | Status | Wordmark | Eyebrow |
|---------|------|------|--------|----------|---------|
| Parent | Vinotheca | `vinotheca` | Live | Vinotheca | A LIBRARY OF WINE WORKS |
| Maps | The Estate Atlas | `estate-atlas` | Live | The Estate *Atlas* | An Atlas of Vinotheca |
| Maps | The Grand Cru Atlas | `grand-cru-atlas` | Live | The Grand Cru *Atlas* | An Atlas of Vinotheca |
| Works → Tool | Grape Affinities | `tasterank-explorer` | Live | Grape *Affinities* | A Tool of Vinotheca |
| Works → Study | The Body of Wine | `body-of-wine` | Live | The *Body* of Wine | A Study of Vinotheca |
| Works → Tool | Region Affinities | `region-affinities` | Live | Region *Affinities* | A Tool of Vinotheca |
| Works → Study | The Soul of Wine | `soul-of-wine` | Live | The *Soul* of Wine | A Study of Vinotheca |
| Works → Tool | Winemaker Affinities | *(tbd)* | Forthcoming 2026 | Winemaker *Affinities* | A Tool of Vinotheca |
| Works → Study | The Hand of Wine | *(tbd)* | Forthcoming 2026 | The *Hand* of Wine | A Study of Vinotheca |
| Correspondence | Region Resonances | `region-resonances` | Live | Region *Resonances* | A Correspondence of Vinotheca |
| Correspondence | Grape Resonances | `grape-resonances` | Live | Grape *Resonances* | A Correspondence of Vinotheca |
| Correspondence | Winemaker Resonances | *(tbd)* | Planned — see §6.4 | Winemaker *Resonances* | A Correspondence of Vinotheca |
| Reference | *(no leaves yet)* | `vinotheca-reference` | Repo to be created — empty for now | — | A Reference of Vinotheca |
| Personal Codex | Codex Vini | `codex-vini` | Live | Codex *Vini* | A Codex of Vinotheca |
| Personal Codex | Codex Vinitorum | `codex-vinitorum` | Live | Codex *Vinitorum* | A Codex of Vinotheca |

All repos are public under `github.com/jskarabot18/`. Pages URLs follow
`https://jskarabot18.github.io/<repo>/`.

The repo `tasterank-explorer` is a working name; the user-facing wordmark
is "Grape Affinities". The repo name is preserved so external links and
bookmarks don't break — repo names are infrastructure, the wordmark is
what visitors see. TasteRank stays as the algorithm name (referenced in
the panel subtitle and the documentation).

### 3.1 Current Works pairings

| Work | Tool face | Study face |
|------|-----------|-----------|
| Grape similarity | Grape Affinities (live) | The Body of Wine (live) |
| Region kinship | Region Affinities (live) | The Soul of Wine (live) |
| Winemaker character | Winemaker Affinities (forthcoming) | The Hand of Wine (forthcoming) |

The triptych of Study titles — *Body / Soul / Hand of Wine* — names
three distinct ways of seeing wine: through the material network of
grape varieties (Body), through the cultural temperament of regions
(Soul), and through the character of the people who make it (Hand).
Each is necessary; none is sufficient.

---

## 4. Cross-cutting design decisions

These rules govern every leaf in the family. New leaves should follow them.

### 4.1 Wordmark — italic emphasis on the noun

`<roman first half> <em>italic noun</em>`. The Estate *Atlas*. Region
*Affinities*. The *Soul* of Wine. Codex *Vini*. Codex *Vinitorum*. The
parent ("Vinotheca") is the only exception — single word, no italicisation.

### 4.2 Eyebrow grammar — "X OF VINOTHECA"

Every leaf has an eyebrow declaring its category in the same grammar.
See §3 for the full table. The parent itself uses "A LIBRARY OF WINE
WORKS", establishing itself as the named container. Eyebrows render in
small caps, letter-spaced, in a muted accent colour.

### 4.3 Footer — canonical pattern

Every leaf footer contains, in order:

1. Centred motto: `❧ in vino, cognitio ❧` (fleurons, never em-dashes)
2. Link row: `GitHub · License · CC BY-NC 4.0 · Vinotheca · Correspondence`
3. Copyright: `© Jure Skarabot · MMXXVI`

"License · CC BY-NC 4.0" is a single link to the LICENSE file. The
"Vinotheca" link is omitted on the parent itself. The "Correspondence"
link goes to `mailto:hello@codexvini.com` — the **email contact**. Note
this is distinct from the `Correspondence` content section in Part I,
which is a content section (currently containing Region Resonances).
Codex Vini is the layout exception: its links live in the header rather
than the footer, but the motto and copyright still appear in the footer.

The licence file itself lives at the repo root as `LICENSE` (no
extension, all caps). This is the filename GitHub's licence-recognition
reads — the "View license" sidebar entry and the "Other" tag in the repo
list both depend on it. Every leaf in the family carries an identical
CC BY-NC 4.0 text with a per-leaf header line naming the wordmark (e.g.
`Region Resonances © 2026 by Jure Skarabot is licensed under CC BY-NC
4.0.`), following the convention established by Codex Vini. The footer
"License · CC BY-NC 4.0" link points at this file.

### 4.4 Documentation menu — one pattern per section

- **Tools** (Grape Affinities, Region Affinities, Winemaker Affinities):
  `Documentation ▾` dropdown in the masthead, single-line entries, one
  per PDF in the canonical framework.
- **Studies** (Soul of Wine, Body of Wine, The Hand of Wine): in-page
  anchor menu and document cards. The study-class template will be
  properly defined when there are three live studies.
- **Maps** (Estate Atlas, Grand Cru Atlas): single `Download X Atlas PDF`
  button in the masthead. Atlases ship one consolidated PDF rather than
  the multi-document framework.
- **Correspondence** (Region Resonances and Grape Resonances, with
  Winemaker Resonances forthcoming): pattern tbd. Likely the Tool
  dropdown pattern, since Correspondence is tool-class.

### 4.5 Documents are aligned to a canonical framework

Each Work ships its documentation as a fixed set of PDFs:

- Summary (plain-language overview)
- Technical Appendix (algorithms and computation)
- Methods Primer (guide to the methods)
- Data Appendix (sources, edge tables)
- *Optional fifth: domain Reference* (e.g. "Grape Reference" on Grape Affinities)

The same PDFs are linked from **both faces** of a Work — the Tool face
surfaces them in its dropdown; the Study face weaves them into the
narrative or lists them as documents.

LaTeX sources for all documents are archived in each tool repo's
`docs-source/` folder. This means PDFs can be regenerated without losing
source material if amendments are needed.

### 4.6 Studies don't embed tools; tools don't appear inside studies

A **Study** presents an argument and supports it with documents. It does
not embed interactive tools.

A **Tool** is a standalone interactive instrument with its own page.

Cross-linking happens through the parent Vinotheca catalogue (which
shows pairings) and through prose ("Explore this interactively in
[Region Affinities]"), never through embedding a tool inside a study's
page. Soul of Wine previously had an "Interactive Tools" section that
violated this rule — it embedded four prototype tools (Cluster Explorer,
Cluster Map, Movement Map, D-Score Dashboard), all superseded by Region
Affinities. The section and the four prototype HTML files were removed
on 2026-05-08 (see §7).

### 4.7 The study-class template will be defined when a stable set of studies exists

Soul of Wine and Body of Wine are live. The proper study-class template
should be defined against the full set of studies (currently two live,
with The Hand of Wine forthcoming) so they can be designed together
rather than retrofitting earlier studies to a template-of-one.

Visual harmonisation work was completed in Pass 3 (May 2026) at the
palette and typography level. Deeper layout-level template work remains
open and is gated on The Hand of Wine joining the live set.

### 4.8 Visual systems — currently three subsystems, target one

The family currently has three visual subsystems:

- **The Library** (parent, Estate Atlas, Soul of Wine): warm parchment,
  EB Garamond + Cormorant Garamond
- **The Tools (React)** (Region Affinities, Region Resonances):
  parchment-warm, Tailwind-driven
- **The Atlases (static)** (Grape Affinities, Grand Cru Atlas):
  whiter ground, DM Sans body + Cormorant Garamond wordmark
- **Codex Vini**: own palette

Target is one canonical palette and one canonical font system across the
whole family, with permitted variation for Codex Vini. This is Pass 3 work,
deferred until the second study exists per §4.7.

The wordmarks have already been brought to a shared serif (Cormorant
Garamond). Body text systems still differ.

### 4.9 Reference — quietly signposted, not foregrounded

Reference is the deepest layer of the library. It contains intellectual
foundations (theoretical, technical, practical) that ground the
character-based analysis methodology underlying the wine work. Reference
documents are **not foregrounded** — a casual visitor came for wine, not
Bourdieu. But Reference must exist, be findable, and be linked, so
serious readers can find the conceptual scaffolding.

Reference items are written deliberately to be readable on their own
terms years later. They predate Vinotheca-the-implementation conceptually
and would survive if Vinotheca went away.

### 4.10 Operational independence between Reference and the wine domain

The Reference section's content describes the *general* methodology
(character-based analysis as a domain-neutral pattern). Vinotheca is the
*wine-specific instantiation*. A future application of the same methodology
to a different domain (film, architecture, music — see Technical
Foundations document) would draw on the same Reference content.

This is why Reference has its own repo (`vinotheca-reference`) rather than
living inside the wine-specific repos.

### 4.11 Correspondence is oracular, not search — design implications

Correspondence tools are not recommendation systems. They are **oracles in
the classical sense** — instruments of self-recognition where the user
brings a question and receives a compressed, considered offering against
which their own situation becomes legible. The success state is the
user's pause and recognition: *yes, that is exactly the wine I would
drink with that feeling*. The framework underneath (Soul of Wine's 59
region narratives) makes the recognition non-arbitrary; the compression
of the response is what makes the recognition possible.

This frame has direct design consequences for every Correspondence tool:

- **Compression over comprehensiveness.** Few results, tightly framed.
  Two to four grapes — not ten. Five regions — not twenty. The oracle's
  authority comes partly from its restraint.
- **One framing sentence carries the response.** The user reads the
  result and one sentence of context. Long explanation breaks the
  oracle frame and shifts authority from the user back to the tool.
- **The framework is traceable but not foregrounded.** A "see how the
  framework arrived at this" fold can exist for curious users, but it
  is collapsed by default. The user gets the answer, not the working.
- **Verification is invited, not measured.** A *Does this resonate?*
  prompt creates the moment of recognition without recording the
  response (privacy-first, per the existing ethos). The pause is the
  data; nothing is logged.
- **Graceful refusal of wrong-shaped queries.** Pairing questions,
  catalogue questions, and varietal-search questions are not in the
  oracle's domain. The tool detects them and redirects honestly. The
  refusal preserves the tool's character.
- **No personalization, no learning.** The tool's authority comes from
  the fixed framework, not from optimization against the user's
  history. Same query, same response, on the hundredth use as on the
  first.
- **Bullseye queries vs. prism queries.** Some queries land on a single
  coherent temperament (one cluster, one framing); some refract into
  multiple coherent facets (the user's word holds several registers at
  once). The tool detects which kind of query it received and frames
  accordingly. Forcing a prism query into bullseye framing flattens it;
  forcing a bullseye query into prism framing manufactures complexity
  that isn't there.

Region Resonances was the first Correspondence tool and established the
input-feeling-out-place pattern. Grape Resonances extends the pattern to
grape-as-output, completing the move from feeling to wine via region as
the temperament-mediator. Winemaker Resonances
(planned, see §6.4) extends the Correspondence section to the winemaker
work — though, per §4.12, that leaf matches directly against winemaker
character profiles rather than via region-mediation. Future Correspondence
tools, if any, should be designed to this character.

The deeper claim that grounds this section: Vinotheca is, structurally,
a small library of serious instruments for paying attention to wine and,
through wine, to oneself. Correspondence is the part of the library
where this second-order attention is most directly available — where the
analytical apparatus of the studies and tools meets the user's interior
life. *In vino, cognitio* describes both directions.

### 4.12 Character-mediated association — the architectural principle

The Correspondence tools rest on a principle worth stating explicitly,
because it is more general than wine and may govern leaves not yet
imagined. **The framework refuses to claim direct associations between
feelings and surface-level objects.** It does not claim that *Pinot Noir
is the grape of falling in love*. There is no defensible substrate on
which such a claim could be supported, and the framework would not
produce one without inventing it.

What the framework does instead is mediate every such association
through a **layer that genuinely carries character**. In the wine
domain there are two such layers, used differently depending on the
surface object.

**Case 1 — Intermediate-layer mediation** (surface object does not
itself carry character). For grapes and wines, the intermediate layer
is regions — the 59 narratives of *Soul of Wine* embed temperament
because regions, as cultural entities, are the kind of thing actually
capable of having a temperament. Regions have histories, customs,
hierarchies, and ways of being; grapes do not, chocolates do not,
music does not. The temperament work is done at the layer where
temperament can live, once, in a single embedding.

Surface-level objects are then surfaced by **association from the
intermediate layer**, not by their own connection to feelings:

```
feeling → matched regions ──► grapes the region grows
                         ├─► chocolates the region pairs with
                         ├─► music the region produced
                         ├─► writers the region shaped
                         └─► foods the region cooks
```

This is what the Planning Doc calls *"region as the temperament-carrier,
grape as the consequence."* But the principle generalises: **any object
genuinely rooted in regional culture can be derived from the same
matching engine by adding one more association file** (analogous to
`region_grapes.json`). The embedding work, the cluster structure, the
matching engine, and the response shape are all reusable. A new leaf
costs the curation of one new region-to-object table plus a thin
authored layer of object narratives.

The claim every Correspondence leaf can defensibly make has the same
two-step shape:

1. *The regions whose temperament matches your phrase are these.*
   (Supported by *Soul of Wine*'s region narratives and the embedding
   match.)
2. *Those regions are culturally associated with these objects.*
   (Supported by the curated association file for that domain.)

The framework joins two existing defensible claims. It does not
invent a third claim that connects feeling to object directly.

This principle has practical consequences for the family:

- **The 59 region narratives are the load-bearing asset of Vinotheca.**
  Investment in their quality, internal coherence, and continued
  refinement pays out across every present and future Correspondence
  leaf. They are the single point against which everything is matched.
- **Curated association files are the marginal cost of a new leaf.**
  `region_grapes.json` (101 grapes curated against 59 regions) is the
  Grape Resonances version. Future leaves require their own equivalent
  but reuse everything else.
- **Object narratives are authored separately.** Each leaf has its
  own equivalent of `grape_narratives.json` — a thin authored layer
  of character notes for the surface objects, in the same trace-fold
  register.
- **The matching engine, aggregator, response shape, and trace fold
  are reusable across leaves.** Different leaves will tune the
  aggregator selection rule to the cardinality of their object set
  (e.g. *recurrence as finding* may behave differently for 101 grapes
  vs 200 chocolates), but the architecture remains the same.
- **What disqualifies a candidate leaf:** the object class must be
  genuinely rooted in regional culture for the principle to work
  honestly. Grapes, foods, traditional music, regional literature,
  vernacular architecture — all candidates. Generic consumer goods
  (sneakers, smartphones, cocktails-as-international-category) are
  not regional in this sense; their association files would be
  curatorial fictions rather than findings.

**Case 2 — Direct mediation** (surface object itself carries character).
For winemakers, the surface object is itself a temperament-carrying
entity. Winemakers are people; they have disposition, posture, ways of
working, and a stance in the world. They are exactly the kind of entity
that can carry character in the strong sense. When this is true, the
matching engine runs against the surface object directly, without
needing an intermediate layer:

```
feeling → matched winemaker character profiles → those winemakers (and their wines)
```

The general principle: **the mediation layer must be something that
genuinely carries character.** Where the surface object cannot, the
framework needs an intermediate layer that can. Where the surface object
can, no intermediate layer is required.

Region Resonances is the leaf where the user receives the regions
directly. Grape Resonances is the first leaf where the user receives
something *derived* from regions through cultural association.
Winemaker Resonances (planned, see §6.4) is the first leaf in the Case 2
register — the user receives the winemakers directly, no intermediate
layer needed. Future leaves following this architecture extend the same
moves to other object classes; their feasibility is governed by whether
the candidate mediation layer (intermediate or direct) genuinely carries
character.

The conceptual work generalising this principle beyond Vinotheca is
held separately in `FRAMEWORK_NOTES.md` and is explicitly conditional
on Vinotheca's completion. It is not an active task.

---

## 5. Process notes

These workflow patterns have been found to work reliably:

- **One repo at a time.** Don't download multiple file bundles into
  Downloads simultaneously — files with the same name (`README.md`,
  `Header.jsx`, `index.html`) get auto-renamed by browsers. Finish one
  repo's commit, move/delete its files from Downloads, then start the next.

- **Sanity checks before commit.** Use `grep` and `head -1` to confirm
  the right file is in the right place before staging. Catches typos like
  `README.m` (missing extension character) and wrong-repo file mixups.

- **`git status` before AND after `git add`.** Before catches stray files
  in the working tree; after confirms the staging is clean.

- **Static sites deploy in ~1 minute. React tools deploy in 1-3 minutes**
  via GitHub Actions. **Hard refresh (Cmd+Shift+R)** to bypass browser
  cache after deploys, especially when CSS changes.

- **Conversation context is not memory.** Decisions made in conversation
  must be written to this file or they will be lost when the conversation
  is summarised or the next conversation begins.

- **PROJECT.md is read first, every session.** Any new conversation about
  Vinotheca should begin with a fetch of this file. The fetch URL is
  `https://raw.githubusercontent.com/jskarabot18/vinotheca/main/PROJECT.md`.

---

## 6. Open questions and active tasks

### 6.1 To be built — `vinotheca-reference` repo

Per §1 and §4.9–§4.10, Reference is its own section with its own repo.
The repo `vinotheca-reference` is to be created. **No content yet** —
the foundation documents (Theoretical Foundations of Character-Based
Analysis, Technical Foundations of Character-Based Analysis, Practical
Foundations) will be added when ready. The repo will follow the same
family pattern (wordmark, eyebrow `A Reference of Vinotheca`, footer
matching §4.3).

**Pending:**
- Repo creation
- Page structure for the Reference site
- Decision on whether to include the foundation documents at launch or
  delay until they are ready for public release

### 6.2 To be built — Winemaker Affinities (tool) and The Hand of Wine (study)

The third Work in the Vinotheca catalogue. Forthcoming 2026. A working
framework document exists (the April 2026 *Vigneron Kinship* framework,
held in project material) but is no longer a complete description of
the planned approach — see below.

**Architectural posture (revised 2026-05-11).** The earlier framework
proposed claim-based winemaker profiles as the primary analytical unit.
A subsequent brainstorming session (recorded as v0.21 in §8) reframed
the winemaker work in the context of §4.12's character-mediated
association principle. The revised posture:

- **Winemakers are themselves temperament-carrying entities.** Per
  §4.12 Case 2, they do not require an intermediate mediation layer;
  the matching engine for the Correspondence leaf (§6.4) runs directly
  against winemaker character profiles.
- **The Works leaf and the Correspondence leaf share their
  load-bearing asset.** The winemaker character profiles power both:
  the analytical clustering in Winemaker Affinities, and the
  character-matching in Winemaker Resonances. This is tighter than the
  grape case, where Body of Wine and Grape Resonances have somewhat
  different needs.
- **The unit and shape of the winemaker character profile is the
  central open question.** The April framework's claim-based approach
  is more verifiable per element but flatter in temperament signal. A
  portrait-based approach (closer to the 59 region narratives) is
  richer in temperament signal but verified at the portrait level
  rather than per-claim. Possibly a hybrid: structured claims as the
  evidentiary layer, a portrait as the matching layer. To be resolved
  during build.

**Pending:**
- Lock the winemaker character profile shape (claims vs. portrait vs. hybrid)
- Confirm the corpus (the April framework proposes 60–80; an earlier
  note mentions 32 — to be reconciled)
- Build the corpus
- Build the analytical pipeline (Winemaker Affinities)
- Write the Study (The Hand of Wine)
- Build the oracle (see §6.4 — shares this corpus)

This is the largest remaining piece of work in the Vinotheca build.

### 6.3 Built — Grape Resonances (closed 2026-05-11; documentation closed 2026-05-13; recorded in §7)

The second Correspondence leaf is live at
`https://jskarabot18.github.io/grape-resonances/`. Build history, the
shipped architecture, and the findings from live testing are recorded
in the §7 entry for 2026-05-11. Detailed planning preserved in
`grape-resonances/Grape_Resonances_PlanningDoc.md`; the planning doc's
three locked worked examples are revised against curated data + the
live matcher in the §7 entry — the framework's actual readings differ
from the predictions in interesting ways, recorded as findings rather
than defects.

The four canonical PDFs per §4.5 (Summary, Methods Primer, Technical
Appendix, Data Appendix) were authored and deployed in the 2026-05-13
session; the Documentation dropdown now resolves all four entries
correctly, plus the cross-link to Region Profiles — Identity. LaTeX
sources archived alongside the family's other 12 source files. See
§7 entry for 2026-05-13 for the authoring methodology and the v1
caveats logged for the planned sanity-check pass against the live
data files.

### 6.4 To be built — Winemaker Resonances (third Correspondence leaf)

The Correspondence leaf for the winemaker work. Maps user input
(feeling, phrase, situation) to a small number of winemakers whose
character corresponds to that state. Per §4.12 Case 2, this leaf does
**not** use region-mediation; it matches directly against winemaker
character profiles, since winemakers themselves carry temperament in
the strong sense.

Example queries the instrument is designed for: *I am feeling
exploratory · I am homesick · I need a vacation · I am about to make a
difficult decision · I want to be reminded what care looks like.* The
response is one to three winemakers whose character resonates with
that state, with their wines as the cultural object the user can then
drink.

**Architecture:** inherits from Region Resonances (same stack, same
response shape, same oracle frame from §4.11). The matching layer is
the winemaker character profiles authored as part of §6.2 (the
load-bearing asset is shared between Winemaker Affinities and
Winemaker Resonances).

**Pending:**
- All of §6.2 — this leaf cannot be built until winemaker character
  profiles exist
- Engineering work (after profiles exist): aggregator, coherence
  detector, React scaffold, deployment

This is the most emotionally consequential leaf in Vinotheca. The
character profiles need to be honest about real people without
flattening them, and true enough that a stranger feeling homesickness
can recognise themselves in the match. The writing register and
ethical care will be unusually demanding.

### 6.5 Built — Codex Vinitorum (closed 2026-05-14; recorded in §7)

The personal Codex for winemakers met in person, paralleling Codex
Vini's role for wines tasted. *Codex Vinitorum* = "Book of Winemakers"
in Latin; mirrors Codex Vini's noun-plus-genitive form. *Vinitor*
(pl. *vinitores*, gen. pl. *vinitorum*) is the classical Latin word for
vine-dresser / winemaker.

The codex records winemakers met in person with personal attributes —
analogous to Codex Vini's tasting records but for the person rather
than the bottle. The 35 winemakers from the existing Winemaker's
Compass (v6) populate the initial entries.

**Live at:** [jskarabot18.github.io/codex-vinitorum](https://jskarabot18.github.io/codex-vinitorum/) · repo: `codex-vinitorum`

**Architectural rule (locked).** Library (Part I) and Personal Codex
(Part II) do not interact. Codex Vinitorum is a standalone Part II
artefact, designed on its own terms. Its content does not feed the
Works leaf (§6.2) or the Correspondence leaf (§6.4). The Compass
winemakers appear in the Works/Correspondence corpus because they are
significant winemakers with rich source material, not because they
are recorded in Codex Vinitorum. The two domains are sealed.

**Affinity signals (locked 2026-05-11).** Codex Vinitorum entries
carry three optional, orthogonal experience-side signals rather than
a numeric rating:

- *Felt close to* — felt personal closeness with the winemaker
- *Memorable encounter* — the meeting itself stood out
- *Stayed with me* — the encounter persisted in your thinking after it ended

Each signal is independently present or absent on an entry. The three
describe the user's experience of the encounter, not the winemaker as
object; they do not compose into a score and do not produce a ranking.
The discomfort of rating people on a personal record was the design
constraint that surfaced this choice. The signals also distinguish
Codex Vinitorum's entry register from Codex Vini's (which carries a
numeric rating of the wine), honouring the architectural rule that
Library and Personal Codex differ in kind, and adding a quiet
differentiation between the two Personal Codex leaves themselves.

**Bio register (locked at build).** Per-winemaker bios are written in
a factual, encyclopedic register at roughly 80–110 words per entry:
lineage and training, substantive decisions, estate facts (varieties,
hectarage, key cuvées). No quality-claims ("foremost," "greatest,"
"rivals"). No comparative judgements. No personal-impression
sentences — character and disposition belong to the affinity signals,
not the bio. The bios were derived from the Winemaker's Compass v6
through a light editing pass that stripped wine-critic register and
preserved factual content; some of the more uncertain dates were
softened to decades or ranges rather than committed to specific years
that might be wrong. The bios are working content and will be refined
as new information surfaces; this is consistent with the framework's
broader stance that publishable Library-adjacent leaves can launch
with material that's honest about its provisional state.

**Built (2026-05-14):** The leaf shipped with the full Codex Vini
sibling pattern — *The Book* (sortable, searchable, filterable table),
*The Atlas* (Leaflet map with uniform pins, one per winemaker), and
*The Collection* (six aggregate charts: by country, by region, by
event, by year, signal distribution, signal combinations). The
affinity signals render as three signal-specific columns in the Book
(*Close* / *Memorable* / *Stayed*, short-form headers with tooltip
expansions); each cell shows a fleuron if the signal is on. Pins are
uniform — no size or colour variation by signal — honouring the
no-ranking commitment at the visual level. The build folded in the
output of the Codex Vinitorum signals workbook (an interactive HTML
tool authored mid-week that let the workbook user mark signals across
multiple sessions and export structured JSON); 19 of 35 entries carry
at least one signal at launch (8 *felt close to*, 10 *memorable*, 7
*stayed with me*). See §7 entry under 2026-05-14 for the full
multi-day arc and follow-up refinements (three-column display,
auto-pan popups, scroll-wheel zoom).

### 6.6 Atlas wordmark renames — deferred

A naming alignment for the two atlases in the Maps section is locked
as the intended future state but not executed: **Grand Cru Atlas $\rightarrow$
Vineyard Atlas** and **Estate Atlas $\rightarrow$ Maker Atlas**. The renames
affect *only the displayed wordmark and catalogue-side names*. The
GitHub repository names (`grand-cru-atlas`, `estate-atlas`) and
deployment URLs stay unchanged.

**Why the change.** The current names break the family's
`{Subject} {Operation}` naming pattern that holds elsewhere
(Grape Affinities, Region Affinities, Grape Resonances, Region
Resonances, etc.). *Grand Cru* names a prestige tier rather than a
subject category; *Estate* names an organisational unit but doesn't
visibly anchor what the atlas catalogues. After rename, the Maps
section will read as **Vineyard Atlas + Maker Atlas** — two atlases
whose names declare their subject (vineyards as places; makers as
the producing entities holding the work), parallel to the rest of
the family.

**The Maker Atlas distinction.** *Maker* deliberately names a broader
scope than *Winemaker*: an estate, domaine, or house is a *maker*,
while *Winemaker Affinities*, *Winemaker Resonances*, and *Codex
Vinitorum* are about the person carrying temperament. The shared
word root across *Maker Atlas* and the Winemaker leaves signals
shared subject domain; the different scope (entity vs.\ person) is
disambiguated by section heading (Maps vs.\ Works / Correspondence /
Personal Codex). The renamed catalogue then completes a subject-
across-operations matrix in which *Maker Atlas* fills the Maps
column for the winemaker subject.

**Scope when executed.** Wordmark in each atlas's HTML; page
titles; the parent Vinotheca catalogue page; any cross-links from
other six leaves that name the atlases; the consolidated atlas
PDFs' title blocks and on-page references (file names follow the
repo and stay the same per the no-repo-rename decision above);
§3.1 leaves table in this document; the §4.1 wordmark example
referencing *The Estate Atlas*; §4 incidental references; a new
§7 entry recording the rename and a §8 changelog block. The
mechanical-text scope is similar to the TasteRank Explorer $\rightarrow$
Grape Affinities rename of 2026-05-09 (see §7 entry that day),
which kept the repo URL and changed only the displayed wordmark
and catalogue-side naming. That precedent's pattern carries here
directly.

**Status.** The names are locked; execution is queued for a
future session. No deadline. Low urgency — the misalignment is
real but not blocking, and the leaves themselves are stable.

---

## 7. Recently completed (reverse chronological)

### 2026-05-14

- **Codex Vinitorum launched — second Personal Codex leaf live at
  `jskarabot18.github.io/codex-vinitorum/` per §6.5.** The multi-day
  arc that produced the leaf is worth recording as a unit because the
  decisions and the build interleaved in ways that the chronological
  changelog only thinly captures. The arc began on 2026-05-11 when
  the winemaker section was rearchitected into three coordinated
  leaves (§6.2 Works, §6.4 Correspondence, §6.5 Personal Codex) and
  the affinity-signals decision was locked. The signals workbook was
  authored mid-week as a preparation tool — an interactive HTML
  artifact with persistent storage that let the workbook user mark
  signals across multiple sessions and export structured JSON; the
  workbook design surfaced a small ranking-trap (when 0–3 fleurons
  were proposed coloured by count, this would have re-introduced
  ranking; the fix was uniform colour with positional ordering — a
  good real-time application of the §6.5 no-ranking rule). The
  workbook export then fed the build, which proceeded in five
  stages: the data file (`winemakers.json`, 35 entries merging
  bios + signals + region coordinates), the regions lookup
  (`regions.json`), the main app (`index.html` with The Book / The
  Atlas / The Collection sections), the add-winemaker form
  (`add_winemaker.html`), and the supporting files (README, LICENSE
  at `LICENSE` per the §4.3 convention locked in v0.25). The bios
  were authored in a factual encyclopedic register per the §6.5
  *Bio register* commitment — light editing pass over the Compass v6
  bios that stripped wine-critic register ("foremost," "almost
  single-handedly elevated") and preserved factual content. Deployment
  to GitHub Pages required three corrective steps because the first
  attempt accidentally set the source to "GitHub Actions" rather than
  "Deploy from a branch," creating a stale `github-pages` environment
  that broke deploys; the fix was to delete the environment, push a
  `.nojekyll` file, and let Pages auto-recreate the environment in
  the correct state. Follow-up refinements completed the same day:
  the single Signals column in The Book was replaced with three
  signal-specific columns (*Close* / *Memorable* / *Stayed*, short
  headers with tooltip expansions, fleurons centred per column);
  Leaflet popup positioning was fixed with `autoPan` and `maxHeight`
  so popups always sit fully inside the visible map area; and
  scroll-wheel zoom was enabled on the map matching Codex Vini's
  interaction pattern. The leaf launched with 19 of 35 entries
  carrying at least one signal — 8 *felt close to*, 10 *memorable
  encounter*, 7 *stayed with me*. The signal distribution observed
  the rarity hierarchy predicted during the workbook design phase:
  memorable encounter is most common (most encounters of vivid
  professional tastings stand out); felt close to and stayed with me
  are rarer and more selective. The discipline held — an entry
  without signals is as honest a record as one with three. Codex
  Vinitorum is the second Library-adjacent personal artefact (with
  Codex Vini), sealed from the Library per the §6.5 architectural
  rule.

- **Grape Resonances Data Appendix sanity-check pass closed —
  11 findings, 11 corrections applied, v1.1 deployed.** The caveat
  logged in the §7 entry for 2026-05-13 has been resolved. The four
  live JSON files (`region_grapes.json`, `cluster_framings.json`,
  `grape_aliases.json`, `grape_narratives.json`) were uploaded and
  diffed against the Data Appendix across six sections (§B canonical
  101-grape surface, §C alias map, §D silent-skip list, §E framing
  sentences, §F per-region signature table, §G.3 cross-region pattern
  table). Two sections were clean: §B (all 101 canonical grape names
  match across reds and whites; identical sets) and §E (all 10 framing
  sentences render verbatim). The other four sections had findings:
  three in §C (alias keys), one in §D (silent-skip display), eight in
  §F (five signature mismatches plus three temperament-seconds
  mismatches), and one in §G.3 (the Sémillon cross-region row).

  *Substantive findings — 4.* These were factual errors a reader would
  rely on. (i) Bordeaux signature was listed as
  \[Cabernet Sauvignon, Merlot] but the live data has three pillars
  \[Cabernet Sauvignon, Merlot, Cabernet Franc] — Cabernet Franc as
  the third signature is the curatorial position, in keeping with
  Bordeaux's actual blend traditions. (ii) Northern Rhône signature
  was listed as \[Syrah] alone but the live data has \[Syrah, Viognier]
  — Viognier is signature for the Condrieu/Château-Grillet expression
  the region is also known for. (iii) Paso Robles temperament-seconds
  was listed as Mourvèdre but the live data has Grenache — this was
  a fact mismatch in the original Data Appendix authoring. (iv) The
  §G.3 cross-region table listed Sémillon as appearing 3x (Bordeaux,
  Patagonia, Margaret River), but the live data uses two distinct
  spellings: Sémillon (with accent) in 2 regions (Bordeaux, Patagonia)
  and Semillon (no accent) in 1 region (Margaret River). The Curation
  State doc's "spelling note" documents this as intentional regional
  spelling preserved per local convention; the v1 Data Appendix
  conflated the two spellings rather than acknowledging the
  distinction.

  *Cosmetic findings — 7.* These preserve identity but use different
  display forms. The live data uses parenthetical disambiguation in
  keys (e.g.\ "Garnatxa (Grenache)", "Rebula (Ribolla Gialla)",
  "Semillon (Hunter Valley)", "Muscat (Blanc à Petits Grains +
  Ottonel)", "Gamay Noir") where the v1 Data Appendix had dropped
  the parentheticals. The parentheticals matter because that is
  exactly how the strings appear in the aggregator's lookup at the
  signature-tier stage, and bringing the displayed forms in line
  with what the aggregator actually reads improves the document's
  value as a reference. Affected: §C (3 alias key entries),
  §D (1 silent-skip display name), §F (5 signature rows, 3
  temperament-seconds entries).

  *Corrections applied.* All 11 findings were applied to the
  GrapeResonances\_Data\_Appendix.tex source via str\_replace edits
  and the document was recompiled. §G.3's intro paragraph was
  rewritten to explain the Sémillon/Semillon spelling distinction
  before showing the corrected table (5 grape identities recurring,
  with Sémillon split into two rows reflecting the intentional
  spelling decision). The other four §G.3 rows (Cabernet Franc 3x,
  Zinfandel 2x, Cinsault 2x, Grenache 2x, Syrah 2x) were unchanged.
  The corrected PDF grew from 9 to 10 pages (the §G.3 intro
  rewrite and the row split spilled over to a new page); all other
  pages render identically to v1 apart from the corrected table cells.
  The corrections were deployed to `grape-resonances/app/public/docs/
  grape-resonances-data-appendix.pdf` and the corrected source to
  `grape-resonances/docs-source/GrapeResonances\_Data\_Appendix.tex`,
  bringing the file to v1.1.

  *Summary, Methods Primer, and Technical Appendix are unchanged.*
  These three PDFs do not contain per-region or per-grape data and
  are not affected by the sanity-check scope. Their v1 state remains
  canonical.

  *Method observation worth recording.* The diff methodology was
  rigorous: each section of the Data Appendix that contained
  enumerated data was checked entry-by-entry against the live JSON
  file that supplies it, with mismatches classified as substantive
  (factual errors) or cosmetic (display-form differences). Three
  of the four substantive findings were factual errors in the v1
  authoring (Bordeaux missing Cab Franc, Northern Rhône missing
  Viognier, Paso Robles misnaming the temperament-seconds grape).
  These errors traced to the v1 authoring relying on past-chat
  fragments rather than the live JSON directly, as explicitly
  acknowledged in the §7 entry for 2026-05-13. The sanity-check
  pass caught all three substantive errors plus the §G.3 spelling
  conflation, plus seven cosmetic findings that improve the
  document's accuracy as a reference. For future canonical PDF
  authoring, the lesson is: when the live data file exists, diff
  against it before shipping, even when comprehensive past-chat
  reconstruction looks complete.

### 2026-05-13

- **Grape Resonances documentation closed — four canonical PDFs
  authored, compiled, and deployed across a single session.** The
  four documents per §4.5's canonical framework (Summary, Methods
  Primer, Technical Appendix, Data Appendix) were drafted, compiled
  with `pdflatex` against the shared `vinotheca-preamble.tex` /
  `vinotheca.sty` setup, reviewed page-by-page, and shipped to
  `grape-resonances/app/public/docs/` under their canonical
  filenames (`grape-resonances-summary.pdf`, `grape-resonances-
  methods-primer.pdf`, `grape-resonances-technical-appendix.pdf`,
  `grape-resonances-data-appendix.pdf`). The Documentation dropdown
  in Header.jsx had already been pointing at these filenames since
  the leaf shipped on 2026-05-11; all four 404s now resolve
  correctly. The cross-link to Region Profiles — Identity continues
  to work unchanged.

  *Authoring stance.* The four PDFs were authored under a deliberate
  deference rule: where Grape Resonances inherits infrastructure
  from Region Resonances (the matcher, the embedding model, the
  unit-sphere geometry, the cosine-similarity formulation, the
  clip-and-rescale display calibration), the Grape Resonances
  documents do not re-derive or re-teach the material — they cite
  the Region Resonances counterpart and proceed to what is genuinely
  new in Grape Resonances. This keeps the family's PDF set from
  duplicating itself and makes the per-tool documents proportionate
  to what each tool actually adds. The Summary opens with a one-
  paragraph cross-reference to Region Resonances and spends its real
  depth on the two-stage architecture; the Methods Primer's §1
  recaps the matcher in one page and defers the full plain-language
  treatment to the Region Resonances Methods Primer; the Technical
  Appendix's preface notes the deference explicitly and formalises
  only the new layers (alias resolution as a partial function with
  silent-skip state, the aggregator's three-mode piecewise rule, the
  coherence detector's cluster-count rule, the response object as
  a tuple, three propositions with proofs); the Data Appendix is
  comprehensive on what is specific to Grape Resonances (the 101
  canonical grape surface split 53 reds / 48 whites, the 12-entry
  alias map, the 11 silent-skipped non-canonical grapes, the 10
  framing sentences in full, the per-region signature curation in
  one 59-row table, the curation methodology with six principles
  and the same-grape cross-region pattern table) but explicitly
  cites the Region Resonances Data Appendix for the embedding model
  spec and operating characteristics rather than re-listing.

  *Doc-by-doc summary.* Summary: 8 pages, mirrors the Region
  Resonances Summary structure (Abstract → Intro → Data →
  Methodology → Results → Robustness → Conclusion → References),
  includes three live worked examples drawn from the deployed tool
  (the falling-in-love / brotherhood / move-decision queries from
  the §7 entry for 2026-05-11) plus the independent-Claude
  convergence on Furmint for *late summer* as evidence the region
  narratives carry semantic temperament that survives embedding.
  Methods Primer: 8 pages, plain-language register in the family's
  paragraph-style-with-bolded-headings format, eight sections
  closing with the canonical nine-step *Pipeline in Summary* recap.
  Technical Appendix: 9 pages, three top-level sections (A.
  Mathematical Framework with ten subsections including three
  propositions and proofs; B. Algorithms with four pseudocode
  blocks; C. Implementation with six subsections covering runtime,
  data shapes, complexity, caching, determinism, and failure modes).
  Data Appendix: 9 pages, nine top-level sections (A. Region Corpus,
  B. Canonical 101-Grape Surface, C. Alias Map, D. Silent-Skip List,
  E. Framing Sentences, F. Per-Region Signature Curation, G. Curation
  Methodology, H. Data File Inventory, I. References).

  *Source archive.* LaTeX sources for all four PDFs deployed to
  `grape-resonances/docs-source/`, joining the family's growing
  LaTeX archive. The full Grape Resonances source-file count is now
  four (Summary, Methods Primer, Technical Appendix, Data Appendix)
  alongside the shared `vinotheca-preamble.tex`. With Region
  Affinities' 4 + Region Resonances' 4 + Grape Resonances' 4 + the
  shared preamble, the family LaTeX corpus stands at 13 source
  files.

  *Caveat logged for sanity-check pass.* The Data Appendix's §F
  (per-region signature table) and §G.3 (same-grape cross-region
  pattern table) were assembled from past-chat fragments rather
  than from the live `region_grapes.json` directly, because that
  file was not at hand during the authoring session. The cluster
  framings in §E and the alias entries in §C are verbatim from
  past-chat extractions of the authored files but have not yet
  been diff-confirmed against the deployed JSON. A sanity-check
  pass against the four live JSON files (`region_grapes.json`,
  `cluster_framings.json`, `grape_aliases.json`,
  `grape_narratives.json`) is queued for the next session;
  corrections, if any, will be applied as a single follow-up
  commit to the Data Appendix sources rather than reissued as
  v1.1 across all four documents. The Summary, Methods Primer,
  and Technical Appendix do not contain per-region or per-grape
  data and are not affected by the sanity-check scope.

  This closure brings Grape Resonances to family-level
  documentation parity with Region Resonances and Region
  Affinities. Both currently-live Correspondence tools (Region
  Resonances, Grape Resonances) and both currently-live
  Affinities-side Works tools (Grape Affinities, Region
  Affinities) now have the full four-PDF canonical set per §4.5.
  The next documentation work in this register will be for
  Winemaker Affinities + The Hand of Wine (§6.2) and Winemaker
  Resonances (§6.4), neither yet built.

### 2026-05-12

- **LICENSE coverage closed at 10/10 across the family.** A
  family-wide audit surfaced three repos still missing a LICENSE
  file at the repo root — `region-resonances`, `grape-resonances`,
  and `region-affinities` — even though every leaf's README and
  footer already declared CC BY-NC 4.0 as the governing licence.
  The gap was small but real: without the LICENSE file at root,
  GitHub's licence recognition does not register the licence, the
  "View license" sidebar entry does not appear, and the licence
  text is not bundled alongside the source. README prose is not a
  legal grant; the LICENSE file is. Three identically-structured
  files were prepared, each personalised in its header line with
  the leaf's own wordmark per the family convention established by
  Codex Vini (e.g. `Region Resonances © 2026 by Jure Skarabot is
  licensed under CC BY-NC 4.0.`), and deployed one at a time. All
  three repos now show "View license" in their right sidebar and
  the "Other" tag in the repo list. §4.3 amended with a new
  paragraph making the LICENSE-at-root convention explicit so it
  is followed by default when the remaining forthcoming leaves
  (`winemaker-affinities`, `vinotheca-reference`, etc.) are
  spun up.

- **Region Resonances PLANNING.md and PROJECT.md archived to
  OLD_FILES/.** The two working documents — left over from the
  build phase and superseded by the canonical PROJECT.md in the
  `vinotheca` repo and by §6 / §7 entries here — were moved into
  an `OLD_FILES/` folder in the `region-resonances` repo. The move
  surfaced as a pending uncommitted change during the LICENSE
  audit session; it was committed separately to keep the LICENSE
  addition cleanly isolated in its own commit. Both files are
  retained in `OLD_FILES/` rather than deleted outright — the
  history is recoverable if any of the planning material proves
  useful later.

### 2026-05-11

- **Codex Vinitorum — affinity signals locked (§6.5).** A
  brainstorming conversation about how Codex Vinitorum should
  represent the user's relationship to each winemaker surfaced a
  decision worth recording at the architectural level. The
  discomfort of giving numeric ratings to people on a personal
  record was the design constraint. Standard recommender-style
  scoring (1–5, 1–10) was rejected as treating the winemaker as
  an object of judgment in a way the broader Vinotheca framework
  refuses. A single binary like/favorite indicator was considered
  but rejected as collapsing too much. The locked choice: three
  optional, orthogonal experience-side signals — *Felt close to*,
  *Memorable encounter*, *Stayed with me* — each independently
  present or absent on an entry. The signals are user-side (they
  name the user's experience of the encounter, not the winemaker
  as object), they do not compose into a score, and they do not
  produce a ranking. Selection of the three signals was the work
  of the conversation: *Felt close to* and *Memorable encounter*
  surfaced early as user-side facets of the encounter; *Stayed
  with me* was selected from a wider search across families of
  candidates (recognition / aftermath / attention / alignment) as
  the strongest fit — it names persistence in the user's
  subsequent thinking without claiming anything about the
  winemaker as a person, and it sits cleanly orthogonal to the
  other two (memorable is about vividness during; stayed with me
  is about afterlife). All three were also reworded mid-
  conversation to align in grammatical register (short verb
  phrases, user as implicit subject) — *Affinity* (the original
  first candidate) was set aside in favour of *Felt close to* for
  consistency. The decision aligns Codex Vinitorum's entry
  register with the framework's broader posture: the Codex marks
  what your experience was, not what the people are worth. The
  decision also adds a quiet differentiation between Codex Vini
  (numeric rating of the wine) and Codex Vinitorum (no rating;
  three optional facet signals), which the architectural rule
  that Library and Personal Codex differ in kind makes welcome.
  Recorded as a new locked block in §6.5; PROJECT.md entry-
  schema pending sub-item amended to reference the locked
  decision.

- **Correspondence chip registers refreshed for both Region Resonances
  and Grape Resonances — a small but real piece of family design
  work.** After Grape Resonances shipped, the hint chips on both
  Correspondence leaves were re-examined and revised. The work
  surfaced three findings worth recording. *(i) Chip register as a
  design dimension.* Region Resonances now ships short, adjective-led,
  aesthetic-contemplative chips (*old soul · careful joy · stubborn
  quiet · borrowed time · bright sorrow · gentle ruin*); Grape
  Resonances ships long-form, state-naming, poetic-register chips
  (*falling deeply in love · the feeling of brotherhood · the weight
  of a decision · the slow undoing of an old certainty · the quiet
  authority of having survived something · what you keep when
  everything else is gone*). The visual contrast between the two
  chip rows tells users something honest: Region Resonances reads
  the *character* of a feeling (compressible to 2–3 words); Grape
  Resonances reads a *state someone is carrying* (which needs a
  longer phrase to name precisely). The shared family chrome
  (eyebrow, wordmark, footer, masthead) keeps them recognisably
  siblings; the chip registers signal they're not the same tool with
  a different output surface. *(ii) Shared-trio design path
  considered and discarded.* During the chip work, an intermediate
  state had both tools sharing three contemplative-aesthetic chips
  (*borrowed time · bright sorrow · gentle ruin*) as a deliberate
  family rhyme. That decision held for about an hour. On reflection,
  the shared trio didn't survive contact with the register-coherence
  decision for Grape Resonances — once we settled on long-form
  state-naming as Grape Resonances' chip register, the short
  aesthetic-contemplative chips no longer fit alongside the longer
  ones. The shared trio remains only on Region Resonances. Worth
  recording as a design path that was considered, tested briefly,
  and consciously discarded. *(iii) Live use will reveal which chips
  actually get clicked.* Today's chip refreshes are design bets, not
  validated decisions. Worth revisiting in a few weeks; if certain
  chips never get clicked, swap them. This is the first articulated
  case of the principle that chip selection is downstream of register
  decisions but upstream of validated use — and validated use is the
  next step. Future Correspondence leaves (Winemaker Resonances)
  should consciously choose their own chip register rather than
  inherit either default. The refresh required two small commits, one
  per repo; no infrastructure or code changes beyond the
  `EXAMPLE_QUERIES` array in each leaf's `InputPanel.jsx`.

- **Grape Resonances — built, deployed, and cross-linked from Vinotheca
  parent.** The second Correspondence leaf is live at
  `https://jskarabot18.github.io/grape-resonances/` and listed at
  position vii in the Vinotheca parent's §3 Correspondence section
  alongside Region Resonances. The repo at
  `github.com/jskarabot18/grape-resonances` was scaffolded by forking
  Region Resonances' app/ infrastructure (Tailwind, Vite, deploy
  workflow, matcher, embedding hook) and overlaying the new
  grape-resonances bundle: aggregator + coherence detector +
  OracleResponse component + TraceFold component + 5 data files
  (region_grapes.json, grape_narratives.json, cluster_framings.json,
  grape_aliases.json, layer1_narratives.json) + region_embeddings.json.
  The Cloudflare Worker was reused byte-identical from Region Resonances;
  no new Worker spun up, no CORS allowlist edits needed (`https://
  jskarabot18.github.io` already permitted the production origin).
  Sub-items 4, 5, and 6 of §6.3 all closed in this session. The hint
  chips in InputPanel were swapped from Region Resonances' set
  (old soul / careful joy / stubborn quiet / the feeling of late summer
  / quiet defiance / earned ease / second chances) to a grape-shaped
  set covering the locked worked examples plus three new probe shapes:
  *falling deeply in love · the feeling of brotherhood · late summer ·
  the weight of a decision · starting over · the courage to wait*.

- **Grape Resonances — aggregator, coherence detector, and 12-entry
  alias file shipped (sub-item 4 closure).** The recurrence-as-finding
  rule from Planning Doc §"Aggregator selection rule" is implemented
  as `aggregate(matchedRegions, regionGrapes, grapeNarratives, aliases)`
  returning `{mode, grapes, skippedRegions}` where mode is one of
  `strong_recurrence` (≥3 of N matched regions share a grape),
  `multi_bullseye` (2–4 grapes each in ≥2 regions), or `prism` (top
  2–3 by similarity-weighted score). The coherence detector
  (`detectCoherence`) reads bullseye if ≥4 of N regions share a
  cluster, prism otherwise. The 12-entry `grape_aliases.json`:
  Spätburgunder → Pinot Noir, Shiraz → Syrah, Pinot Grigio → Pinot
  Gris, Pinot Bianco → Pinot Blanc, Weissburgunder → Pinot Blanc,
  Grauburgunder → Pinot Gris, Tinto Fino → Tempranillo, Cannonau →
  Grenache, Garnatxa (Grenache) → Grenache, Carinyena (Carignan) →
  Carignan, Carignano → Carignan, Semillon (Hunter Valley) → Sémillon.
  Eleven signature grapes left unaliased and non-canonical (Carricante,
  Glera, Greco di Tufo, Grillo, Macabeu, Pigato, Pinot Meunier, Pošip,
  Rebula, Rossese, Savagnin), silent-skipped per the v1 scope decision.
  The trace fold preserves the regional spelling for aliased
  contributions (e.g., "Barossa Valley — fortitude · as Shiraz")
  rendering the cross-cultural connection visibly to the user. Node
  test harness covers six cases; all pass.

- **Grape Resonances — four findings from live testing worth recording.**
  *(i) Multi-grape responses are the default, not the exception.*
  Strong-recurrence (single-grape) requires the matcher to land ≥3
  same-signature regions in the top-5, which is rare because the
  matcher ranks by temperament narrative — independent of grape
  distribution. All three Planning Doc worked examples returned
  multi-grape responses live: *falling deeply in love* → Pinot Noir ·
  Furmint · Chardonnay (Planning Doc predicted Pinot Noir alone);
  *the feeling of brotherhood* → Syrah · Pinot Noir · Riesling
  (Planning Doc predicted Grenache · Gamay · Shiraz); *decision about
  the move across the country* → Cabernet Sauvignon · Merlot (Planning
  Doc predicted Riesling · Chenin · Furmint threshold whites). The
  framework's actual readings are interpretively richer than the
  doctrinaire predictions — brotherhood reads as cross-cultural
  conviction (Walla Walla / Barossa / Burgundy / Pfalz / Finger Lakes),
  falling-in-love as facets-of-love (devotion / melancholy / obsession /
  awakening / sentimentality), decision-about-move as new-world
  ambition. *(ii) Validation moment — Furmint convergence on "late
  summer".* An independent Claude with no Vinotheca context, asked to
  identify grape varieties resonant with the same four metaphors,
  returned Furmint as primary for late summer — same as the framework's
  reading, on the same grounds (Tokaj's late-harvest patience, the
  knowing-it-will-become-something-else quality). Two different
  reasoning paths converging on the same answer is real evidence that
  the region narratives carry semantic temperament that survives
  embedding and ranks correctly. *(iii) Defensible disagreement, not
  defect.* On the other three metaphors, the independent Claude reached
  for grape character (Riesling for falling-in-love's slow reveal,
  Nebbiolo for decision-deliberation, Tempranillo for brotherhood's
  long shared meal); the framework reached for regional temperament.
  Both readings are honest; they're different lenses on the same
  domain. The framework's job is to render Soul of Wine's reading, not
  to be the most comprehensive wine-character argument. *(iv) One
  genuine matcher miss to log: Piedmont/Nebbiolo for decision-about-
  move.* The independent Claude's Nebbiolo argument was strong (the
  rose-and-tar contradictions, the long deliberation, the resolution
  arriving in bottle), and Piedmont didn't surface in the framework's
  top-5 — its Soul of Wine metaphor "Philosophy" didn't trigger on
  the move-decision query. Either Piedmont's narrative didn't carry
  the philosophy metaphor through to embedding space, or the
  embedding model reads "decision about move" as practical
  reinvention (Napa, Columbia Valley) rather than philosophical
  deliberation. Worth re-reading Piedmont's narrative against
  decision-shaped queries in a future Soul of Wine revision pass.

- **Grape Resonances documentation deferred.** The four PDFs (Summary,
  Methods Primer, Technical Appendix, Data Appendix) per §4.5's
  canonical framework are not yet authored. The Header.jsx Documentation
  dropdown surfaces the menu items as scaffolding (the menu's presence
  signals the leaf follows §4.4 Tool pattern), but four of five hrefs
  currently 404. The fifth — Region Profiles — Identity — cross-links
  to Soul of Wine's existing layer1-descriptions.pdf and works. PDFs
  to be authored in a follow-up session using the shared
  `vinotheca-preamble.tex` LaTeX template, mirroring the Region
  Resonances PDF set.

- **Winemaker section architecture clarified — three leaves planned
  across Works, Correspondence, and Personal Codex.** A brainstorming
  session reframed the winemaker work in the context of §4.12's
  character-mediated association principle. The earlier conception
  (a single Work in Works, based on the April 2026 *Vigneron Kinship*
  framework) is replaced by three coordinated leaves: Winemaker
  Affinities + The Hand of Wine (Works, §6.2), Winemaker Resonances
  (Correspondence, §6.4), and Codex Vinitorum (Personal Codex, §6.5).
  The Works leaf and the Correspondence leaf share their load-bearing
  asset (winemaker character profiles); the Personal Codex leaf is
  sealed from both per the Library/Codex independence rule. Decisions
  captured: §4.12 extended to cover the case where the surface object
  itself carries character (Case 2 — winemakers); the
  Body/Soul/Constellation Study triptych renamed to Body/Soul/Hand
  for grammatical alignment across the three Study faces (Body of
  Wine, Soul of Wine, The Hand of Wine); the third Correspondence
  leaf named Winemaker Resonances per the Region/Grape pattern; the
  second Personal Codex leaf named Codex Vinitorum.
- **`FRAMEWORK_NOTES.md` created.** A separate companion document at
  the vinotheca repo root, holding the conceptual scaffolding for the
  general framework underlying Vinotheca's architecture
  (character-companion frame, mediation-layer architecture, structural
  distinction from general-purpose LLM tools, strategy for
  build-then-validate-then-generalise). The document is explicitly
  conditional on Vinotheca's completion and validation; it is not a
  plan and is not an active task. Pointer added to §4.12 closing
  paragraph. A separate *Limitations and known objections* section
  was added to the file capturing the strongest academic objections
  (Forer-effect critique, projective-with-transparency nature of the
  mediation layer, resolution mismatch with empirical preference
  science, wine-domain reliability findings, generalisability
  question, and the metaphysical weight of the "carries temperament"
  claim) and reframing the framework's overall posture in the more
  modest register those limitations justify: the framework is an
  instrument design, not an empirical claim about how minds work.
  The eventual polished home for these ideas remains the Reference
  section's *Theoretical Foundations of Character-Based Analysis*
  document; `FRAMEWORK_NOTES.md` is where the formulation develops in
  the meantime.

### 2026-05-10

- **Grape Resonances — `cluster_framings.json` authored and validated.**
  §6.3 sub-item 3 closed. All ten framings drafted: six bullseye
  framings (one per Soul of Wine cluster, used when matched regions
  fall predominantly in one cluster) plus four prism framings (used
  when matched regions span multiple clusters). The bullseye set is a
  synthesis between the Planning Doc's example framings and a blind
  redraft against the canonical cluster metaphor lists in
  `layer1-narratives_6_34_57_AM.json`. Three Planning Doc framings
  locked verbatim where they were already at landing strength (Old
  World Interior's *patient, custodial cultures ... keeper, not a
  maker*; Against the Odds' *cultures of endurance ... difficulty is
  the substance*; New World Reinvention's *conviction-without-evidence
  ... decided they should exist*). Three Planning Doc framings
  synthesised with blind drafts to better fit the actual cluster
  diversity (Outward Ease broadened from *communal* to also include
  the market and the gathering, so the framing accommodates Marlborough's
  Assertion and Veneto's Commerce alongside Beaujolais's Joy; Old
  World Exterior recast from *institutional* to *cultures of inheritance*
  so the framing accommodates Pfalz's Warmth and Dalmatian Coast's
  Tranquility alongside Bordeaux's Business; The Moderates recast from
  *cultures of equilibrium* to *cultures of found voice* so the
  framing accommodates the 15-metaphor diversity from Tuscany's Art
  to Wachau's Monumentality without forcing all 15 into a single
  *equilibrium* claim). Four prism framings drafted: a general
  refraction case plus three specific cluster dyads identified as
  likely common refractions (interior+reinvention, difficulty+ease,
  interior+moderate). Held locally as
  `grape-resonances/working_files/cluster_framings.json` alongside
  the other two authored files. **All Grape Resonances authoring
  work is now complete.** The remaining four §6.3 sub-items are
  engineering: aggregator + coherence detector, React app scaffold,
  test, deploy. Per the Planning Doc's original estimate, this is
  ~2 working days of work remaining.
- **New family-level architectural principle locked: §4.12
  Region-mediated association.** A conversation that began as a check
  on the Grape Resonances design surfaced what may be the most
  generalisable insight of the Soul of Wine project. The principle, in
  plain words: **the framework refuses any direct claim between
  feelings and surface-level objects, and instead mediates every such
  claim through an intermediate cultural layer that genuinely carries
  temperament.** In Vinotheca's wine domain that intermediate layer is
  regions; regions are the kind of thing capable of having
  temperament. Surface-level objects (grapes, foods, music, writers)
  are surfaced by association from the intermediate layer, never by
  direct embedding against feelings. The principle generalises: any
  object class genuinely rooted in regional culture can be derived
  from the same matching engine by adding one more region-to-object
  association file plus a thin authored layer of object narratives.
  The 59 region narratives become the load-bearing asset of Vinotheca,
  reusable across all present and future Correspondence leaves; the
  marginal cost of a new leaf is curation of one new association
  table. Recorded as §4.12 with five practical consequences listed
  (load-bearing-regions, marginal-cost curation files, separate
  object narratives, reusable engine, disqualification criteria for
  candidate leaves). The principle was articulated by Jure in
  conversation while reviewing the falling-in-love worked example
  during the Grape Resonances build, and is now permanent record at
  the family level rather than only inside the Grape Resonances
  Planning Doc.
- **Grape Resonances — `grape_narratives.json` authored and validated.**
  §6.3 sub-item 2 closed. All 101 canonical grape narratives drafted
  across ten batches in a single session, following the blind-drafting
  methodology locked earlier today. The breakdown: 53 reds (Aglianico
  through Zweigelt) across batches 1–5; 48 whites (Albariño through
  Welschriesling) across batches 6–10. Four entries are the canonical
  exemplars locked in the Planning Doc and included verbatim (Pinot
  Noir, Aligoté, Furmint, St. Laurent). Voice register: trace-fold
  Soul of Wine — region-tethered, character-first, semicolon-split,
  ~25 words median (soft range 19–28; some entries 29–31 where
  compression would distort character). Methodology validated as
  intended: a first batch was initially drafted under defensive
  cross-referencing discipline, found to be contorted, and redrafted
  blind; the blind version was approved without changes and the
  methodology held for the remaining nine batches. Four mid-batch
  revisions captured genuine encyclopaedia-register intrusions that
  the methodology had missed (Petite Sirah's "properly Durif"
  parenthetical, Sagrantino's "DOCG" acronym, Friulano's EU-renaming
  aside, Trebbiano's "as Ugni Blanc for Cognac" parenthetical) — these
  led to a documented self-check rule against ampelographic asides for
  future batches. Review pass after completion ran a content-word
  recurrence diagnostic across all 101 entries and found 342 echoes,
  of which the large majority were factual repetition (Bordeaux,
  Burgundy, thin-skinned, late-ripening, etc., per the methodology's
  accept-factual rule), plus several genuine pattern findings
  (1970s-rescues, human-crossings, volcanic-terroirs) preserved as
  signal rather than edited away. Six word-level stylistic echoes
  warranted revision: *workhorse* (kept for Petite Sirah; revised
  away from Tinta Roriz, Ugni Blanc), *wall* (kept for Sagrantino;
  revised away from Tannat), *spine* (kept for Assyrtiko; revised
  away from Blaufränkisch), *quiet* (kept for St. Laurent per the
  locked exemplar; revised away from Chasselas, Silvaner). The
  first-round revisions of Tinta Roriz and Blaufränkisch introduced
  two new echoes (*contributor*, *iron*) caught by re-running the
  diagnostic and corrected with a second round. Final file holds 101
  entries with metadata block documenting schema version, voice
  anchors, methodology pointer, and scope statement. Held locally as
  `grape-resonances/working_files/grape_narratives.json` alongside
  `region_grapes.json` and the Planning Doc until the dedicated
  Grape Resonances repo is scaffolded.
- **Grape Resonances — four architectural decisions locked, Planning
  Doc updated.** Working through the end-to-end pipeline together
  surfaced four under-resolved questions in the Planning Doc; all four
  now have locked answers. *(1) Where do grape narratives surface in
  v1?* — trace fold only, not the default oracle response. The default
  response keeps its line-150 form (grape names + framing sentence +
  verification + collapsed trace), preserving the §4.11 compression
  principle. *(2) What is the v1 default response shape, exactly?* —
  exactly the Planning Doc's line 150 form, now marked locked. The
  earlier (now-revised) wording on Planning Doc line 102 that suggested
  narratives appeared in the default response was a contradiction; the
  contradiction is resolved in favour of compression. *(3) What does the
  trace fold contain?* — a grape-organised layout: each response-grape
  shown with its narrative (from `grape_narratives.json`), a list of
  contributing matched regions (region name + similarity score + the
  region's locked Soul of Wine cluster metaphor), and a one-sentence
  interpretive close drawn from response templates (bullseye-single-
  grape / multi-grape-bullseye / prism). The cross-link to Region
  Resonances closes the fold. This closes Planning Doc open question
  5. *(4) How does the aggregator turn matched regions into response
  grapes?* — by a "recurrence as finding" rule: if one grape recurs as
  signature in ≥3 of N matched regions, return that grape alone and
  name the recurrence in the framing; if 2–4 grapes recur in ≥2 regions
  each, return those; if no grape recurs, return the top 2–3 grapes by
  similarity-weighted score and name the prism. Validated against the
  worked example "falling deeply in love" — Pinot Noir as signature in
  3 of 5 matched regions, returned alone with the three cluster
  metaphors (devotion / idealism / patient continuation) doing the
  framing work. Confirms v1 uses Tier 1 (`signature`) only, closing
  Planning Doc open question 6. The four decisions are recorded in
  `Grape_Resonances_PlanningDoc.md` as three new "locked 2026-05-10"
  subsections plus two open-question closures. PROJECT.md §6.3
  sub-item 4 amended with a parenthetical pointer to the aggregator
  selection rule.
- **Grape Resonances — `grape_narratives.json` scope and methodology
  decisions locked.** Two related decisions captured ahead of authoring
  work beginning. *Scope decision:* `grape_narratives.json` covers the
  canonical 101 grapes from Body of Wine / Grape Affinities, not the
  293-grape universe of `region_grapes.json`. Reason: oracular responses
  must surface grapes the user can plausibly drink; deep-cut varieties
  curated as `temperament_seconds` for specific regions (Pinela, Canaiolo,
  Pineau d'Aunis, Frühroter Veltliner, Babić, and others) carry real
  framework signal but exceed the wine-curious user's reachable set. The
  larger 293-grape curation in `region_grapes.json` remains valid as
  data; the aggregator (§6.3 sub-item 4) will surface only grapes in the
  canonical 101 in user-facing output, with the deeper layer available
  to v1.1 or v2 if warranted. *Methodology decision:* `grape_narratives.json`
  is authored via *blind drafting* — each grape narrative written without
  reference to previously drafted entries, so that vocabulary serves the
  grape rather than differentiation from the prior batch. The reasoning
  is recorded in `Grape_Resonances_PlanningDoc.md` (new subsection
  *Authoring methodology — blind drafting*). The methodology was adopted
  after an initial batch drafted under cross-referencing discipline was
  found to be contorted; a blind-draft redraft of the same batch produced
  more natural prose without manufacturing differentiation. PROJECT.md
  §6.3 sub-item 2 updated with a parenthetical pointer to the methodology.
- **Grape Resonances — `region_grapes.json` curated and validated** —
  §6.3 sub-item 1 closed. For each of the 59 Soul of Wine regions, four
  fields populated: signature (1–4 grapes), lesser_known (3–7 grapes),
  rare (0–4 grapes), temperament_seconds (0–1 grapes, drawn from
  lesser_known). 59 of 59 regions complete across four curation sessions
  (10 / 5 / 17 / 27 regions per session); subset rule
  (`temperament_seconds` ⊆ `lesser_known`) clean throughout; 4 regions
  with empty temperament_seconds (Beaujolais, Marlborough, Central
  Otago, Wachau) on narrative grounds — single- or two-grape regional
  assertions where signature *is* the identity. One mid-session
  amendment to a previously-closed region: Provence's Cinsault moved
  from `signature` to `lesser_known` to honour the subset rule, with
  Grenache becoming Provence's sole signature. Six same-grape-across-
  regions patterns documented for the aggregator (Cabernet Franc 3×,
  Sémillon / Semillon 3×, Zinfandel / Cinsault / Grenache / Syrah 2×
  each); spelling normalisation between Sémillon (French / Spanish-
  speaking regions) and Semillon (Australian convention) noted as
  intentional regional spelling. Companion deliverable note:
  `Grape_Resonances_CurationState.md`. The file is ready to drop into
  the `grape-resonances` repo's `public/data/` when the React scaffold
  is built (§6.3 sub-items 5–6).
- **Pass 3 closed** — §6.3 (Pass 3 — visual harmonisation) retired
  from open items. Nine of nine palette-bearing surfaces are now at
  family canonical alignment for palette and tokens; six Decisions
  resolved; four deferred Questions answered. The Vinotheca family is
  visually coherent across its full surface area.
- **Pass 3 Tier 3 (Tasterank Explorer) shipped** — the final
  execution piece. Token system introduced from scratch (canonical
  10-token `:root`); 15 wine references, 9 paper references, 8
  border references, and 6 raised-panel `#fff` backgrounds replaced
  with `var()` references; 3 high-contrast `#fff` preserved.
  Typography per Decisions 5 and 6: display font DM Serif Display →
  Cormorant Garamond (7 uses); body font DM Sans **preserved** (12
  uses) as the family's only instrument-class register signal.
  Tasterank Explorer is now the only leaf with the Cormorant Garamond
  + DM Sans combination — visibly within the family, register
  distinct. Commit `8c4f0ce` in `tasterank-explorer`.
- **Tasterank Explorer LICENSE attribution fix** — first line corrected
  from "TasteRank Explorer" to "Grape Affinities" to match the leaf's
  display name (the leaf was renamed earlier in the project; LICENSE
  was missed). Small clean-up commit immediately after the Tier 3
  ship.
- **Wine Atlas circular-reference fix** — yesterday's Wine Atlas Tier
  3 commit (`2617c76`) shipped with two circular references in `:root`
  (`--wine: var(--wine);` and `--border: var(--border);`) introduced
  by an over-eager sed substitution that caught the values inside the
  `:root` declaration as well as their references in the body of the
  file. The bug silently broke wine-red and border rendering across
  the page — every `var(--wine)` reference resolved to inherited
  near-black; every `var(--border)` to currentColor. Caught this
  morning when preparing Tasterank Explorer Tier 3 (the same sed
  pattern would have produced the same bug; visual verification of
  the `:root` block during prep caught it). Fix shipped as commit
  `64e839e` in `grand-cru-atlas`. Lesson recorded: *post-edit visual
  verification of the `:root` block is mandatory after sed
  substitutions; counting hex occurrences is not enough*.

### 2026-05-09

- **Pass 3 Tier 3 — Wine Atlas (Grand Cru Atlas)** — the most
  substantial single visual change of Pass 3. Token system introduced
  from scratch (no prior `:root` block) with the canonical 10-token set
  (`--wine`, `--wine-dark`, `--wine-light`, `--paper`, `--paper-raised`,
  `--paper-deep`, `--ink`, `--ink-soft`, `--ink-muted`, `--border`).
  Hard-coded values across the file replaced with `var()` references:
  15 wine-red occurrences, 8 paper backgrounds (revalued from drift
  `#FAF8F5` to canonical `#FAF6F1`), 7 borders, 4 raised-panel `#fff`
  backgrounds (panel, search-results, reset-btn, atlas-footer);
  4 `#fff` preserved for high-contrast use cases (button hover text,
  SVG icon, hover state, map marker border for legibility against
  varied map tiles). Typography migrated per Decisions 5 and 6: DM
  Serif Display → Cormorant Garamond (3 display uses); DM Sans → EB
  Garamond (7 body uses). Google Fonts `<link>` tag updated. Grape
  variety category colours in the JS data structure preserved unchanged
  (domain content, not style); local one-off decorative colours
  (`#a86259` fleuron, `#d4a89a` button border, `#fdf6f0` reset-bar)
  and local greys (`#222`–`#999`) preserved as too-local to deserve
  canonical tokens. Eight of nine palette-bearing surfaces now
  aligned. Wine Atlas now reads as a sibling volume to Estate Atlas.
  Commit `2617c76` in `grand-cru-atlas`.
- **Pass 3 PDF naming convention** — divergent PDF naming across the
  family resolved. Tasterank Explorer's five PDFs renamed from
  `TasteRank_Title_Case_With_Underscores.pdf` to
  `lowercase-with-hyphens.pdf` (canonical pattern matching Soul of
  Wine's existing convention). Coordinated commits across two repos:
  `tasterank-explorer` (rename PDFs in `docs/`, update 5 links in
  `index.html` Documentation dropdown, update README files table —
  including adding the previously-missing Methods Primer row), then
  `body-of-wine` (update 5 cross-repo links in `index.html` doc cards
  and 5 in `README.md` docs table). Brief ~30-second window of 404s
  on Body of Wine's doc-card links between the two pushes; acceptable
  for a personal project, no redirects added. Naming map: `Summary` /
  `Technical_Appendix` / `Methods_Primer` / `Data_Appendix` /
  `Grape_Reference` → `summary` / `technical-appendix` /
  `methods-primer` / `data-appendix` / `grape-reference`.
- **Pass 3 follow-up: Estate Atlas display font alignment** —
  Cormorant → Cormorant Garamond per Decision 6 (Question D resolved).
  17 font-family references in CSS plus the Google Fonts `<link>` tag
  URL parameter. Estate Atlas's display font now reads in the same
  register as the rest of the Library. Single commit (`d855598`).
- **Pass 3 hard-questions session** — Decisions 5 and 6 resolved,
  closing the four deferred questions (A, B, C, D) that the original
  PASS3_SPEC.md flagged. **Decision 5**: body fonts are
  artefact-class-distinguished — Reading work (parent + atlases +
  reference) uses EB Garamond, Studies use Source Sans 3,
  instrument-class Tools use DM Sans, Personal Codex uses DM Sans as
  Part-II signature. **Decision 6**: display fonts unify the family
  (Cormorant Garamond family-wide), so display = family identity, body
  = register. The two-axis system avoids the family fragmenting
  visually while preserving meaningful class distinctions. Codex Vini
  required no changes — its existing fonts already implemented Stance X
  correctly. Wine Atlas Tier 3 work now includes typography migration
  (DM Serif Display + DM Sans → Cormorant Garamond + EB Garamond);
  Tasterank Explorer Tier 3 includes display-only migration (DM Serif
  Display → Cormorant Garamond) with DM Sans body preserved as
  instrument-class signal. Estate Atlas's "Cormorant" → "Cormorant
  Garamond" becomes a small follow-up commit. Spec updated to mark
  Questions A–D as resolved.
- **Pass 3 React execution** — the two React leaves (Region Affinities,
  Region Resonances) brought into family-canonical alignment for paper
  tokens. Both `tailwind.config.js` files updated: `parchment.DEFAULT`
  changed from `#FAF7F2` to `#FAF6F1` (one hex unit, family
  canonical); new `parchment.raised: #FFFDF8` added as the Tailwind
  equivalent of `--paper-raised`. Wine and ink palettes unchanged
  (already canonical). The two files differ only in the deliberate
  header comment block in `region-resonances/app/tailwind.config.js`
  noting that it tracks `region-affinities/tailwind.config.js`. Build
  pipeline: GitHub Actions (Vite); ~1–3 min deploy each. Seven of
  nine palette-bearing surfaces now aligned. Remaining: 2 Tier 3
  leaves (Wine Atlas, Tasterank Explorer) — gated on the hard-
  questions session per PASS3_SPEC.md.
- **Pass 3 Tier 2 executed** — the parent Vinotheca and Estate Atlas
  brought into family-canonical alignment. *Vinotheca*: token
  `--accent` (`#6a2430`) renamed to `--wine` (`#7B2D26`) with global
  find-replace across 25 uses; `--accent-soft` (`#8a3240`) renamed to
  `--wine-light` (`#A04038`) across 4 uses; `--paper` (`#f6f1e8`)
  changed to `#FAF6F1`; `--wine-dark` and `--paper-raised` added.
  *Estate Atlas*: `--wine` (`#6e1f2a`) → `#7B2D26`; `--paper`
  (`#f5efe6`) → `#FAF6F1`; `--wine-dark` and `--paper-raised` added.
  **Corrections from PASS3_SPEC.md original draft**: Estate Atlas had
  a `--wine-soft` token not documented in the spec, renamed to
  `--wine-light` with simultaneous value change (3 uses);
  `--pin-shadow` rgba updated to track the new wine value;
  Estate Atlas's "Cormorant" display font (17 deliberate uses, not
  a typo as originally assumed) deferred to a new Question D in the
  spec, alongside the existing three deferred hard questions. Both
  changes meaningfully visible — the parent's warm-yellow paper
  becomes the family-canonical neutral cream; Estate Atlas's
  slightly cooler wine becomes the canonical. Five of nine surfaces
  now aligned; remaining: 2 React leaves + 2 Tier 3 leaves.
- **Pass 3 Tier 1 executed** — three of nine palette-bearing surfaces
  brought into family-canonical alignment for paper tokens.
  *Body of Wine* (`f8e23b0`): renamed `--cream` → `--paper`, added
  `--paper-raised: #FFFDF8`, switched five raised-panel backgrounds
  from `var(--white)` to `var(--paper-raised)`. *Soul of Wine*
  (`c578109`): identical token-system changes, kept byte-identical to
  Body of Wine; differs only in number of raised-panel uses (seven,
  not five — Soul of Wine has more card sections). *Codex Vini*
  (`cbcd2d8`): single value swap `--paper: #FAF6EF` → `#FAF6F1`. The
  Studies' `--white` token preserved for one specific use each (the
  "Open PDF" button text — high-contrast white on wine-red,
  explicitly preserved per PASS3_SPEC.md Decision 3). Per
  PASS3_SPEC.md, six leaves remain (Tier 2: Vinotheca + Estate Atlas;
  React: Region Affinities + Region Resonances; Tier 3: Wine Atlas +
  Tasterank Explorer).
- **Pass 3 Phase 2 spec written** — the visual-harmonisation work
  unblocked by the Body of Wine deploy was scoped, harvested, and
  partially decided in a single session. All nine palette-bearing
  surfaces (eight leaves plus the parent) were inventoried for wine
  red, paper cream, raised-panel surfaces, and fonts. Four decisions
  were locked in (canonical wine `#7B2D26`; canonical paper `#FAF6F1`;
  universal `--paper-raised: #FFFDF8`; rename Vinotheca's `--accent`
  to `--wine`). Three hard questions deferred (body font, atlas
  distinctness, Codex differentiation depth) plus the PDF naming
  convention. The full spec lives in `PASS3_SPEC.md`; PROJECT.md §6.3
  now points at it. Execution remains for future sessions, scoped at
  three Tier 1 + two Tier 2 + two React + two Tier 3 + one hard-
  questions session + one PDF naming session.
- **`documents_old/` folders deleted** — the gitignored rollback safety
  nets in `tasterank-explorer/` (5 PDFs) and `region-resonances/`
  (2 PDFs) were `rm -rf`'d locally after confirming the live docs in
  both repos work end-to-end. PROJECT.md previously listed three repos
  with `documents_old/` folders; in fact `region-affinities/` never
  had one. Closes the cleanup task tracked as §6.4 in v0.5.
- **The Body of Wine deployed** — the Study face of the Grape similarity
  Work is now live at `https://jskarabot18.github.io/body-of-wine/`,
  completing the first Work in the family with both faces live (Grape
  Affinities Tool + Body of Wine Study). The Study is written in the
  voice of Soul of Wine: question, three findings, why this matters,
  documents, method. The page is a structural sibling to Soul of Wine
  but five body sections rather than six — Soul of Wine's "Beyond Wine"
  cross-disciplinary section was deliberately not replicated, since
  Body of Wine makes a single-system network claim rather than Soul of
  Wine's two-systems-disagree claim. Repo: `body-of-wine` at root of
  `~/Documents/jure/wine/`. Three files: `index.html`, `LICENSE` (CC
  BY-NC 4.0, copied from Soul of Wine), `README.md`. CSS character-for-
  character matches Soul of Wine, per §4.7's loose reading (don't
  redesign now, save the redesign for Pass 3 with both studies in view).
- **Parent catalogue updated** — the Body of Wine face card on the
  Works subsection went from "In preparation" placeholder to a live
  link, mirroring Soul of Wine's pattern. The Grape Work's body text
  was also rewritten so it describes the Study's actual claim (network
  reading, three findings) rather than the false-parallel framing the
  earlier draft carried over from the v0.4 session.
- **Tasterank Explorer PDFs reorganised** — the five PDFs were moved
  from the repo root into `tasterank-explorer/docs/` to match the
  family pattern (Soul of Wine ships PDFs in `docs/`). The five
  internal links in `tasterank-explorer/index.html`'s Documentation
  dropdown were updated in the same commit. This was prerequisite
  groundwork for Body of Wine, which links to those PDFs cross-repo.
- **Parent catalogue restructured to match §1 architecture** — the
  parent Vinotheca page's Tools and Studies subsections were merged
  into a single **Works** subsection, with three Work entries each
  showing both faces side by side: *The Body of Wine* (Grape Affinities
  live + study to be built), *The Soul of Wine* (Region Affinities live
  + Soul of Wine live), *The Winemaker's Constellation* (Winemaker
  Affinities and the Constellation, both forthcoming). New `.work`,
  `.work-faces`, and `.work-face` CSS classes implement the paired-card
  pattern; the existing `.instrument` pattern is retained for unpaired
  entries (Maps, Correspondence, Codex). Closes the active task that
  was tracked as §6.1 (move Region Resonances from Tools to
  Correspondence) by completing the deeper restructure that task
  pointed at.
- **Region Resonances moved from Tools to Correspondence** — eyebrow
  changed from `A Tool of Vinotheca` to `A Correspondence of Vinotheca`
  in `app/src/components/Header.jsx`. The repo name stays
  `region-resonances` (working name, per §3 — repo names are
  infrastructure). Region Resonances is now the founding member of
  the Correspondence subsection on the parent, sitting alongside
  Grape Resonances (forthcoming, §6.6).
- **"The Body of Wine" adopted as working title** for the unbuilt
  Grape Affinities study, completing the triptych of study titles
  (Body / Soul / Constellation) — each naming a way of seeing wine:
  through the senses, through cultural identity, through the character
  of those who make it. Title is open to revision until the Study is
  written.
- **Catalogue numerals renumbered i–viii** (was i–ix) — three pairs
  collapsed into three Works.
- **Introduction prose and Part I description rewritten** to enumerate
  the four-section architecture (atlases / works / correspondence /
  record) instead of the old Tools-and-Studies-and-Codex three.

### 2026-05-08

- **Soul of Wine brought into conformance with §4.6** — the "Interactive
  Tools" section was removed from Soul of Wine's `index.html`, along with
  the corresponding "Explore" entry in the in-page nav. The four
  superseded prototype HTML files (`cluster-explorer.html`,
  `cluster-map.html`, `movement-map.html`, `d-score-dashboard.html`) were
  deleted from `soul-of-wine/visualizations/`. A single contextual prose
  link to Region Affinities was added to the "Why This Matters" intro
  paragraph. Closes the active task that was tracked as §6.1.
- **PROJECT.md created** — canonical project state document, this file.
- **Documentation source archival** — `docs-source/` folder added to each
  of the three tool repos (region-affinities, region-resonances,
  tasterank-explorer) containing the `.tex` sources and shared preamble.

### 2026-05-07 to 2026-05-08

- **Pass 2 — naming and structural decisions**:
  - Step 1: TasteRank Explorer renamed to Grape Affinities (wordmark and
    page title; repo name unchanged)
  - Step 2: Soul of Wine "Source-available and free…" disclaimer removed;
    Documentation dropdown unified to single-line entries on Grape Affinities
  - Step 3: Eyebrow standardisation across all seven leaves to "X OF
    VINOTHECA" grammar
  - Step 4: Documentation menu placement on atlases — decided to keep
    single PDF button (atlases ship one consolidated PDF)
  - Step 5: Wordmark font alignment on Grand Cru Atlas (DM Serif Display
    → Cormorant Garamond, matching Estate Atlas and the Library)

### 2026-05-06 to 2026-05-07

- **Pass 1 — mechanical text consistency** across five repos:
  - License link fixed in Region Affinities and Region Resonances footers
  - *Atlas* italicised in Grand Cru Atlas wordmark
  - Soul of Wine motto fleurons + footer link reorder + "Region Profiles"
    renamed to "Region Reference"
  - Codex Vini motto fleurons in header and footer

### 2026-05-05 to 2026-05-06

- **Documentation alignment** across the three tools to canonical framework
  (Summary, Technical Appendix, Methods Primer, Data Appendix, optional
  Reference). 13 PDFs produced and deployed; `Header.jsx` updated for the
  React tools.

---

## 8. Document changelog

Append a new entry whenever PROJECT.md is updated. Newest at the top.

### 2026-05-14 — v0.29

- **§3 (Leaves table).** Codex Vinitorum row updated to reflect the
  shipped state: repository name changed from `*(tbd)*` to
  `codex-vinitorum`, status changed from `Planned — see §6.5` to
  `Live`. No other rows touched.
- **§6.5 (Codex Vinitorum).** Section heading changed from
  *To be built — Codex Vinitorum (second Personal Codex leaf)* to
  *Built — Codex Vinitorum (closed 2026-05-14; recorded in §7)*, in
  line with the §6.3 Grape Resonances pattern for shipped leaves.
  Corpus reference updated from "29 winemakers" to "35 winemakers
  from the existing Winemaker's Compass (v6)" reflecting the current
  Compass size. A *Live at* line added immediately under the intro
  pointing to the deployment URL and repository. The two locked
  blocks (Architectural rule, Affinity signals) preserved verbatim
  as durable records of the decisions that shaped the leaf. A new
  *Bio register* block added below the Affinity signals block,
  recording the factual encyclopedic register the bios were written
  in and the light-edit derivation from the Compass; the block also
  acknowledges the working-content stance for bios that contain some
  inference and may need refinement as new information surfaces. The
  *Pending* list replaced with a *Built (2026-05-14)* block
  describing the shipped scope: Codex Vini sibling structure (Book /
  Atlas / Collection), three signal-specific columns in The Book,
  uniform pins on The Atlas honouring the no-ranking commitment, and
  the launch-day signal distribution (19 of 35 marked; rarity
  hierarchy held). The block points to the §7 entry for the full
  multi-day arc and follow-up refinements.
- **§7 entry under 2026-05-14.** New entry inserted at the top of
  the 2026-05-14 day (above the existing Grape Resonances Data
  Appendix entry). The entry records the multi-day arc that
  produced Codex Vinitorum: the 2026-05-11 rearchitecture, the
  signals workbook authored mid-week (including the small
  ranking-trap caught during its design — proposing 0–3 fleurons
  coloured by count would have re-introduced ranking; the fix was
  uniform colour with positional ordering), the five-stage build,
  the bio-register discipline, the three-step GitHub Pages
  deployment fix (stale `github-pages` environment from accidental
  GitHub Actions source setting; resolved by environment deletion
  and `.nojekyll` push), and the follow-up refinements done the
  same day (three-column signal display, popup auto-pan, scroll-
  wheel zoom). The signal distribution observed the predicted
  rarity hierarchy: memorable encounter most common (10),
  felt close to (8) and stayed with me (7) more selective.

This v0.29 entry is the most substantive Codex change in several
days. It records the launch of the second Personal Codex leaf —
sibling to Codex Vini and sealed from the Library per the §6.5
architectural rule — and completes the Personal Codex section of
the Vinotheca family. No structural changes to PROJECT.md beyond
§3, §6.5, §7, and this changelog entry.

### 2026-05-14 — v0.28

- **§6.6 (Atlas wordmark renames — deferred).** New sub-block
  appended at the end of §6 recording a locked-but-not-executed
  naming change for the two atlases in Maps. Grand Cru Atlas $\rightarrow$
  Vineyard Atlas and Estate Atlas $\rightarrow$ Maker Atlas. The renames
  affect only the displayed wordmarks and catalogue-side naming;
  the GitHub repository names (`grand-cru-atlas`, `estate-atlas`)
  and deployment URLs stay unchanged. The block records the
  rationale (the current names break the family's
  `{Subject} {Operation}` pattern; *Grand Cru* names a prestige
  tier rather than a subject; *Estate* doesn't visibly anchor
  what the atlas catalogues), the Maker Atlas semantic distinction
  (maker is broader-scope than winemaker, completing the subject-
  across-operations matrix while the section-heading context
  disambiguates entity from person), the mechanical-text scope
  when execution arrives (paralleling the TasteRank Explorer
  $\rightarrow$ Grape Affinities rename pattern), and the queued
  status (low urgency, no deadline).

This v0.28 entry is a forward-looking decision record, not a
structural or executed change. No §3, §4, §6.1–6.5, §7 entries
were modified. The atlases continue to ship as *Grand Cru Atlas*
and *Estate Atlas* until the rename is executed in a future
session.

### 2026-05-14 — v0.27

- **§7 entry under 2026-05-14.** New date subsection inserted at the
  top of §7. One substantive entry recording the Grape Resonances
  Data Appendix sanity-check pass and the deployment of v1.1. Six
  sub-paragraphs cover: substantive findings (the four factual
  errors — Bordeaux signature missing Cabernet Franc, Northern Rhône
  signature missing Viognier, Paso Robles temperament-seconds
  misnamed as Mourvèdre when the live data has Grenache, and the
  §G.3 Sémillon conflation that missed the intentional regional
  spelling distinction); cosmetic findings (seven parenthetical-
  disambiguation differences in display forms); corrections applied
  (all 11 findings landed via str_replace edits, document recompiled,
  §G.3 intro rewritten to explain the Sémillon/Semillon spelling
  distinction, PDF grew from 9 to 10 pages); unaffected documents
  (Summary, Methods Primer, Technical Appendix are unchanged because
  they don't contain per-region or per-grape data); and a method
  observation worth recording for future canonical PDF authoring
  (diff against the live data file before shipping, even when
  past-chat reconstruction looks comprehensive).

This v0.27 entry resolves the sanity-check caveat logged in the
2026-05-13 §7 entry. No structural changes to PROJECT.md; no §4 or
§6 sections changed. The substantive record is the §7 entry; the
§6.3 block's "documentation closed 2026-05-13" heading remains
accurate (the four canonical PDFs were authored and deployed on
that date; the v1.1 Data Appendix correction is a follow-up
revision within the closure rather than a new closure event).

### 2026-05-13 — v0.26

- **§6.3 (Grape Resonances built block).** Section heading updated
  from *closed 2026-05-11* to *closed 2026-05-11; documentation
  closed 2026-05-13*. A new closing paragraph appended noting that
  the four canonical PDFs per §4.5 (Summary, Methods Primer,
  Technical Appendix, Data Appendix) were authored and deployed in
  the 2026-05-13 session, that the Documentation dropdown now
  resolves all four entries plus the existing cross-link to Region
  Profiles — Identity, that the LaTeX sources are archived alongside
  the family's other 12 source files (bringing the family LaTeX
  corpus to 13), and pointing to the §7 entry for the authoring
  methodology and v1 caveats.
- **§7 entry under 2026-05-13.** New date subsection inserted at the
  top of §7. One substantive entry recording the four-PDF closure,
  with five sub-paragraphs covering: authoring stance (the deference
  rule — defer matcher material to Region Resonances, spend depth on
  what Grape Resonances adds); per-document summary (page counts,
  section structures, anchor content for each of the four PDFs);
  source archive (the four .tex files added to docs-source/,
  bringing the family LaTeX corpus to 13); the sanity-check caveat
  logged for the next session (the Data Appendix's §F per-region
  signature table and §G.3 same-grape pattern table were assembled
  from past-chat fragments rather than the live JSON, and a diff
  pass against the four live data files is queued; the other three
  PDFs do not contain per-region or per-grape data and are not
  affected by the sanity-check scope); and family-state summary
  (both currently-live Correspondence tools and both currently-live
  Affinities-side Works tools now at four-PDF parity, with
  Winemaker Affinities, The Hand of Wine, and Winemaker Resonances
  identified as the next documentation work in this register).

This v0.26 entry is a documentation-closure recording rather than
a structural or design change. No §4 or §6 sections changed in
substance; the §6.3 amendment is a status update on a leaf already
marked Built. The §7 entry is the substantive record of the work.

### 2026-05-12 — v0.25

- **§4.3 (Footer canonical pattern).** New paragraph appended
  making the LICENSE-at-root convention explicit. The convention
  records that the file is named `LICENSE` (no extension, all
  caps) at the repo root, that GitHub's licence-recognition
  depends on this exact filename, and that the per-leaf header
  line follows the Codex Vini precedent. Adding this to §4.3 means
  it propagates by default to future leaves rather than being
  rediscovered each time a new repo is spun up.
- **§7 entry under 2026-05-12.** New date subsection at the top of
  §7. Two entries: (i) the LICENSE coverage closure — three repos
  (`region-resonances`, `grape-resonances`, `region-affinities`)
  brought from 0 to 1 LICENSE file each via three coordinated
  commits, all following the per-leaf header convention; the
  family is now at 10/10 LICENSE coverage. (ii) The
  `region-resonances` PLANNING.md and PROJECT.md archive move to
  `OLD_FILES/`, committed separately to keep the LICENSE addition
  cleanly isolated.

This v0.25 entry is light — the technical work was three single-
file commits, and the structural change to PROJECT.md is one
short paragraph in §4.3. The value is the codification: a small
omission that affected three of ten repos becomes a documented
family rule.

### 2026-05-11 — v0.24

- **§6.5 (Codex Vinitorum).** New locked block added — *Affinity
  signals (locked 2026-05-11)* — between the existing
  *Architectural rule (locked)* block and the *Pending* list. The
  block records that Codex Vinitorum entries carry three optional,
  orthogonal experience-side signals — *Felt close to*, *Memorable
  encounter*, *Stayed with me* — rather than a numeric rating. The
  block explains the design constraint (discomfort of rating people
  on a personal record), the rejection of numeric rating and
  single-binary alternatives, the orthogonality and user-side
  register of the three signals, and the quiet differentiation
  this creates between Codex Vini and Codex Vinitorum. The
  *Pending* list's entry-schema sub-item was amended to reference
  the locked decision.
- **§7 entry under 2026-05-11.** One new entry inserted at the top
  of the day (above the chip-registers entry): the Codex Vinitorum
  affinity-signals decision. The entry records the discomfort of
  rating people as the originating design constraint, the
  rejection of numeric-rating and binary-like alternatives, and
  the selection process for the three signals — including the
  late rewording of *Affinity* to *Felt close to* for grammatical
  register consistency with the other two facets. The entry also
  notes the broader framework alignment: the Codex marks
  experience, not worth.

This v0.24 is a light entry — no structural changes to PROJECT.md,
no §6 renumbering, no §3 leaves table changes. The decision
recorded here is purely architectural and concerns a leaf that
remains forthcoming (§6.5).

### 2026-05-11 — v0.23

- **§7 entry under 2026-05-11.** One new entry inserted above the
  Grape Resonances build entry (newest-first within the day):
  Correspondence chip registers refreshed for both Region Resonances
  and Grape Resonances. The entry records three findings: (i) chip
  register as a family design dimension, with Region Resonances
  shipping short adjective-led aesthetic-contemplative chips and
  Grape Resonances shipping long-form state-naming poetic-register
  chips; (ii) the shared-trio design path that was considered,
  briefly tested, and consciously discarded once register coherence
  trumped surface rhyme; (iii) live-use as the next validation step
  for the chip refresh, with future Correspondence leaves expected
  to consciously choose their own chip register.

This v0.23 is a light entry — no structural changes to PROJECT.md,
no §6 renumbering, no §3 leaves table changes. The shipped work
required two small commits (one per Correspondence leaf), editing
only the `EXAMPLE_QUERIES` array in each leaf's `InputPanel.jsx`.

### 2026-05-11 — v0.22

- **§3 leaves table.** Grape Resonances row updated from `Planned — see
  §6.3` to `Live`; repo column from `grape-resonances` (tbd) to
  `grape-resonances`.
- **§4.4 (Documentation menu).** Correspondence list phrasing tightened:
  Region Resonances and Grape Resonances are both named as the current
  live leaves, Winemaker Resonances still flagged as forthcoming.
- **§4.11 (Correspondence is oracular).** Closing paragraph: stripped
  the `(planned, see §6.3)` qualifier from the Grape Resonances mention,
  since the leaf is now live.
- **§6.3 collapsed to a tombstone.** The full To-be-built subsection
  removed; replaced by a short Built block pointing readers to the §7
  entry for build history, shipped architecture, and live-testing
  findings. The detailed Planning Doc lives at
  `grape-resonances/Grape_Resonances_PlanningDoc.md` and the worked-
  examples revision is recorded in §7. Subsequent §6 subsections
  (§6.4 Winemaker Resonances, §6.5 Codex Vinitorum) are not renumbered
  — the convention is to retain stable section numbers once §6 items
  are closed, with closed items prefixed `Built —` instead of
  `To be built —`.
- **§7 entries under 2026-05-11.** Four new entries above the existing
  winemaker-architecture entry, in reverse chronological order within
  the day: (i) Grape Resonances built, deployed, and cross-linked
  (sub-items 4, 5, 6 of §6.3 closed); (ii) Aggregator + coherence
  detector + 12-entry alias file shipped (the sub-item 4 detail);
  (iii) Four findings from live testing — multi-grape responses are
  default, Furmint-on-late-summer convergence with independent Claude
  as validation moment, defensible-disagreement vs defect framing for
  the other Planning Doc deviations, Piedmont/Nebbiolo as a genuine
  matcher miss worth flagging for a future Soul of Wine narrative
  pass; (iv) Documentation PDFs deferred for a follow-up session.

### 2026-05-11 — v0.21

- **§1 (Architecture).** Part II description updated to reflect
  forthcoming Codex Vinitorum alongside Codex Vini.
- **§3 leaves table.** Renamed Winemaker Study: tool stays *Winemaker
  Affinities*; study renamed from *The Winemaker's Constellation* to
  *The Hand of Wine* for grammatical alignment with the Body of Wine /
  Soul of Wine sibling pattern. Wordmark italics updated to *Hand*
  (matching *Body*, *Soul* pattern). Added *Winemaker Resonances* as a
  planned Correspondence leaf. Added *Codex Vinitorum* as a planned
  Personal Codex leaf. Section references in the table corrected:
  Grape Resonances at §6.3 (was §6.4 — a pre-existing typo from
  earlier drift), Winemaker Resonances at §6.4, Codex Vinitorum at §6.5.
- **§3.1 Works pairings table.** Updated Winemaker Work row to reflect
  the new Study name and updated row label from "Winemaker kinship" to
  "Winemaker character" to match the §6.2 architectural revision.
  Added a paragraph naming the Body/Soul/Hand triptych and what each
  title picks out.
- **§4.1 (Wordmark).** Codex *Vinitorum* added to the list of
  italicisation examples.
- **§4.4 (Documentation menu).** Studies list expanded to include
  Body of Wine and The Hand of Wine (was Soul of Wine + Winemaker's
  Constellation). Correspondence list expanded to include Grape
  Resonances and Winemaker Resonances as forthcoming.
- **§4.7 (Study-class template).** Rewritten to reflect Body of Wine
  being live alongside Soul of Wine; template work now gated on The
  Hand of Wine joining the live set rather than the second study
  generally. Visual harmonisation note updated to acknowledge Pass 3
  closure.
- **§4.11 (Correspondence is oracular).** Closing paragraph updated:
  Grape Resonances section reference corrected from §6.4 to §6.3
  (existing typo); a sentence added introducing Winemaker Resonances
  (§6.4) and noting it operates in the §4.12 Case 2 register (direct
  mediation, no region intermediary).
- **§4.12 (Character-mediated association — the architectural
  principle).** Renamed from "Region-mediated association — the
  generalisable Soul of Wine architecture" to reflect that the
  principle is now broader. Restructured around an explicit
  **Case 1 / Case 2** distinction: Case 1 (intermediate-layer
  mediation, for grapes/wines via regions) preserves all existing
  v0.20 content verbatim; Case 2 (direct mediation, for winemakers as
  themselves temperament-carrying) is the new addition. Closing
  paragraph extended to include Winemaker Resonances as the first
  Case 2 leaf, and to point to `FRAMEWORK_NOTES.md` as the home for
  further conceptual work, explicitly conditional on Vinotheca's
  completion.
- **§6.2 (Winemaker Affinities + The Hand of Wine).** Substantially
  rewritten. The April 2026 *Vigneron Kinship* framework is
  acknowledged as project material but no longer a complete
  description of the planned approach. New architectural posture
  documented: winemaker character profiles serve as the shared
  load-bearing asset for both the Works leaf (§6.2) and the
  Correspondence leaf (§6.4); the unit and shape of the profile
  (claim-based, portrait-based, or hybrid) is the central open
  question to resolve during build. Corpus size question (60–80 vs.
  32) flagged for reconciliation.
- **§6.4 (Winemaker Resonances) — new subsection.** Documents the
  third Correspondence leaf. Per §4.12 Case 2, this leaf does not use
  region-mediation; it matches directly against winemaker character
  profiles. Shares its load-bearing asset with §6.2.
- **§6.5 (Codex Vinitorum) — new subsection.** Documents the second
  Personal Codex leaf, mirroring Codex Vini's pattern for winemakers
  met in person. The Library/Codex independence rule explicitly
  preserved: Codex Vinitorum does not feed the Works or Correspondence
  leaves.
- **§7 entry under 2026-05-11.** Two entries: the winemaker
  architecture clarification, and the creation of `FRAMEWORK_NOTES.md`
  (with its limitations section) as the conditional companion document
  for framework-generalisation thinking.

The April 2026 *Vigneron Kinship Framework* document is preserved as
project material and remains a valuable reference for corpus design,
validation strategy, and methodological lineage. Its
claim-based-clustering proposal is no longer the locked approach for
§6.2, but its corpus thinking, validation pairs, and intellectual
lineage section all carry forward.

### 2026-05-10 — v0.20

- §6.3 sub-item 3 (`cluster_framings.json` authoring): closed with
  strikethrough. Ten framings authored — six bullseye (one per cluster)
  plus four prism (general refraction + three cluster dyads). Three
  Planning Doc framings locked verbatim; three synthesised with blind
  redrafts to better fit cluster diversity; four prism framings newly
  drafted. §7 entry under 2026-05-10 documents the synthesis decisions
  and cites the canonical Soul of Wine cluster metaphor lists as the
  authority against which the framings were calibrated.
- §6.3 progress: three of six sub-items now complete. **All Grape
  Resonances authoring is now done** (sub-items 1, 2, 3 closed in
  v0.15, v0.18, v0.20 respectively, all on 2026-05-10). The remaining
  three sub-items are engineering: aggregator + coherence detector
  (~½ day), React app scaffold (~1 day), test and deploy. The
  Planning Doc's original split — "~4 days authoring + ~2 days
  engineering" — has been honoured; the authoring took one day.

### 2026-05-10 — v0.19

- §4.12 added: **Region-mediated association — the generalisable
  Soul of Wine architecture.** A new family-level architectural
  principle stating that the framework refuses direct claims between
  feelings and surface-level objects, and instead mediates every such
  claim through regions (or, for non-wine domains, whatever
  intermediate cultural layer genuinely carries temperament). The
  principle generalises: any object class rooted in regional culture
  can be derived from the same matching engine by adding one new
  region-to-object association file. The 59 region narratives become
  the load-bearing asset of all present and future Correspondence
  leaves; new leaves cost only a curated association table plus a
  thin object-narrative layer. Five practical consequences listed
  (load-bearing regions, marginal cost per leaf, separate object
  narratives, reusable engine, disqualification criteria for
  candidate object classes). The principle was articulated by Jure
  while reviewing the falling-in-love worked example during the
  Grape Resonances build, and is now permanent family-level record
  rather than only inside the Grape Resonances Planning Doc.
- §7 entry under 2026-05-10 documents the principle's articulation,
  scope, and consequences.

### 2026-05-10 — v0.18

- §6.3 sub-item 2 (`grape_narratives.json` authoring): closed with
  strikethrough. All 101 canonical grape narratives drafted, reviewed,
  and saved. §7 entry under 2026-05-10 documents the work, including
  the blind-drafting methodology in practice, the four mid-batch
  encyclopaedia-register revisions caught and corrected, and the
  post-completion review pass that surfaced six word-level stylistic
  echoes (revised in two rounds with diagnostic re-runs to confirm
  no new echoes introduced).
- §6.3 progress: two of six sub-items now complete (sub-item 1 closed
  in v0.15 with `region_grapes.json`; sub-item 2 closed in this
  release with `grape_narratives.json`). Remaining four sub-items are
  `cluster_framings.json` authoring (~2 hours), aggregator + coherence
  detector build (~½ day), React app scaffold (~1 day), and
  deployment. The most authoring-heavy phase is now behind us.

### 2026-05-10 — v0.17

- §7 entry under 2026-05-10 added documenting four architectural
  decisions locked for Grape Resonances: (1) grape narratives surface
  in trace fold only, (2) v1 default response shape locked to Planning
  Doc line 150, (3) trace fold layout locked as grape-organised with
  four content kinds, (4) aggregator selection rule locked as
  "recurrence as finding". Decisions emerged from walking the
  end-to-end pipeline together and stress-testing the "falling
  deeply in love" worked example with actual `region_grapes.json` data.
- §6.3 sub-item 4 (aggregator) amended with parenthetical pointer
  to the locked Planning Doc rule.
- `Grape_Resonances_PlanningDoc.md` updated separately with three
  new "locked 2026-05-10" subsections (Default response shape,
  Aggregator selection rule, Trace fold spec) and two open-question
  closures (§5 trace fold contents, §6 Tier 2). The file grew from
  304 to 356 lines (52 lines added). Held locally per existing
  practice with the other Grape Resonances drafting files.

### 2026-05-10 — v0.16

- §6.3 sub-item 2 (`grape_narratives.json` authoring): two decisions
  captured ahead of writing. *Scope* — limited to the canonical 101
  grapes from Body of Wine / Grape Affinities; the 293-grape universe
  of `region_grapes.json` remains as data but is not all surfaced in
  user-facing oracle output. *Methodology* — blind drafting, recorded
  in `Grape_Resonances_PlanningDoc.md` as a new subsection. Both
  decisions recorded in §7 above.
- §6.3 sub-item 2 itself amended with a parenthetical pointer to the
  Planning Doc methodology section.
- `Grape_Resonances_PlanningDoc.md` updated separately (not in the
  vinotheca repo, held locally with the other Grape Resonances drafting
  files alongside `region_grapes.json` and `Grape_Resonances_CurationState.md`).

### 2026-05-10 — v0.15

- §6.3 (Grape Resonances build) sub-item 1 closed: `region_grapes.json`
  curated and validated across four sessions (10 / 5 / 17 / 27 regions
  per session, 59 of 59 complete). Recorded in §7. The remaining five
  sub-items in §6.3 are unchanged.
- The curation produced one mid-session amendment to a previously-
  closed region (Provence: Cinsault moved from `signature` to
  `lesser_known` to honour the subset rule; Grenache becomes
  Provence's sole signature). Mentioned for completeness; the change
  does not alter Provence's role in the Outward Ease cluster.
- Companion file `Grape_Resonances_CurationState.md` produced as a
  working deliverable note. It does not duplicate §6.3 — it records
  the curation rules, cluster reflections, and aggregator-relevant
  patterns (same-grape-across-regions, spelling normalisation,
  empty-fall-through) specifically.

### 2026-05-10 — v0.14

- **Pass 3 closed.** §6.3 retired from open items. Nine of nine
  palette-bearing surfaces aligned. Six Decisions resolved; four
  deferred Questions answered. The Library family is visually
  coherent across its full surface area: book serifs for Reading
  work, research sans for Studies, instrument sans for Tasterank
  Explorer, Codex's Part-II signature, all unified under Cormorant
  Garamond display.
- §6 numbering compacted: former §6.4 (Grape Resonances) renumbered
  to §6.3.
- Tasterank Explorer Tier 3 shipped (commit `8c4f0ce`); LICENSE
  attribution fixed to "Grape Affinities" (small clean-up commit
  immediately after).
- Wine Atlas circular-reference fix shipped (commit `64e839e`);
  yesterday's Tier 3 shipped a silent bug where `:root` defined
  `--wine: var(--wine);` and `--border: var(--border);`, causing
  wine-red and border rendering to fall through to inherited values.
  Caught this morning during Tasterank Explorer prep. Lesson logged
  in §7: post-edit visual verification of `:root` blocks is
  mandatory after sed substitutions.
- PASS3_SPEC.md updated: status block reflects Pass 3 closure;
  recommended sequence step 8 marked shipped; Tasterank Explorer
  change-list row marked shipped.

### 2026-05-09 — v0.13

- Pass 3 Tier 3 (Wine Atlas / Grand Cru Atlas) shipped. Token system
  introduced from scratch; typography migrated to family canonical
  (Cormorant Garamond display + EB Garamond body) per Decisions 5 and 6.
  Eight of nine palette-bearing surfaces aligned.
- §6.3 (Pass 3 — visual harmonisation) remains open with one execution
  item left: Tier 3 for Tasterank Explorer (full tokenisation + display
  font migration only; DM Sans body preserved per Decision 5 as
  instrument-class signal).
- Discovered during deploy: the `wine atlas/` working directory contains
  the actual git repo at a nested path (`wine atlas/grand-cru-atlas/`)
  rather than directly. Worth flagging for a future cleanup session
  (move repo up one level, or rename parent folder). Non-blocking.
- Also noted: `wine atlas/grand-cru-atlas/The_Grand_Cru_Atlas.pdf`
  uses `Title_Case_With_Underscores.pdf` naming, the same divergence
  pattern we just fixed for Tasterank Explorer. Should be renamed to
  family-canonical `lowercase-with-hyphens.pdf` form in a future small
  follow-up.

### 2026-05-09 — v0.12

- Pass 3 PDF naming convention shipped: Tasterank Explorer's five PDFs
  renamed to `lowercase-with-hyphens.pdf` form, matching Soul of Wine.
  Coordinated commits across `tasterank-explorer` and `body-of-wine`
  repos. Tasterank Explorer's README also now includes the
  previously-missing Methods Primer row in its Files table.
- Estate Atlas display font alignment shipped earlier in the session
  (Cormorant → Cormorant Garamond, commit `d855598`), separately
  logged in §7.
- §6.3 (Pass 3 — visual harmonisation) remains open with two execution
  items left: Tier 3 sessions for Wine Atlas and Tasterank Explorer,
  each its own dedicated session because of the larger scope (full
  tokenisation plus typography migration per Decisions 5 and 6).
- PASS3_SPEC.md updated: recommended-sequence step 6 (PDF naming)
  marked complete.

### 2026-05-09 — v0.11

- Pass 3 hard-questions session: Decisions 5 (body fonts class-
  distinguished) and 6 (display fonts family-unified) resolved,
  closing all four deferred questions from PASS3_SPEC.md (A, B, C, D).
  No code changes from the session itself — the decisions reshape the
  remaining execution work (notably Tier 3 for Wine Atlas, which now
  includes typography migration alongside tokenisation).
- PASS3_SPEC.md updated: Decisions 5 and 6 added; Questions A–D
  rewritten as "resolved" with their resolutions; status block updated
  to reflect spec completion; recommended sequence updated to mark
  steps 1–4 done and add Estate Atlas font follow-up + PDF naming
  ahead of the two Tier 3 sessions.
- §6.3 (Pass 3 — visual harmonisation) remains open. Three execution
  items remain ahead of full closure: Estate Atlas font follow-up
  (small commit), PDF naming convention (coordinated commits across
  two repos), and the two Tier 3 sessions (Wine Atlas, Tasterank
  Explorer).

### 2026-05-09 — v0.10

- Pass 3 React execution shipped: Region Affinities and Region
  Resonances both updated to canonical paper colour and `--paper-raised`
  equivalent. Seven of nine palette-bearing surfaces now aligned.
- §6.3 (Pass 3 — visual harmonisation) remains open. Two leaves remain
  (Wine Atlas, Tasterank Explorer), both Tier 3 (hard-coded values, no
  token system) and gated on the hard-questions session for body-font
  and atlas-distinctness decisions.
- The change visible only on careful inspection: the parchment colour
  shift was one hex unit (`#FAF7F2` → `#FAF6F1`). The `parchment.raised`
  utility is now available via the `bg-parchment-raised` class for any
  components that want the warm off-white treatment matching the rest
  of the family.

### 2026-05-09 — v0.9

- Pass 3 Tier 2 executed across two repos. Five of nine palette-bearing
  surfaces now aligned (Tier 1: Body of Wine, Soul of Wine, Codex Vini;
  Tier 2: Vinotheca, Estate Atlas). PASS3_SPEC.md updated with shipped-
  status marks for these five, plus a Question D added to the deferred-
  decisions list (Estate Atlas display font: Cormorant vs. Cormorant
  Garamond — 17 deliberate uses of "Cormorant" make this a real
  question, not a typo as originally assumed).
- §6.3 (Pass 3 — visual harmonisation) remains open. Remaining work:
  React leaves (Region Affinities + Region Resonances), Tier 3 leaves
  (Wine Atlas + Tasterank Explorer), the hard-questions session
  covering Questions A through D, and the PDF naming convention.
- The Tier 2 execution meaningfully visible: Vinotheca's warm-yellow
  paper becomes the canonical neutral cream; Estate Atlas's cooler wine
  becomes the canonical. The parent now reads chromatically the same
  as the eight live leaves it catalogues.

### 2026-05-09 — v0.8

- Pass 3 Tier 1 executed across three repos. No structural changes
  to PROJECT.md; §6.3 (Pass 3 — visual harmonisation) remains open
  with six of nine surfaces still to align. The work is recorded in §7.
- Per PASS3_SPEC.md's recommended sequence, the next execution
  session is Tier 2 (Vinotheca parent + Estate Atlas) — the leaves
  with non-canonical token names that need renaming alongside
  value swaps.

### 2026-05-09 — v0.7

- New file: `PASS3_SPEC.md` at the root of the `vinotheca` repo. Contains
  the full Phase 2 specification for Pass 3 — harvest results across
  all nine palette-bearing surfaces, four locked-in decisions, three
  deferred hard questions, and the per-leaf execution change list.
- §6.3 (Pass 3 — visual harmonisation): rewritten to point at
  `PASS3_SPEC.md` rather than holding the spec inline. The §6.3 prose
  in PROJECT.md is now a one-paragraph pointer; the substantive
  content lives in the spec document.
- Phase 2 decisions locked in this session:
  - Canonical wine red: `#7B2D26` (Codex Vini's `#5B1A2D` exempted as
    intentional Part-II differentiation per §1)
  - Canonical paper cream: `#FAF6F1`
  - Universal `--paper-raised` token at `#FFFDF8` (Codex's existing value)
  - Vinotheca's `--accent` → `--wine` token rename
- Phase 3 hard questions deferred: body font canonical, atlas distinctness
  policy, Codex differentiation depth.

### 2026-05-09 — v0.6

- §6.4 (Local cleanup — `documents_old/` folders) closed: the gitignored
  rollback folders in `tasterank-explorer/` and `region-resonances/`
  were deleted locally after confirming live docs work. Recorded in §7.
  Subsequent §6 subsection renumbered down by one (old §6.5 → §6.4).
  Four remaining open subsections.
- §3 leaves table and §4.11 cross-references for Grape Resonances
  updated from §6.5 to §6.4.
- Minor correction: PROJECT.md previously listed three repos with
  `documents_old/` folders (`tasterank-explorer`, `region-affinities`,
  `region-resonances`). In fact only two had them — `region-affinities`
  never had one. The §6.4 description carried this small inaccuracy
  forward through three versions; flagging here for the record.

### 2026-05-09 — v0.5

- §6.1 (To be built — The Body of Wine) closed: the Study is built and
  deployed in the same session. Recorded in §7. Subsequent §6
  subsections renumbered down by one (old §6.2 → §6.1, old §6.3 → §6.2,
  old §6.4 → §6.3, old §6.5 → §6.4, old §6.6 → §6.5). Five remaining
  open subsections.
- §3 leaves table: Body of Wine row updated from "Working title — to
  be built (§6.1)" to "Live"; repo column from `*(tbd)*` to
  `body-of-wine`.
- §3.1 Works pairings table: Body of Wine row updated from "(working
  title — to be built)" to "(live)". The Grape similarity Work is now
  the first Work in the family with both faces live.
- §6.3 (formerly §6.4, Pass 3 — visual harmonisation): gating language
  updated. Per §4.7, two live studies were the precondition for proper
  template design; that condition is now met. Section now reads
  "unblocked" rather than "deferred." Also added a new Pass 3 item:
  settle PDF naming convention across the family, currently divergent
  between Soul of Wine (`lowercase-with-hyphens.pdf`) and Tasterank
  Explorer (`TasteRank_Title_Case_With_Underscores.pdf`).

### 2026-05-09 — v0.4

- §6.1 (Active task — Move Region Resonances from Tools to
  Correspondence) closed: the work was completed in the same session and
  is now recorded in §7. The deploy went further than §6.1's stated
  scope by also restructuring the parent's Tools and Studies subsections
  into a single Works subsection per §2 (paired Tool+Study entries) —
  the original §6.1 had been written before §2's paired-Work model was
  fully thought through, so closing §6.1 properly required completing
  the §2-implied restructure as well. Subsequent §6 subsections
  renumbered down by one (old §6.2 → §6.1, old §6.3 → §6.2, …, old §6.7
  → §6.6).
- §3 leaves table: Region Resonances row updated from "Live, but
  currently filed in Tools — to be moved" to simply "Live"; the Grape
  Work's Study row updated from `*(paired study tbd)*` to **The Body
  of Wine** (working title) with wordmark The *Body* of Wine.
- §3.1 Works pairings table: Body of Wine (working title) inserted as
  the Study face for the grape similarity Work.
- §6.1 (formerly §6.2) — *To be built — The Body of Wine*: section
  retitled from "*The Grape Affinities study*" to "*The Body of Wine
  (paired study for Grape Affinities)*", expanded with a paragraph on
  the title's origin (the Body / Soul / Constellation triptych as three
  ways of seeing wine — through the senses, through cultural identity,
  through the character of those who make it), and pending items
  refined.

### 2026-05-09 — v0.3

- §3 leaves table: added **Grape Resonances** as a planned Correspondence
  leaf (sibling to Region Resonances). Repo name `grape-resonances` (tbd).
  Wordmark: Grape *Resonances*. Eyebrow: A Correspondence of Vinotheca.
- New **§4.11 — Correspondence is oracular, not search**: codifies the
  conceptual finding that Correspondence tools are instruments of
  self-recognition rather than recommendation systems, with concrete
  design implications (compression, single framing sentence, traceable
  but not foregrounded framework, verification invited but not measured,
  graceful refusal of wrong-shaped queries, no personalization or
  learning, bullseye vs. prism query handling). This frame applies to
  Region Resonances retrospectively and governs Grape Resonances by
  design.
- New **§6.7 active task — Grape Resonances build**: detailed pending
  items, with the build broken into curatorial work
  (`region_grapes.json`, `grape_narratives.json`,
  `cluster_framings.json`), engineering work (aggregator, coherence
  detector, React scaffold from Region Resonances), and deployment.
  Total estimated build: ~6 working days.
- Companion planning doc created: `Grape_Resonances_PlanningDoc.md`,
  sibling to `Region_Resonances_PlanningDoc.md`, documenting
  architecture decisions (region-mediation chosen over TasteRank-driven
  matching), worked examples that validated the oracle frame
  (*brotherhood*, *falling deeply in love*, *making a decision about the
  move across the country*), and open questions to resolve before build.

### 2026-05-08 — v0.2

- §6.1 (Active task — Bring Soul of Wine into conformance with §4.6)
  closed: the work was completed in the same session and is now recorded
  in §7. Subsequent §6 subsections renumbered down by one (old §6.2 → §6.1,
  old §6.3 → §6.2, …, old §6.7 → §6.6).
- §4.6 updated: the paragraph describing Soul of Wine's "Interactive
  Tools" section moved from present-tense ("currently has", "will be
  deleted") to past-tense, reflecting the completed cleanup, and
  cross-references §7 rather than the now-closed §6 entry.

### 2026-05-08 — v0.1 (initial)

- Initial draft of PROJECT.md.
- Architecture: established five-section model organised by operational
  purpose (Maps / Works / Correspondence / Reference / Personal Codex).
- Works model: defined "Work" as paired Tool + Study sharing supporting
  documents, replacing the previous separate-Tools/separate-Studies split
  on the parent page.
- Reference section established as the home for intellectual foundations;
  `vinotheca-reference` repo to be created (empty for now).
- Region Resonances reclassified from Tools to Correspondence.
- Soul of Wine: confirmed the four embedded prototype tools (Cluster
  Explorer, Cluster Map, Movement Map, D-Score Dashboard) will be deleted
  as superseded by Region Affinities.
- Eyebrow grammar extended to include "A Correspondence of Vinotheca"
  and "A Reference of Vinotheca".
