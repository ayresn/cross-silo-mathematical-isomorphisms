---
sid_metadata:
  entry_id: "SID-0020"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "xAI"
  model_family: "Grok"
  model_version: "4.5 Fast"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "computational-micromagnetics"
  domain_b: "nematic-liquid-crystal-director-dynamics"
  structural_family: "dissipative-unit-length-orientational-torque-dynamics"
  triple_correspondence_vectors:
    - "shared_variational_effective_field_from_free_energy_functional"
    - "shared_unit_length_constraint_enforced_by_cross_product_torque_form"
    - "shared_rayleigh_dissipation_structure_linking_damping_to_rotational_viscosity"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_computational_communities / mismatched_long-range_interaction_kernels"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 8.2
  expected_methodological_transfer_score: 8.9
  community_separation_score: 7.8
  representation_mismatch_score: 6.4
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.6
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "constitutive_law_mismatch_in_long-range_kernels"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "Section 3 claims the LLG and nematic torque operators 'coincide exactly' under a stated identification, but LLG retains an intrinsic energy-conserving precession term that survives at zero damping, while the nematic equation as written is strictly dissipative for any rotational viscosity, so the two are provably different equation classes and no rescaling of the stated identification reconciles them."
    failed_checks: ["Check 1: Equation-class mismatch — LLG is damped-precessional (has a non-dissipative limit); the stated nematic torque equation is purely dissipative (gradient flow, no non-dissipative limit)"]
    flagged_checks: ["Check 4c: Prior-art recognition — pairing overlaps known numerical-analysis literature on constraint-preserving geometric integrators for unit-sphere-valued gradient flows spanning micromagnetics and liquid-crystal/harmonic-map models"]
    quoted_evidence: [
      "the correspondence holds exactly for the torque operator and the geometric constraint, and extends to the structure of the free-energy variations provided the long-range kernels are identified after nondimensionalization",
      "Under the simultaneous identification m↔n, γH_eff↔h/γ1, α↔γ1 (after nondimensionalization by the respective energy and time scales) the torque operators coincide exactly",
      "∂m/∂t = −γ m×H_eff + (α/|m|) m×(∂m/∂t)  [LLG equation, Section 3]",
      "γ1 n×(∂n/∂t) = n×h  [nematic torque-balance equation, Section 3]"
    ]
    stage_3_watch_items: [
      "Verify whether any consistent nondimensionalization reconciles α (dimensionless damping ratio in normalized LLG) with γ1 (dimensionful rotational viscosity) as asserted in Section 3; the entry invokes nondimensionalization but never carries it out.",
      "Consider whether re-scoping Silo A to the γ→0 (pure energy-relaxation / geometric-optimization) limit of LLG, rather than the full dynamic LLG, would repair the claimed torque-operator correspondence, since that limit is structurally a pure gradient flow matching the stated nematic equation.",
      "The claimed nonlocal long-range-kernel correspondence ('magnetostatic kernel...replaced by the corresponding dielectric or elastic long-range interaction') has no written counterpart in the entry's own F[n]; the stated dielectric term is a local coupling to an externally fixed field, structurally parallel to H_ext, not to the self-consistent nonlocal H_dem.",
      "Check whether Section 4's asymmetric-maturity claim partly reflects the liquid-crystal community's general preference for Q-tensor/Landau-de Gennes formulations (which avoid the unit-vector constraint entirely) rather than a genuine solver-maturity gap for the director (vector) formulation specifically.",
      "Cross-check the Section 4 transfer proposal against convergent finite-element / geometric-integrator literature that already treats LLG and harmonic-map-type liquid-crystal models within a unified framework, for direct precedent."
    ]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "FLAG"
    verdict_rationale: "The listed correspondence vectors are supported, but Section 1 overstates exact torque-operator equivalence because the displayed LLG equation contains a conservative precessional term with no counterpart in the displayed nematic torque balance."
    failed_checks: []
    flagged_checks: ["Check 1: Section 1 claims instantaneous angular velocity is exactly a cross product with the variational derivative, but the LLG equation also contains a precessional term and does not reduce to the purely dissipative nematic torque balance without an additional limit."]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether an overdamped or tangent-projected LLG limit is intended, since the nematic equation lacks the LLG precessional term.", "Confirm the nondimensionalization mapping dimensionless Gilbert damping alpha to dimensional rotational viscosity gamma_1, including the alpha versus alpha M_s Rayleigh prefactors.", "Search for prior work on unit-sphere geometric integrators shared by micromagnetics, liquid-crystal director dynamics, and harmonic-map gradient flows."]
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a dimensionally incorrect micromagnetic effective-field definition and a false claimed exact torque-operator identity between LLG and nematic director dynamics."
    failed_checks:
      - "Check 1: Equation Validity — H_eff = -δE/δm is missing the 1/(μ0 M_s) factor; the claimed exact LLG/nematic torque-operator identity is false; the LLG Rayleigh dissipation functional is dimensionally inconsistent."
      - "Check 2: Vocabulary Matrix Coherence — The effective field ↔ molecular field mapping is not type-consistent as written because the micromagnetic side uses an incorrect variational-derivative definition."
      - "Check 3: Correspondence Vector Support — Vectors shared_variational_effective_field_from_free_energy_functional and shared_rayleigh_dissipation_structure_linking_damping_to_rotational_viscosity are not validly demonstrated because their supporting equations are erroneous."
    flagged_checks:
      - "Check 2: The nematic director order-parameter space is RP^2, not S^2; this is a real but non-fatal mismatch in the unit-vector mapping."
      - "Check 4: Prior art advisory — micromagnetics ↔ nematic order-parameter dynamics is a recognizable analogy; Stage 3 should search for prior transfer literature."
    quoted_evidence:
      - "\\mathbf{H}_{\\rm eff}=-\\delta E/\\delta\\mathbf{m}"
      - "Under the simultaneous identification \\mathbf{m}\\leftrightarrow\\mathbf{n}, \\gamma\\mathbf{H}_{\\rm eff}\\leftrightarrow\\mathbf{h}/\\gamma_1, \\alpha\\leftrightarrow\\gamma_1 (after nondimensionalization by the respective energy and time scales) the torque operators coincide exactly."
      - "the Gilbert term derives from the Rayleigh dissipation \\mathcal{R}=\\frac12\\int\\alpha M_s|\\partial_t\\mathbf{m}|^2\\,dV"
      - "shared_variational_effective_field_from_free_energy_functional"
      - "shared_rayleigh_dissipation_structure_linking_damping_to_rotational_viscosity"
    stage_3_watch_items:
      - "Search for prior work on LLG/nematic order-parameter analogies and geometric integrators for orientational dynamics."
      - "Check whether correcting H_eff = -(1/(μ0 M_s)) δE/δm preserves or breaks the claimed correspondence."
      - "Probe whether the purely dissipative nematic director equation can support the LLG precessional term; if not, the structural family classification is too broad."
      - "Examine the Rayleigh dissipation function for micromagnetics, including the missing 1/γ factor, and its effect on the damping ↔ rotational-viscosity correspondence."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "Equation-class mismatch: the entry claims exact operator coincidence between a mixed conservative-dissipative equation (LLG) and a purely dissipative gradient flow (nematics)."
    failed_checks: ["Check 1: Equation Validity"]
    flagged_checks: []
    quoted_evidence: ["Under the simultaneous identification $\\mathbf{m}\\leftrightarrow\\mathbf{n}$, $\\gamma\\mathbf{H}_{\\rm eff}\\leftrightarrow\\mathbf{h}/\\gamma_1$, $\\alpha\\leftrightarrow\\gamma_1$ (after nondimensionalization by the respective energy and time scales) the torque operators coincide exactly."]
    stage_3_watch_items: []
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "All three equations are genuine, from the stated domains, of compatible classes; all three correspondence vectors are demonstrated with explicit operator identities in Section 3; the transfer direction and falsifiable prediction are sound."
    failed_checks: []
    flagged_checks: ["Check 4c: prior-art advisory — the unit-sphere constrained cross-product torque parallel between micromagnetics and nematic director dynamics is a known structural analogy in geometric-integration and soft-matter-computation literature"]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the specific transfer of Cayley-map/projected-geometric integrators from micromagnetic codes to director solvers has been explicitly proposed in the published literature, or whether only the abstract mathematical parallel has been noted; consult textbooks and reviews on geometric numerical integration for constrained dissipative systems (e.g. Hairer–Lubich–Wanner) and on computational methods for nematic liquid crystals", "Confirm that the nondimensionalization mapping alpha ↔ gamma_1 is dimensionally consistent once the stated energy and time scales are applied — the entry asserts this but does not display the nondimensionalized equations explicitly"]
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "Both equations are correct standard forms from their respective domains, share the same first-order geometric evolution structure on S² with cross-product torque and Rayleigh dissipation, all three correspondence vectors are demonstrated with explicit equations, and the falsifiable prediction names specific measurable thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["The micromagnetics ↔ nematic liquid crystal structural parallel (gradient flow on S² with cross-product torque and Rayleigh dissipation) is a mathematically transparent analogy that may be recognized in the soft-matter or geometric-integration literature; Stage 3 should verify novelty.", "The 'torque operators coincide exactly' claim in Section 3 is slightly loose: LLG contains a precessional (Hamiltonian) term -γm×H_eff absent from the purely dissipative director equation; the shared structure is the cross-product operator on S² and the dissipative Gilbert/viscous term, not the full equation. Stage 3 should check whether prior work notes this distinction.", "The asymmetry rationale assumes the LC community lacks production-grade constraint-preserving geometric integrators; Stage 3 should verify whether Cayley-map or Lie-group methods for director dynamics already exist in the computational LC literature."]
  seventh_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry claims exact coincidence of the torque operators, but the displayed LLG equation contains a reactive precession term and an implicit Gilbert damping term whereas the displayed nematic equation is pure rotational-viscous gradient relaxation, so the claimed operator-level identity is mathematically false."
    failed_checks: ["Check 1: The two displayed evolution equations do not have the same torque/operator structure despite the entry's claim that their torque operators coincide exactly."]
    flagged_checks: ["Check 2: The mapping \"Gilbert damping α ↔ Rotational viscosity γ1\" identifies coefficients with different dimensional/status roles and relies on an unstated-in-Section-2 nondimensionalization to make the correspondence meaningful."]
    quoted_evidence: ['"\frac{\partial\mathbf{m}}{\partial t}=-\gamma\mathbf{m}\times\mathbf{H}_{\rm eff}+\frac{\alpha}{|\mathbf{m}|}\mathbf{m}\times\frac{\partial\mathbf{m}}{\partial t}," versus "\gamma_1\mathbf{n}\times\frac{\partial\mathbf{n}}{\partial t}=\mathbf{n}\times\mathbf{h},\qquad\mathbf{h}=-\frac{\delta F}{\delta\mathbf{n}}," — the LLG equation has a precessional term and Gilbert term, while the nematic equation has only the rotational-viscous gradient term; consequently the later claim that "the torque operators coincide exactly" is not supported by the displayed equations.']
    stage_3_watch_items: ["Probe the asserted α ↔ γ1 correspondence carefully: α is presented as the Gilbert damping parameter while γ1 is rotational viscosity, so the claimed identification requires explicit dimensional/time-scale normalization rather than a literal coefficient equality.", "Probe the claimed extension from local variational/operator structure to the nonlocal-kernel correspondence, because the entry itself concedes that the concrete kernels differ."]
  eighth_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "FLAG"
    verdict_rationale: "Mathematical checks 1–3 pass, but Check 4 records a canonical prior-art analogy that the human Stage 3 should verify."
    failed_checks: []
    flagged_checks:
      - "Check 4: prior-art canonical analogy recognition and advisory for Stage 3"
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify prior-art overlap between LLG-type torque formulations and Ericksen‑Leslie / director-torque formulations in the literature (canonical textbook and review sources)."
      - "Examine the nondimensionalization mapping used to equate Gilbert damping α with rotational viscosity γ1 and the mapping γ H_eff ↔ h/γ1 for any hidden assumptions about time/energy scales and kernel normalization."
      - "Check the claim that micromagnetic FFT-evaluated dipolar kernels map directly to nematic long-range elastic or dielectric kernels in practical implementations; assess constitutive-kernel mismatches noted in primary_failure_risk."
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "All three vectors demonstrated with matching dissipative S2 torque operators, compatible vocabulary types, and a quantitative falsifiable integrator prediction; no class mismatch or category error."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Stage 3 should verify novelty of LLG geometric integrator → nematic director claim against Ericksen-Leslie literature and confirm long-range kernel distinction (magnetostatic vs dielectric) is properly scoped", "Confirm Freedericksz benchmark thresholds (1.5x threshold, |n|-1 <1e-12 for 1e4 times vs 1e-8 for 1e3 times, 20x energy drift reduction) are not sourced from existing liquid-crystal integrator studies"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0020

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Computational micromagnetics — continuum evolution of the magnetization vector field under exchange, anisotropy, magnetostatic and external fields, governed by the Landau–Lifshitz–Gilbert (LLG) torque equation.
* **Silo B (Field 2):** Continuum director dynamics of nematic liquid crystals (flow-aligned or quiescent limit) — evolution of the unit director field under Frank elastic, dielectric and surface anchoring energies, governed by the torque balance with rotational viscosity.
* **Mathematical Isomorphism:** Both systems are dissipative, geometrically constrained orientational dynamics on the unit sphere whose instantaneous angular velocity is given by the cross product of the order-parameter vector with the variational derivative of a free-energy functional, the dissipative coefficient entering as a Rayleigh-type linear friction that preserves the unit-length constraint identically; the correspondence holds exactly for the torque operator and the geometric constraint, and extends to the structure of the free-energy variations provided the long-range kernels are identified after nondimensionalization.

