# Framework Notes

*Companion document to PROJECT.md · working notes · not a plan*

---

## Status and scope

This document records conceptual work on the general framework underlying Vinotheca's architecture. It is **exploratory and conditional**: it presupposes that Vinotheca is successfully completed and validated as a working instrument for wine lovers before any generalisation is attempted. Nothing here is a commitment to build anything beyond Vinotheca.

The document exists so that thinking accumulated during the Vinotheca build is not lost. The eventual polished home for these ideas is the *Theoretical Foundations of Character-Based Analysis* document slated for the Reference section of the Library. These notes are where the formulation develops in the meantime.

The notes will be revised as the winemaker leaf is built, since that leaf is the case where the framework gets most directly tested. Any formulations that read as settled here should be treated as current-best rather than locked.

Last meaningful update: 2026-05-11

---

## 1. What the instrument is and is not

The framework describes a kind of instrument that gives the user back to themselves through a structured mediation layer.

The user brings a state — a feeling, a phrase, a situation, a disposition in a particular moment — and the instrument offers, in compressed form, the cultural objects whose character corresponds to that state. The user's experience is one of recognition rather than discovery: *yes, that is exactly the wine I would drink with that feeling.* The success state is the user's own pause and acknowledgment, not a metric the tool can measure.

The instrument is therefore not a recommender. A recommender optimises a predicted utility function; this instrument offers a structured surface on which the user can recognise themselves. The instrument is not a personality assessment. It does not tell the user who they are; it gives them a vocabulary in which their own state becomes articulable. The instrument is not a preference-learning system. It does not adapt to the user across sessions; the same query produces the same response, on the hundredth use as on the first, because the framework is fixed.

What the instrument offers, on each use, is a small number of carefully prepared cultural objects together with the framework's reasoning for the match — visible to the user if they want it, collapsed if they do not. The authority of the instrument comes from the care taken in building the mediation layer, not from any claim about knowing the user.

---

## 2. The mediation-layer architecture

The framework's central architectural commitment: it refuses to claim direct associations between user states and surface-level objects, and instead mediates every such claim through an intermediate layer that genuinely carries character.

Many cultural objects do not carry character in any strong sense on their own. A grape variety, a dish, a piece of clothing, a fragrance — these have associations, but the associations live in the cultures that produced and use them, not in the object itself. The framework's move is to identify, for any given domain, an intermediate layer that *can* carry character honestly, and to match user states against that layer rather than against the surface objects directly.

In the wine domain, regions are the canonical intermediate layer. A wine region has a history, a way of working, a set of customs and hierarchies, a posture in the world — the kind of attributes that can be written as a character portrait and matched against a user's phrase. Grapes do not have these attributes on their own, but they are associated with regions, and the framework surfaces grapes via region matches rather than via any direct grape-to-feeling claim.

A useful refinement, surfaced while thinking through the winemaker case: sometimes the surface-level object is itself capable of carrying character. Winemakers are people, and people can carry temperament in the strong sense. When this is true, the surface object and the intermediate layer coincide — the matching engine runs against the winemakers themselves, without needing an additional layer between them and the user.

The general principle: the mediation layer must be something that genuinely carries character. Where the surface object cannot, the framework needs an intermediate layer that can. Where the surface object can, no intermediate layer is required.

The architecture joins two claims that are each defensible on their own ground: that the mediation layer has the character ascribed to it (supported by careful authored portraits and embedding matches), and that the surface object is associated with that layer (supported by curated, transparent association data). The framework does not invent a third claim that connects user state to surface object directly.

Practical consequences:

The intermediate layer's portraits are the load-bearing asset. Investment in their internal coherence, distinctiveness, and stylistic care pays out across every instrument that draws from the same layer. They are not data; they are written work.

New instruments within a domain cost the curation of one association table and one set of object-narrative notes, plus light engineering. The matching engine, response shape, and trace structure are reusable across instruments.

What disqualifies a candidate domain: the intermediate layer must be something that can honestly carry character. If the candidate intermediate is itself a thin or arbitrary classification, the architecture does not work — there is nothing real for the matching to engage.

---

## 3. Why this design is distinct from general-purpose language model tools

The framework was developed partly in response to the observation that general-purpose language model tools, when asked questions of the kind this instrument is built for, behave in ways that work against the user's interest.

Three structural problems with general-purpose tools used for character-mediated questions:

*The output is shaped by base rates in the model's training distribution.* When a general-purpose model is asked which winemaker corresponds to a feeling, the response tends toward famous names, consensus framings, and whatever associations between the query terms and the domain happen to recur in the training data. There is no commitment to any particular curated corpus; the answer is statistical rather than considered.

