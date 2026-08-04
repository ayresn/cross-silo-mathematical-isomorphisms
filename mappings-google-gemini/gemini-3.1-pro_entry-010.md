---
sid_metadata:
  entry_id: "SID-010"
  schema_version: "1.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Google"
  model_family: "Gemini"
  model_version: "3.1 Pro"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "transformation-optics"
  domain_b: "macroscopic-pedestrian-dynamics"
  structural_family: "anisotropic-eikonal-wave-propagation"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "symmetry_groups"
    - "conserved_quantities"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / physical_electromagnetic_fields_vs_discrete_cognitive_human_agents / distinct_disciplinary_language"
prior_discovery_metrics:
  structural_isomorphism_score: 9.6
  vocabulary_divergence_score: 9.4
  expected_methodological_transfer_score: 9.8
  community_separation_score: 9.9
  representation_mismatch_score: 9.7
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 9.3
    uncertainty: "±0.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "panic_induced_breakdown_of_eikonal_rational_pathfinding"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "Only one of the three listed correspondence vectors (governing_differential_operator) is demonstrated by an equation; symmetry_groups and conserved_quantities are each asserted only in prose with no equation, operator identity, or derivation anywhere in the entry, leaving fewer than three vectors demonstrated as Check 3 requires."
    failed_checks: ["Check 3: fewer than three correspondence vectors demonstrated with an equation, operator identity, or derivation"]
    flagged_checks: []
    quoted_evidence: ["Both represent the fundamental symmetry group of the system. The equations retain their exact mathematical structure when the spatial grid is continuously deformed (e.g., tearing a hole in space to hide an object), provided the corresponding metric tensor is inversely scaled to compensate for the topological distortion.", "Both define the strictly conserved, directional transport of the underlying quantity (electromagnetic energy / human mass) along the orthogonal gradient of the potential field. The divergence of this vector dictates the temporal accumulation of density."]
    stage_3_watch_items: ["Search for prior work applying transformation-optics/metamaterial cloaking design to pedestrian, crowd, or granular flow control, and check this pairing against the established 'transformation X' cloaking analogy family (acoustic cloaking, thermal cloaking/transformation thermodynamics, elastodynamic cloaking).", "Section 3 shows only the eikonal/route-choice half of the Hughes pedestrian model — the coupled continuity equation for density ρ is never written out anywhere in the entry, so only the potential equation, not the full coupled system, has been compared.", "The falsifiable prediction's quantitative figures (scattering cross-section of zero, throughput increase of at least 35%) are asserted with no derivation or citation; verify whether they originate from an existing study or simulation."]
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.4 Thinking-Mini"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "The entry’s main mathematical correspondence is mostly consistent, but the conserved-quantity vector is only gestured at in prose and is not demonstrated by an equation or derivation on both sides."
    failed_checks: []
    flagged_checks: ["Check 3: conserved-quantity correspondence is only partially demonstrated"]
    quoted_evidence: []
    stage_3_watch_items:
      - "Section 2 and Section 3: verify that the Poynting-vector ↔ pedestrian-flux correspondence is backed by an explicit conservation law or operator identity, not just descriptive language."
  third_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "The two eikonal equations are structurally compatible and the core operator correspondence is sound, but the conserved_quantities correspondence vector is only verbally described without a supporting conservation equation in the body."
    failed_checks: []
    flagged_checks: ["Check 3: conserved_quantities vector is partially covered — the Poynting/flux conservation structure is described in the Section 2 vocabulary matrix but no conservation equation (Poynting's theorem or continuity equation) appears in Section 3 to establish the correspondence on both sides."]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether an anisotropic (tensor-valued) extension of the Hughes model has been published; the entry's Section 3 acknowledges the standard Hughes model is isotropic and that the anisotropic slowness tensor is introduced by the entry itself, yet Section 1 claims the Hughes model 'maps identically' to the optical eikonal.", "Check whether transformation-optics cloaking techniques have been applied to pedestrian dynamics or crowd-flow engineering in any prior publication.", "Probe the claimed directional correspondence: the vocabulary matrix states both the Poynting vector and pedestrian flux travel 'along the orthogonal gradient of the potential field,' but in anisotropic media the Poynting vector (energy flow direction) generally deviates from the wave-vector direction (phase gradient) — verify whether transformation-optics cloaks preserve collinearity of these directions.", "Assess whether the 35% throughput improvement prediction has any basis in existing crowd-flow simulation literature."]
  fourth_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "Only governing_differential_operator is demonstrated with equations; symmetry_groups and conserved_quantities are asserted only in prose, so fewer than three listed correspondence vectors are supported."
    failed_checks: ["Check 3: symmetry_groups and conserved_quantities are listed but not demonstrated by equations, operator identities, or derivations, leaving fewer than three demonstrated vectors"]
    flagged_checks: []
    quoted_evidence:
      - '    - "symmetry_groups"'
      - '    - "conserved_quantities"'
      - "Both represent the fundamental symmetry group of the system."
      - "The divergence of this vector dictates the temporal accumulation of density."
    stage_3_watch_items:
      - "Verify whether the Hughes model's density conservation law is required for the claimed isomorphism, since Section 3 displays only the route-choice Eikonal equation."
      - "Verify whether anisotropic transformation-optics media support the simple scalar metric Eikonal equation used here, and whether Poynting flux is intended as metric-dual to the phase gradient."
      - "Search for prior work on Eikonal or transformation-based crowd-flow control, obstacle cloaking, and anisotropic pedestrian slowness tensors."
  fifth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "Both displayed equations are valid anisotropic Eikonal (Hamilton-Jacobi) equations from their stated domains, vocabulary mappings are type-compatible second-rank tensors / conserved flux vectors / diffeomorphism groups with explicit shared structure, and all three correspondence vectors are demonstrated with falsifiable 35% throughput prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  sixth_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "Check 3 fails because the entry does not demonstrate the required correspondence vectors 'symmetry_groups' and 'conserved_quantities' with equations, operator identities, or derivations, leaving fewer than three vectors demonstrated."
    failed_checks: ["Check 3: Correspondence Vector Support — fewer than three vectors demonstrated; 'symmetry_groups' and 'conserved_quantities' are not demonstrated with equations, operator identities, or derivations."]
    flagged_checks: []
    quoted_evidence: ["Both define the strictly conserved, directional transport of the underlying quantity (electromagnetic energy / human mass) along the orthogonal gradient of the potential field. The divergence of this vector dictates the temporal accumulation of density.", "Both represent the fundamental symmetry group of the system. The equations retain their exact mathematical structure when the spatial grid is continuously deformed (e.g., tearing a hole in space to hide an object), provided the corresponding metric tensor is inversely scaled to compensate for the topological distortion."]
    stage_3_watch_items: ["Prior art: Hughes (2002) pedestrian model is based on an eikonal equation from geometric optics; the analogy between pedestrian potential and optical phase is a known canonical correspondence. Stage 3 should probe whether the anisotropic extension and transformation-optics cloaking transfer constitute a novel isomorphism or merely an incremental extension of a textbook analogy."]
  seventh_adversarial_review:
    reviewer_model: "xAI Grok 4.5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are matching anisotropic Eikonal operators supporting the claimed correspondence, vocabulary pairs are type-compatible with shared structure, all three listed vectors are demonstrated in the body, and transfer is asymmetric with a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 010

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Transformation Optics (Specifically: the design of metamaterial "invisibility cloaks" by applying coordinate transformations to manipulate the permittivity and permeability tensors of space).
*   **Silo B (Field 2):** Macroscopic Pedestrian Dynamics (Specifically: the continuum modeling of high-density crowd evacuation, bottleneck formation, and cognitive route-choice optimization).
*   **Mathematical Isomorphism:** The high-frequency geometric optics limit of Maxwell’s equations in an anisotropic metamaterial maps identically to the macroscopic Hughes continuum model for pedestrian crowd flow; both are governed by a diffeomorphism-invariant, non-linear Eikonal equation where the spatial warping of the optical metric tensor precisely corresponds to the localized architectural manipulation of cognitive crowd-friction, allowing crowd fluxes to be mathematically "cloaked" around obstacles.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Inverse Optical Metric Tensor ($g^{ij}$ or $\epsilon^{-1} \mu^{-1}$)** ↔ **Anisotropic Pedestrian Slowness Matrix ($\Lambda^{ij}$)**
    *   *Operator Role:* Both act as the spatially varying, second-rank tensor embedded within the Hamilton-Jacobi/Eikonal operator. They dictate the directional characteristic speed of the wave-front or crowd-front, determining exactly how the path of least time curves through the spatial domain.