## 2. DIAGNOSTIC VOCABULARY MATRIX
* Magnetization vector \(\mathbf{m}\) ↔ Director \(\mathbf{n}\)
    * *Operator Role:* Both are unit-length vector fields (\(|\mathbf{m}|=1\), \(|\mathbf{n}|=1\)) that enter the evolution equation solely through the Lie-algebra cross-product operator that generates infinitesimal rotations on \(S^2\); the shared mathematical type is a smooth map from a spatial domain into the unit sphere.
* Effective field \(\mathbf{H}_{\rm eff}=-\delta E/\delta\mathbf{m}\) ↔ Molecular field \(\mathbf{h}=-\delta F/\delta\mathbf{n}\)
    * *Operator Role:* Both are the \(L^2\)-gradient of a free-energy functional (exchange + anisotropy + magnetostatic versus Frank elastic + dielectric); after nondimensionalization by the respective energy scales they occupy identical slots inside the cross-product torque operator.
* Gilbert damping \(\alpha\) ↔ Rotational viscosity \(\gamma_1\)
    * *Operator Role:* Both appear as the coefficient of the Rayleigh dissipation functional \(\mathcal{R}=\frac12\int\alpha|\partial_t\mathbf{m}|^2\) (respectively \(\frac12\int\gamma_1|\partial_t\mathbf{n}|^2\)) whose variational derivative with respect to angular velocity supplies the dissipative torque; the shared structure is a positive-definite quadratic form on the tangent space of the unit sphere.

