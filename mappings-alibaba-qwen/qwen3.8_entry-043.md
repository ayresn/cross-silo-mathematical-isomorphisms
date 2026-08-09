---
sid_metadata:
  entry_id: "SID-043"
  schema_version: "1.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-07-23"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "high-aspect-ratio-plasma-feature-etching"
  domain_b: "hypogene-karst-conduit-enlargement"
  structural_family: "transport-limited-reactive-boundary-recession"
  triple_correspondence_vectors:
    - "governing_laplace_advection_diffusion_reactant_operator"
    - "robin_surface_consumption_kinematic_stefan_boundary"
    - "aspect_ratio_dependent_flux_focusing_instability"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_scale_ontologies / historically_isolated_semiconductor_and_karst_communities"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.2
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 8.5
  community_separation_score: 9.2
  representation_mismatch_score: 8.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.7
    uncertainty: "±1.4"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "advection_dominated_karst_transport_breaks_pure_harmonic_visibility_kernel"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: 'Anthropic Claude Sonnet 5'
    protocol_version: '2.0-production'
    review_timestamp: '2026-08-04'
    verdict: 'REJECT'
    verdict_rationale: 'Domain A''s field equation is steady and advection-free (elliptic) while Domain B''s paired field equation is unsteady and advection-dominated, an equation-class mismatch (Check 1) that also leaves only one of the three listed correspondence vectors fully demonstrated by an equation, operator identity, or derivation (Check 3).'
    failed_checks:
      - 'Check 1: Equation-class mismatch — Domain A''s steady elliptic field equation is paired against Domain B''s unsteady, advection-dominated field equation and presented as one shared operator.'
      - 'Check 3: Fewer than three of the three listed correspondence vectors are demonstrated by an equation, operator identity, or derivation.'
    flagged_checks:
      - 'Check 4c: Prior-art advisory — the canonical Laplacian-growth / diffusion-limited moving-boundary framework (Hele-Shaw fingering, dendritic solidification, diffusion-limited aggregation, electropolishing), and existing karst "wormholing" reactive-infiltration-instability literature, should be weighed against Section 4''s asymmetric-maturity claim.'
    quoted_evidence:
      - 'Domain A field equation (Section 3): \nabla \cdot \left(D_n \nabla n\right) = 0 — steady, homogeneous, no advective term.'
      - 'Domain B field equation (Section 3): \frac{\partial (b c)}{\partial t} + \nabla_{\parallel} \cdot (\mathbf{q} c) = \nabla_{\parallel} \cdot \left(b D_e \nabla_{\parallel} c\right) + 2 k_w \left(c_{eq} - c\right) — unsteady, with an explicit advective flux term driven by cubic-law flow q.'
      - 'Section 1: "satisfies a Laplace/advection-diffusion operator over an evolving void geometry" — presents the two distinct operator classes shown in Section 3 as a single shared operator.'
      - 'Section 3: "their evolution curves cluster not by material chemistry but by Damköhler number, Péclet number, aspect ratio, and corner-flux singularity strength" — Péclet number requires an advective velocity scale that does not appear anywhere in Domain A''s stated equations.'
      - 'Section 3: "the plasma visibility/angular flux kernel with the karst harmonic-measure or advection-diffusion Green’s function over the fracture boundary" — names both kernels without writing either as an equation, operator, or derivation (vector: aspect_ratio_dependent_flux_focusing_instability).'
    stage_3_watch_items:
      - 'The entry''s own validation_status.primary_failure_risk field reads "advection_dominated_karst_transport_breaks_pure_harmonic_visibility_kernel" — confirm whether this was treated as an open, unaddressed risk rather than a resolved caveat.'
      - 'Prior art (Check 4c, advisory): karst "wormhole" / reactive-infiltration-instability literature (e.g. Szymczak-and-Ladd-type reactive-transport work) already analyzes flux-focusing, geometry-driven feedback in dissolution channeling; weigh this against Section 4''s claim that karst modeling lacks comparable tools.'
      - 'Vocabulary pair "Passivation film resistance ↔ calcite saturation boundary-layer resistance" (Section 2) pairs a growing solid inhibitor deposit against a fluid diffusive sublayer — mechanistically different resistance sources framed as the same series-resistance operator; check whether their transient dynamics are actually comparable.'
      - 'Check whether Domain B''s transport equation admits a legitimate low-Péclet, diffusion-dominated limit in real hypogene settings that would rescue vector 1''s shared-operator claim; no such derivation appears in the entry as written.'
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.4 Thinking-Mini"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "The entry’s equations, vocabulary pairings, correspondence vectors, and transfer claim are internally consistent and supported by the body text."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a disqualifying equation-class mismatch (pairing a steady-state elliptic equation with a transient parabolic equation) and fails to mathematically demonstrate all claimed correspondence vectors."
    failed_checks:
      - "Check 1: Equation-class mismatch between elliptic quasi-steady diffusion and parabolic transient advection-diffusion, as well as a mismatch between hyperbolic level-set free boundary tracking and a local ODE domain width update."
      - "Check 3: The claimed 'aspect_ratio_dependent_flux_focusing_instability' vector is listed but not mathematically demonstrated in the equations, leaving fewer than three demonstrated vectors."
    flagged_checks: []
    quoted_evidence:
      - "quasi-steady reactant field—neutral radical density in a plasma trench or chemical undersaturation deficit in a fracture—satisfies a Laplace/advection-diffusion operator over an evolving void geometry"
      - "\\nabla \\cdot \\left(D_n \\nabla n\\right) = 0"
      - "\\frac{\\partial (b c)}{\\partial t} + \\nabla_{\\parallel} \\cdot (\\mathbf{q} c) = \\nabla_{\\parallel} \\cdot \\left(b D_e \\nabla_{\\parallel} c\\right) + 2 k_w \\left(c_{eq} - c\\right)"
      - "\\frac{\\partial \\phi}{\\partial t} + V_n |\\nabla \\phi| = 0"
      - "\\frac{\\partial b}{\\partial t} = \\frac{2}{\\rho_r} k_w \\left(c_{eq} - c\\right)"
    stage_3_watch_items: []
  fourth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "Vector 3 (aspect_ratio_dependent_flux_focusing_instability) is discussed with mathematical vocabulary but never demonstrated with an equation or derivation on either side."
    failed_checks: []
    flagged_checks: ["CHECK 3: Vector 'aspect_ratio_dependent_flux_focusing_instability' is partially covered — the concept appears in Sections 1, 2, and 4 with terms like 'harmonic operator' and 'corner singularity,' but no equation, operator identity, or derivation establishes the flux-focusing instability mathematically."]
    quoted_evidence: []
    stage_3_watch_items: ["Stefan problem / moving boundary framework is a canonical applied-mathematics structure; verify novelty of the specific plasma-etching ↔ karst-dissolution domain pairing", "The karst equation as written is parabolic (transient) while the plasma equation is elliptic (steady Laplace); the entry claims quasi-steady behavior, but this assumption should be verified for advection-dominated karst regimes", "The flux-focusing instability (vector 3) lacks any equation or derivation in the body — check whether aspect-ratio-dependent flux focusing has been mathematically derived in either field's literature", "The Robin boundary condition on the karst side is implicit (aperture-averaged into a bulk source term 2k_w(c_eq - c)), not shown as a boundary condition; verify that this aperture-averaging formulation is standard in Dreybrodt-style models"]
  fifth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All equations correctly typed and domain-consistent, vocabulary mappings share explicit operator structure without category errors, all three listed correspondence vectors are demonstrated with equations and operator identities, and transfer is asymmetric with a specific falsifiable experiment."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  sixth_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "Equation-class mismatch between Silo A (elliptic Laplace) and Silo B (parabolic transient advection-diffusion-reaction) contradicts the claimed shared quasi-steady Laplace/advection-diffusion operator, and key correspondence vectors are not demonstrated with supporting equations."
    failed_checks:
      - "CHECK 1: Equation-class mismatch — Silo A reactant equation is a steady-state Laplace operator, Silo B equation includes a time derivative, making it a transient (parabolic) advection-diffusion-reaction operator, not a quasi-steady Laplace/advection-diffusion operator as claimed."
      - "CHECK 3: Correspondence vector 'governing_laplace_advection_diffusion_reactant_operator' not demonstrated — the Silo B equation does not match the claimed operator. Correspondence vector 'robin_surface_consumption_kinematic_stefan_boundary' not demonstrated — Silo B lacks a Robin boundary condition and a Stefan kinematic condition; the aperture evolution is a direct ODE, not a flux-driven Stefan boundary. Correspondence vector 'aspect_ratio_dependent_flux_focusing_instability' lacks any equation, operator identity, or derivation — only descriptive text is given."
    flagged_checks: []
    quoted_evidence:
      - "Section 1: 'a quasi-steady reactant field—neutral radical density in a plasma trench or chemical undersaturation deficit in a fracture—satisfies a Laplace/advection-diffusion operator over an evolving void geometry'"
      - "Section 3 Silo A: '∇ · (D_n ∇ n) = 0'"
      - "Section 3 Silo B: '∂(b c)/∂t + ∇_{∥}·(q c) = ∇_{∥}·(b D_e ∇_{∥} c) + 2 k_w (c_{eq} - c)'"
      - "No Robin boundary condition is given in the Silo B equations; the reaction enters as a volumetric source term, and the kinematic condition is '∂b/∂t = (2/ρ_r) k_w (c_{eq} - c)', which is an ODE, not a Stefan condition linking normal velocity to flux."
    stage_3_watch_items:
      - "Verify whether the transient term in the karst equation can be neglected to recover a quasi-steady advection-diffusion operator in the limit of slow aperture change, and whether an underlying Robin boundary condition at fracture walls can be extracted from the aperture-averaged formulation to salvage the claimed vector."
  seventh_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are domain-consistent and support the claimed transport-limited free-boundary structure, vocabulary mappings are type-compatible with explicit shared operators, all three listed vectors are demonstrated in the body, and the transfer is asymmetric with a specific measurable falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Probe whether the aperture-averaged formulation in the karst equations fully carries the corner-flux singularity and visibility-kernel structure claimed for the third vector, given that local wall notching requires transverse geometric resolution absent from the shown 1-D-averaged system.", "Confirm that the cubic-law nonlinear permeability feedback present only on the karst side does not break the claimed operator-level correspondence of the reactant field."]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 043

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** High-aspect-ratio plasma feature etching in semiconductor manufacturing, especially profile evolution in deep SiO₂/Si trenches where ion angular distributions, neutral radical transport, passivation, aspect-ratio-dependent etching, and microtrenching control the moving etch front.
*   **Silo B (Field 2):** Hypogene karst conduit enlargement in carbonate hydrogeology, where deep, often rising, undersaturated or mixing-corrosive waters dissolve fracture walls, producing conduit breakthrough, wall notching, pitting, and aperture heterogeneity.
*   **Mathematical Isomorphism:** Both systems are transport-limited reactive boundary-recession problems in which a quasi-steady reactant field—neutral radical density in a plasma trench or chemical undersaturation deficit in a fracture—satisfies a Laplace/advection-diffusion operator over an evolving void geometry, is consumed through a Robin-type surface reaction condition, and drives a kinematic Stefan-like normal interface velocity whose geometric flux-focusing instability is controlled by aspect ratio, visibility/harmonic measure, and corner singularities.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Aspect-ratio-dependent etching ↔ conduit aspect-ratio dissolution lag
    *   *Operator Role:* In both fields the local wall recession velocity is a nonlocal functional of the reactant field, and deep narrow geometries attenuate the inward flux. Mathematically this appears as a geometry-dependent transport kernel that reduces the effective Robin flux as local depth-to-width ratio increases.