*   **Poynting Vector ($\mathbf{S}$)** ↔ **Pedestrian Flux Vector ($\mathbf{J}$)**
    *   *Operator Role:* Both define the strictly conserved, directional transport of the underlying quantity (electromagnetic energy / human mass) along the orthogonal gradient of the potential field. The divergence of this vector dictates the temporal accumulation of density.
*   **Form Invariance (Coordinate Transformation)** ↔ **Obstacle Diffeomorphism (Architectural Mapping)**
    *   *Operator Role:* Both represent the fundamental symmetry group of the system. The equations retain their exact mathematical structure when the spatial grid is continuously deformed (e.g., tearing a hole in space to hide an object), provided the corresponding metric tensor is inversely scaled to compensate for the topological distortion.

## 3. CORE MATHEMATICAL PARALLELISM
In Transformation Optics, the propagation of light through a metamaterial is analyzed in the geometric optics limit using the Eikonal equation. To design an "invisibility cloak" (e.g., the Pendry cloak), a coordinate transformation is applied to map a point in virtual space to a physical volume (an annulus) hiding an object. Because Maxwell's equations are form-invariant, this distortion is encoded into an anisotropic inverse metric tensor $g^{ij}(\mathbf{x})$. The phase front $\Psi$ evolves over this warped manifold as:
```math
\sum_{i,j} g^{ij}(\mathbf{x}) \frac{\partial \Psi}{\partial x^i} \frac{\partial \Psi}{\partial x^j} = n_0^2
```

