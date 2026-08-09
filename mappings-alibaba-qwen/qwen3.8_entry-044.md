---
sid_metadata:
  entry_id: "SID-044"
  schema_version: "1.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-07-23"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "nuclear-criticality-transport"
  domain_b: "spatial-invasion-ecology"
  structural_family: "linear-multiplicative-transport-eigenproblems"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "boundary_conditions"
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
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.9
  community_separation_score: 9.0
  representation_mismatch_score: 8.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.8
    uncertainty: "±0.7"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 4.6"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: both equations are correctly identified integro-differential transport eigenproblems of matching operator class, all vocabulary mappings are type-coherent with shared mathematical structure explicitly stated, all three correspondence vectors are demonstrated in the body, and the falsifiability prediction names specific quantitative thresholds and a directional null outcome."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "PRIOR ART (Check 4c advisory): The Silo B governing equation is structurally the velocity-jump / kinetic transport model established in mathematical biology (Othmer, Hillen, Stevens, Erban lineage). Stage 3 bibliometric search should determine whether the specific nuclear criticality apparatus — adjoint importance maps, source iteration, discrete-ordinates spatial discretization — has been previously adapted for invasion ecology or landscape-level persistence eigenvalue problems; the governing-equation identity itself is known territory and novelty rests entirely on the applied-toolkit transfer."
      - "FISSION KERNEL NOTATION: The Silo A equation writes the fission term as the integral of νΣ_f(x, Ω'→Ω) ψ(x,Ω') over S², making fission angle-to-angle dependent. Standard one-speed criticality assumes isotropic fission (νΣ_f(x)/4π, no Ω-dependence). The generalization is mathematically valid and structurally necessary to parallel the ecology fecundity kernel F(x,Ω'→Ω), but Stage 3 should confirm whether the claimed Silo A domain (heterogeneous fissile assemblies in criticality safety analysis) physically supports anisotropic fission sources, or else confirm this is an explicit deliberate generalization for the isomorphism."
      - "ATTENUATION FUNCTIONAL ASYMMETRY: Total removal cross section Σ_t(x) in Silo A is position-only; μ(x,Ω) in Silo B is direction-dependent. The mapping is mathematically valid (Silo A is the special case where μ is Ω-independent), but the vocabulary matrix entry does not acknowledge this asymmetry. Stage 3 should assess whether real directional invasion scenarios genuinely require direction-dependent attenuation or whether the ecology problem reduces to direction-independent loss in the calibrated scenarios used to test the falsifiable prediction, and note implications for the constitutive correspondence confidence."
      - "NUMERICAL SOLUTION FAMILY INDEPENDENCE: The numerical_solution_family vector is demonstrated via a joint Perron-Frobenius statement in Section 3 final paragraph ('the two equations occupy the same latent operator topology: ... a source-iteration trajectory converging to that ray') rather than by independent ecological-side numerical equations. Stage 3 should check whether velocity-jump ecology literature already possesses source-iteration-equivalent eigenvalue solvers; if so, the methodological transfer claim in Section 4 should be scoped specifically to discrete-ordinates spatial resolution and calibrated adjoint importance maps, not to source iteration as such."
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.4 Thinking-Mini"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "The body does not actually demonstrate the listed numerical_solution_family correspondence, so the required three correspondence vectors are not all established."
    failed_checks: ["Check 3: Correspondence vector support"]
    flagged_checks: []
    quoted_evidence: ["\"dominant eigenvalue, inflow boundary trace, and discrete-ordinates/adjoint solution family obey an equivalent Perron-Frobenius threshold structure.\""]
    stage_3_watch_items: ["Verify whether the numerical_solution_family vector can be supported by an explicit solver-level equivalence rather than a named analogy; the current body names discrete-ordinates and adjoint methods but does not derive a matching solution-family correspondence."]
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "The entry lists exactly three correspondence vectors but fails to mathematically demonstrate one of them, resulting in fewer than the mandatory minimum of three demonstrated vectors."
    failed_checks: ["Check 3: Fewer than three demonstrated correspondence vectors"]
    flagged_checks: ["Check 4: Prior art identified"]
    quoted_evidence: ["discrete-ordinates/adjoint solution family obey an equivalent Perron-Frobenius threshold structure", "a source-iteration trajectory converging to that ray"]
    stage_3_watch_items: ["Verify whether the adjoint eigenvalue sensitivity transfer provides novel utility compared to existing mathematical biology literature on velocity-jump processes and persistence in transport equations (e.g., Othmer, Hillen, Lutscher)."]
  fourth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "Both equations are genuine first-order linear transport eigenproblems of the same operator class with compatible vocabulary mappings, three demonstrated correspondence vectors, genuinely asymmetric transfer, and a specific falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Transport equations for biological movement (velocity-jump processes, run-and-tumble models) are well-established in mathematical biology literature (Othmer, Hillen, Alt, et al.). Stage 3 should determine whether the specific k-eigenvalue nuclear-criticality ↔ population-growth-eigenvalue pairing has been explicitly drawn before."
      - "The next-generation matrix eigenvalue approach in epidemiology/ecology is itself a spectral threshold method. Stage 3 should probe whether adjoint perturbation theory from nuclear transport has already been applied to ecological persistence eigenvalues under a different name."
      - "The Silo B equation's directional dependence of mortality μ(x,Ω) is unusual in standard ecological models; Stage 3 should verify whether direction-dependent mortality appears in the invasion ecology literature or is a novel modeling assumption introduced by this entry."
  fifth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "Both equations are correctly typed linear first-order transport eigenproblems with matching streaming, removal, scattering and multiplicative fission/fecundity structure, all vocabulary mappings preserve mathematical type, and all three correspondence vectors are demonstrated with a specific falsifiable asymmetric transfer."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Related diffusion analogy of critical reactor size ↔ critical patch size (Kierstead-Slobodkin 1953, Skellam 1951, Okubo 1980) is textbook; Stage 3 should verify whether this angular Boltzmann transport version with discrete-ordinates/adjoint extends beyond that known diffusion isomorphism", "Verify novelty of importing discrete-ordinates k-eigenvalue solvers and adjoint importance maps into velocity-jump invasion ecology vs existing integrodifference and next-generation matrix approaches"]
  sixth_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "All mathematical and structural consistency checks pass; prior art recognition under Check 4c triggers an advisory flag."
    failed_checks: []
    flagged_checks: ["Check 4c: Prior art recognition — nuclear transport eigenvalue ↔ population growth eigenvalue analogy exists in established literature (e.g., Rotenberg 1972)."]
    quoted_evidence: []
    stage_3_watch_items: ["Rotenberg, M. (1972) 'Theory of population transport', J. Theor. Biol. 37(2), 291-305, and subsequent velocity-jump/dispersal transport models that draw on neutron transport formalism. Human bibliometric reviewer should verify whether the specific discrete-ordinates/adjoint transfer and the directional sensitivity prediction are novel."]
  seventh_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: matching transport eigenproblem structure, compatible vocabulary types, fully demonstrated correspondence vectors, and a specific asymmetric falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 044

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Nuclear criticality transport, specifically steady one-speed neutron multiplication in heterogeneous fissile assemblies, where the core observable is the angular neutron flux and the threshold eigenvalue is the effective multiplication factor.
*   **Silo B (Field 2):** Spatial invasion ecology, specifically stage-structured population persistence and spread with directional dispersal across heterogeneous habitat, where the core observable is the directional density of moving individuals and the threshold eigenvalue is the asymptotic population growth factor.
*   **Mathematical Isomorphism:** Both systems are positive linear transport eigenproblems in which a first-order streaming/removal operator is balanced by an angular redistribution integral and a local multiplicative birth/fission integral, so the dominant eigenvalue, inflow boundary trace, and discrete-ordinates/adjoint solution family obey an equivalent Perron-Frobenius threshold structure.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Effective multiplication factor ↔ Asymptotic population growth factor
    *   *Operator Role:* Both are the dominant positive eigenvalue of a linear phase-space transport operator; crossing unity separates subcritical decay or extinction from supercritical growth or invasion.