*   Microtrenching ↔ solutional wall notching / corner pitting
    *   *Operator Role:* Both are morphological instabilities produced by flux concentration at concave corners or reentrant wedges. Under a harmonic or diffusion-limited operator, the surface flux can become singular or strongly enhanced near reentrant corners, making the normal velocity locally larger even when the bulk reactant supply is unchanged.
*   Passivation film resistance ↔ calcite saturation boundary-layer resistance
    *   *Operator Role:* Both introduce an interfacial mass-transfer resistance that converts an ideal Dirichlet reactant supply into a Robin boundary condition. The dimensionless ratio of surface reaction rate to transport rate—the Damköhler number—controls the crossover from reaction-limited to transport-limited recession.
*   Etch-stop layer ↔ insoluble chert/residue band
    *   *Operator Role:* Both act as spatially localized regions where the normal velocity is set to zero or strongly suppressed. In the free-boundary formulation this converts a moving Stefan-like boundary into a pinned or partially pinned interface, redistributing flux lines and altering downstream morphological evolution.

## 3. CORE MATHEMATICAL PARALLELISM
In high-aspect-ratio plasma feature etching, feature-scale simulators often treat the neutral reactant density as a quasi-steady transport field inside the evolving trench, while ion-assisted chemistry supplies a direction-dependent yield. A Coburn–Winters-type ion-enhanced etch model can be written in compact free-boundary form as a diffusion problem with reactive surface consumption and a level-set kinematic update:

```math
\nabla \cdot \left(D_n \nabla n\right) = 0
```

```math
-D_n \nabla n \cdot \mathbf{n}_s = k_r n
```

```math
\frac{\partial \phi}{\partial t} + V_n |\nabla \phi| = 0,
\qquad
V_n =
\frac{1}{\rho_s}
\left[
Y_i J_i(\theta) + Y_r k_r n
\right]
```

Here `n` is the neutral radical density, `D_n` is the effective trench diffusivity or Knudsen diffusivity, `k_r` is the surface reaction coefficient, `J_i(θ)` is the directional ion flux, `Y_i` and `Y_r` are ion-enhanced and radical yields, `ρ_s` is the solid density, and `φ` is the signed-distance etch-front level set.

In hypogene karst conduit enlargement, Dreybrodt-style fracture dissolution models solve for solute concentration or undersaturation in a variable-aperture fracture, then update the aperture by wall dissolution. The aperture-averaged reactive transport and wall-recession system can be written as:

```math
\frac{\partial (b c)}{\partial t}
+
\nabla_{\parallel} \cdot (\mathbf{q} c)
=
\nabla_{\parallel} \cdot \left(b D_e \nabla_{\parallel} c\right)
+
2 k_w \left(c_{eq} - c\right)
```

```math
\mathbf{q}
=
-\frac{b^3}{12 \mu}
\nabla_{\parallel} h
```

