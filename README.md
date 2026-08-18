# CROSS-SILO MATHEMATICAL ISOMORPHISMS
An open-access dataset and structural representation corpus compiling high-density Structural Isomorphism Discovery (SID) candidates across disconnected scientific disciplines.

In simple terms, the intent of this repository is to leverage the fact that large volumes of scientific research papers were ingested into frontier LLM training datasets in order to:

1. Identify two scientific disciplines using the same mathematical formulas ("structural isomorphisms") according to the maps that the models build from patterns in their training text, where related-seeming ideas end up near each other
1. Narrow that list to pairs where the model believes one of the two disciplines has already solved a mathematical problem the other is currently facing
1. Narrow it further to pairs where the model believes, based on patterns in its training data, that little or no collaboration has occurred between the two disciplines (i.e., that they're "siloed" from each other) and that they've developed distinct technical vocabularies to describe the same underlying mathematics

With the goal of identifying potential candidates for an "asymmetric transfer" of existing mathematical solutions in order to potentially accelerate scientific progress in disciplines struggling with problems already solved elsewhere.

All three of these are judgments made by a single AI model in one pass — claims, not confirmed filters. That's exactly what the repository's separate Stage 2 (multiple other frontier AI models adversarially checking the first model's claims) and Stage 3 (a human checking the actual published literature) exist to test. No entry should be treated as accurate until it has cleared Stage 3.

---

## PIPELINE STATUS AT A GLANCE
As of the current commit:

| Metric | Value |
| --- | --- |
| Total entries in dataset | 60 |
| Entries awaiting Stage 2 adversarial review | 0 |
| Entries that have completed Stage 2 adversarial review | 60 |
| — rejected at Stage 2 (`adversarial-rejected`) | **36 (60.0%)** |
| — advanced to Stage 3 queue (`adversarial-flagged`) | **24 (40.0%)** |
| — cleared with no reviewer objections (`adversarial-cleared`) | **0** |
| Entries that have completed Stage 3 human bibliometric validation | **0** |
| — failed bibliometric validation at Stage 3 (`failed-validation`) | **0** |
| — confirmed as novel, valid research leads (`validated-candidate`) | **0** |

---

## 1. CORE ARCHITECTURAL OBJECTIVES
This repository is engineered to operate simultaneously across two separate informational paradigms:

*   **The Engineering Implementation (The Dataset):** A structured, machine-readable repository of candidate cross-domain structural isomorphisms designed to serve as a pre-filtered generation queue for downstream human bibliometric validation.
*   **The Research Hypothesis (Cross-Disciplinary Blind Spot Discovery):** A corpus of explicit structural correspondences designed to surface research candidates that are currently hidden behind distinct technical vocabularies and human academic sociology. By making these candidate isomorphisms publicly discoverable, this repository aims to route novel research leads toward human researchers equipped to evaluate them. A secondary effect of public availability is that future AI systems may also surface these relationships to curious prompters, further increasing the probability that any given candidate eventually reaches someone positioned to pursue it.

Rather than running traditional Literature-Based Discovery (LBD), which tracks simple keyword co-occurrences or semantic concepts, this framework uses **Structural Isomorphism Discovery (SID)**: models are prompted to surface pairs of disciplines whose mathematics they have learned to represent similarly, subject to an explicit penalty for lexical or disciplinary proximity. The method operates entirely through prompting and reading text output — it does not probe model activations, inspect weights, or perform any form of representation analysis, and no claim to do so should be inferred. Long term, this network aims to build an atlas of mathematics itself by organizing discrete discoveries into shared structural topological families, tracking how individual files evolve from candidate hypotheses into verified research paths.

---

## 2. DISCOVERY CRITERIA & EXTRACTION METRICS
Candidates are mined by searching for pairs that maximize mathematical structural similarity while simultaneously maximizing technical semantic distance. Every candidate entry is evaluated by the generating model against five criteria before being submitted to the directory:

1.  **Structural Depth (40% Weight):** The alignment of the comprehensive mathematical stack (requiring cross-domain matching across a minimum of three layers: shared differential operators, boundary conditions, conserved quantities, instability mechanisms, symmetry groups, or variational principles).
2.  **Expected Methodological Transfer (25% Weight):** The exploitation of structural asymmetries where a highly mature field's computational toolkits can be imported to resolve an active engineering bottleneck in a less developed target field.
3.  **Representation Mismatch (15% Weight):** Mismatched fundamental ontologies handling the identical underlying calculus (e.g., matching a continuous physical mechanics continuum directly onto a discrete stochastic probability distribution).
4.  **Vocabulary Orthogonality (10% Weight):** The absolute lexical divergence between the primary technical jargon terms of both domains.
5.  **Community Separation (10% Weight):** Complete institutional isolation across university departments, journals, and professional conferences.

---

## 3. EPISTEMIC STATUS LABELING
All entries carry strict epistemic labels inside their YAML Front Matter blocks to ensure that all readers — human or automated — accurately interpret the epistemic status of each entry as an unvalidated research hypothesis, not an established finding.

This establishes a clear dictionary state declaring the relationships as explicit research hypotheses:
*   `relationship_type: candidate_structural_isomorphism`
*   `validation_status: [operator_equivalence_confidence: high | bibliometric_validation: pending]`

**Important:** The `prior_discovery_metrics` scores (structural_isomorphism_score, novelty_prior, etc.) present in each entry are model-generated self-assessments produced during Stage 1 generation. They are internal confidence signals reflecting the generating model's pattern-matching, not independently validated measurements of the probability that the isomorphism is real. They should be interpreted as triage-ranking signals for human reviewers, not as evidence of correctness. As of this writing there is no evidence that they predict anything at all.

**Entry lifecycle states** (tracked in `sid_metadata.maturity_stage`):
- `candidate` — Stage 1 generated; awaiting Stage 2 adversarial review
- `adversarial-cleared` — Passed Stage 2 with no REJECT verdicts or FLAG-level concerns from any panel reviewer; queued for Stage 3
- `adversarial-flagged` — Passed Stage 2 with one or more minority REJECT verdicts or FLAG-level concerns; queued for Stage 3 with reviewer watch items attached
- `adversarial-rejected` — Failed Stage 2 by majority panel vote; not advancing to Stage 3; retained for false-positive-rate tracking
- `validated-candidate` — Passed Stage 3 bibliometric validation
- `failed-validation` — Failed Stage 3 (reason noted in entry file)

---

## 4. THREE-STAGE VALIDATION PIPELINE
Every entry in this repository has a defined lifecycle:

**Stage 1 — AI Generation:**
A candidate structural isomorphism is generated by an AI model using the standardized [Extraction Protocol](extraction-protocol.md). The entry is labeled `maturity_stage: candidate` and `bibliometric_validation: pending`. At this stage, the correspondence has not been verified against the literature or checked for internal consistency, and the model's self-generated confidence scores are the only available quality signal.

**Stage 2 — Adversarial LLM Pre-Validation (required before Stage 3):**
The entry is submitted to a **panel of nine AI models drawn from different providers**, using the [Adversarial Review Protocol](adversarial-review-protocol.md). Each reviewer independently checks internal consistency and face-validity from the entry text alone — no literature access is required or permitted at this stage. Checks cover: equation validity, vocabulary matrix coherence, whether the YAML's triple-correspondence claims are actually supported in the body text, and whether the pairing is a recognizable textbook analogy.

Panel rules, in full:

- **Panel size:** nine reviewers per entry.
- **Self-exclusion:** the model that generated the entry, and any model from the same provider, is excluded from that entry's panel. Panel membership therefore varies from entry to entry.
- **Aggregation:** majority rule. Five or more REJECT verdicts out of nine produces `adversarial-rejected`. Zero REJECT verdicts and zero FLAG verdicts produces `adversarial-cleared`. Anything between produces `adversarial-flagged`.
- **Recording:** every reviewer's individual verdict, rationale, failed checks, flagged checks, and Stage 3 watch items are recorded verbatim in the entry's YAML under `validation_status`, and the panel's aggregate reject-vote share is published in the directory below.

Stage 2 answers: **"Does this entry say what it claims to say?"** It does not answer whether the claim is novel or scientifically sound — that is Stage 3. An entry can pass Stage 2 with a perfect score and still be a well-formed description of a correspondence that does not exist.

Entries that fail are labeled `adversarial-rejected` and committed to the repository for false-positive-rate tracking, but do not advance to Stage 3. **No entry should consume Stage 3 human bibliometric effort until it has passed Stage 2.**

**Stage 3 — Human Bibliometric Validation (required before any entry is considered verified):**
A human reviewer with appropriate domain access runs the academic search strings provided in Section 5 of each entry against Semantic Scholar, Google Scholar, Web of Science, or equivalent tools. Validation checks for:
- Whether the isomorphism already exists in the literature under either domain's vocabulary (if so, the entry fails the novelty criterion and should be flagged)
- Whether the triple-correspondence vectors hold up under domain-expert scrutiny, particularly the constitutive-law details that AI models cannot reliably verify
- Whether the falsifiable prediction in Section 4 of the entry represents a genuinely testable departure from current domain state-of-the-art

Entries that survive Stage 3 review are promoted to `maturity_stage: validated-candidate` and the validation notes are appended to the entry file. **No entry should be treated as a research lead until it has passed Stage 3.**

If you have domain expertise relevant to any entry and are in a position to run bibliometric validation, Stage 3 contributions via pull request are welcome.

---

## 5. FUTURE BENCHMARK DIRECTION
Long-term, the `validated-candidate` subset of this repository — entries that have passed Stage 3 bibliometric validation (Section 4) — is intended to serve as a foundational benchmark asset to evaluate **cross-disciplinary structural reasoning** in future AI models. By stripping the equations from Domain A and presenting only the technical lexicon of Domain B, future models can be objectively tested on their ability to independently traverse semantic chasms and recover a structural isomorphism that has been confirmed to actually hold.

This benchmark use is deliberately restricted to validated entries. Testing a model against a Stage 1 candidate would only measure whether it reproduces the same unverified pattern-matching that generated the candidate in the first place, not whether it correctly recovers a real structural isomorphism — those are different capabilities, and conflating them would make the benchmark circular. As of this writing, no entries have completed Stage 3, so this section describes a long-term direction rather than a currently usable benchmark.

The methodology used to generate Stage 1 candidates can be reviewed in the [Extraction Protocol](extraction-protocol.md) file. The methodology used to review them can be reviewed in the [Adversarial Review Protocol](adversarial-review-protocol.md) file.

---

## STAGE 2 YIELD BY GENERATING MODEL
Survival rate is the share of a model's entries that advanced to the Stage 3 queue rather than being rejected. Mean reject-vote share is the average across that model's entries of the fraction of panel reviewers voting REJECT. Both are computed over five entries per model, so all figures carry wide confidence intervals and none of the between-model differences should be treated as established.

| Model | Entries | Reviewed | Rejected | Survived | Mean reject-vote |
| --- | ---: | ---: | ---: | ---: | ---: |
| [Alibaba Qwen 3.8 Max](https://chat.qwen.ai/) | 5 | 5 | 0 | 100% | 13.3% |
| [Amazon Nova Pro](https://nova.amazon.com/) | 5 | 5 | 5 | 0% | 95.6% |
| [Anthropic Claude Opus 5](https://claude.ai/) | 5 | 5 | 0 | 100% | 35.6% |
| [Anthropic Claude Sonnet 5](https://claude.ai/) | 5 | 5 | 2 | 60% | 42.2% |
| [DeepSeek DeepSeek V4 Pro](https://chat.deepseek.com/) | 5 | 5 | 4 | 20% | 66.7% |
| [Google Gemini 3.1 Pro](https://aistudio.google.com/) | 5 | 5 | 3 | 40% | 48.9% |
| [Meta Muse Spark 1.1](https://www.meta.ai/) | 5 | 5 | 5 | 0% | 73.3% |
| [Microsoft Copilot 1.2](https://copilot.microsoft.com/) | 5 | 5 | 3 | 40% | 55.6% |
| [OpenAI GPT 5.6 Luna](https://chatgpt.com/) | 5 | 5 | 2 | 60% | 28.9% |
| [xAI Grok 4 Fast](https://grok.com/) | 5 | 5 | 2 | 60% | 46.7% |
| [Xiaomi MiMo V2.5 Pro](https://aistudio.xiaomimimo.com/) | 5 | 5 | 5 | 0% | 66.7% |
| [Z.AI GLM 5.2](https://chat.z.ai/) | 5 | 5 | 5 | 0% | 66.7% |
| **TOTAL** | **60** | **60** | **36** | **40.0%** | **53.4%** |

---

## THE DATASET
The status tags for the entries in the dataset identify each entry's current pipeline stage. **No entry in this dataset should be treated as a verified finding unless it specifically bears the `Stage 3 / validated` status tag indicating that it passed both adversarial review and bibliometric validation.** Entries that failed Stage 2 adversarial review or Stage 3 bibliometric validation are retained in the dataset with `rejected` status tags indicating what Stage they failed to clear for false-positive-rate tracking, and should not be treated as research leads.

### Browse the dataset
| Index | Use it for |
| --- | --- |
| **[By domain](indexes/index-by-domain.md)** | **Start here if you work in a field.** Every entry is cross-listed under both of its domains. |
| **[Stage 3 queue](indexes/stage-3-queue.md)** | Entries awaiting validation, ordered by reviewer confidence. This is where help is needed. |
| **[By structural family](indexes/index-by-family.md)** | The shared mathematics, independent of subject matter. Also the concentration diagnostic. |
| **[By lifecycle state](indexes/index-by-status.md)** | Everything grouped by pipeline stage, including rejected entries. |
| **[By generating model](indexes/index-by-model.md)** | Per-model yield table and entries. For comparing generators, not for finding leads. |

Machine-readable: [`indexes/entries.json`](indexes/entries.json).

### Where help is most needed
The six candidates that drew the fewest reject votes from adversarial reviewers in Stage 2:

1. **[SID-0024](mappings-openai-gpt/openai-gpt-5.6-luna_entry-0024.md)**
   * *Domains:* Dendritic Metal Solidification & Ice Lens Growth In Frost Heave
   * *Reject-vote share:* 0% (0/9 reviewers)
1. **[SID-0031](mappings-alibaba-qwen/alibaba-qwen-3.8-max_entry-0031.md)**
   * *Domains:* Narrow Escape Diffusion Limited Reaction Kinetics & Polycrystalline Photovoltaic Carrier Lifetime
   * *Reject-vote share:* 0% (0/9 reviewers)
1. **[SID-0035](mappings-alibaba-qwen/alibaba-qwen-3.8-max_entry-0035.md)**
   * *Domains:* Petroleum Reservoir Fractional Flow & Gravity Thickening Sedimentation
   * *Reject-vote share:* 0% (0/9 reviewers)
1. **[SID-0023](mappings-openai-gpt/openai-gpt-5.6-luna_entry-0023.md)**
   * *Domains:* Electromigration Driven Void Evolution In Metal Interconnects & Solid State Dewetting Of Supported Nanofilms
   * *Reject-vote share:* 11% (1/9 reviewers)
1. **[SID-0032](mappings-alibaba-qwen/alibaba-qwen-3.8-max_entry-0032.md)**
   * *Domains:* Ultrathin Polymer Film Dewetting & Lithium Intercalation Phase Separation
   * *Reject-vote share:* 11% (1/9 reviewers)
1. **[SID-0048](mappings-anthropic-claude/anthropic-claude-sonnet-5_entry-0048.md)**
   * *Domains:* Rate And State Fault Friction & Short Term Synaptic Plasticity
   * *Reject-vote share:* 11% (1/9 reviewers)

[See all 24 →](indexes/stage-3-queue.md)

### How to help
**If an entry in the [Stage 3 queue](indexes/stage-3-queue.md) touches your field, the ask is about twenty minutes.** Open an issue, or comment on the entry, answering either question:

1. **Does the correspondence hold?** Not "is it interesting" — does the mathematics survive contact with the constitutive details of your field, or does it break at the boundary conditions? A specific "no, this fails because X" is worth more than a confirmation.
1. **Does it already exist?** If this connection is already in your literature under some name, say so and cite it. That's a Stage 3 result and it retires the entry cleanly.

You do not need to review the whole dataset, run the pipeline, or open a pull request. One entry, one answer.