## 3. CORE MATHEMATICAL PARALLELISM
In computational micromagnetics the magnetization \(\mathbf{m}(\mathbf{x},t)\) with \(|\mathbf{m}|=1\) obeys the Landau–Lifshitz–Gilbert equation
```math
\frac{\partial\mathbf{m}}{\partial t}=-\gamma\mathbf{m}\times\mathbf{H}_{\rm eff}+\frac{\alpha}{|\mathbf{m}|}\mathbf{m}\times\frac{\partial\mathbf{m}}{\partial t},
```
where the effective field is the variational derivative of the micromagnetic free-energy functional
```math
E[\mathbf{m}]=\int\Bigl(A|\nabla\mathbf{m}|^2+K\,f_{\rm an}(\mathbf{m})-\frac12\mu_0 M_s\mathbf{m}\cdot\mathbf{H}_{\rm dem}-\mu_0 M_s\mathbf{m}\cdot\mathbf{H}_{\rm ext}\Bigr)\,dV
```
and \(\mathbf{H}_{\rm eff}=-\delta E/\delta\mathbf{m}\). The cross-product form guarantees that \(\partial_t(|\mathbf{m}|^2)=0\) identically, while the Gilbert term derives from the Rayleigh dissipation \(\mathcal{R}=\frac12\int\alpha M_s|\partial_t\mathbf{m}|^2\,dV\).