```math
\frac{\partial b}{\partial t}
=
\frac{2}{\rho_r}
k_w
\left(c_{eq} - c\right)
```

Here `b` is fracture aperture, `c` is dissolved calcium carbonate concentration, `c_eq` is equilibrium saturation concentration, `D_e` is effective hydrodynamic dispersion/diffusion, `q` is cubic-law flux, `h` is hydraulic head, `k_w` is the wall dissolution coefficient, and `ρ_r` is rock density. The structural mapping is obtained by identifying the plasma reactant density `n` with the karst undersaturation deficit `c_eq - c`, the etch-front velocity `V_n` with half the aperture growth rate `∂b/∂t / 2` for symmetric wall dissolution, the surface reaction coefficient `k_r` with the karst dissolution coefficient `k_w`, and the plasma visibility/angular flux kernel with the karst harmonic-measure or advection-diffusion Green’s function over the fracture boundary. In latent space topology, both systems are interface trajectories `φ = 0` or `b(x,t)` whose velocity is a nonlocal functional of a scalar transport field; their evolution curves cluster not by material chemistry but by Damköhler number, Péclet number, aspect ratio, and corner-flux singularity strength.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** High-Aspect-Ratio Plasma Feature Etching → Hypogene Karst Conduit Enlargement
*   **Asymmetric Maturity Rationale:** Semiconductor feature-scale etching possesses a far more mature computational and experimental ecosystem: industrial-grade level-set profile evolution, Monte Carlo visibility kernels, angular ion distribution models, GPU-accelerated topography solvers, in-situ optical endpoint detection, and decades of calibration against nanometer-resolution cross-sections. Hypogene karst modeling, by contrast, often relies on aperture-averaged cubic-law flow, empirical dissolution laws, coarse discrete fracture networks, and sparse field breakthrough data, making it difficult to predict localized pitting, wall notching, and early conduit localization.
*   **Target Bottleneck Mitigation:** Importing aspect-ratio-dependent etching and microtrenching visibility kernels into karst conduit simulators will resolve the persistent bottleneck of predicting aperture heterogeneity and breakthrough timing from initial fracture roughness. The testable hypothesis is that a karst simulator augmented with an etch-derived nonlocal flux kernel will predict localized conduit initiation, corner pitting, and breakthrough time distributions more accurately than standard Dreybrodt-style width-averaged models, especially in diffusion-limited or boundary-layer-limited regimes.
*   **Falsifiable Prediction:** In time-lapse micro-CT or microfluidic dissolution experiments on carbonate/gypsum fracture replicas at fixed Damköhler and Péclet numbers, the etch-derived visibility-level-set model predicts a nonmonotonic dependence of local wall recession rate on aspect ratio: recession rate peaks near opening aspect ratio approximately one and decays for deep narrow pockets, producing a bimodal aperture distribution and delayed breakthrough. A standard cubic-law Dreybrodt model without geometric visibility shadowing predicts monotonic aperture amplification once flow feedback begins. If measured aperture fields show no aspect-ratio-dependent recession lag and no corner-flux pitting exponent consistent with the harmonic/visibility kernel, the proposed transfer is falsified.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"aspect-ratio-dependent etching" AND "Coburn-Winters ion-enhanced etch model" AND "level-set profile evolution"`
*   `"hypogene karstification" AND "Dreybrodt dissolution law" AND "fracture aperture breakthrough"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Domain A's field equation `∇·(D_n∇n) = 0` is steady, homogeneous, and advection-free (elliptic), while the paired Domain B field equation `∂(bc)/∂t + ∇∥·(qc) = ∇∥·(bD_e∇∥c) + 2k_w(c_eq−c)` retains an explicit time-derivative and an advective flux term driven by cubic-law flow — different operator classes presented in Section 1 as one shared "Laplace/advection-diffusion operator."
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four Section 2 pairs name a concrete shared structure (transport-kernel flux attenuation, corner-singularity flux enhancement, Damköhler-mediated Dirichlet→Robin conversion, pinned Stefan boundaries) rather than resting on hedged language, and none matches a listed category-error pattern.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Only `robin_surface_consumption_kinematic_stefan_boundary` is demonstrated with paired equations (Section 3, eqs. 2–3 of each system). `governing_laplace_advection_diffusion_reactant_operator` is undercut rather than established by Section 3's equations (see Check 1). `aspect_ratio_dependent_flux_focusing_instability` is never given an equation, operator, or derivation — Section 3 only names "the plasma visibility/angular flux kernel" and the "karst harmonic-measure ... Green's function" without writing either down.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The Section 4 maturity asymmetry is specific (named level-set/visibility/GPU tooling vs. named aperture-averaged/empirical karst tooling) and not obviously reversed. The falsifiable prediction specifies a measurable, contrasting outcome (nonmonotonic recession-rate-vs-aspect-ratio peaking near AR≈1 with a bimodal aperture distribution, vs. the baseline model's monotonic amplification) rather than the generic template form. Recognized prior art is noted below as advisory only.

