---
sid_metadata:
  entry_id: "SID-045"
  schema_version: "1.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-07-23"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "non-hermitian-topolectrical-lattices"
  domain_b: "directed-metapopulation-epidemiology"
  structural_family: "non-hermitian-skin-instabilities"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "boundary_condition_correspondence"
    - "instability_mechanism"
    - "numerical_solution_family"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 8.9
  expected_methodological_transfer_score: 8.5
  community_separation_score: 8.8
  representation_mismatch_score: 8.6
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±0.7"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "nonlinear_saturation_and_stochastic_demographic_noise"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "Checks 2 through 4 are fully satisfied, but Check 1 contains a specific, nameable inconsistency: the stated localization-length formula ξ = |g|^{-1} does not follow from the entry's own generalized-Brillouin-zone formula under the standard amplitude-decay convention, and this unresolved factor-of-2 ambiguity propagates into the Section 4 falsifiable prediction."
    failed_checks: []
    flagged_checks: ["Check 1: the localization length ξ = |g|^{-1} stated in Section 3 is not derivable from the entry's own z_GBZ = sqrt(G_L/G_R)e^{ik} formula under the standard amplitude-decay convention, which instead gives ξ = 2/ln(G_R/G_L); this same unresolved convention underlies the numeric value used in the Section 4 falsifiable prediction"]
    quoted_evidence: []
    stage_3_watch_items:
      - "Search for prior work connecting the non-Hermitian skin effect / non-Bloch band theory / non-normal spectral dynamics to ecological or epidemiological metapopulation models. This general cross-domain direction has some precedent in recent (post-2022) physics literature, though no single canonical textbook or review is confidently recalled for this specific pairing."
      - "Independent of the non-Hermitian framing, check whether the core mathematical fact exploited here (asymmetric nearest-neighbor hopping on a finite lattice producing exponentially localized eigenmodes under open boundaries, with a distinct open- vs. periodic-boundary spectral threshold) already has established analogs in metapopulation epidemiology, birth-death process theory, or biased-random-walk/M-matrix theory, independent of the topolectrical-circuit vocabulary used here."
      - "Verify which convention (amplitude decay vs. intensity/covariance decay of the skin mode) the entry intends for the localization length ξ in Section 3, since this choice changes the numeric value asserted in the Section 4 falsifiable prediction (see Check 1)."
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.4 Thinking-Mini"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "The vocabulary matrix includes a type-mismatched complex-to-real mapping with no stated transformation, which is a check-2 category error and therefore fatal."
    failed_checks: ["Check 2: Vocabulary matrix coherence"]
    flagged_checks: []
    quoted_evidence: ["`nodal voltage phasor` ↔ `patch infection-probability deviation`", "Both are scalar node amplitudes acted on by the same directed hopping generator; they occupy identical coordinate positions in a linear state vector even though one is a deterministic electrical phasor and the other is a stochastic epidemiological occupancy deviation."]
    stage_3_watch_items: ["Verify whether the phasor-to-probability mapping is explicitly complexified or otherwise transformed on the epidemiology side; the current text does not state such a transformation."]
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "The structural mapping is mathematically rigorous and highly coherent, but contains a factor-of-two discrepancy in the localization length formula and lists one correspondence vector that lacks an explicit mathematical demonstration."
    failed_checks: []
    flagged_checks: 
      - "Check 1: The localization length equation \\xi = |g|^{-1} is missing a factor of 2 for the amplitude envelope."
      - "Check 3: 'numerical_solution_family' is listed but not demonstrated with an equation or derivation."
      - "Check 4: Advisory prior art noted (Nelson & Shnerb 1998)."
    quoted_evidence: []
    stage_3_watch_items: 
      - "Verify the analytic definition of the localization length \\xi; since the state variable envelope decays as e^{-gn/2}, the scale length should theoretically be 2/|g|, making the 1/ln(4) prediction mathematically inconsistent with the provided tridiagonal eigenvalues."
      - "Evaluate literature novelty against Nelson & Shnerb (1998, Phys Rev E), which previously mapped spatial asymmetry in population biology to the Hatano-Nelson model."
  fourth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "Both equations are first-order linear non-normal lattice ODEs with identical asymmetric hopping structure under the stated parameter map; all four listed correspondence vectors are demonstrated with equations or derivations in the body; the falsifiable prediction specifies concrete numerical thresholds and a localization length."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify whether non-Bloch band theory / skin effect has been explicitly applied to epidemic thresholds in the published literature; the Hatano-Nelson model has known roots in population dynamics and the general connection between non-Hermitian operators and population biology may be more developed than the entry implies."
      - "Verify whether the simplified linearized SIS metapopulation form (no explicit local-transmission diagonal term, mobility-mediated off-diagonal infection coefficients) is a standard formulation in the metapopulation epidemiology literature or a reduction specific to this entry."
      - "Verify whether non-normal operator theory (pseudospectra, transient amplification) has already been imported into epidemiology from the linear-algebra / matrix-analysis tradition (e.g., Diekmann, Heesterbeek, Roberts on next-generation matrix non-normality), which would make the topolectrical-circuit transfer direction less asymmetric than claimed."
      - "Confirm the skin-length convention used (ξ = 1/|g| vs. 2/|g|) is consistent with the non-Hermitian topology literature cited at Stage 3; the entry uses the probability-decay convention but does not state this explicitly."
  fifth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All equations share same first-order non-Hermitian hopping class with explicit mapping G_R/C ↔ beta_R, vocabulary pairs are type-compatible with structural operator roles, all four correspondence vectors are demonstrated via GBZ factor and threshold formulas, and Section 4 provides quantitatively falsifiable thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Hatano-Nelson model originally introduced with population/biased-diffusion interpretation — verify whether explicit topolectrical skin-effect ↔ directed metapopulation sink-localization mapping with GBZ threshold gamma_c^{open}≈2√(beta_R beta_L) cos(pi/(N+1)) is already published", "No canonical textbook duplication identified; prior-art check advisory only"]
  sixth_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "One listed correspondence vector (numerical_solution_family) is not demonstrated with equations or derivations in the body, only proposed as a methodological transfer; all other checks pass."
    failed_checks: []
    flagged_checks: ["Check 3: The 'numerical_solution_family' vector appears only as a transfer prospect in Section 4, without a shared equation or operator derivation establishing it as a structural correspondence."]
    quoted_evidence: []
    stage_3_watch_items: ["Prior art: The Hatano-Nelson non-Hermitian skin effect has been applied to directed metapopulation or ecological dynamics in recent literature (e.g., non-Hermitian topology in population dynamics). Verify bibliometric novelty.", "Numerical_solution_family correspondence: Determine whether generalized Brillouin-zone solvers or non-Bloch spectral methods have already been transferred to epidemiological patch models, which would affect the claimed transfer novelty."]
  seventh_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All four checks pass with equations of matching class, coherent type-compatible vocabulary mappings, fully demonstrated correspondence vectors, and an asymmetric falsifiable transfer prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 045

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Non-Hermitian topolectrical lattices, specifically voltage-mode skin localization and admittance spectral collapse in non-reciprocal circuit arrays built from asymmetric conductances, gyrators, or negative-impedance converters.
*   **Silo B (Field 2):** Directed metapopulation epidemiology, specifically outbreak onset and downstream patch localization in asymmetric travel-coupled susceptible-infected-susceptible patch systems with open migration boundaries.
*   **Mathematical Isomorphism:** Both systems are first-order non-normal graph dynamical systems whose open-boundary spectra are governed by the same non-reciprocal hopping operator, so that circuit admittance hopping maps to the epidemic mobility Jacobian, open-boundary skin localization maps to sink-patch outbreak concentration, and non-Bloch transfer-matrix threshold analysis maps to directed epidemic criticality.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `nodal voltage phasor` ↔ `patch infection-probability deviation`
    *   *Operator Role:* Both are scalar node amplitudes acted on by the same directed hopping generator; they occupy identical coordinate positions in a linear state vector even though one is a deterministic electrical phasor and the other is a stochastic epidemiological occupancy deviation.