*The output is shaped by the model's optimisation for coherent, authoritative-sounding prose.* When the underlying claim is uncertain or contested, the prose flows anyway, and the apparent confidence is a property of the language model rather than of the substantive question. The user receives a smooth response that feels grounded but is not traceable to anything specific.

*The reasoning is not inspectable.* The user has no way to check why the model produced its response, because the response was generated by a high-dimensional weight matrix rather than by any chain of claims that can be examined.

The framework's design is built to avoid all three:

*Base rates are replaced by an authored mediation layer.* The portraits of the intermediate layer are deliberately written and stable across queries. The same user state produces the same matched portraits, and those portraits do not drift toward famous-and-frequent.

*Coherence pressure is replaced by compression and traceability.* The instrument returns few results, framed minimally, with the framework's reasoning available in a fold for users who want it. There is no prose surplus pretending to be considered judgment.

*Reasoning is fully inspectable.* The match between user state and mediation-layer portrait is a transparent embedding operation against named, readable texts. The association between mediation layer and surface object is a curated table the user can see. Every step is open to the user.

These three commitments are what make the instrument a defensible character companion rather than a stylish front end on a probabilistic text generator.

---

## 4. The Vinotheca case

Vinotheca is the first worked instance of this framework. The wine domain is well-suited to it because both regions and winemakers are unusually rich character-carriers, the surface objects (wines, grapes) have well-attested cultural rootedness, and the audience of careful wine readers is patient enough to recognise the care that goes into building the mediation layer.

The strategy for the framework is therefore:

*Complete Vinotheca on this design, including all three winemaker leaves (the Works leaf, the Correspondence leaf, the personal Codex Winemakers).*

*Validate with actual readers that the instruments produce the recognition effect — that they give users back to themselves in a way they find valuable.*

*If and only if validation succeeds, write up the framework as a general architecture for character-mediated cultural instruments, with Vinotheca as the worked case. The natural home for that writing is the Reference section's Theoretical Foundations document.*

*If validation succeeds further still, consider applying the same architecture to a different domain whose surface objects are rooted in some genuine intermediate character-carrying layer.*

The sequencing is deliberate. The framework should not be claimed as general until at least one instance demonstrably works. Vinotheca's completion is the precondition for everything downstream.

---

## 5. Open questions for future revision

Things that are genuinely uncertain and that the building work may clarify:

How richly the mediation-layer portraits need to be written for the instrument to feel like recognition rather than approximation. The 59 region narratives provide one data point; the winemaker portraits will provide a second. Whether other domains can sustain portraits of comparable quality is unknown.

Whether the framework remains honest at scale. The current instruments work with intermediate layers of tens to low hundreds of entities. Whether the same design holds when the layer is much larger, or much smaller, is not yet tested.

What the right verification register is. The Region Resonances pattern (a quiet *does this resonate?* prompt, no logging) is one approach. Whether richer or different verification serves the user better is an open question.

How the framework handles user states that are unusually specific, ambiguous, or compound. The bullseye-vs-prism distinction in the Correspondence design handles some of this; whether it handles enough of it is something the building work will reveal.

Whether the framework's commitments hold up under adversarial use — users who are testing the instrument, gaming it, or asking in bad faith. The current design has no defence against this beyond compression and fixed framing; whether that is enough is unknown.

These questions do not need to be answered before Vinotheca is completed. They are flagged here so that observations during the build can be recorded against them.

---

## 6. Limitations and known objections

The framework should not be presented or held in the mind as stronger than it is. The following are real limitations and serious objections that an academic or scientific reviewer could reasonably raise. They are noted here so that the framework's claims can be calibrated against them, and so that future writing about the framework (including the eventual Reference document) does not overstate what the architecture demonstrates.

*The framework cannot empirically distinguish recognition of real structure from skilled projection.* The success criterion is the user's experience of recognition — *yes, that is exactly the wine I would drink with that feeling.* This experience is also what well-written horoscopes, cold readings, and skilled character descriptions reliably produce, regardless of whether they track anything real about the recipient. The Forer effect (1948 and replicated extensively) shows that people will reliably recognise themselves in sufficiently well-written generic descriptions. The framework's design choice to invite verification without logging it protects user privacy but forecloses any empirical separation of "the framework matched something real" from "the writing was good enough that the user projected themselves onto it." The framework's only defense is that it makes the construction transparent — the user can inspect the mediation portraits and the matching reasoning — but transparency establishes inspectability, not external validity.

*The mediation layer encodes a particular author's structuring of cultural space rather than purely surfacing natural structure.* The 59 region narratives, the 101 grape narratives, and the forthcoming winemaker portraits are authored by a single mind with particular sensibilities. The clusters and matches that emerge from the architecture are surfaced by clustering and embedding similarity, but the structure that gets surfaced is the structure the author embedded into the portraits in the first place. The framework presents itself as inductive (letting structure emerge from text) but is more accurately *projective with transparency* (the author's distinctions are stably embedded and then made inspectable). This is a more curatorial activity than the framework's self-description sometimes implies. The honest version of the claim is that the architecture surfaces *one author's careful structuring of cultural space, made stable, inspectable, and matchable* — rather than discovering structure that is in the world independently of the author.