*   Macroscopic fission source ↔ Local fecundity or reproduction kernel
    *   *Operator Role:* Both supply positive multiplication into the phase-space density, converting an attenuating streaming problem into a spectral growth problem.
*   Total removal cross section ↔ Mortality plus directional emigration loss rate
    *   *Operator Role:* Both appear as diagonal attenuation terms in the transport operator, setting the residence time of particles or organisms in a phase-space cell.
*   Angular neutron flux ↔ Directional dispersal density
    *   *Operator Role:* Both are nonnegative densities over position and direction, advected by the same first-order streaming operator before scattering, removal, or reproduction.
*   Vacuum inflow boundary ↔ Absorbing or no-immigration habitat boundary
    *   *Operator Role:* Both impose a zero incoming trace on the inflow portion of the phase-space boundary, making the spectral problem self-contained within the spatial domain.
*   Adjoint neutron importance ↔ Conservation or intervention sensitivity
    *   *Operator Role:* Both are left eigenvectors of the same transport operator and give the first-order change in the dominant eigenvalue under localized removal, sterilization, or control.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models steady neutron criticality with the one-speed Boltzmann transport eigenvalue equation, in which streaming and total loss are balanced by scattering redistribution and fission multiplication. The incoming angular flux is set to zero on a vacuum boundary, making the problem a positive spectral problem for the dominant eigenvalue.