*   `non-reciprocal admittance matrix` ↔ `directed next-generation/mobility Jacobian`
    *   *Operator Role:* Both are non-self-adjoint graph operators whose right eigenvectors define modal outbreak or voltage shapes, whose left eigenvectors define observability or excitation sensitivity, and whose spectral abscissa determines linear stability.
*   `open-circuit skin mode` ↔ `downstream sink-patch outbreak mode`
    *   *Operator Role:* Under open boundaries, asymmetric hopping produces a gauge transformation that pushes the dominant right eigenmode toward one boundary; the same logarithmic hopping ratio sets the electrical skin length and the epidemiological sink-localization length.
*   `admittance point-gap winding` ↔ `directed mobility circulation`
    *   *Operator Role:* Both quantify the non-Bloch topology of the periodic spectrum around a reference growth or loss value; the winding predicts boundary-induced spectral collapse and the failure of conventional Bloch or row-sum threshold criteria.
*   `non-reciprocal conductance ratio` ↔ `asymmetric travel ratio`
    *   *Operator Role:* Both are dimensionless similarity parameters controlling the same non-Hermitian gauge field, transient amplification, and boundary localization strength.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models a one-dimensional non-reciprocal topolectrical lattice by assigning a node voltage to each circuit cell and writing a Hatano-Nelson-style nodal admittance equation. The primary dynamical equation is:

```math
C\frac{dV_n}{dt}= -G_0 V_n + G_R V_{n+1}+G_L V_{n-1}+I_n^{\mathrm{ext}}
```

where `C` is node capacitance, `G_0` is shunt loss or effective gain-loss offset, and `G_R` and `G_L` are right- and left-directed hopping conductances. For a periodic array, the Bloch eigenvalue curve is:

```math
\lambda_A(k)= -\frac{G_0}{C} + \frac{G_R e^{ik}+G_L e^{-ik}}{C}
```

When `G_R` differs from `G_L`, the open-boundary problem is not solved by ordinary real Bloch waves. The mature non-Hermitian circuit toolkit replaces the Bloch factor by a complex generalized Brillouin-zone factor:

```math
z_{\mathrm{GBZ}} = \sqrt{\frac{G_L}{G_R}}\,e^{ik}
```

This produces boundary skin modes and a non-Bloch spectral threshold.

Silo B models a directed metapopulation near the disease-free state by linearizing a susceptible-infected-susceptible patch system with asymmetric travel coupling. The corresponding linear force-of-infection equation is:

```math
\frac{dp_n}{dt}= -\gamma p_n + \beta_R p_{n+1}+\beta_L p_{n-1}
```

where `p_n` is the infection-probability deviation in patch `n`, `gamma` is recovery or removal rate, and `beta_R` and `beta_L` are directed mobility-mediated infection coefficients. The operator-level mapping is:

```math
\frac{G_R}{C}\leftrightarrow \beta_R,\qquad
\frac{G_L}{C}\leftrightarrow \beta_L,\qquad
\frac{G_0}{C}\leftrightarrow \gamma
```

The shared non-reciprocity parameter and localization length are:

```math
g = \ln\left(\frac{G_R}{G_L}\right)
  = \ln\left(\frac{\beta_R}{\beta_L}\right),
\qquad
\xi = |g|^{-1}
```