*The framework operates below the resolution at which empirical preference and personality science has established reliable findings.* Empirical work on aesthetic preference, personality, and individual differences supports broad dimensions (openness, sensation-seeking, conscientiousness) with reasonable replication. The framework's mediation layer asks users to find resonance with character distinctions that are much finer-grained than this — the difference between "the embattled craftsman register" and "the patient custodian register," say. There is no direct empirical support that distinctions at this resolution are reliably detectable, stable, or shared across users. The framework's response is that it does not need this kind of reliability — it needs enough coherence that the user's recognition feels earned within the act of using the instrument — but this is a lower bar than empirical personality science would underwrite, and the framework should be explicit about operating below that bar.

*Wine-domain reliability findings suggest caution about scaling user-facing claims.* Studies on wine expert judgment (Hodgson 2008–2009 on California State Fair judges; subsequent work on critic reliability) show that even highly trained experts cannot reliably reproduce their own evaluations of the same wine across blind re-tastings. If expert judgment about the wine itself is this noisy, the framework's matching of user feelings to mediation-layer character should be held with corresponding modesty. The framework's claim is not that the match is empirically validated; it is that the match is non-arbitrary because the mediation layer is authored carefully. These are different claims and the framework should not be presented as if it inherits validation from the wine literature.

*Wine is unusually favorable territory; the framework's generalisability is therefore harder to claim than the strategy document implies.* The wine domain has features that other candidate domains may lack: a multi-century written tradition of character description, a stable cast of cultural mediation entities (regions, producers, appellations) with intersubjective agreement about their character, a community of readers culturally pre-disposed to receive aesthetic claims with patience, and a domain where commercial recommender systems perform notoriously poorly. Music has the written tradition but unstable cultural mediation layers; fragrance has neither; literature has the tradition but reasonable recommender performance already. Whether the framework generalises beyond wine is genuinely unknown, and the framework's general claims should be held provisionally until at least one non-wine instance has been built and tested.

*The "carries temperament" distinction is harder to defend rigorously than its use suggests.* The framework's central architectural move — that regions (and winemakers) "genuinely carry character" in a way that grapes do not — is harder to ground than it appears. An anthropologist or critical theorist could argue that "the temperament of Burgundy" is itself an artefact of a particular cultural conversation (Anglo wine writing, French regional discourse, appellation marketing) rather than a property of the place. The framework treats authored portraits as honest distillations of something real; a skeptical reading would say the portraits *construct* the temperament they claim to capture, then match users against the writer's categories rather than against any underlying reality. The honest response is that all character description has this constructed quality, and the framework's contribution is to make the construction stable and transparent rather than to access an unmediated truth — but this is a more modest claim than "the mediation layer genuinely carries character."

The framework's overall posture, in light of these objections, should be:

The framework does not claim empirical validation of any psychological, sociological, or aesthetic theory. It does not claim that user recognition reflects access to real structure rather than skilled projection. It does not claim that its mediation layers surface natural categories independent of authorship.

What the framework does claim is more modest: that for users seeking to make their own taste, feeling, and disposition more articulable through engagement with cultural objects, a carefully authored, stable, inspectable, and compressed mediation layer is more honest and more useful than the alternatives currently available (general-purpose language model tools, commercial recommenders, or unmediated browsing). The framework is an instrument design, not an empirical claim about how minds work.

This more modest framing is sufficient to motivate Vinotheca's value. It is also more defensible than the stronger version, and more durable as the framework is presented to readers who will reasonably ask the questions in this section.

---

## Changelog

**2026-05-11 — limitations section added.** Section 6 (Limitations and known objections) added in response to a follow-up conversation about what the strongest academic objections to the framework would be. Six limitations documented: the recognition-vs-projection problem (Forer effect), the projective-with-transparency nature of the mediation layer, the resolution mismatch with empirical preference science, the wine-domain reliability findings, the generalisability question, and the "carries temperament" claim's metaphysical weight. Closing paragraph reformulates the framework's overall posture in the more modest register the limitations justify: the framework is an instrument design, not an empirical claim about how minds work.

**2026-05-11 — initial draft.** Document created from a brainstorming conversation about the winemaker section of Vinotheca that surfaced the general framework underlying the architecture. Three sections of conceptual scaffolding drafted: the instrument's character (what it is and is not), the mediation-layer architecture (a generalisation of PROJECT.md §4.12), and the structural distinction from general-purpose language model tools. Strategy and open-questions sections added to record the build-first, generalise-later sequencing.