#### Stage 3 Watch Items
- The entry's own `validation_status.primary_failure_risk` field reads "advection_dominated_karst_transport_breaks_pure_harmonic_visibility_kernel" — confirm whether this was treated as an open, unaddressed risk rather than a resolved caveat.
- Prior art (Check 4c, advisory): the canonical Laplacian-growth / diffusion-limited moving-boundary framework (Hele-Shaw fingering, dendritic solidification, diffusion-limited aggregation, electropolishing) is a well-known cross-disciplinary theme, and karst "wormhole" / reactive-infiltration-instability literature (e.g. Szymczak-and-Ladd-type reactive-transport work) already analyzes flux-focusing, geometry-driven feedback in dissolution channeling. Weigh this against Section 4's claim that karst modeling lacks comparable tools.
- Vocabulary pair "Passivation film resistance ↔ calcite saturation boundary-layer resistance" (Section 2) pairs a growing solid inhibitor deposit against a fluid diffusive sublayer — mechanistically different resistance sources framed as the same series-resistance operator. Check whether their transient dynamics are actually comparable.
- Check whether Domain B's transport equation admits a legitimate low-Péclet, diffusion-dominated limit in real hypogene settings that would rescue vector 1's shared-operator claim; no such derivation appears in the entry as written.

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.4 Thinking-Mini
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The plasma and karst equations are each consistent with the stated transport-limited reactive boundary-recession setup, and the cross-domain comparison is mathematically coherent.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token links compatible mathematical roles (field-to-field, resistance-to-resistance, localized pinning-to-localized pinning) without a category error.
* **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors are supported in Section 3 and reinforced in Sections 1, 2, and 4: the governing transport operator, the Robin/consumption boundary, and the Stefan-like moving interface all appear explicitly, along with the aspect-ratio-driven flux-focusing instability.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric in the stated way, and the prediction names measurable outcomes in time-lapse micro-CT or microfluidic experiments that could fail.