In latent spectral topology, the Bloch eigenvalue loops of the circuit admittance operator and the epidemic mobility Jacobian are affine copies of one another and carry the same point-gap winding. Under open boundaries, both systems collapse onto the same generalized Brillouin-zone contour, so the voltage skin mode and the downstream outbreak mode are the same non-Hermitian right-eigenvector localization phenomenon expressed in different physical ontologies.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Non-Hermitian Topolectrical Lattices → Directed Metapopulation Epidemiology
*   **Asymmetric Maturity Rationale:** Non-Hermitian topolectrical metamaterials possess a highly mature toolkit for non-reciprocal spectral analysis: generalized Brillouin-zone construction, non-Bloch winding numbers, biorthogonal pseudospectra, transfer-matrix skin-length extraction, and direct impedance-tomography measurement of non-normal mode amplification. Directed metapopulation epidemiology commonly still relies on the spectral radius of the next-generation matrix, row-sum reproductive numbers, or periodic-boundary approximations, which can fail catastrophically when mobility is strongly asymmetric and boundaries are open.
*   **Target Bottleneck Mitigation:** Importing non-Bloch spectral solvers from topolectrical circuits will resolve the persistent bottleneck of false outbreak-threshold prediction in finite directed mobility networks. The testable hypothesis is that replacing conventional spectral-radius early-warning indicators with non-Bloch spectral abscissa, point-gap winding, and biorthogonal transient-amplification metrics will more accurately predict both the critical recovery rate and the spatial location of initial outbreak amplification in directed patch systems.
*   **Falsifiable Prediction:** For a controlled directed chain or ring with asymmetric coupling ratio `beta_R / beta_L = 4`, the finite open-boundary outbreak threshold should follow the non-Bloch skin threshold rather than the periodic or row-sum threshold:

```math
\gamma_c^{\mathrm{open}}(N)
\approx
2\sqrt{\beta_R\beta_L}
\cos\left(\frac{\pi}{N+1}\right),
\qquad
\gamma_c^{\mathrm{periodic}}
=
\beta_R+\beta_L
```