```math
\Omega \cdot \nabla \psi(x,\Omega) + \Sigma_t(x)\psi(x,\Omega)
=
\int_{S^2} \Sigma_s(x,\Omega' \to \Omega)\psi(x,\Omega')\,d\Omega'
+
\frac{1}{k_{\mathrm{eff}}}
\int_{S^2} \nu\Sigma_f(x,\Omega' \to \Omega)\psi(x,\Omega')\,d\Omega'
```

Silo B models directional population spread with a linearized stage-structured transport-growth equation, in which organisms move along directed trajectories, suffer mortality or emigration, change direction through a movement-turning kernel, and produce new individuals through a local fecundity kernel. With zero immigration at the habitat boundary, the dominant eigenvalue determines whether the metapopulation persists, grows, or goes extinct.

```math
\Omega \cdot \nabla n(x,\Omega) + \mu(x,\Omega)n(x,\Omega)
=
\int_{S^2} K(x,\Omega' \to \Omega)n(x,\Omega')\,d\Omega'
+
\frac{1}{\lambda}
\int_{S^2} F(x,\Omega' \to \Omega)n(x,\Omega')\,d\Omega'
```

Under the mapping from neutron angular flux to directional organism density, total removal cross section to mortality/emigration, scattering kernel to turning kernel, and fission kernel to fecundity kernel, the two equations occupy the same latent operator topology: a positive cone of phase-space densities, a dominant positive eigenfunction ray, a source-iteration trajectory converging to that ray, and a threshold bifurcation at eigenvalue unity.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Nuclear Criticality Transport → Spatial Invasion Ecology
*   **Asymmetric Maturity Rationale:** Nuclear transport possesses a far more mature toolkit for high-dimensional linear transport eigenproblems: discrete ordinates and method-of-characteristics solvers, source iteration and Krylov acceleration, adjoint perturbation theory, variance-reduced Monte Carlo, and routine criticality safety workflows. Spatial invasion ecology more often relies on individual-based simulations, coarse reaction-diffusion approximations, or network eigenvector centrality, which can lose directional streaming effects and rarely provide calibrated adjoint intervention maps at landscape scale.
*   **Target Bottleneck Mitigation:** Importing deterministic discrete-ordinates transport solvers and adjoint eigenvalue sensitivity from nuclear criticality will let invasion ecologists compute the landscape growth factor and rank habitat cells or corridors by true first-order impact on persistence, thereby resolving the bottleneck of expensive, non-adjoint, diffusion-limited management prioritization for strongly directional dispersal.
*   **Falsifiable Prediction:** For a calibrated wind-borne or current-borne invasion scenario on a heterogeneous landscape, removing or sterilizing the top five percent of habitat cells ranked by transport adjoint importance will reduce the dominant population growth eigenvalue by at least fifteen percent more than removing the same number of cells ranked by current state-of-the-art next-generation-matrix eigenvector centrality or reaction-diffusion sensitivity; the transport model also predicts at least one low-fecundity upstream shadow corridor whose localized suppression reduces the eigenvalue by more than five percent despite low occupancy, and failure to observe either effect in replicated field or high-fidelity simulation removals would falsify the operational transfer.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"effective multiplication factor" AND "Boltzmann transport equation" AND "adjoint importance"`
*   `"stage-structured dispersal" AND "velocity-jump movement" AND "asymptotic growth rate"`
*   `"discrete ordinates" AND "k-eigenvalue" AND "heterogeneous multiplying media"`
*   `"landscape persistence" AND "directional dispersal kernel" AND "population growth eigenvalue"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 4.6
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both equations are correctly identified integro-differential transport eigenvalue problems of the same operator class: first-order streaming operator Ω·∇ plus a diagonal loss term, balanced by an angular redistribution integral and a multiplicative birth/fission integral acting on the same phase-space variable (x,Ω); the equation-class identity is exact (not cross-class), and the structural correspondence claimed in Section 1 — a positive linear transport eigenproblem with Perron-Frobenius threshold at unity — is fully supported by both equations as written.

- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six mapping pairs carry mathematically compatible types (dominant scalar eigenvalue ↔ dominant scalar eigenvalue; integral multiplication kernel ↔ integral multiplication kernel; phase-space density ↔ phase-space density; diagonal loss coefficient ↔ diagonal loss coefficient; zero-inflow boundary trace ↔ zero-inflow boundary trace; left eigenvector ↔ left eigenvector), and each operator-role description specifies a concrete shared mathematical structure rather than hedged similarity language; one structural asymmetry — Σ_t(x) being position-only in Silo A while μ(x,Ω) is direction-dependent in Silo B — is not a category error but goes unacknowledged in the matrix and is logged as a Stage 3 watch item.

- **CHECK 3 (Correspondence Vector Support):** PASS — `governing_differential_operator` is demonstrated by explicit side-by-side equations in Section 3 with a full term-by-term mapping stated in the closing paragraph; `boundary_conditions` is demonstrated across Section 2 and Section 3 by mathematically precise specification of the zero-inflow trace condition on both sides ("incoming angular flux is set to zero on a vacuum boundary" for Silo A; "With zero immigration at the habitat boundary" for Silo B; Section 2 unifies these as "zero incoming trace on the inflow portion of the phase-space boundary"); `numerical_solution_family` is demonstrated in Section 3 by the joint Perron-Frobenius argument that explicitly attributes "a source-iteration trajectory converging to that ray" to both equations as a shared consequence of their shared operator topology — this is a mathematical demonstration, not mere vocabulary, though it is established jointly rather than by independent ecological-side equations, which is noted as a watch item.

- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetry is correctly directed: nuclear criticality possesses demonstrably more mature discrete-ordinates spatial solvers, Krylov-accelerated source iteration, adjoint perturbation workflows, and variance-reduced Monte Carlo than ecology's reaction-diffusion or individual-based alternatives for directional eigenvalue problems, and no plausible case exists for reversing the direction; the falsifiability prediction is not a template non-prediction — it names specific quantitative thresholds (at least fifteen percent greater eigenvalue reduction from adjoint-ranked cell removal versus NGM/reaction-diffusion sensitivity ranking; at least one low-occupancy shadow corridor showing greater than five percent eigenvalue reduction), a specific experimental design (top-five-percent habitat cell removal in a calibrated wind-borne or current-borne invasion scenario), and a directional null outcome (failure to observe either effect in replicated field or high-fidelity simulation removals falsifies the transfer). Advisory prior-art notice: the Silo B governing equation belongs to the velocity-jump / kinetic transport family in mathematical biology (Othmer–Hillen lineage); Stage 3 should determine whether the nuclear criticality eigenvalue toolkit has been previously imported into that framework before this entry advances.