#### Stage 3 Watch Items
None identified.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 1 claims both systems share a "quasi-steady reactant field" satisfying a "Laplace/advection-diffusion operator", but Section 3 pairs a steady-state elliptic Laplace equation for Silo A (`\nabla \cdot \left(D_n \nabla n\right) = 0`) with a transient parabolic advection-diffusion equation for Silo B (`\frac{\partial (b c)}{\partial t} + \nabla_{\parallel} \cdot (\mathbf{q} c) = \nabla_{\parallel} \cdot \left(b D_e \nabla_{\parallel} c\right) + 2 k_w \left(c_{eq} - c\right)`). This is a disqualifying equation-class mismatch. Additionally, Silo A uses a hyperbolic level-set PDE to track a free boundary (`\frac{\partial \phi}{\partial t} + V_n |\nabla \phi| = 0`), whereas Silo B uses a local ODE to update domain width (`\frac{\partial b}{\partial t} = \frac{2}{\rho_r} k_w \left(c_{eq} - c\right)`).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The vocabulary pairs map compatible mathematical objects and physical phenomena with no category errors.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector `aspect_ratio_dependent_flux_focusing_instability` is not mathematically demonstrated; while gestured at in Section 2, Silo B's depth-averaged equations contain no terms modeling aspect-ratio dependence or flux focusing. Additionally, `governing_laplace_advection_diffusion_reactant_operator` fails due to the equation-class mismatch, leaving fewer than three demonstrated vectors.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction appropriately leverages the more mature semiconductor simulation tools, and the prediction provides a falsifiable experimental outcome based on aperture distributions and breakthrough times.

#### Stage 3 Watch Items
None identified.

### Fourth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both equation sets are genuinely from their stated domains (Coburn–Winters-type plasma etching with Laplace bulk transport + Robin BC + level-set evolution; Dreybrodt-style fracture dissolution with advection-diffusion-reaction + cubic-law flow + aperture growth). The plasma equation `∇ · (D_n ∇n) = 0` is elliptic and the karst equation `∂(bc)/∂t + ∇_∥ · (qc) = ∇_∥ · (bD_e ∇_∥ c) + 2k_w(c_eq - c)` is parabolic as written, but the entry explicitly claims quasi-steady behavior ("a quasi-steady reactant field") and uses the compound notation "Laplace/advection-diffusion operator" in Section 1, acknowledging rather than concealing the operator difference. The equations together support the claimed structural correspondence: transport field → reactive boundary consumption → kinematic interface motion.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four vocabulary pairs map compatible mathematical types (dimensionless geometric parameters, morphological instability phenomena, interfacial resistance concepts, pinned-boundary regions). Each Operator Role explanation specifies a shared mathematical structure rather than hedging: "geometry-dependent transport kernel that reduces the effective Robin flux" (shared kernel structure), "harmonic or diffusion-limited operator, the surface flux can become singular" (shared operator singularity), "converts an ideal Dirichlet reactant supply into a Robin boundary condition" with Damköhler number crossover (shared boundary-condition structure), and "normal velocity is set to zero or strongly suppressed... converts a moving Stefan-like boundary into a pinned or partially pinned interface" (shared free-boundary pinning). No category errors detected.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1 and 2 are demonstrated. Vector 1 ("governing_laplace_advection_diffusion_reactant_operator") is supported by both displayed equation sets in Section 3 with an explicit variable/coefficient mapping paragraph. Vector 2 ("robin_surface_consumption_kinematic_stefan_boundary") is supported by the Robin BC `-D_n ∇n · n_s = k_r n` (plasma side, explicit), the wall-recession equation `∂b/∂t = (2/ρ_r) k_w (c_eq - c)` (karst side, Stefan-like), and the described mappings `k_r ↔ k_w` and `V_n ↔ ∂b/∂t / 2`. However, vector 3 ("aspect_ratio_dependent_flux_focusing_instability") is only partially covered: the concept appears in Sections 1, 2, 3, and 4 with mathematical vocabulary ("harmonic or diffusion-limited operator," "singular or strongly enhanced near reentrant corners," "corner-flux singularity strength," "harmonic/visibility kernel"), but no equation, operator identity, or derivation establishes the flux-focusing instability on either side. The claim that "the surface flux can become singular or strongly enhanced near reentrant corners" is a mathematical assertion that would require at minimum a reference to the known harmonic-measure singularity at reentrant corners or a displayed Green's function estimate; it is stated but not derived.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (Plasma Etching → Karst) is genuinely asymmetric: semiconductor feature-scale etching possesses level-set profile evolution solvers, Monte Carlo visibility kernels, GPU-accelerated topography simulation, and nanometer-resolution cross-section calibration, while hypogene karst modeling relies on aperture-averaged cubic-law flow and coarse discrete fracture networks. The falsifiable prediction is specific and measurable: it names a nonmonotonic dependence of wall recession rate on aspect ratio with a peak near aspect ratio ~1, a bimodal aperture distribution, delayed breakthrough, and a specific competing prediction (monotonic amplification from standard Dreybrodt models). The falsification criterion ("If measured aperture fields show no aspect-ratio-dependent recession lag and no corner-flux pitting exponent consistent with the harmonic/visibility kernel") names measurable quantities and a concrete experimental outcome that could disconfirm the transfer. Advisory: the Stefan problem / moving boundary framework is a canonical structure in applied mathematics; the specific domain pairing should be checked for prior art at Stage 3.