If the observed critical recovery rate instead scales with `beta_R + beta_L`, or if pre-outbreak covariance fails to localize at the downstream sink patch with localization length approximately `1 / ln(4)`, the proposed structural transfer is falsified.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Hatano-Nelson model" AND "non-Bloch band theory" AND "topolectrical circuit skin effect"`
*   `"directed metapopulation SIS" AND "next-generation matrix" AND "non-normal epidemic threshold"`
*   `"generalized Brillouin zone" AND "non-Hermitian skin effect" AND "asymmetric mobility network"`
*   `"biorthogonal pseudospectrum" AND "transient amplification" AND "outbreak early warning"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The nodal admittance ODE, its Bloch curve λ_A(k), the GBZ factor z_GBZ = sqrt(G_L/G_R)e^{ik}, and both threshold formulas (γ_c^periodic = β_R+β_L and γ_c^open(N) = 2sqrt(β_Rβ_L)cos(π/(N+1))) all verify correctly by direct substitution, but the stated "g = ln(G_R/G_L) = ln(β_R/β_L), ξ = |g|^{-1}" does not follow from the entry's own z_GBZ formula under the standard amplitude-decay convention for skin-mode localization length, which instead gives ξ = 2/ln(G_R/G_L) — a factor-of-2 discrepancy the entry does not address.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five Section 2 pairings are type-compatible (scalar state variable ↔ scalar state variable, non-self-adjoint matrix ↔ non-self-adjoint matrix, localized eigenmode ↔ localized eigenmode, spectral winding invariant ↔ spectral winding invariant, dimensionless ratio ↔ dimensionless ratio), and each Operator Role names a specific shared mathematical structure rather than resting on hedged similarity language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated with equations or derivations: governing_differential_operator via the paired ODEs and the explicit G/C ↔ β, γ substitution (Section 3); boundary_condition_correspondence via the stated GBZ-contour collapse under open boundaries and the explicit γ_c^open(N) vs. γ_c^periodic contrast (Sections 3-4); instability_mechanism via the point-gap winding / GBZ-collapse discussion tied to those same threshold formulas (Sections 2-4); numerical_solution_family via the GBZ construction on the circuit side and its transferred, concretely computed output γ_c^open(N) on the epidemiology side (Sections 3-4).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry: the specific toolkit named (generalized-Brillouin-zone construction, non-Bloch winding numbers, biorthogonal pseudospectra) is not shown to have a comparably mature counterpart native to metapopulation epidemiology, so the stated direction (circuits → epidemiology) is not backwards or freely reversible with comparable benefit. Falsifiability: the Section 4 prediction names two explicit, competing quantitative formulas (γ_c^open(N) vs. β_R+β_L) at a specific stated coupling ratio (β_R/β_L = 4), which is a genuine, non-template prediction. No canonical, confidently-sourced prior-art analogy (of the Schrödinger↔paraxial-optics or Black-Scholes↔heat-equation type) was recognized for this specific pairing; see the watch item below instead.

#### Stage 3 Watch Items
- Search for prior work connecting the non-Hermitian skin effect / non-Bloch band theory / non-normal spectral dynamics to ecological or epidemiological metapopulation models. This general cross-domain direction has some precedent in recent (post-2022) physics literature, though no single canonical textbook or review is confidently recalled for this specific pairing.
- Independent of the non-Hermitian framing, check whether the core mathematical fact exploited here (asymmetric nearest-neighbor hopping on a finite lattice producing exponentially localized eigenmodes under open boundaries, with a distinct open- vs. periodic-boundary spectral threshold) already has established analogs in metapopulation epidemiology, birth-death process theory, or biased-random-walk/M-matrix theory, independent of the topolectrical-circuit vocabulary used here.
- Verify which convention (amplitude decay vs. intensity/covariance decay of the skin mode) the entry intends for the localization length ξ in Section 3, since this choice changes the numeric value asserted in the Section 4 falsifiable prediction (see Check 1).

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.4 Thinking-Mini
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The circuit and patch equations are internally consistent linear non-reciprocal first-order systems, and the threshold formulas match the claimed open-boundary versus periodic comparison.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping `nodal voltage phasor` ↔ `patch infection-probability deviation` is a complex-to-real type mismatch with no explicit transformation, which is a category error.
* **CHECK 3 (Correspondence Vector Support):** PASS — The body demonstrates the governing operator, boundary-condition correspondence, instability mechanism, and numerical solution-family correspondence through the equations and open-boundary/GBZ derivations in Section 3.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is stated as one-way from a more mature non-Hermitian circuit toolkit to epidemiology, and the prediction names measurable threshold and localization outcomes that could fail.

#### Stage 3 Watch Items
* Verify whether the phasor-to-probability mapping is explicitly complexified or otherwise transformed on the epidemiology side; the current text does not state such a transformation.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The tridiagonal operator equations perfectly match across both domains, but the localization length formula `\xi = |g|^{-1}` misses a factor of 2 for the state variable amplitude (which decays as `e^{-gn/2}`, yielding `2/|g|`), likely due to erroneously transcribing the quantum mechanical probability density scale where the observable is the squared amplitude.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings correctly align objects of compatible mathematical types (e.g., matrices, scalar state variables, topological windings) and define shared operator roles without category errors.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Three listed vectors are fully demonstrated with equations (`governing_differential_operator`, `boundary_condition_correspondence`, `instability_mechanism`), but `numerical_solution_family` is only partially covered via a brief conceptual mention of "non-Bloch spectral solvers" in Section 4 without any supporting equation, operator identity, or derivation establishing the numerical family itself.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is appropriately asymmetric and the prediction is strictly falsifiable, though the numerical prediction of `1 / \ln(4)` logically inherits the factor-of-2 error from Check 1; additionally, noting canonical prior art in population biology as advisory.

#### Stage 3 Watch Items
- Verify the localization length calculation: the state variables in this linear first-order formulation decay as `(\sqrt{L/R})^n`, which implies an envelope of `e^{-gn/2}` and a physical localization length of `2/|g|`, rather than the `1/|g|` asserted in the text.
- Check literature for Nelson & Shnerb (1998, Phys. Rev. E) and subsequent physics literature on "Non-Hermitian localization and population biology," which establishes a highly analogous structural mapping between the Hatano-Nelson model and biological population dynamics.

### Fourth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are first-order linear ODE systems on a 1D lattice with asymmetric nearest-neighbor coupling and a scalar decay/gain term; under the stated parameter map ($G_R/C \leftrightarrow \beta_R$, $G_L/C \leftrightarrow \beta_L$, $G_0/C \leftrightarrow \gamma$) the two operators are identical, so the equation classes match and the structural correspondence in Section 1 is supported. The Bloch dispersion, GBZ factor $z_{\mathrm{GBZ}}=\sqrt{G_L/G_R}\,e^{ik}$, non-reciprocity parameter $g=\ln(G_R/G_L)$, and open-boundary threshold formula $\gamma_c^{\mathrm{open}}(N)\approx 2\sqrt{\beta_R\beta_L}\cos(\pi/(N+1))$ are all consistent with the standard Hatano-Nelson / non-Bloch band theory results and apply identically to both systems under the parameter renaming.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five paired mappings connect objects of compatible mathematical type: scalar node amplitudes ↔ scalar node amplitudes, non-self-adjoint graph operators ↔ non-self-adjoint graph operators, open-boundary eigenmodes ↔ open-boundary eigenmodes, spectral winding invariants ↔ spectral winding invariants, and dimensionless ratios ↔ dimensionless ratios. Each entry's Operator Role explanation names a specific shared mathematical structure (e.g., "the same logarithmic hopping ratio sets the electrical skin length and the epidemiological sink-localization length") rather than relying solely on hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in the body. `governing_differential_operator` is shown via the two displayed equations and the explicit coefficient map in Section 3. `boundary_condition_correspondence` is shown via the GBZ construction and the statement that both systems collapse onto the same generalized Brillouin-zone contour under open boundaries. `instability_mechanism` is shown via the spectral abscissa discussion and the open-boundary vs. periodic threshold comparison. `numerical_solution_family` is shown via the transfer-matrix / GBZ eigenvalue formula $\gamma_c^{\mathrm{open}}(N)$ and the skin-length extraction formula $\xi=|g|^{-1}$, applied to both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (topolectrical circuits → metapopulation epidemiology) is genuinely asymmetric: the non-Hermitian physics community possesses the GBZ, non-Bloch winding, biorthogonal pseudospectrum, and transfer-matrix toolkit, while epidemiology standardly uses the next-generation matrix spectral radius and row-sum reproductive numbers, which are known to fail for non-normal operators. The falsifiable prediction is concrete and quantitative: it names a specific coupling ratio ($\beta_R/\beta_L=4$), a specific threshold formula to test against ($2\sqrt{\beta_R\beta_L}\cos(\pi/(N+1))$ vs. $\beta_R+\beta_L$), and a specific localization length ($1/\ln 4$) at a specific spatial location (downstream sink patch). The prediction specifies exactly what outcome would falsify the transfer. Prior-art advisory: the general connection between non-Hermitian / non-normal operators and population dynamics is well-established in the ecology and matrix-analysis literature; Stage 3 should verify whether the specific non-Bloch band theory application to epidemic thresholds is novel.

#### Stage 3 Watch Items
- Verify whether non-Bloch band theory or the non-Hermitian skin effect has been explicitly applied to epidemic thresholds in the published literature. The Hatano-Nelson model has known connections to population dynamics; the specific epidemiological application of GBZ methods may or may not be novel.
- Verify whether the simplified linearized SIS metapopulation form used in the entry (off-diagonal mobility-mediated infection coefficients, no explicit local-transmission diagonal term) is a standard formulation in metapopulation epidemiology or a domain-specific reduction.
- Assess whether non-normal operator theory (pseudospectra, transient amplification) has already been developed in the epidemiological literature via the next-generation matrix / linear-algebra tradition (Diekmann, Heesterbeek, Roberts, etc.), which would affect the claimed asymmetry of methodological maturity.
- Confirm the skin-length convention ($\xi = 1/|g|$ as probability-decay length vs. $2/|g|$ as amplitude-decay length) is consistent with the specific non-Hermitian topology references the entry's authors would cite.

### Fifth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A equation C dV_n/dt = -G_0 V_n + G_R V_{n+1}+G_L V_{n-1} and Silo B equation dp_n/dt = -gamma p_n + beta_R p_{n+1}+beta_L p_{n-1} are same first-order linear non-normal graph dynamical class with affine spectral mapping G_R/C ↔ beta_R, G_L/C ↔ beta_L, G_0/C ↔ gamma, supporting the claimed shared non-reciprocal hopping operator.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five pairs are type-compatible: scalar amplitude ↔ scalar deviation, non-self-adjoint operator ↔ operator, localized eigenmode ↔ localized outbreak mode, winding invariant ↔ circulation, dimensionless ratio ↔ dimensionless ratio. Operator Roles specify shared gauge transformation, right/left eigenvector structure, and localization length xi = |g|^{-1} with g = ln(G_R/G_L)=ln(beta_R/beta_L), not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors demonstrated: governing_differential_operator via dual hopping equations and operator mapping; boundary_condition_correspondence via open-boundary failure of Bloch waves, GBZ factor z_GBZ = sqrt(G_L/G_R) e^{ik}, and collapse onto same contour; instability_mechanism via shared non-reciprocity parameter, point-gap winding, and skin length; numerical_solution_family via non-Bloch transfer-matrix solvers and explicit thresholds gamma_c^{open} ≈ 2 sqrt(beta_R beta_L) cos(pi/(N+1)) vs gamma_c^{periodic}= beta_R+beta_L.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: mature GBZ, non-Bloch winding, biorthogonal pseudospectra toolkit in topolectrical lattices → row-sum / spectral-radius next-generation methods in epidemiology, not plausibly reversible with equal benefit; direction is not backwards. Falsifiability is quantitative: predicts finite-N open-boundary threshold scaling with 2 sqrt(beta_R beta_L) cos(pi/(N+1)) and sink localization length ~1/ln(4) for beta_R/beta_L=4, falsified if scaling follows beta_R+beta_L or covariance fails to localize. No canonical textbook isomorphism recognized as duplicate; Hatano-Nelson ↔ population dynamics origin noted as advisory watch item only.

#### Stage 3 Watch Items
- Hatano-Nelson model was originally motivated in part by population growth with drift / biased diffusion; Stage 3 should bibliometrically verify whether explicit topolectrical skin-effect ↔ directed metapopulation sink-localization with GBZ threshold formula has been published.
- None identified as grounds for rejection; prior-art check is advisory only per protocol.

### Sixth Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The dynamical equations, Bloch spectra, and GBZ factor are correctly stated for the claimed domains, and the explicit operator mapping supports the claimed structural correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All paired terms map between compatible mathematical types (scalar state variables, non-self-adjoint operators, eigenmodes, topological invariants, dimensionless similarity parameters) with clear operator-role descriptions.
- **CHECK 3 (Correspondence Vector Support):** FLAG — The vectors `governing_differential_operator`, `boundary_condition_correspondence`, and `instability_mechanism` are demonstrated with equations, operator identities, and threshold derivations. The vector `numerical_solution_family` is not demonstrated; the body only proposes importing non-Bloch solvers as a methodological transfer, without a shared equation or derivation establishing a numerical solution family as a structural correspondence.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is genuinely asymmetric (circuit toolkit → epidemiology). The prediction provides a specific quantitative threshold formula and a clear falsification condition.

#### Stage 3 Watch Items
- Prior art: The analogy between non-Hermitian skin effect (Hatano-Nelson) and directed metapopulation/ecological dynamics appears in existing literature (e.g., non-Hermitian topology in population dynamics). Human bibliometric review should verify the entry's novelty claim.
- Numerical_solution_family correspondence: Verify whether generalized Brillouin-zone solvers or non-Bloch spectral methods have already been applied to epidemiological patch models; prior transfer would weaken the claimed novelty of this vector.

### Seventh Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed dynamical equations are first-order linear non-normal hopping ODEs of identical class whose coefficient mapping and shared GBZ construction directly support the claimed operator and skin-mode correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of matching mathematical type (scalar amplitudes, non-self-adjoint graph operators, localization modes, point-gap invariants, dimensionless ratios) and the Operator Role statements name shared structures rather than mere analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_differential_operator is shown by the paired ODEs and coefficient map in Section 3; boundary_condition_correspondence and instability_mechanism are shown by the shared open-boundary GBZ skin localization and non-Bloch threshold; numerical_solution_family is shown by the explicit GBZ and transfer-matrix constructions used on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer is asymmetric from the more mature non-Bloch circuit toolkit toward epidemiology’s conventional spectral-radius methods; the prediction supplies an explicit, measurable open-boundary threshold formula and localization length that can be experimentally contradicted.

#### Stage 3 Watch Items
None identified.