#### Stage 3 Watch Items
- **Prior art (Check 4c advisory):** The Silo B equation is the velocity-jump kinetic transport model from mathematical biology (Othmer, Hillen, Stevens, Erban). Some structural correspondence between neutron transport and biological dispersal transport has precedent in the mathematical biology literature. Novelty of this entry rests on the applied transfer of the nuclear criticality toolkit (adjoint importance maps, source iteration acceleration, discrete-ordinates spatial resolution) to invasion ecology; Stage 3 bibliometric search should specifically probe this applied claim, not just the governing-equation identity.
- **Fission kernel notation:** The Silo A equation writes νΣ_f(x, Ω'→Ω) as angle-to-angle dependent, which is a non-standard generalization; conventional one-speed criticality assumes isotropic fission and no Ω-dependence. The form is mathematically valid and structurally necessary to parallel F(x,Ω'→Ω) in Silo B, but Stage 3 should confirm whether this generalization is physically justified for the claimed Silo A use case or is a deliberate formal extension made for the isomorphism.
- **Attenuation functional asymmetry:** Σ_t(x) is position-only in Silo A; μ(x,Ω) is direction-dependent in Silo B. The vocabulary matrix does not acknowledge this difference. Stage 3 should assess whether calibrated real invasion scenarios genuinely require direction-dependent attenuation and note implications for the constitutive correspondence confidence listed in the entry metadata.
- **Numerical solution family independence:** The `numerical_solution_family` vector is established by a joint Perron-Frobenius argument in Section 3 rather than by independent ecological-side numerical equations. Stage 3 should determine whether velocity-jump ecology literature already has source-iteration-equivalent eigenvalue solvers; if so, the Section 4 transfer claim should be narrowed to discrete-ordinates spatial discretization and calibrated adjoint importance maps specifically.

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.4 Thinking-Mini
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The two displayed transport eigenvalue equations are internally consistent with the stated steady linear phase-space transport setting in Sections 1 and 3.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired terms are compatible objects of the same mathematical type, and the operator-role descriptions identify shared eigenvalue/transport structure rather than only loose analogy.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Section 1 and Section 4 support the governing_differential_operator and boundary_conditions vectors, but the listed numerical_solution_family vector is only named as “discrete-ordinates/adjoint solution family” and is not demonstrated by an equation, operator identity, or derivation.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetrically justified as a tool transfer from a more mature transport-eigenproblem toolkit to a less developed ecological setting, and the prediction specifies measurable eigenvalue reductions under a defined intervention.

#### Stage 3 Watch Items
* Verify whether the discrete-ordinates/adjoint solution-family correspondence can be backed by an explicit derivation or solver-level identity.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both equations correctly present the steady-state, linear integro-differential transport equation for their respective domains, accurately matching the structural correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings pair mathematically compatible objects (e.g., eigenvalues, boundary constraints, continuous phase-space densities) and provide explicit shared structural operator roles without relying on hedged language.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The `numerical_solution_family` vector is merely named in the text (e.g., "discrete-ordinates/adjoint solution family obey an equivalent Perron-Frobenius threshold structure" and "a source-iteration trajectory converging to that ray") without being demonstrated via an equation, operator identity, or derivation on both sides. Because the entry relies on this to reach its total count, it fails to demonstrate the required minimum of three independent correspondences.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is strongly asymmetric and the falsifiable prediction provides specific, measurable thresholds. However, the foundational structural mapping is known prior art: using integro-differential transport equations for spatial ecology (velocity-jump processes) is an established paradigm in mathematical biology (e.g., Othmer, Hillen, Lutscher).

#### Stage 3 Watch Items
- Check the proposed methodological transfer (adjoint sensitivity for targeted habitat removal) against existing mathematical ecology literature on velocity-jump models and integro-difference equations (e.g., Othmer, Hillen, Lutscher) to determine if this specific management application is genuinely novel.