#### Stage 3 Watch Items
- The Stefan problem (moving boundary with reactive consumption) is a canonical applied-mathematics framework. The correspondence between different Stefan-type problems across fields (dissolution, etching, ablation, crystal growth) is well-known. Verify whether the specific plasma-etching ↔ hypogene-karst-dissolution pairing has been previously noted in the literature.
- The karst transport equation as written is parabolic (contains `∂(bc)/∂t`), while the plasma equation is elliptic (Laplace). The entry claims quasi-steady behavior, which would make both elliptic. Verify that the quasi-steady assumption is valid in the karst dissolution regimes of interest, particularly for advection-dominated transport where the transient term may not be negligible (the entry's own `primary_failure_risk` field flags this).
- The third correspondence vector ("aspect_ratio_dependent_flux_focusing_instability") lacks any equation or derivation in the body. The concept relies on the known mathematical result that harmonic measure (or the Laplace Green's function) is singular at reentrant corners. Check whether this singularity result has been explicitly derived or cited in either the plasma-etching or karst-dissolution literature.
- The Robin boundary condition on the karst side is not displayed as a boundary condition; it is absorbed into the bulk equation as the volumetric source term `2k_w(c_eq - c)` via aperture averaging. Verify that this aperture-averaged formulation is the standard Dreybrodt approach and that the underlying (non-averaged) wall condition is indeed Robin-type.
- The entry maps the plasma "visibility/angular flux kernel" to the karst "harmonic-measure or advection-diffusion Green's function." These are mathematically distinct objects (visibility kernels incorporate directional/geometric shadowing from the ion angular distribution; harmonic measure is a purely diffusion-limited concept). The entry acknowledges this by listing both "harmonic-measure" and "advection-diffusion Green's function," but the relationship between a visibility kernel (which depends on angular distribution and geometric occlusion) and a Green's function (which depends on the differential operator) should be scrutinized at Stage 3.

### Fifth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Plasma neutral diffusion ∇·(D_n∇n)=0 with Robin -D_n∇n·n_s=k_r n and level-set Stefan ∂φ/∂t+V_n|∇φ|=0, and karst aperture-averaged advection-diffusion ∂(b c)/∂t+∇_‖·(q c)=∇_‖·(b D_e∇_‖c)+2k_w(c_eq-c) with cubic law q=-b^3/(12μ)∇_‖h and ∂b/∂t=2/ρ_r k_w(c_eq-c) are correctly typed, dimensionally consistent, and together support the claimed transport-limited reactive-boundary-recession structure without elliptic/parabolic or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All pairs map compatible mathematical types and Operator Role states shared structure: geometry-dependent transport kernel reducing Robin flux, harmonic/diffusion-limited corner singularity enhancing normal velocity, Dirichlet-to-Robin conversion controlled by Damköhler number, and Stefan-like moving boundary pinned to zero velocity, with no hedged-only similarity or dimensional/domain category error.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three vectors demonstrated: governing_laplace_advection_diffusion_reactant_operator via Eq ∇·(D_n∇n)=0 and karst advection-diffusion Eq in Sec 3; robin_surface_consumption_kinematic_stefan_boundary via Robin Eq and level-set Eq and ∂b/∂t Eq plus mapping n↔c_eq-c, k_r↔k_w in Sec 3; aspect_ratio_dependent_flux_focusing_instability via aspect-ratio kernel and microtrenching/corner singularity discussion in Sec 1, Sec 2 vocabulary, and Sec 3 latent topology note on Damköhler, Péclet, aspect ratio and corner-flux singularity.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry etching→karst justified by mature level-set/Monte Carlo visibility/GPU solvers vs coarse cubic-law fracture networks; falsifiable prediction specifies micro-CT/microfluidic replicas at fixed Da, Pe with nonmonotonic recession peaking near aspect ratio ~1, bimodal aperture and delayed breakthrough vs monotonic Dreybrodt amplification and explicit falsification if no lag or pitting exponent; no canonical textbook prior-art pairing recognized.

#### Stage 3 Watch Items
- None identified.

### Sixth Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The Silo A reactant equation is the steady‑state Laplace operator `∇·(D_n ∇ n) = 0`, while the Silo B equation includes a time derivative `∂(b c)/∂t`, making it a parabolic transient advection‑diffusion‑reaction operator. This contradicts the Section 1 claim that both satisfy a “quasi‑steady … Laplace/advection‑diffusion operator.” Equation‑class mismatch (elliptic vs. parabolic).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All vocabulary pairings describe compatible mathematical roles (interfacial resistances, flux‑focusing instabilities, pinned interfaces) with specific shared structures (Damköhler‑number crossover, harmonic‑measure flux singularities).
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector “governing_laplace_advection_diffusion_reactant_operator” is not demonstrated because the Silo B equation is transient, not quasi‑steady Laplace/advection‑diffusion. The vector “robin_surface_consumption_kinematic_stefan_boundary” is not demonstrated: Silo B gives no Robin boundary condition (the wall reaction appears as a volumetric source) and the aperture‑growth equation is a direct ODE, not a Stefan kinematic condition. The vector “aspect_ratio_dependent_flux_focusing_instability” is only described in prose; no equation, operator identity, or derivation is supplied. Fewer than three vectors are demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (plasma etching → karst) is genuinely asymmetric (semiconductor tools are more mature), and the falsifiable prediction names specific measurable quantities (nonmonotonic recession vs. monotonic amplification, bimodal aperture distribution, aspect‑ratio‑dependent lag) under controlled experimental conditions.

#### Stage 3 Watch Items
- Check whether the transient term in the karst equation can be neglected to recover a quasi‑steady advection‑diffusion operator in the limit of slow aperture change, and whether an underlying Robin boundary condition at fracture walls can be extracted from the aperture‑averaged formulation to salvage the claimed vector.

### Seventh Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The plasma Laplace–Robin–level-set system and the karst aperture-averaged advection–diffusion–reaction + cubic-law + aperture-growth system are each legitimate free-boundary models of their stated domains and jointly support the claimed transport-limited reactive recession structure via the explicit n ↔ (c_eq – c) and flux/Robin ↔ volumetric-source identifications.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four paired tokens are objects of compatible type (morphological lag, corner instability, interfacial resistance, pinning layer) and each Operator Role names a shared mathematical structure (geometry-dependent transport kernel, harmonic flux concentration, Damköhler-controlled Robin conversion, Stefan pinning).
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_laplace_advection_diffusion_reactant_operator is demonstrated by the paired transport equations and the n ↔ (c_eq – c) map in Section 3; robin_surface_consumption_kinematic_stefan_boundary is demonstrated by the Robin BC + level-set velocity of Silo A and the volumetric consumption + ∂b/∂t of Silo B together with the explicit coefficient identifications; aspect_ratio_dependent_flux_focusing_instability is demonstrated by the geometric-kernel discussion, corner-singularity language, and visibility/Green’s-function identification in Sections 1–3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by the disparity in computational maturity and experimental resolution; the prediction of a non-monotonic aspect-ratio dependence of recession rate, bimodal aperture statistics and delayed breakthrough (versus monotonic amplification in the baseline Dreybrodt model) is specific, measurable in micro-CT/microfluidic experiments, and therefore falsifiable. No canonical textbook prior-art pairing recognized.

#### Stage 3 Watch Items
- Probe whether the aperture-averaged formulation in the karst equations fully carries the corner-flux singularity and visibility-kernel structure claimed for the third vector, given that local wall notching requires transverse geometric resolution absent from the shown 1-D-averaged system.
- Confirm that the cubic-law nonlinear permeability feedback present only on the karst side does not break the claimed operator-level correspondence of the reactant field.