In the continuum theory of nematic liquid crystals (quiescent or flow-aligned limit) the director \(\mathbf{n}(\mathbf{x},t)\) with \(|\mathbf{n}|=1\) obeys the torque-balance equation
```math
\gamma_1\mathbf{n}\times\frac{\partial\mathbf{n}}{\partial t}=\mathbf{n}\times\mathbf{h},\qquad\mathbf{h}=-\frac{\delta F}{\delta\mathbf{n}},
```
where the Frank free-energy functional is
```math
F[\mathbf{n}]=\int\Bigl(\frac12 K_1(\nabla\cdot\mathbf{n})^2+\frac12 K_2(\mathbf{n}\cdot\nabla\times\mathbf{n})^2+\frac12 K_3|\mathbf{n}\times\nabla\times\mathbf{n}|^2-\frac12\varepsilon_0\Delta\varepsilon(\mathbf{n}\cdot\mathbf{E})^2\Bigr)\,dV
```
(plus surface anchoring). The identical cross-product structure again enforces \(\partial_t(|\mathbf{n}|^2)=0\), and \(\gamma_1\) is the coefficient of the Rayleigh dissipation \(\mathcal{R}=\frac12\int\gamma_1|\partial_t\mathbf{n}|^2\,dV\).

Under the simultaneous identification \(\mathbf{m}\leftrightarrow\mathbf{n}\), \(\gamma\mathbf{H}_{\rm eff}\leftrightarrow\mathbf{h}/\gamma_1\), \(\alpha\leftrightarrow\gamma_1\) (after nondimensionalization by the respective energy and time scales) the torque operators coincide exactly. The variational structure of the effective/molecular fields coincides once the exchange stiffness \(A\) is mapped onto the Frank constants and the magnetostatic kernel is replaced by the corresponding dielectric or elastic long-range interaction; the correspondence therefore holds at the level of the differential operators, the geometric constraint, and the dissipation functional, and stops only at the concrete form of the nonlocal kernels.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
* **Preferred Transfer Direction:** computational-micromagnetics → nematic-liquid-crystal-director-dynamics
* **Asymmetric Maturity Rationale:** Micromagnetics possesses a mature ecosystem of geometric integrators (projected Runge–Kutta, Cayley-map and Lie-group methods) that exactly preserve the unit-sphere constraint and the Lyapunov structure of the free energy for systems containing long-range dipolar kernels evaluated by FFT; the liquid-crystal community has highly developed continuum rheology and defect topology but comparatively fewer production-grade, constraint-preserving, large-scale parallel solvers for the pure director equation in complex three-dimensional geometries with nonlocal elastic interactions.
* **Target Bottleneck Mitigation:** Importation of a micromagnetic geometric integrator (specifically a second-order projected or Cayley-transform scheme that stays on \(S^2\) to machine precision) into a finite-element or finite-difference director code eliminates the need for intermittent renormalization and the associated artificial dissipation, thereby removing a well-documented source of long-term energy drift and topological charge violation in extended defect simulations.
* **Falsifiable Prediction:** On the standard Freedericksz-transition benchmark (planar nematic cell, dielectric anisotropy \(\Delta\varepsilon>0\), sudden voltage step to \(1.5\times\) threshold), a Cayley-map integrator transferred from micromagnetics will keep the pointwise deviation \(\bigl||\mathbf{n}|-1\bigr|_\infty<10^{-12}\) for at least \(10^4\) director relaxation times while a conventional explicit Runge–Kutta scheme with periodic renormalization will exceed \(10^{-8}\) after fewer than \(10^3\) relaxation times; the same integrator will reduce the secular drift of the Frank free energy by at least a factor of twenty relative to the renormalized baseline at identical time-step size. Observation of comparable or larger drift under the geometric integrator would falsify the claimed operator-level transferability.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
* `"Landau-Lifshitz-Gilbert" AND "unit sphere constraint" AND "geometric integrator" AND "Cayley"`
* `"nematic director dynamics" AND "Frank free energy" AND "rotational viscosity" AND "torque balance"`
* `"micromagnetic geometric integrator" AND "liquid crystal director" AND "unit length preservation"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 3 states that under the identification m↔n, γH_eff↔h/γ1, α↔γ1, "the torque operators coincide exactly," but this is false. The LLG equation "∂m/∂t = −γ m×H_eff + (α/|m|) m×(∂m/∂t)" contains a precession term (−γ m×H_eff) that survives independently of damping: at α=0 it gives dE/dt=0 exactly (a genuine energy-conserving regime), since H_eff·(m×H_eff)=0 identically. The nematic equation "γ1 n×(∂n/∂t) = n×h," solved explicitly via n×(both sides) and n·(∂n/∂t)=0, reduces to ṅ = h⊥/γ1, giving dF/dt = −(1/γ1)∫|h⊥|²dV ≤ 0 for every γ1>0 — strictly dissipative with no parameter choice yielding a conservative regime, because γ1 multiplies the entire (sole) term rather than an independent damping sub-term. A damped-precessional operator with a non-trivial conservative limit cannot "coincide exactly," under any rescaling of constants, with an operator that is dissipative for all parameter values; this is an equation-class mismatch, not a labeling or normalization issue.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The three pairs (m↔n, H_eff↔h, α↔γ1) each pair objects of compatible mathematical type: unit-length vector fields on S², L²-gradients of a free-energy functional, and scalar coefficients of a quadratic Rayleigh dissipation functional, respectively. None of Check 2's disqualifying category errors (domain-to-time-point, continuum-to-threshold, rate-to-position, etc.) is present. See Stage 3 watch items regarding the α/γ1 dimensional asymmetry, which bears on Check 1 but is not itself a type mismatch.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors have direct equational support in Section 3. "shared_variational_effective_field_from_free_energy_functional" is shown via H_eff=−δE/δm and h=−δF/δn, both applied to explicitly written functionals E[m] and F[n]. "shared_unit_length_constraint_enforced_by_cross_product_torque_form" is shown via the explicit statements that the cross-product form enforces ∂t(|m|²)=0 and ∂t(|n|²)=0. "shared_rayleigh_dissipation_structure_linking_damping_to_rotational_viscosity" is shown via the explicit R=½∫αMs|∂tm|²dV and R=½∫γ1|∂tn|²dV functionals. Note that Section 1's further claim that this "extends to the structure of the free-energy variations provided the long-range kernels are identified" is not itself carried out anywhere in the body (Section 3 states the correspondence merely "stops only at the concrete form of the nonlocal kernels") — this bears on the overall isomorphism claim addressed under Check 1, not on whether the three named vectors individually have body support.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (4a) is adequately argued: Section 4 names specific micromagnetic tooling (projected/Cayley-map geometric integrators, FFT-evaluated dipolar kernels) and a specific gap on the nematic side (fewer production-grade constraint-preserving large-scale solvers for the pure director equation), rather than asserting reversibility. Falsifiability (4b) is satisfied: the Freedericksz-transition prediction names specific measurable thresholds (||n|−1|∞<10⁻¹² over ≥10⁴ relaxation times vs. >10⁻⁸ within <10³ for the renormalized baseline, ≥20× reduction in secular free-energy drift) and an explicit falsification condition, not a template non-prediction. Prior art (4c, advisory only): this pairing overlaps a recognizable numerical-analysis literature on constraint-preserving geometric integrators for unit-sphere-valued gradient flows spanning micromagnetics (LLG) and harmonic-map-type liquid-crystal models — e.g., convergent finite-element treatments developed in the tradition of Alouges/Bartels/Prohl that address both LLG and Ericksen–Leslie/harmonic-map director models. Flagged for Stage 3 bibliometric follow-up; not grounds for rejection on its own.

#### Stage 3 Watch Items
- Verify whether any consistent nondimensionalization actually reconciles α (dimensionless in normalized LLG) with γ1 (dimensionful rotational viscosity) as Section 3 asserts; the nondimensionalization is invoked but never carried out in the entry.
- Consider whether re-scoping Silo A to the γ→0 (pure relaxation / energy-minimization) limit of LLG, rather than the full dynamic LLG, would repair the Check 1 finding, since that limit is structurally a pure gradient flow matching the stated nematic equation.
- The claimed nonlocal-kernel correspondence has no written counterpart in the entry's own F[n]; the stated dielectric term (n·E)² is a local coupling to an externally fixed field, parallel to H_ext, not to the self-consistent nonlocal H_dem — probe whether a genuine long-range nematic analog exists before accepting this part of the isomorphism.
- Check whether the Section 4 asymmetric-maturity claim partly reflects the liquid-crystal community's general preference for Q-tensor/Landau–de Gennes formulations (which sidestep the unit-vector constraint) rather than a true solver gap for the director formulation itself.
- Cross-check the Section 4 transfer proposal against existing convergent finite-element / geometric-integrator literature already unifying LLG and harmonic-map-type liquid-crystal numerics, for direct precedent.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The equations are domain-appropriate, but the Section 1 claim that "instantaneous angular velocity is given by the cross product of the order-parameter vector with the variational derivative" is not exactly supported by the displayed LLG equation, which contains the precessional term \(-\gamma\mathbf{m}\times\mathbf{H}_{\rm eff}\) and does not reduce to the purely dissipative nematic torque balance without an additional overdamped or projected limit.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are type-compatible (unit vector fields, variational fields, dissipation coefficients), and the dimensional alpha/gamma_1 issue is qualified by the Section 3 nondimensionalization statement.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are supported: variational fields by \( \mathbf{H}_{\rm eff}=-\delta E/\delta\mathbf{m} \) and \( \mathbf{h}=-\delta F/\delta\mathbf{n} \) in Section 3; unit-length cross-product structure by the norm-preservation statements in Section 3; Rayleigh dissipation by the Rayleigh functionals and coefficient mapping in Sections 2–3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric as stated, and the Freedericksz prediction supplies quantitative thresholds; no canonical textbook prior art is recognized here, but related geometric-integrator literature should be checked at Stage 3.

#### Stage 3 Watch Items
- Verify whether an overdamped or tangent-projected LLG limit is intended, because the displayed nematic equation has no counterpart to the LLG conservative precession term.
- Confirm the nondimensionalization that maps dimensionless Gilbert damping alpha to rotational viscosity gamma_1, and reconcile the Rayleigh prefactors alpha and alpha M_s between Sections 2 and 3.
- Examine prior literature on unit-sphere/geometric integrators across micromagnetics, liquid-crystal director dynamics, and harmonic-map gradient flows.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry states \(\mathbf{H}_{\rm eff}=-\delta E/\delta\mathbf{m}\), but \(\delta E/\delta\mathbf{m}\) has units of energy density (\(J/m^3\)), not magnetic field (\(A/m\)); the standard relation is \(\mathbf{H}_{\rm eff}=-(1/(\mu_0 M_s))\delta E/\delta\mathbf{m}\). In addition, the claimed exact torque-operator identity is false: the LLG equation contains the precessional term \(-\gamma\mathbf{m}\times\mathbf{H}_{\rm eff}\) plus damping, while the nematic equation is equivalent to \(\partial_t\mathbf{n}=(1/\gamma_1)\mathbf{h}_\perp\), a purely dissipative gradient flow with no precessional term.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The pair \(\mathbf{H}_{\rm eff}=-\delta E/\delta\mathbf{m} \leftrightarrow \mathbf{h}=-\delta F/\delta\mathbf{n}\) is not type-consistent as written because the micromagnetic side uses the incorrect effective-field definition already identified. The unit-vector mapping also elides the nematic \(RP^2\) head-tail symmetry, though this is a separate, non-fatal issue.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 2, shared unit-length constraint enforced by the cross-product torque form, is demonstrated. Vectors 1 and 3, the shared variational effective field and the shared Rayleigh dissipation structure, are not validly demonstrated because their supporting equations are erroneous.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction micromagnetics → liquid crystal is plausibly asymmetric and the Freedericksz prediction is falsifiable with specific thresholds. However, this domain pairing is a recognizable analogy, so Stage 3 should probe prior art.

#### Stage 3 Watch Items
- Search for prior work on LLG/nematic order-parameter analogies and geometric integrators for orientational dynamics.
- Check whether correcting \(\mathbf{H}_{\rm eff}=-(1/(\mu_0 M_s))\delta E/\delta\mathbf{m}\) preserves or breaks the claimed correspondence.
- Probe whether the purely dissipative nematic director equation can support the LLG precessional term; if not, the structural family classification is too broad.
- Examine the Rayleigh dissipation function for micromagnetics, including the missing \(1/\gamma\) factor, and its effect on the damping ↔ rotational-viscosity correspondence.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The claim that "Under the simultaneous identification $\mathbf{m}\leftrightarrow\mathbf{n}$, $\gamma\mathbf{H}_{\rm eff}\leftrightarrow\mathbf{h}/\gamma_1$, $\alpha\leftrightarrow\gamma_1$ (after nondimensionalization by the respective energy and time scales) the torque operators coincide exactly" is mathematically false. The Landau-Lifshitz-Gilbert equation contains a conservative precessional term ($-\gamma\mathbf{m}\times\mathbf{H}_{\rm eff}$) tied to angular momentum, making it a mixed conservative-dissipative system, whereas the nematic equation ($\gamma_1\mathbf{n}\times\frac{\partial\mathbf{n}}{\partial t}=\mathbf{n}\times\mathbf{h}$) is a purely dissipative gradient flow without precession; substituting the proposed mapping into LLG yields an equation that physically and mathematically contradicts the nematic one.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped terms are of compatible mathematical types and have explicit shared structures (both unit vector fields, $L^2$-gradients of free energy, and coefficients of Rayleigh dissipation functionals).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (shared variational effective field, shared unit length constraint, shared Rayleigh dissipation structure) are explicitly demonstrated in Section 3 with equations and derivations.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric with a valid rationale (mature geometric integrators in micromagnetics applied to nematics), and the falsifiable prediction names a specific, measurable difference in topological charge violation ($\bigl||\mathbf{n}|-1\bigr|_\infty<10^{-12}$ vs $10^{-8}$) and energy drift against a defined baseline.

#### Stage 3 Watch Items
None identified.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Landau–Lifshitz–Gilbert equation, the micromagnetic free-energy functional, the nematic torque-balance equation, and the Frank–Oseen free-energy functional are all genuine, correctly stated, and belong to compatible equation classes (first-order-in-time, second-order-in-space parabolic evolution on the unit sphere with cross-product constraint-preserving structure). The entry correctly acknowledges that the correspondence extends to the torque operator and geometric constraint but stops at the concrete form of the nonlocal kernels (magnetostatic dipolar versus dielectric/elastic).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mapped pairs (m ↔ n, H_eff ↔ h, α ↔ γ_1) are between objects of compatible mathematical type. Each Operator Role explanation names a specific shared mathematical structure (Lie-algebra cross-product generating S² rotations; L² gradient of free-energy functional; positive-definite quadratic Rayleigh dissipation form on the tangent space) rather than relying on hedged similarity language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in Section 3 with equations: (1) the variational effective-field structure is shown explicitly via δE/δm and δF/δn; (2) the unit-length constraint enforced by cross-product torque is shown by computing ∂_t(|m|²)=0 and ∂_t(|n|²)=0 identically from the cross-product form; (3) the Rayleigh dissipation structure is displayed for both systems with explicit functional forms and linked to the damping coefficients.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer is genuinely asymmetric (magnetics geometric integrators → liquid-crystal director codes, with a plausible maturity gap rationale). The falsifiable prediction names a specific benchmark (Freedericksz transition at 1.5× threshold), specific measurable quantities (pointwise unit-deviation < 10⁻¹² vs. 10⁻⁸, and a factor-of-twenty reduction in free-energy secular drift), and an explicit falsification condition (comparable or larger drift under the geometric integrator would falsify the claim). Prior-art advisory: the unit-sphere cross-product torque parallel between micromagnetics and nematic director dynamics is a recognized structural analogy in the geometric-integration and computational-soft-matter communities.

#### Stage 3 Watch Items
- Verify whether the specific proposal to transfer Cayley-map or projected geometric integrators from micromagnetic solvers to nematic director codes has appeared in the published literature, or whether prior work only notes the abstract mathematical parallel without proposing a concrete solver transfer. Relevant sources include textbooks and reviews on geometric numerical integration for constrained dissipative systems and on computational methods for nematic liquid crystal dynamics.
- The nondimensionalization that makes α ↔ γ₁ dimensionally consistent is asserted but not displayed — Stage 3 should confirm that the entry's claimed identification is achievable with a self-consistent choice of reference scales.
- The minor inconsistency between the Rayleigh dissipation prefactors in Section 2 (α without M_s) and Section 3 (α M_s) is cosmetically inconsistent but not mathematically consequential since M_s is a constant; no action required but worth noting during editorial pass.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the LLG equation and the Ericksen-Leslie director torque-balance equation are correct standard forms; both are first-order-in-time geometric evolution equations on S² with cross-product torque structure and Rayleigh dissipation. The free-energy functionals (micromagnetic exchange + anisotropy + demagnetizing + Zeeman, and Frank elastic + dielectric) are standard and correctly stated. No equation-class mismatch: neither equation is elliptic, parabolic, or hyperbolic in the PDE sense — both are first-order ODE-in-time geometric flows with spatial operator structure entering through the variational derivative. One minor imprecision: the entry claims "the torque operators coincide exactly," but the LLG contains a precessional (conservative) term −γ**m**×**H**_eff that has no counterpart in the purely dissipative director equation γ₁**n**×∂_t**n** = **n**×**h**. The shared structure is the cross-product Lie-algebraic operator on S² and the Rayleigh-dissipative term, not the full equation. This is compression, not a mathematical error — the cross-product torque operator and unit-length constraint preservation are genuinely shared.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mappings pair objects of compatible mathematical type: (**m**, **n**) are both unit-length vector fields (smooth maps into S²); (**H**_eff, **h**) are both L²-gradients of free-energy functionals; (α, γ₁) are both coefficients of positive-definite quadratic Rayleigh dissipation functionals on the tangent space of S². The dimensional mismatch between the dimensionless α and the dimensional γ₁ is explicitly acknowledged with a stated nondimensionalization. No category errors detected.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body with explicit equations. (1) "shared_variational_effective_field_from_free_energy_functional" is demonstrated by **H**_eff = −δE/δ**m** and **h** = −δF/δ**n** with both functionals written out (Section 3). (2) "shared_unit_length_constraint_enforced_by_cross_product_torque_form" is demonstrated by the cross-product structure in both equations and the explicit statements that ∂_t(|**m**|²) = 0 and ∂_t(|**n**|²) = 0 identically (Section 3). (3) "shared_rayleigh_dissipation_structure_linking_damping_to_rotational_viscosity" is demonstrated by the explicit Rayleigh functionals R = ½∫αM_s|∂_t**m**|² dV and R = ½∫γ₁|∂_t**n**|² dV (Section 3).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetry direction (micromagnetics → LC) is plausible and specifically motivated: the micromagnetics community has developed mature geometric integrators (Cayley-map, projected RK, Lie-group methods) for constraint-preserving S² dynamics with nonlocal kernels, while the LC community's computational effort has focused more on continuum rheology and defect topology than on production-grade constraint-preserving director solvers. The falsifiable prediction is specific and measurable: it names a standard benchmark (Freedericksz transition, Δε > 0, 1.5× threshold voltage), specific quantitative thresholds (||**n**| − 1|_∞ < 10⁻¹² for 10⁴ relaxation times vs. > 10⁻⁸ after < 10³ relaxation times; Frank energy drift reduction by factor ≥ 20), and an explicit falsification condition. Advisory: the micromagnetics ↔ nematic LC structural parallel is a mathematically transparent analogy that may have prior articulation in the soft-matter or geometric-integration literature; flagged for Stage 3 bibliometric verification.

#### Stage 3 Watch Items
- Verify whether the LLG ↔ Ericksen-Leslie director equation isomorphism has been previously published, particularly in geometric mechanics or computational soft-matter contexts. The shared cross-product torque / Rayleigh dissipation structure on S² is mathematically obvious to practitioners in both fields.
- Probe whether the "torque operators coincide exactly" claim (Section 3) overstates the correspondence: the LLG precessional term −γ**m**×**H**_eff is conservative (Hamiltonian), while the director equation is purely dissipative. The exact correspondence holds for the dissipative structure and the cross-product operator, not for the full equations. Check whether prior work makes this distinction.
- Verify the asymmetry claim: check whether Cayley-map or Lie-group geometric integrators for nematic director dynamics already exist in the computational LC literature (e.g., in finite-element or spectral method contexts).
- Assess whether the Freedericksz-transition benchmark prediction (factor-of-20 drift reduction, 10⁻¹² constraint preservation) is consistent with known performance of geometric integrators applied to similar S²-constrained dynamics.

### Seventh Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The displayed LLG equation `\frac{\partial\mathbf{m}}{\partial t}=-\gamma\mathbf{m}\times\mathbf{H}_{\rm eff}+\frac{\alpha}{|\mathbf{m}|}\mathbf{m}\times\frac{\partial\mathbf{m}}{\partial t},` contains reactive precession plus Gilbert damping, whereas `\gamma_1\mathbf{n}\times\frac{\partial\mathbf{n}}{\partial t}=\mathbf{n}\times\mathbf{h}` is pure rotational-viscous gradient relaxation, so the entry's later claim that “the torque operators coincide exactly” is false.
* **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping `Gilbert damping \(\alpha\) ↔ Rotational viscosity \(\gamma_1\)` pairs coefficients of different dimensional/status roles; the entry only makes them comparable after nondimensionalization in Section 3, so the direct Section 2 mapping is insufficiently established.
* **CHECK 3 (Correspondence Vector Support):** PASS — The variational-field vector is supported by the two explicit free-energy functionals and variational derivatives in Section 3; the unit-length vector is supported by the explicit (|\mathbf m|=|\mathbf n|=1) constraints and cross-product preservation; and the Rayleigh-dissipation vector is supported by the two explicit quadratic dissipation functionals in Section 3.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated micromagnetics-to-director-dynamics direction is given an internal maturity rationale, and the Freedericksz benchmark supplies concrete norm-error and Frank-energy-drift thresholds that can in principle falsify the transfer claim.

#### Stage 3 Watch Items
* Probe the claimed (\alpha\leftrightarrow\gamma_1) coefficient correspondence, particularly its dimensional consistency and dependence on nondimensionalization.
* Probe the claimed extension from shared variational structure to correspondence of the distinct nonlocal magnetostatic versus dielectric/elastic kernels.

### Eighth Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Landau–Lifshitz–Gilbert form and the nematic torque-balance equation are presented in consistent rotational (cross-product) torque form and belong to the same class of constrained orientational evolution equations; both display the unit-length-preserving cross-product structure and appropriate variational definitions of effective/molecular fields.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens (\(\mathbf{m}\leftrightarrow\mathbf{n}\), \(\mathbf{H}_{\rm eff}\leftrightarrow\mathbf{h}\), \(\alpha\leftrightarrow\gamma_1\)) are all objects of compatible mathematical type (unit-vector fields, variational gradients, positive dissipation coefficients) and the entry explicitly invokes nondimensionalization where needed.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed correspondence vectors are demonstrated in the body:  
  - **shared_variational_effective_field_from_free_energy_functional:** shown by \(\mathbf{H}_{\rm eff}=-\delta E/\delta\mathbf{m}\) and \(\mathbf{h}=-\delta F/\delta\mathbf{n}\) with mapping of exchange/Frank terms and discussion of long-range kernels (Section 3).  
  - **shared_unit_length_constraint_enforced_by_cross_product_torque_form:** shown by the cross-product forms that enforce \(\partial_t(|\mathbf{m}|^2)=0\) and \(\partial_t(|\mathbf{n}|^2)=0\) (Section 3).  
  - **shared_rayleigh_dissipation_structure_linking_damping_to_rotational_viscosity:** shown by the Rayleigh dissipation functionals \(\mathcal{R}=\tfrac12\int\alpha M_s|\partial_t\mathbf{m}|^2\,dV\) and \(\mathcal{R}=\tfrac12\int\gamma_1|\partial_t\mathbf{n}|^2\,dV\) and the stated mapping \(\alpha\leftrightarrow\gamma_1\) (Section 2 and 3).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The methodological transfer is asymmetric and the entry supplies a concrete, falsifiable benchmark (Freedericksz transition with explicit numerical thresholds). However, I recognize the domain pairing as a canonical analogy between LLG-type magnetization torque dynamics and director torque formulations (Ericksen‑Leslie / director torque balance) from standard disciplinary knowledge; this prior-art recognition is advisory and should be probed by the Stage 3 bibliometric review.

#### Stage 3 Watch Items
- Verify canonical prior-art: check classic texts/reviews on nematic director dynamics and micromagnetics for previously published mappings between LLG and director torque equations (e.g., standard Ericksen‑Leslie formulations and LLG analogies).
- Inspect the nondimensionalization steps and scale choices that justify mapping the dimensionless Gilbert damping \(\alpha\) to rotational viscosity \(\gamma_1\) and the mapping \(\gamma\mathbf{H}_{\rm eff}\leftrightarrow\mathbf{h}/\gamma_1\); ensure no hidden assumptions about kernel normalization or time-scale separation.
- Examine the practical mapping of magnetostatic dipolar kernels to nematic long-range elastic/dielectric kernels in numerical implementations; Stage 3 should assess whether the noted "constitutive_law_mismatch_in_long-range_kernels" is already resolved in prior literature or remains a substantive obstacle.
- Confirm whether the claimed advantage of micromagnetic geometric integrators for large-scale, nonlocal nematic director simulations has been previously implemented or benchmarked in the literature.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations correctly model their claimed domains (LLG with precession plus Gilbert damping and nematic torque balance γ1 n×∂t n = n×h), share first-order dissipative S2-valued cross-product structure with no elliptic/parabolic or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairs are type-compatible (unit vector field ↔ unit vector field, L2-gradient field ↔ L2-gradient field, scalar Rayleigh coefficient ↔ scalar Rayleigh coefficient) and each Operator Role specifies shared structure (Lie-algebra cross-product on S2, identical slot in torque operator, positive-definite quadratic form on tangent space).
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors are demonstrated: shared_variational_effective_field_from_free_energy_functional via E and F with H_eff=-δE/δm and h=-δF/δn in Section 3; shared_unit_length_constraint_enforced_by_cross_product_torque_form via cross-product evolution forms and explicit ∂t(|m|^2)=0 and ∂t(|n|^2)=0 statements in Section 3; shared_rayleigh_dissipation_structure_linking_damping_to_rotational_viscosity via Rayleigh functionals R=½∫α|∂t m|² and R=½∫γ1|∂t n|² in Sections 2 and 3.[m][n]
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is plausible (mature Cayley-map/projected RK ecosystem in micromagnetics → fewer production-grade constraint-preserving solvers in director dynamics) and not backwards; falsifiability is satisfied with specific Freedericksz-transition benchmark, quantitative thresholds for |||n|-1||_∞ <1e-12 for 1e4 times vs >1e-8 for <1e3 times and 20× reduction in Frank free-energy drift at identical dt, plus explicit falsification condition. No canonical textbook prior-art requiring advisory FLAG.

#### Stage 3 Watch Items
- Verify bibliometric novelty of geometric integrator transfer against Ericksen-Leslie and liquid-crystal defect simulation literature; check whether Cayley-map methods have already been applied to nematic director codes.
- Confirm long-range kernel caveat (magnetostatic vs dielectric/elastic) acknowledged in Sections 1 and 3 does not collapse operator identity, as entry explicitly scopes correspondence to differential operators and dissipation structure.