### Fourth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are first-order linear integro-differential transport eigenproblems with identical operator structure (streaming + diagonal removal = integral redistribution + eigenvalue-weighted integral birth). The Silo A equation is the standard one-speed k-eigenvalue Boltzmann transport equation from nuclear criticality. The Silo B equation is a directional transport-growth eigenvalue equation that arises naturally from velocity-jump movement processes with fecundity, and is not a relabeled equation from a third field. Both are linear, first-order in space, and share the same Perron-Frobenius spectral structure claimed in Section 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six vocabulary pairs map objects of compatible mathematical type: eigenvalue ↔ eigenvalue, integral birth kernel ↔ integral birth kernel, diagonal attenuation coefficient ↔ diagonal attenuation coefficient, phase-space density ↔ phase-space density, inflow boundary condition ↔ inflow boundary condition, and left eigenfunction ↔ left eigenfunction. Every Operator Role explanation names the specific shared mathematical structure (e.g., "dominant positive eigenvalue of a linear phase-space transport operator," "left eigenvectors of the same transport operator") rather than hedging with vague analogy language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body. `governing_differential_operator` is demonstrated by the paired equations in Section 3 showing operator-identical structure. `boundary_conditions` is demonstrated in both Section 2 (vacuum inflow ↔ absorbing no-immigration boundary, with shared zero-incoming-trace structure) and Section 3 (both equations' prose descriptions specify zero inflow). `numerical_solution_family` is demonstrated in Section 3 ("source-iteration trajectory converging to that ray") and Section 4 (discrete ordinates, Krylov acceleration, adjoint perturbation theory named as the transfer vehicle).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (nuclear → ecology) is genuinely asymmetric: nuclear criticality possesses mature deterministic transport eigenvalue solvers, adjoint perturbation theory, and variance-reduced Monte Carlo, while invasion ecology relies on individual-based simulations and reaction-diffusion approximations that lose directional streaming. The prediction is falsifiable: it specifies a concrete intervention (remove top 5% of cells by adjoint importance), a comparison baseline (next-generation-matrix eigenvector centrality or reaction-diffusion sensitivity), a quantitative threshold (≥15% more eigenvalue reduction), a secondary prediction (≥1 upstream shadow corridor with >5% reduction despite low occupancy), and an explicit falsification condition (failure in replicated field or high-fidelity simulation). Advisory note: transport equations for biological movement (velocity-jump processes) are established in mathematical biology; Stage 3 should assess novelty of the specific nuclear-criticality ↔ invasion-ecology eigenvalue pairing.