In Macroscopic Pedestrian Dynamics, the Hughes model treats a high-density crowd as a thinking fluid. Pedestrians attempt to minimize their travel time to an exit by continuously solving a cognitive potential field $\phi(\mathbf{x}, t)$ (route choice), while their actual density $\rho$ advects along the gradient of this field. By replacing the standard isotropic walking speed with an engineered architectural environment (e.g., varied floor textures or sub-obstacles), we introduce an anisotropic slowness tensor $\boldsymbol{\Lambda}(\rho, \mathbf{x})$. The crowd's cognitive route-choice is governed by a mathematically identical anisotropic Eikonal operator:
```math
\sum_{i,j} \Lambda^{ij}(\rho, \mathbf{x}) \frac{\partial \phi}{\partial x^i} \frac{\partial \phi}{\partial x^j} = \frac{1}{v_{max}^2}
```
In latent space topology, a crowd fluid flowing around a physical pillar is mathematically identical to a light wave striking an opaque cylinder. Left untreated, both create a massive "scattering cross-section"—in optics, a shadow and backscatter; in crowd dynamics, a deadly, backward-propagating high-density shockwave (crowd crush).

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Transformation Optics → Macroscopic Pedestrian Dynamics
*   **Asymmetric Maturity Rationale:** The metamaterials community has spent the last two decades developing exact analytical coordinate-transformation techniques to calculate the precise spatial gradients required to eliminate scattering cross-sections entirely. Conversely, architectural crowd control relies on heuristic "rule-of-thumb" obstacle placements (like placing a single circular pillar in front of an exit) or trial-and-error agent-based simulations that routinely fail to prevent phase-transition crush events in high-stakes environments like stadium stampedes or religious pilgrimages.
*   **Target Bottleneck Mitigation:** By directly importing the spatial metric tensor solutions of an optical invisibility cloak (specifically a 2D cylindrical cloak), architects can design a "pedestrian metamaterial." Instead of varying dielectric constants, they vary the spatial density of small, passive architectural bollards surrounding a primary structural column. This forces the crowd's slowness tensor to exactly match the optical metric, mathematically guiding the pedestrian flux vector smoothly around the column and perfectly recombining it on the other side without triggering a shockwave.
*   **Falsifiable Prediction:** In a high-density continuum simulation (or physical experiment using a rat-swarm analog), an impassable central column surrounded by a gradient array of micro-obstacles structurally mapped to a Pendry transformation-optics tensor will exhibit an effective kinematic scattering cross-section of zero. This will entirely prevent upstream density phase transitions (shockwaves) and increase total throughput by at least 35% compared to the state-of-the-art "streamlined" heuristic pillar designs.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"transformation optics" AND "diffeomorphism invariance" AND "Eikonal equation" AND "metric tensor"`
*   `"Hughes model" AND "pedestrian crowd dynamics" AND "anisotropic Eikonal" AND "macroscopic model"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are anisotropic-tensor eikonal/Hamilton-Jacobi-type PDEs (a rank-2 tensor contracted with the squared gradient of a scalar potential, set equal to a scalar), so the equation classes match between domains and support the eikonal-operator correspondence claimed in Section 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three Section 2 mappings pair type-compatible objects (tensor ↔ tensor, flux vector ↔ flux vector, coordinate transformation ↔ coordinate transformation), and each Operator Role names a specific shared mechanism rather than resting on hedged language alone.
- **CHECK 3 (Correspondence Vector Support):** FAIL — governing_differential_operator is demonstrated via the two eikonal PDEs displayed in Section 3; symmetry_groups is named only in Section 2's third mapping ("Form Invariance ↔ Obstacle Diffeomorphism") with no transformation equation shown anywhere in the entry; conserved_quantities is named only in Section 2's second mapping ("Poynting Vector ↔ Pedestrian Flux Vector") with no conservation or continuity equation shown anywhere in the entry — only one of three listed vectors is actually demonstrated, below the three-vector floor.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The stated direction (optics' mature analytical cloaking toolkit → heuristic-driven crowd control) is not backwards, and the prediction names concrete measurable outcomes (a scattering cross-section of zero, throughput increase of at least 35%) rather than a generic "might work better" template; no specific canonical prior-art pairing was recognized with confidence, though the broader cloaking-analogy family merits a Stage 3 check (see watch items).

#### Stage 3 Watch Items
- Search for prior work applying transformation-optics/metamaterial cloaking design to pedestrian, crowd, or granular flow control, and check this pairing against the established "transformation X" cloaking analogy family (acoustic cloaking, thermal cloaking/transformation thermodynamics, elastodynamic cloaking).
- Section 3 shows only the eikonal/route-choice half of the Hughes pedestrian model — the coupled continuity equation for density ρ is never written out anywhere in the entry, so only the potential equation, not the full coupled system, has been compared.
- The falsifiable prediction's quantitative figures (scattering cross-section of zero, throughput increase of at least 35%) are asserted with no derivation or citation; verify whether they originate from an existing study or simulation.

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.4 Thinking-Mini
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The two displayed equations are both anisotropic Eikonal-type operators and are consistent with the transformation-optics and Hughes-model descriptions given in Section 3.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped objects in Section 2 are type-compatible pairs of tensors, vectors, and transformations, and none is an obvious category error.
* **CHECK 3 (Correspondence Vector Support):** FLAG — `governing_differential_operator` and `symmetry_groups` are demonstrated in Section 3, but `conserved_quantities` is only described in prose via the Poynting/flux analogy and lacks an explicit conservation-law equation or derivation on both sides.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is stated as Transformation Optics → Macroscopic Pedestrian Dynamics, and the prediction names measurable outcomes (“effective kinematic scattering cross-section of zero” and “increase total throughput by at least 35%”), so it is falsifiable.

#### Stage 3 Watch Items
* Section 2 and Section 3: verify that the Poynting-vector ↔ pedestrian-flux correspondence is backed by an explicit conservation law or operator identity, not just descriptive language.

### Third Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are first-order nonlinear anisotropic eikonal (Hamilton-Jacobi) equations with rank-2 tensor coefficients; no equation-class mismatch exists, and the optical eikonal is correctly attributed to the geometric-optics limit of Maxwell's equations.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three vocabulary pairs map objects of compatible mathematical type (rank-2 tensor ↔ rank-2 tensor, flux vector ↔ flux vector, symmetry group ↔ symmetry group), and each operator-role entry names a specific shared structure rather than relying on hedged language.
- **CHECK 3 (Correspondence Vector Support):** FLAG — The `governing_differential_operator` vector is fully demonstrated by the two eikonal equations in Section 3, and `symmetry_groups` is supported by the shared general-tensor form of both equations (which establishes covariance under diffeomorphism). However, `conserved_quantities` is only partially covered: the Section 2 vocabulary matrix describes the Poynting-vector ↔ pedestrian-flux conservation structure verbally ("The divergence of this vector dictates the temporal accumulation of density"), but Section 3 presents no conservation equation — neither Poynting's theorem nor the pedestrian continuity equation — to establish the correspondence on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is genuinely asymmetric: transformation optics possesses a mature, two-decade-old analytical coordinate-transformation toolkit for metric-tensor design, while crowd-obstacle placement relies on heuristics. The falsifiable prediction is specific and quantitative: a "gradient array of micro-obstacles structurally mapped to a Pendry transformation-optics tensor" must yield "an effective kinematic scattering cross-section of zero" and "increase total throughput by at least 35%," both of which are measurable outcomes that could fail to hold. No canonical textbook prior-art pairing between transformation optics and pedestrian dynamics was recognized.

#### Stage 3 Watch Items
- Verify whether an anisotropic (tensor-valued) extension of the Hughes model has been published. The entry's Section 3 states: "By replacing the standard isotropic walking speed with an engineered architectural environment … we introduce an anisotropic slowness tensor," acknowledging that the standard Hughes model is isotropic. Yet Section 1 claims the Hughes model "maps identically" to the optical eikonal. Determine whether this anisotropic extension is the entry's own proposal or builds on existing work.
- Check whether transformation-optics cloaking techniques have been applied to pedestrian dynamics or crowd-flow engineering in any prior publication.
- Probe the claimed directional correspondence in the vocabulary matrix: "Both define the strictly conserved, directional transport of the underlying quantity … along the orthogonal gradient of the potential field." In anisotropic media, the Poynting vector (energy-flow direction) generally deviates from the wave-vector direction (phase gradient). Verify whether the specific cloak geometries discussed preserve collinearity of these directions, or whether the directional claim is an unstated restriction to isotropic sub-cases.
- Assess whether the 35% throughput improvement prediction and the "zero scattering cross-section" claim have any precedent or supporting evidence in crowd-flow simulation literature.

### Fourth Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The two displayed equations are both first-order Eikonal/Hamilton-Jacobi equations with spatial tensor coefficients, so there is no equation-class mismatch between the displayed optical and pedestrian operators.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired terms are mathematically compatible types (tensor↔tensor, flux vector↔flux vector, transformation/symmetry↔transformation/symmetry), and the roles name shared structures rather than only hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The entry lists `- "symmetry_groups"` and `- "conserved_quantities"`, but the only support is prose saying "Both represent the fundamental symmetry group of the system" and "The divergence of this vector dictates the temporal accumulation of density"; no transformation law/invariance identity or conservation equation is given, so only `governing_differential_operator` is demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The stated Transformation Optics → Pedestrian Dynamics transfer is asymmetric in the entry's own description, and the prediction names measurable outcomes (zero effective scattering cross-section, no upstream shockwaves, ≥35% throughput increase); no canonical prior-art pairing is recognized, but related Eikonal crowd models should be checked.

#### Stage 3 Watch Items
- Verify whether the Hughes model's density conservation law is required for the claimed isomorphism, since Section 3 displays only the route-choice Eikonal equation.
- Verify whether anisotropic transformation-optics media support the simple scalar metric Eikonal equation used here, and whether Poynting flux is intended as metric-dual to the phase gradient.
- Search for prior work on Eikonal or transformation-based crowd-flow control, obstacle cloaking, and anisotropic pedestrian slowness tensors.

### Fifth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both equations are presented as anisotropic Eikonal equations sum g^{ij} ∂iΨ ∂jΨ = n0^2 and sum Λ^{ij} ∂iφ ∂jφ = 1/v_max^2, correctly typed as first-order nonlinear Hamilton-Jacobi from transformation optics and Hughes pedestrian models, same operator class, no elliptic/parabolic/hyperbolic or linear/nonlinear mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairs are type-compatible: tensor↔tensor (g^{ij} ↔ Λ^{ij}) with shared Eikonal-operator role, vector↔vector (Poynting S ↔ Pedestrian flux J) with explicit conservation/divergence role, and symmetry group↔symmetry group (Form Invariance ↔ Obstacle Diffeomorphism) with explicit structure-preservation under spatial deformation; no spatial-domain↔time-point or rate↔position category errors and no hedged-only assertions.
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_differential_operator demonstrated in Section 3 by the paired Eikonal equations; symmetry_groups demonstrated in Section 2 (Operator Role: equations retain exact structure under continuous deformation) and Section 1/3 (diffeomorphism-invariant, form-invariance, Pendry cloak mapping); conserved_quantities demonstrated in Section 2 via the Poynting/Flux vector mapping stating divergence dictates temporal accumulation, referenced in Section 1 (crowd fluxes cloaked) and Section 3 (density advects along gradient).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: Transformation Optics → Pedestrian Dynamics with rationale of mature analytical coordinate-transformation toolkit versus heuristic trial-and-error in crowd architecture, not plausibly reversible with comparable benefit. Falsifiability is specific: zero effective kinematic scattering cross-section, prevention of upstream density phase transitions, and ≥35% throughput increase over heuristic pillar designs in simulation or rat-swarm analog, with measurable quantities and threshold. No canonical textbook prior-art pairing recognized.

#### Stage 3 Watch Items
None identified.

### Sixth Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed Eikonal equations correctly model the claimed anisotropic geometric optics and Hughes-type pedestrian potential, with no equation-class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All token pairs map objects of compatible mathematical type (tensor ↔ tensor, vector ↔ vector, symmetry mapping ↔ symmetry mapping) without category errors.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The listed vectors 'symmetry_groups' and 'conserved_quantities' are not demonstrated with equations, operator identities, or derivations in the body. The entry only asserts the roles in prose (e.g., “Both define the strictly conserved, directional transport …” and “Both represent the fundamental symmetry group …”) without providing any conservation law or explicit symmetry transformation. Only 'governing_differential_operator' is demonstrated via the Eikonal equations in Section 3. Thus fewer than three vectors are demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric, and the prediction names a specific measurable outcome (zero scattering cross-section, ≥35% throughput increase) that is falsifiable.

#### Stage 3 Watch Items
- Prior art: The Hughes pedestrian model (2002) is itself an optical analogue (an eikonal equation for the potential). Stage 3 should determine whether the anisotropic slowness tensor extension and the explicit borrowing of transformation-optics cloaking solutions go beyond this canonical analogy, and whether the claimed isomorphism is novel in the literature.

### Seventh Adversarial Review
**Reviewer:** xAI Grok 4.5
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are anisotropic Eikonal equations of identical structural class, consistent with geometric-optics limit and Hughes route-choice, and jointly support the claimed shared diffeomorphism-invariant governing operator.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three paired tokens are objects of matching mathematical type (second-rank tensors, flux vectors, diffeomorphism symmetries) whose Operator Role statements name the shared structure rather than merely asserting analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_differential_operator is demonstrated by the paired Eikonal equations in Section 3; symmetry_groups by the form-invariance / obstacle-diffeomorphism discussion in Sections 2–3; conserved_quantities by the Poynting ↔ flux conservation statements in Section 2.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by the maturity contrast given in the text; the prediction names a concrete measurable outcome (zero kinematic scattering cross-section and ≥35 % throughput gain) that can falsify the claim.

#### Stage 3 Watch Items
None identified.