#### Stage 3 Watch Items
- Transport equations for biological movement (velocity-jump processes, run-and-tumble models) are well-established in mathematical biology (Othmer, Hillen, Alt, et al.). Stage 3 should determine whether the specific k-eigenvalue nuclear-criticality ↔ population-growth-eigenvalue transport pairing has been explicitly drawn before, or whether only the broader transport-equation-for-movement analogy exists.
- The next-generation matrix eigenvalue approach in epidemiology/ecology is itself a spectral threshold method. Stage 3 should probe whether adjoint perturbation theory from nuclear transport has already been applied to ecological persistence eigenvalues under a different name (e.g., sensitivity analysis of the basic reproduction number).
- The Silo B equation's directional dependence of mortality μ(x,Ω) is somewhat unusual in standard ecological models; Stage 3 should verify whether direction-dependent mortality appears in the invasion ecology literature or whether this is a modeling assumption introduced to enforce structural parallelism.
- The fecundity kernel F(x,Ω'→Ω) mapping offspring into direction Ω from parents in direction Ω' should be verified against actual ecological dispersal kernel formulations; if ecological fecundity is typically isotropic or position-only, the directional coupling may be an artifact of the isomorphism construction.

### Fifth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are first-order linear Boltzmann-type k-eigenvalue problems (Omega·∇ + removal = scattering integral + (1/eigenvalue)*fission/fecundity integral) correctly modeling steady one-speed neutron criticality and linearized directional population spread, with shared positive-operator structure as claimed in Section 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six mappings preserve type (eigenvalue↔eigenvalue, kernel↔kernel, attenuation coefficient↔loss rate, phase-space density↔phase-space density, inflow trace↔inflow trace, left eigenvector↔left eigenvector) and each Operator Role states a shared mathematical structure (dominant eigenvalue, diagonal attenuation, same streaming operator, zero incoming trace, left eigenvector sensitivity).
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_differential_operator demonstrated by the two parallel integro-differential equations in Section 3; boundary_conditions demonstrated by "incoming angular flux is set to zero on a vacuum boundary" and "zero immigration at the habitat boundary" plus Section 2 zero incoming trace definition; numerical_solution_family demonstrated by Section 1 "discrete-ordinates/adjoint solution family", Section 3 "source-iteration trajectory converging to that ray", and Section 4 methodology transfer.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: nuclear transport toolkit (discrete ordinates, characteristics, source iteration, Krylov acceleration, adjoint perturbation) is mature for this operator class versus ecology's individual-based and reaction-diffusion approximations. Falsifiability is specific: 5% top cells by adjoint importance vs eigenvector centrality with ≥15% eigenvalue reduction threshold, plus low-fecundity upstream shadow corridor ≥5% effect, with explicit failure condition. Prior-art advisory: diffusion critical size ↔ critical patch size (KISS model) is textbook; Stage 3 should check extension to full angular transport.

#### Stage 3 Watch Items
- Related diffusion analogy reactor critical size ↔ ecological critical patch size from Kierstead-Slobodkin (1953) and Skellam (1951) is canonical; verify whether this angular Boltzmann transport isomorphism with anisotropic scattering/turning and adjoint importance maps is distinct and novel.
- Check whether velocity-jump transport-growth eigenvalue (Section 3 Silo B equation) has prior bibliometric overlap with neutron transport k-eigenvalue literature via branching process / next-generation operator formalism.

### Sixth Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A and Silo B equations are both consistent, linear, first-order transport eigenvalue problems with streaming, attenuation, angular redistribution, and multiplicative birth terms; no equation-class mismatch is present.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six token mappings pair terms of compatible mathematical type (scalar eigenvalues, integral kernels, phase‑space densities, boundary‑condition specifications, adjoint functions) and the operator‑role explanations name shared structural features without hedging.
- **CHECK 3 (Correspondence Vector Support):** PASS — The governing differential operator is demonstrated by the displayed equations and the accompanying operator‑topology summary. Boundary conditions are demonstrated by the explicit zero‑inflow descriptions for both silos. The numerical solution family is demonstrated by the description of a shared source‑iteration trajectory and the transfer of discrete‑ordinates solvers.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — (a) The stated transfer direction (Nuclear Criticality → Spatial Invasion Ecology) is genuinely asymmetric and not backwards. (b) The falsifiable prediction names specific measurable outcomes (≥15 % eigenvalue reduction, >5 % corridor effect) and unambiguous falsification conditions. (c) Prior art: the isomorphism between neutron‑transport criticality and population‑growth transport models has been explored in the literature (e.g., Rotenberg 1972). This does not affect internal consistency but is flagged for Stage 3 bibliometric validation.

#### Stage 3 Watch Items
- Rotenberg, M. (1972). Theory of population transport. *Journal of Theoretical Biology*, 37(2), 291–305 — likely an early formal statement of the analogy.
- Velocity‑jump and linear transport formulations in spatial ecology (e.g., Othmer, Hillen, etc.) that may explicitly reference neutron transport or radiative transfer.
- The human reviewer should determine whether the particular transfer of deterministic discrete‑ordinates solvers, adjoint perturbation sensitivity, and the specific directional dispersal intervention prediction have been published previously.

### Seventh Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are first-order linear transport eigenproblems of identical operator topology (streaming + attenuation = redistribution integral + scaled multiplicative integral), consistent with the claimed positive spectral structure and domains.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired mapping joins objects of matching mathematical type (eigenvalues, positive integral kernels, diagonal attenuation coefficients, phase-space densities, inflow boundary traces, left eigenvectors) with explicit shared operator roles.
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_differential_operator is shown by the explicit parallel equations and latent operator topology in Section 3; boundary_conditions by the vacuum/absorbing inflow statements in Sections 1–3; numerical_solution_family by the discrete-ordinates/source-iteration/adjoint family references in Sections 1, 3 and 4.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer is asymmetric (mature nuclear discrete-ordinates/adjoint toolkit toward ecology’s weaker directional tools); the prediction specifies measurable eigenvalue reductions (≥15 % advantage, >5 % shadow-corridor effect) under concrete removal experiments that can fail.

#### Stage 3 Watch Items
None identified.