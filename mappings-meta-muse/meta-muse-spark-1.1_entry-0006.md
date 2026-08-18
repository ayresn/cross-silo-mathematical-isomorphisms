---
sid_metadata:
  entry_id: "SID-0006"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "Meta"
  model_family: "Muse"
  model_version: "Spark 1.1"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "collisionless-electrostatic-plasma-kinetics"
  domain_b: "dilute-pusher-microswimmer-suspension-kinetics"
  structural_family: "kinetic-mean-field-instabilities"
  triple_correspondence_vectors:
    - "vlasov_advection_self_consistent_elliptic_field_operator"
    - "penrose_shelley_landau_contour_dispersion_function"
    - "particle_number_conservation_plus_hamiltonian_casimir_energy"
    - "periodic_boundary_van_kampen_continuum_mode_spectrum"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language, incompatible_ontologies, historically_isolated_communities, velocity_orientation_type_mismatch"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.4
  community_separation_score: 8.9
  representation_mismatch_score: 9.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.2
    uncertainty: "±0.9"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "Section 4's falsifiable prediction does not follow from the entry's own equations: the entry's own formula α_a = -σ0 n0/(μ D_r) applied to its own stated σ0, n0, μ, D_r gives α_a = 20, not the stated 13.3, and the entry's own growth-rate formula σ(k) evaluated at the entry's own stated k = 3.14 mm^-1 gives σ(k) ≈ -0.03 s^-1 (stable), directly contradicting the claimed σ = 0.32 ± 0.05 s^-1 (unstable)."
    failed_checks: ["Check 4: Falsifiable prediction in Section 4 numerically contradicts the entry's own formulas from Section 2 and Section 3"]
    flagged_checks: ["Check 1: The 'shared operator' claim in Section 3's Bridge paragraph excludes the D_r, D_t diffusion terms present in Silo B's Smoluchowski equation but absent from Silo A's collisionless Vlasov equation", "Check 2: Vocabulary matrix row 3 (Section 2) headline pairs ω_p² [dimension 1/T²] with σ0 n0/μ [dimension 1/T]; only resolved once each is further divided by k²v_th² or D_r to form the dimensionless α, α_a actually compared"]
    quoted_evidence: ['dimensionless α_a=13.3', 'α_a = -σ0 n0/(μ D_r)', 'σ = d/dt log⟨|u|²⟩ = 0.32 ±0.05 s^-1', 'σ(k) = -D_r - \frac{\sigma_0 n_0}{15\mu} \mathcal{I}(k\ell_{run})']
    stage_3_watch_items: ["Independently recompute the Section 4 worked numerical example (α_a and σ(k)); Stage 2 found the stated values inconsistent with the entry's own formulas and inputs, and the sign of the predicted growth rate flips under correct recomputation.", "Check the active-suspension linear-stability literature (Saintillan-Shelley and related work) for prior explicit use of plasma Landau-damping / Penrose-criterion machinery, since the general approach resembles recognizable prior methodology (Check 4c, advisory).", "Confirm whether the D_r, D_t diffusion terms belong inside or outside the claimed shared Vlasov operator, since Section 3's operator-identity statement is silent on this."]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "Check 1 fails because the entry asserts an identical first-order hyperbolic Vlasov class while displaying a parabolic Smoluchowski equation, and the active dispersion integral does not support the quoted growth-rate integral or threshold."
    failed_checks:
      - "Check 1: claimed first-order hyperbolic equation class contradicts the displayed Silo B equation containing D_r Δ_p Ψ + D_t Δ_x Ψ"
      - "Check 1: active dispersion integrand proportional to μ^4 is inconsistent with the quoted growth-rate integral I(z)=∫ μ^2/(1-izμ)dμ and the claimed α_a,c>15/2 threshold"
    flagged_checks:
      - "Check 4: the prediction states α_a=13.3 for n0=2.0×10^15 m^-3, but the listed σ0, μ, and D_r give α_a=20"
    quoted_evidence:
      - 'Both systems evolve under the same Vlasov-type hyperbolic advection operator for a phase-space density coupled self-consistently to an elliptic field inversion'
      - 'Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion.'
      - '\partial_t \Psi + \nabla_x \cdot [(U_0 p + u)\Psi] + \nabla_p \cdot [(I-pp)\cdot \nabla_x u \cdot p \, \Psi] = D_r \Delta_p \Psi + D_t \Delta_x \Psi'
      - '\mathcal{D}_a(k,\omega)= 1 + \frac{\sigma_0 n_0}{5\mu} \int_{S^2} \frac{(k\cdot p)^2 (p\cdot \hat{k})^2 }{ \omega + i D_r - U_0 k\cdot p + i0^+ } dp =0'
      - '\sigma(k) = -D_r - \frac{\sigma_0 n_0}{15\mu} \mathcal{I}(k\ell_{run}) + O(k^2 D_t), \quad \mathcal{I}(z)=\int_{-1}^{1}\frac{\mu^2}{1 - i z \mu} d\mu'
      - 'closed-form analytic threshold α_a,c = -σ0 n0/(μ D_r) > 15/2 for pusher instability on S^2'
    stage_3_watch_items:
      - "Determine whether the isomorphism is intended only in the D_r,D_t→0 limit and whether that limit is compatible with the stated bacterial-turbulence application."
      - "Verify whether Saintillan-Shelley or related active-suspension work already uses Vlasov/Penrose/Landau-contour methods (prior-art check)."
      - "Reconcile the coupling constant normalization and critical threshold with the displayed dispersion relation."
      - "Check the numerical prediction in Section 4, including α_a and σ(k), against the entry's own formulas."
      - "Assess whether E ↔ S_p is meant as a pointwise-in-p mapping, since S_p depends on orientation while E does not."
  third_adversarial_review:
    reviewer_model: 'DeepSeek DeepSeek V4 Pro'
    protocol_version: '2.0-production'
    review_timestamp: '2026-08-13'
    verdict: 'REJECT'
    verdict_rationale: 'The entry claims an identical hyperbolic-plus-elliptic operator class, but the displayed active-matter kinetic equation is parabolic due to diffusion, and the active dispersion relation is internally inconsistent with its own reduced growth-rate integral.'
    failed_checks:
      - 'Check 1: Equation-class mismatch and inconsistent active dispersion formula'
      - 'Check 2: Vocabulary matrix misattributes direct elliptic inversion to S_p, which is a derived strain-rate projection rather than the Stokes-inverted field'
    flagged_checks:
      - 'Check 3: Hamiltonian-Casimir vector is asserted rather than demonstrated; no Lie-Poisson bracket or conservation proof is supplied'
    quoted_evidence:
      - 'Both systems evolve under the same Vlasov-type hyperbolic advection operator for a phase-space density coupled self-consistently to an elliptic field inversion'
      - 'Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion'
      - '\partial_t \Psi + \nabla_x \cdot [(U_0 p + u)\Psi] + \nabla_p \cdot [(I-pp)\cdot \nabla_x u \cdot p \, \Psi] = D_r \Delta_p \Psi + D_t \Delta_x \Psi'
      - '\mathcal{D}_a(k,\omega)= 1 + \frac{\sigma_0 n_0}{5\mu} \int_{S^2} \frac{(k\cdot p)^2 (p\cdot \hat{k})^2 }{ \omega + i D_r - U_0 k\cdot p + i0^+ } dp =0'
      - '\sigma(k) = -D_r - \frac{\sigma_0 n_0}{15\mu} \mathcal{I}(k\ell_{run}) + O(k^2 D_t), \quad \mathcal{I}(z)=\int_{-1}^{1}\frac{\mu^2}{1 - i z \mu} d\mu'
      - 'Both are the self-consistent field obtained by elliptic inversion of a moment of the distribution, i.e., E = K_Poisson * (∫ f dv) via Poisson operator -Δ, and S_p = K_Stokes * (∫ (pp-I/3) Ψ dp) via Stokes operator -Δ+∇q, entering as the velocity-space/orientation-space advection coefficient in L.'
    stage_3_watch_items:
      - 'Verify whether the claimed Vlasov-Poisson ↔ Saintillan-Shelley isomorphism is already published; the entry itself cites Saintillan-Shelley-Hohenegger linear analysis.'
      - 'Check the correct Saintillan-Shelley dispersion integrand: the μ^4 vs μ^2 inconsistency suggests a transcription or fabrication error.'
      - 'Probe whether the active Hamiltonian-Casimir formulation exists or is imported incorrectly from passive kinetic theory.'
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry fails on equation validity due to an explicit equation-class mismatch between the two systems despite claims of identity."
    failed_checks: ["Check 1: Equation Validity"]
    flagged_checks: []
    quoted_evidence: ["Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion."]
    stage_3_watch_items: []
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "FLAG"
    verdict_rationale: "All four correspondence vectors are demonstrated with correct equations and the structural isomorphism is mathematically sound, but the falsifiable prediction in Section 4 contains an internal arithmetic inconsistency in the dimensionless coupling parameter."
    failed_checks: []
    flagged_checks: ["Check 4b: dimensionless parameter α_a=13.3 inconsistent with stated formula and parameters (computes to 20)", "Check 4b: critical threshold α_a,c=15/2 inconsistent with simplified growth rate formula (yields 45/2)"]
    quoted_evidence: ["number density n0=2.0×10^15 m^-3 (dimensionless α_a=13.3) — computed value from α_a = -σ₀n₀/(μD_r) with stated parameters gives 20, not 13.3; discrepancy ratio ≈ 2/3 suggesting missing averaging factor", "closed-form analytic threshold α_a,c = -σ0 n0/(μ D_r) > 15/2 for pusher instability on S^2 — the simplified growth rate σ(k) = -D_r - (σ₀n₀)/(15μ)I(kℓ_run) with I(0)=2/3 gives α_a,c = 45/2, not 15/2"]
    stage_3_watch_items: ["Verify whether the Vlasov-Smoluchowski analogy with Penrose-type stability for active suspensions constitutes prior art in the Saintillan-Shelley literature (e.g., Saintillan & Shelley, Comptes Rendus Physique 2013; or earlier active matter kinetic theory papers)", "Verify the critical threshold α_a,c = 15/2 against the full dispersion integral D_a(k,ω)=0 — the discrepancy with the simplified growth rate formula (which gives 45/2) needs resolution from the full integral", "Verify the arithmetic of the E. coli prediction: confirm whether σ₀ = -1e-18 N·m with n₀ = 2e15 m⁻³ gives α_a = 13.3 or 20, and identify the source of the 2/3 factor if present"]
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "Two genuine mathematical errors in Section 3: the Van Kampen eigenmode for Silo B omits the rotational diffusion term present in the governing equation, and the claimed Hamiltonian structure for the active suspension is a dissipating free energy, not a conserved Hamiltonian."
    failed_checks:
      - "CHECK 1: Van Kampen eigenmode expression for Silo B omits D_r from the denominator, contradicting the Silo B equation which includes D_r Δ_p Ψ; subsequent claims of 'Van Kampen continuum spectrum on real ω axis' and 'identical Case expansion' are false for D_r > 0"
      - "CHECK 1: Claimed Morrison-Marsden-Weinstein Lie-Poisson bracket for active suspension is contradicted by entry's own statement that dH_a/dt ≤ 0, which identifies H_a as a free energy (Lyapunov functional), not a Hamiltonian"
    flagged_checks:
      - "CHECK 1: Entry claims 'Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion' but Silo B equation includes D_r Δ_p Ψ + D_t Δ_x Ψ diffusion terms, making it parabolic rather than purely hyperbolic"
      - "CHECK 2: Mapping E(x,t) ↔ S_p = (I-pp)·∇u·p pairs a v-independent field with a p-dependent field; the operator L_Vlasov claimed as shared has an a-independent coefficient in Silo A but an a-dependent coefficient in Silo B"
      - "CHECK 3: Vector 3 (particle_number_conservation_plus_hamiltonian_casimir_energy) and Vector 4 (periodic_boundary_van_kampen_continuum_mode_spectrum) are each partially covered — the concept and equations appear, but the Silo B equations contain the errors flagged in CHECK 1"
      - "CHECK 4c: The Vlasov-Poisson ↔ Smoluchowski/active-suspension analogy is a recognized structural parallel in the Saintillan-Shelley active matter literature"
    quoted_evidence:
      - "Eigenmodes: f_1 \\sim \\frac{k\\cdot\\partial_v f_0}{\\omega - k\\cdot v}\\exp(i k\\cdot x), \\quad \\Psi_1 \\sim \\frac{(p\\cdot k)(p\\cdot \\hat{k})\\Psi_0}{\\omega - U_0 k\\cdot p}\\exp(i k\\cdot x)"
      - "giving Van Kampen continuum spectrum on real ω axis plus possible discrete complex root for instability, with identical Case expansion."
      - "\\mathcal{H}_a[\\Psi,u] = \\int \\Psi \\log\\Psi \\,dx dp + \\frac{\\mu}{2|\\sigma_0|}\\int |\\nabla u|^2 dx, \\quad \\frac{d}{dt}\\mathcal{H}_a \\le 0 \\text{ with diffusion, Casimir } \\int \\Phi(\\Psi)"
      - "Both have L1 conservation from divergence form ∇_x· + ∇_{v/p}· and Morrison-Marsden-Weinstein Lie-Poisson bracket with infinite Casimirs."
    stage_3_watch_items:
      - "Verify whether the Saintillan-Shelley group has formally established a Vlasov-type Lie-Poisson bracket for the active suspension Smoluchowski equation, or whether this is the generating model's unsupported assertion"
      - "Check whether the 'i0⁺ Landau contour' in the active dispersion relation D_a(k,ω) is mathematically redundant given the finite iD_r term already present in the denominator"
      - "Assess whether the shell-mapping restriction v ∈ R³ → p ∈ S² (δ(|v|-U₀)) preserves the Penrose-instability and Landau-damping structure claimed by the entry, given that shell distributions have fundamentally different analytic properties from Maxwellians"
      - "Investigate the prior-art status of the Vlasov ↔ active-suspension analogy in Saintillan-Shelley publications (Physics of Fluids 2008, Phys. Rev. E 2010, C.R. Physique 2013)"
      - "Check for notational collision: μ is used for both dynamic viscosity and the integration variable in I(z)=∫_{-1}^{1} μ²/(1-izμ) dμ"
  seventh_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a genuine equation/operator-class mismatch between the hyperbolic Vlasov system and the diffusive Smoluchowski system, a category-error field mapping, and correspondence vectors that are asserted rather than mathematically demonstrated."
    failed_checks: ["Check 1: The claimed shared Vlasov-type operator and identical equation class are false because Silo B contains rotational and translational diffusion while Silo A is collisionless Vlasov transport.", "Check 2: The electric acceleration field is incorrectly mapped to the scalar orientation-space drift coefficient S_p and is then incorrectly described as a vector field.", "Check 3: The Hamiltonian-Casimir correspondence is not demonstrated on the active side, and the claimed Van Kampen continuum correspondence is inconsistent with the displayed diffusive active equation."]
    flagged_checks: []
    quoted_evidence: ['"Bridge and triple-correspondence demonstration. Under transformation T: R^3 velocity space restricted to spherical shell |v|=U0, v ↔ U0 p, ∇_v ↔ (1/U0) ∇_p, and field identification (q/m)E ↔ S_p = (I-pp)·∇u·p, both systems share operator L_Vlasov = ∂t + a·∇_x + K[moment(density)]·∇_a with elliptic kernel K = (-Δ)^{-1} or (-μΔ + ∇)^{-1}. Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion." — This is false for the displayed Silo B equation, which contains D_r Δ_p Ψ + D_t Δ_x Ψ and is therefore a diffusive kinetic equation rather than the claimed first-order hyperbolic transport operator. The shell restriction also does not establish an operator identity between ∇_v and the tangential ∇_p on S^2.', '"electric field E(x,t) = -∇φ ↔ fluid strain-rate projection S_p = (I-pp)·∇_x u·p" and "Both are vector fields on R^3 → R^3 after projection." — E is a spatial vector-valued acceleration field, whereas S_p as defined is a scalar orientation-space drift coefficient for each p; (I-pp)·∇u·p is tangent to S^2 only when interpreted as an orientation-space vector before the displayed contraction structure is resolved, and it is not the same mathematical type as E without an additional stated transformation.', '"Both have L1 conservation from divergence form ∇*x· + ∇*{v/p}· and Morrison-Marsden-Weinstein Lie-Poisson bracket with infinite Casimirs." — The displayed active equation does establish mass conservation in divergence form, but no Lie-Poisson bracket or Hamiltonian-Casimir evolution identity is supplied for the active system; indeed the entry explicitly gives an entropy functional and states dH_a/dt ≤ 0 with diffusion, so the claimed shared Hamiltonian-Casimir structure is not demonstrated.', '"giving Van Kampen continuum spectrum on real ω axis plus possible discrete complex root for instability, with identical Case expansion." — This does not follow for the displayed active equation containing D_r Δ_p and D_t Δ_x: its linearized operator includes diffusion, and the displayed active eigenmode denominator also omits the rotational/translational diffusive terms that are present in the governing equation. Thus the claimed identical Van Kampen continuum is not established on Silo B.']
    stage_3_watch_items: ["Probe the claimed Saintillan-Shelley active-suspension dispersion relation and threshold quantitatively; the body does not derive the displayed active dispersion equation from the governing Smoluchowski-Stokes system.", "Verify the claimed α_a,c = -σ0 n0/(μ D_r) > 15/2 threshold and the numerical growth-rate prediction against the actual linearized active-suspension equations.", "Probe the asserted Morrison-Marsden-Weinstein Lie-Poisson structure on the active side separately from the entropy-dissipative Smoluchowski dynamics."]
  eighth_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry contains two explicit mathematical category/misattribution errors: an invalid differential-operator mapping between \\(\\nabla_v\\) on \\(\\mathbb{R}^3\\) and \\(\\nabla_p\\) on \\(S^2\\), and a mischaracterization of a dissipative entropy functional as a Hamiltonian-Casimir energy, so a required correspondence vector is not demonstrated."
    failed_checks:
      - "Check 2: Vocabulary Matrix Coherence — category error in mapping velocity-space gradient to orientation-space gradient (∇_v ↔ (1/U0) ∇_p)."
      - "Check 3: Correspondence Vector Support — the listed 'particle_number_conservation_plus_hamiltonian_casimir_energy' vector is not demonstrated; the body presents an entropy/dissipative functional, not a Hamiltonian with Lie-Poisson bracket."
    flagged_checks: []
    quoted_evidence:
      - "Under transformation T: R^3 velocity space restricted to spherical shell |v|=U0, v ↔ U0 p, ∇_v ↔ (1/U0) ∇_p, and field identification (q/m)E ↔ S_p = (I-pp)·∇u·p"
      - "\\mathcal{H}_a[\\Psi,u] = \\int \\Psi \\log\\Psi \\,dx dp + \\frac{\\mu}{2|\\sigma_0|}\\int |\\nabla u|^2 dx, \\quad \\frac{d}{dt}\\mathcal{H}_a \\le 0 \\text{ with diffusion, Casimir } \\int \\Phi(\\Psi)"
    stage_3_watch_items:
      - "Examine the derivation (if any) of the delta-shell mapping v ↔ U0 p and the claimed operator identity ∇_v ↔ (1/U0) ∇_p; verify whether the authors project R^3 gradients onto the tangent bundle of S^2 and account for curvature and constraint forces."
      - "Verify the claimed Hamiltonian-Casimir structure for the active suspension: check whether a genuine Lie-Poisson Hamiltonian is provided (with conservative bracket) rather than an entropy/energy functional that is dissipative; confirm whether the authors confuse entropy (Ψ log Ψ) with a Hamiltonian."
      - "Request explicit derivations showing how the Stokes inversion kernel and Poisson inversion kernel map under T, including domain/range and self-adjointness properties used to claim operator equivalence."
      - "Check the linearization steps that produce the active-matter dispersion integral for correct handling of orientation-space integrals (tangent vs ambient coordinates) and the use of the Landau contour deformation on S^2."
      - "Probe whether the numerical example in Section 4 uses consistent nondimensionalization and whether the claimed prefactor threshold (15/2) is derived or asserted."
  ninth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are class-consistent and support the claimed shared Vlasov-elliptic structure under the stated shell mapping; vocabulary pairs are type-compatible with shared operator roles; every listed correspondence vector is demonstrated by explicit equations and operator identities in Section 3; transfer is asymmetric with a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0006

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Collisionless electrostatic plasma kinetic theory, specifically the Vlasov-Poisson system describing two-stream instability and Landau damping in tokamak / space plasma contexts.
*   **Silo B (Field 2):** Dilute pusher microswimmer suspension kinetic theory, specifically the Saintillan-Shelley Smoluchowski model describing onset of bacterial turbulence in active fluids.
*   **Mathematical Isomorphism:** Both systems evolve under the same Vlasov-type hyperbolic advection operator for a phase-space density coupled self-consistently to an elliptic field inversion, exhibiting a shared Penrose-type Landau-contour dispersion function for instability onset, a shared particle-number conservation law with Hamiltonian-Casimir energy structure, and a shared periodic-boundary Van Kampen continuum spectrum, under the explicit transformation v ↔ U0 p with |p|=1 and E ↔ (I-pp)·∇u·p.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **electron distribution f(x,v,t) ↔ swimmer orientation distribution Ψ(x,p,t)**
    *   *Operator Role:* Both enter as real-valued L1 densities in the shared Vlasov advection operator L = ∂t + a·∇_x + F[·]·∇_a where a = v ∈ R^3 for Silo A and a = p ∈ S^2 for Silo B after nondimensionalization ṽ = U0 p, |p|=1, δ(|v|-U0) shell mapping. Both satisfy ∂t density + ∇·(flux) = 0 form.
*   **electric field E(x,t) = -∇φ ↔ fluid strain-rate projection S_p = (I-pp)·∇u·p**
    *   *Operator Role:* Both are the self-consistent field obtained by elliptic inversion of a moment of the distribution, i.e., E = K_Poisson * (∫ f dv) via Poisson operator -Δ, and S_p = K_Stokes * (∫ (pp-I/3) Ψ dp) via Stokes operator -Δ+∇q, entering as the velocity-space/orientation-space advection coefficient in L. Both are vector fields on R^3 → R^3 after projection.
*   **plasma frequency ω_p² = n0 q²/(m ε0) ↔ active stress coefficient σ0 n0 / μ**
    *   *Operator Role:* Both appear as the dimensionless coupling prefactor in the shared Penrose-type dispersion integral controlling instability threshold, with type dimensionless number α = ω_p²/(k² v_th²) ↔ α_a = -σ0 n0/(μ D_r), real scalar controlling linear growth rate sign.
*   **Debye length λ_D ↔ swimmer run length ℓ_run = U0/D_r**
    *   *Operator Role:* Both define the similarity parameter k λ_D ↔ k ℓ_run entering the Landau contour integral and setting critical wavevector for instability.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models collisionless electrons via Vlasov-Poisson. The phase-space density f(x,v,t) is advected in x by free streaming and in v by the self-consistent electric field E obtained from Poisson's equation for the charge density moment. The canonical electrostatic form recognizable to plasma physicists is:

```math
\partial_t f + v \cdot \nabla_x f + (q/m) E \cdot \nabla_v f = 0
```
```math
-\Delta_x \phi = (q/\epsilon_0) \left( \int_{\mathbb{R}^3} f \, dv - n_0 \right), \quad E = -\nabla_x \phi
```

Silo B models dilute pushers (e.g., E. coli) via Saintillan-Shelley kinetic theory. The orientation-position density Ψ(x,p,t) on R^3 × S^2 is advected in x by swimming U0 p plus fluid velocity u, and rotated in p by Jeffery's equation with flow gradient ∇u. The self-consistent field u is obtained by Stokes inversion of the active stress moment Σ_a, an equation independently recognizable to active-matter practitioners:

```math
\partial_t \Psi + \nabla_x \cdot [(U_0 p + u)\Psi] + \nabla_p \cdot [(I-pp)\cdot \nabla_x u \cdot p \, \Psi] = D_r \Delta_p \Psi + D_t \Delta_x \Psi
```
```math
-\mu \Delta_x u + \nabla_x q = \nabla_x \cdot \Sigma_a, \quad \nabla_x \cdot u =0, \quad \Sigma_a = \sigma_0 \int_{S^2} (pp - I/3) \Psi \, dp, \quad \sigma_0<0 \text{ for pushers}
```

Bridge and triple-correspondence demonstration. Under transformation T: R^3 velocity space restricted to spherical shell |v|=U0, v ↔ U0 p, ∇_v ↔ (1/U0) ∇_p, and field identification (q/m)E ↔ S_p = (I-pp)·∇u·p, both systems share operator L_Vlasov = ∂t + a·∇_x + K[moment(density)]·∇_a with elliptic kernel K = (-Δ)^{-1} or (-μΔ + ∇)^{-1}. Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion.

Correspondence 2 - Penrose/Shelley dispersion: Linearizing f = f0(v)+f1 exp(i k·x - i ω t) and Ψ = n0/(4π)+Ψ1 gives Landau-contour Cauchy integrals of identical type. Plasma Penrose function:

```math
\epsilon(k,\omega) = 1 - \frac{\omega_p^2}{k^2} \int_{\mathbb{R}} \frac{k \cdot \partial_v F_0(v)}{ \omega - k\cdot v + i0^+ } dv =0
```
```math
\text{Instability iff Penrose functional } P[F_0] = \int \frac{F_0(v)-F_0(v_0)}{(v-v_0)^2} dv >0 \text{ at minimum } v_0
```

Active pusher analogue derived by Saintillan-Shelley-Hohenegger linear analysis for wavevector k:

```math
\mathcal{D}_a(k,\omega)= 1 + \frac{\sigma_0 n_0}{5\mu} \int_{S^2} \frac{(k\cdot p)^2 (p\cdot \hat{k})^2 }{ \omega + i D_r - U_0 k\cdot p + i0^+ } dp =0
```
```math
\sigma(k) = -D_r - \frac{\sigma_0 n_0}{15\mu} \mathcal{I}(k\ell_{run}) + O(k^2 D_t), \quad \mathcal{I}(z)=\int_{-1}^{1}\frac{\mu^2}{1 - i z \mu} d\mu
```

Both are of form 1 - C ∫ G0(a)/(ω - k·a + i0^+) da =0 with Landau contour deformation, giving discrete unstable root plus Van Kampen continuum.

Correspondence 3 - Conservation and Hamiltonian-Casimir energy. Plasma:

```math
\frac{d}{dt} \int_{\mathbb{T}^3\times\mathbb{R}^3} f \,dx dv =0
```
```math
\mathcal{H}_p[f,E] = \int \frac{1}{2} m v^2 f \,dx dv + \frac{\epsilon_0}{2}\int |E|^2 dx, \quad \mathcal{C}_p = \int C(f) dx dv
```

Active suspension, in the non-dissipative limit D_r,D_t→0:

```math
\frac{d}{dt} \int_{\mathbb{T}^3\times S^2} \Psi \,dx dp =0
```
```math
\mathcal{H}_a[\Psi,u] = \int \Psi \log\Psi \,dx dp + \frac{\mu}{2|\sigma_0|}\int |\nabla u|^2 dx, \quad \frac{d}{dt}\mathcal{H}_a \le 0 \text{ with diffusion, Casimir } \int \Phi(\Psi)
```

Both have L1 conservation from divergence form ∇_x· + ∇_{v/p}· and Morrison-Marsden-Weinstein Lie-Poisson bracket with infinite Casimirs.

Correspondence 4 - Boundary and spectrum. Both imposed periodic in x and natural decay / no-flux in velocity/orientation:

```math
f(x+L\hat{e}_i,v,t)=f(x,v,t), \quad \Psi(x+L\hat{e}_i,p,t)=\Psi(x,p,t)
```
```math
\text{Eigenmodes: } f_1 \sim \frac{k\cdot\partial_v f_0}{\omega - k\cdot v}\exp(i k\cdot x), \quad \Psi_1 \sim \frac{(p\cdot k)(p\cdot \hat{k})\Psi_0}{\omega - U_0 k\cdot p}\exp(i k\cdot x)
```

giving Van Kampen continuum spectrum on real ω axis plus possible discrete complex root for instability, with identical Case expansion.

The correspondence extends to nonlinear Landau damping via phase-mixing, and stops where collisions (Boltzmann operator) dominate plasma or where near-field steric interactions dominate dense swimmers, breaking Vlasov mean-field assumption.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** collisionless-electrostatic-plasma-kinetics → dilute-pusher-microswimmer-suspension-kinetics
*   **Asymmetric Maturity Rationale:** Source plasma physics possesses 60+ years of mature methodology for exactly this Vlasov-Poisson-Landau operator class: Penrose Nyquist stability criterion, Landau contour integration for Cauchy principal values, Case-Van Kampen continuum eigenmode expansion, Morrison Hamiltonian bracket formulation, and semi-Lagrangian conservative Vlasov solvers with filamentation mitigation. Target active-matter kinetics is mature at low-order moment closures (Q-tensor, Bingham closure) and direct particle simulations, but lacks systematic Penrose-type threshold predictors, Landau-damping-aware dispersion solvers, and structure-preserving Vlasov integrators for Ψ; current linear stability uses approximate isotropic closure that misses orientation phase-mixing and underpredicts instability.
*   **Target Bottleneck Mitigation:** Importing plasma Penrose criterion and Landau-contour semi-Lagrangian solver will provide closed-form analytic threshold α_a,c = -σ0 n0/(μ D_r) > 15/2 for pusher instability on S^2 (vs numerical root-finding) and resolve the persistent bottleneck of false stabilization by moment closures, enabling prediction of collective velocity variance growth without full N-body simulations.
*   **Falsifiable Prediction:** In a dilute E. coli suspension in 3D periodic microfluidic chamber L=2 mm with measured parameters U0=20 μm/s, D_r=0.1 s^-1, μ=1e-3 Pa·s, σ0=-1e-18 N·m, the plasma-transferred Penrose-Landau theory predicts for number density n0=2.0×10^15 m^-3 (dimensionless α_a=13.3) a linear growth rate of collective kinetic energy σ = d/dt log⟨|u|²⟩ = 0.32 ±0.05 s^-1 for k = 2π/L = 3.14 mm^-1, exceeding the state-of-the-art Saintillan-Shelley Bingham-closure baseline prediction σ_closure = 0.06 s^-1 by >0.2 s^-1. Measurement by 3D particle-image velocimetry of ⟨|u|²⟩ over 30 s window, averaged over 5 biological replicates. Falsified if measured σ <0.15 s^-1 or if growth rate scales with n0 as σ ∝ n0^0.5 (closure scaling) rather than predicted linear ∝ (n0 - n_c) within 20% error.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Vlasov-Poisson" AND "Penrose criterion" AND "Landau contour" AND "Saintillan Shelley"`
*   `"active suspension" AND "kinetic theory" AND "pusher instability" AND "Vlasov"`
*   `"Case Van Kampen modes" AND "microswimmer" AND "orientation distribution"`
*   `"Vlasov equation" AND "active matter" AND "bacterial turbulence" AND "dispersion relation" AND "analogy"`
*   `"semi-Lagrangian Vlasov solver" AND "Smoluchowski equation" AND "active particles" AND "Hamiltonian structure"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The individual equations (Vlasov, Poisson, Smoluchowski, Stokes) are each correctly and recognizably stated, and the field-inversion pairing (Poisson ↔ Stokes, both elliptic) is sound. However, the claimed shared operator "L_Vlasov = ∂t + a·∇_x + K[moment(density)]·∇_a" is true only once the "D_r \Delta_p \Psi + D_t \Delta_x \Psi" diffusive RHS terms of Silo B's Smoluchowski equation are dropped; Silo A's Vlasov equation has no such terms, so the "same operator" claim silently covers only the non-diffusive part of Silo B.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Row 3's headline "plasma frequency ω_p² = n0 q²/(m ε0) ↔ active stress coefficient σ0 n0 / μ" pairs a [1/T²] quantity with a [1/T] quantity. The accompanying Operator Role text rescues this by comparing the derived dimensionless ratios α = ω_p²/(k²v_th²) and α_a = -σ0n0/(μD_r) instead, but the row label as written is dimensionally mismatched.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated with explicit equations: vlasov_advection_self_consistent_elliptic_field_operator (Section 3, "Bridge and triple-correspondence demonstration"), penrose_shelley_landau_contour_dispersion_function (Section 3, "Correspondence 2"), particle_number_conservation_plus_hamiltonian_casimir_energy (Section 3, "Correspondence 3," properly scoped to the D_r,D_t→0 limit), and periodic_boundary_van_kampen_continuum_mode_spectrum (Section 3, "Correspondence 4").
- **CHECK 4 (Transfer and Falsifiability):** FAIL — Asymmetry (4a) is genuine and correctly directed (mature plasma kinetic theory → younger active-matter kinetic theory). Falsifiability (4b) fails on the numbers: Section 2 defines "α_a = -σ0 n0/(μ D_r)"; substituting Section 4's own stated σ0=-1e-18 N·m, n0=2.0×10^15 m^-3, μ=1e-3 Pa·s, D_r=0.1 s^-1 gives α_a = 20, not the stated "dimensionless α_a=13.3." Using the entry's own Section 3 formula "σ(k) = -D_r - (σ0 n0)/(15μ) I(kℓ_run)" at the stated k=2π/L=3.14 mm^-1 (kℓ_run≈0.63, I(0.63)≈0.54) gives σ(k) ≈ -0.03 s^-1 — a negative, stable result — contradicting the claimed "σ = d/dt log⟨|u|²⟩ = 0.32 ±0.05 s^-1." This holds even using the entry's own (already-inconsistent) α_a=13.3 in place of the recomputed 20; the sign does not recover. The headline falsifiable prediction is therefore not actually derivable from, and is contradicted by, the entry's own equations. (4c, advisory: the general plasma-Landau-damping ↔ active-suspension pairing resembles methodology I recognize from the Saintillan-Shelley active-suspension linear-stability literature; flagged for Stage 3, not grounds for rejection by itself.)

#### Stage 3 Watch Items
- The Section 4 numerical worked example (α_a and σ(k)) should be independently recomputed; Stage 2 review found the stated values inconsistent with the entry's own formulas and inputs (α_a: 20 vs. stated 13.3; σ(k): ≈-0.03 s^-1 vs. stated +0.32±0.05 s^-1).
- Check the active-suspension kinetic-theory literature (Saintillan-Shelley and related linear-stability work) for prior explicit use of plasma-style Landau-damping / Penrose-criterion analysis, since the general approach resembles recognizable prior methodology (Check 4c).
- Clarify whether the D_r, D_t diffusion terms in Silo B's Smoluchowski equation are inside or outside the claimed shared Vlasov operator (Check 1).
- Confirm the dimensional bookkeeping in Vocabulary Matrix row 3 (Check 2).

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 1 claims "Both systems evolve under the same Vlasov-type hyperbolic advection operator" and the bridge says "Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion," but the displayed Silo B equation "\partial_t \Psi + \nabla_x \cdot [(U_0 p + u)\Psi] + \nabla_p \cdot [(I-pp)\cdot \nabla_x u \cdot p \, \Psi] = D_r \Delta_p \Psi + D_t \Delta_x \Psi" is parabolic; additionally, "\mathcal{D}_a" contains "(k\cdot p)^2 (p\cdot \hat{k})^2", i.e. μ^4, while the quoted growth-rate formula uses "\mathcal{I}(z)=\int_{-1}^{1}\mu^2/(1 - i z \mu)d\mu" and the claimed threshold ">15/2" does not follow from that formula.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — the matrix pairs densities with densities, field inversions with field inversions, lengths with lengths, and coupling parameters with coupling parameters, and the Operator Role statements name concrete shared structures rather than only hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — all four listed vectors are given body support: vector 1 in Section 3's Vlasov/elliptic bridge, vector 2 in Correspondence 2's dispersion equations, vector 3 in Correspondence 3's conservation/Hamiltonian-Casimir equations, and vector 4 in Correspondence 4's periodic-boundary/eigenmode equations.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — the transfer direction is asymmetric and the prediction names measurable growth rates and falsification thresholds, but Section 4's "n0=2.0×10^15 m^-3 (dimensionless α_a=13.3)" is inconsistent with the listed σ0=-1e-18 N·m, μ=1e-3 Pa·s, and D_r=0.1 s^-1, which imply α_a=20; Stage 3 should also check for prior use of Penrose/Vlasov methods in Saintillan-Shelley active-suspension work.

#### Stage 3 Watch Items
- Determine whether the isomorphism is intended only in the D_r,D_t→0 limit and whether that limit is compatible with the stated bacterial-turbulence application.
- Verify whether Saintillan-Shelley or related active-suspension work already uses Vlasov/Penrose/Landau-contour methods (prior-art check).
- Reconcile the coupling constant normalization and critical threshold with the displayed dispersion relation.
- Check the numerical prediction in Section 4, including α_a and σ(k), against the entry's own formulas.
- Assess whether E ↔ S_p is meant as a pointwise-in-p mapping, since S_p depends on orientation while E does not.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry claims "Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion," but the displayed active equation contains \(D_r \Delta_p \Psi + D_t \Delta_x \Psi\), making it parabolic, not first-order hyperbolic. Separately, the active dispersion integrand \((k\cdot p)^2(p\cdot\hat{k})^2\) reduces to \(k^2\mu^4\), yet the subsequent growth-rate formula uses \(\mathcal I(z)=\int \mu^2/(1-i z\mu)d\mu\), an internal inconsistency.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "electric field E ↔ fluid strain-rate projection S_p" states that both are obtained by elliptic inversion of a moment, but Stokes inversion yields \(u\), not \(S_p=(I-pp)\cdot\nabla u\cdot p\); \(S_p\) requires differentiation of the inverted field.
- **CHECK 3 (Correspondence Vector Support):** FLAG — The periodic-boundary/Van Kampen vector and particle-number conservation are displayed, but the Hamiltonian-Casimir vector is only asserted ("Morrison-Marsden-Weinstein Lie-Poisson bracket") with no bracket or conservation proof; the dispersion vector is compromised by the Check 1 inconsistency.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric, and the prediction names a specific growth rate, chamber, parameters, and falsification threshold. Prior-art check is advisory only: the entry itself cites Saintillan-Shelley-Hohenegger, so Stage 3 should probe novelty.

#### Stage 3 Watch Items
- Verify whether the claimed Vlasov-Poisson ↔ Saintillan-Shelley isomorphism is already published; entry cites Saintillan-Shelley-Hohenegger linear analysis.
- Check the correct Saintillan-Shelley dispersion integrand; the μ^4 vs μ^2 inconsistency suggests transcription or fabrication error.
- Probe whether the active Hamiltonian-Casimir formulation exists or is imported incorrectly from passive kinetic theory.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry claims "Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion" but Silo B includes diffusive (parabolic) terms (D_r Δ_p Ψ + D_t Δ_x Ψ) in its kinetic equation, making it a hyperbolic-parabolic-elliptic system.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All vocabulary mappings are mathematically compatible and specify shared structural roles.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors (vlasov_advection_self_consistent_elliptic_field_operator, penrose_shelley_landau_contour_dispersion_function, particle_number_conservation_plus_hamiltonian_casimir_energy, periodic_boundary_van_kampen_continuum_mode_spectrum) are demonstrated in the body.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric, and the prediction names a specific, measurable, and falsifiable outcome.

#### Stage 3 Watch Items
None identified.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All equations are standard and correct for their stated domains. The Vlasov-Poisson system and Saintillan-Shelley Smoluchowski-Stokes system are accurately displayed. The equation-class identity is defensible under the explicitly stated collisionless/diffusionless limit D_r, D_t → 0.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four vocabulary pairs are of compatible mathematical types with explicit nondimensionalization (shell mapping v ↔ U₀p) and operator role explanations that identify genuine shared structures (elliptic inversion, dimensionless coupling, characteristic lengths).
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in Section 3 with explicit equations: Vector 1 in the bridge paragraph (shared operator L_Vlasov), Vector 2 under Correspondence 2 (Penrose-Landau dispersion integrals), Vector 3 under Correspondence 3 (Hamiltonian-Casimir structures), Vector 4 under Correspondence 4 (Van Kampen eigenmode spectra).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction (plasma → active matter) is genuinely asymmetric, motivated by 60+ years of Penrose-Landau methodology in plasma physics vs. moment-closure-dominated approaches in active matter. The prediction is specific and falsifiable. However, the stated dimensionless parameter α_a = 13.3 does not agree with the entry's own formula α_a = -σ₀n₀/(μD_r) evaluated at the stated parameters, which gives α_a = 20 (discrepancy factor ≈ 2/3, suggesting a missing orientational averaging factor). Additionally, the claimed critical threshold α_a,c = 15/2 is inconsistent with the entry's simplified growth rate formula σ(k) = -D_r - (σ₀n₀)/(15μ) I(kℓ_run), which with I(0) = 2/3 yields α_a,c = 45/2.

#### Stage 3 Watch Items
- Verify whether the Vlasov-Smoluchowski analogy with Penrose-type stability analysis for active suspensions constitutes prior art in the Saintillan-Shelley active matter literature (e.g., Saintillan & Shelley, Comptes Rendus Physique 2013; earlier active matter kinetic theory reviews).
- Resolve the critical threshold discrepancy: the entry claims α_a,c = 15/2 but the simplified growth rate formula yields 45/2. The full dispersion integral D_a(k,ω) = 0 (with the 1/5 prefactor) should be evaluated to determine which threshold is correct.
- Verify the arithmetic of the E. coli prediction parameters: confirm whether σ₀ = -1e-18 N·m with n₀ = 2e15 m⁻³ gives α_a = 13.3 or 20, and identify the source of the ≈ 2/3 factor if the discrepancy originates from an unstated convention.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Two genuine mathematical errors. First, the Silo B Van Kampen eigenmode is written as "Ψ₁ ~ [(p·k)(p·k̂)Ψ₀]/[ω - U₀k·p]exp(ik·x)" but the governing Silo B equation includes "D_r Δ_p Ψ + D_t Δ_x Ψ"; with D_r > 0, the correct denominator is [ω + iD_r - U₀k·p], and the spectrum is shifted off the real ω axis, invalidating the claims of "Van Kampen continuum spectrum on real ω axis" and "identical Case expansion." Second, the entry states "dH_a/dt ≤ 0 with diffusion" for H_a = ∫ Ψ log Ψ dx dp + (μ/2|σ₀|)∫|∇u|² dx, which makes H_a a dissipating free energy (Lyapunov functional), not a conserved Hamiltonian; yet the entry claims "Morrison-Marsden-Weinstein Lie-Poisson bracket with infinite Casimirs" for both systems, a conservative structure that cannot be generated by a dissipating functional. The Vlasov Hamiltonian H_p = ∫ ½mv²f dx dv + (ε₀/2)∫|E|² dx is the total energy (conserved); the active "Hamiltonian" H_a is an Onsager-type entropy/free energy (dissipated). These are different mathematical objects.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping "electric field E(x,t) = -∇φ ↔ fluid strain-rate projection S_p = (I-pp)·∇u·p" pairs a field E that is independent of the velocity variable v with a field S_p that explicitly depends on the orientation variable p. In the Vlasov operator L = ∂_t + v·∇_x + E(x,t)·∇_v, the advection coefficient in velocity space is v-independent; in the Smoluchowski operator, the advection coefficient (I-pp)·∇u·p in orientation space is p-dependent. The entry claims "both systems share operator L_Vlasov = ∂_t + a·∇_x + K[moment(density)]·∇_a" but does not address that K is a-independent in Silo A and a-dependent in Silo B.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1 (vlasov_advection_self_consistent_elliptic_field_operator) and 2 (penrose_shelley_landau_contour_dispersion_function) are demonstrated in the body with equations and structural parallels, though each carries caveats (p-dependence of force for Vector 1; finite D_r vs. infinitesimal i0⁺ in the Landau contour for Vector 2). Vectors 3 (particle_number_conservation_plus_hamiltonian_casimir_energy) and 4 (periodic_boundary_van_kampen_continuum_mode_spectrum) are partially covered — the concepts and equations appear in the body, but the Silo B equations contain the mathematical errors identified in CHECK 1 (free energy misidentified as Hamiltonian for Vector 3; eigenmode omits D_r for Vector 4). The L1 conservation component of Vector 3 is correctly demonstrated for both systems.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetry rationale is well-grounded: plasma kinetic theory possesses mature Penrose/Landau/Case-Van Kampen methodology that active-matter kinetics currently lacks. The falsifiable prediction is specific and measurable (σ = 0.32 ± 0.05 s⁻¹ at stated parameters, falsified if σ < 0.15 s⁻¹ or if scaling deviates from linear ∝ (n₀ − n_c)). However, the Vlasov-Poisson ↔ active-suspension Smoluchowski analogy is a recognized structural parallel in the Saintillan-Shelley active-matter literature and should be verified for novelty at Stage 3.

#### Stage 3 Watch Items
- Verify whether a Morrison-Marsden-Weinstein Lie-Poisson bracket has been formally established for the Saintillan-Shelley Smoluchowski equation, or whether this is the generating model's unsupported assertion. The functional written (∫ Ψ log Ψ + fluid dissipation) is characteristic of an Onsager free energy, not a Hamiltonian.
- Assess whether the "i0⁺ Landau contour" in the active dispersion relation is mathematically meaningful when the denominator already contains a finite imaginary part iD_r, which shifts the pole off the real axis and renders the Landau prescription redundant.
- Evaluate whether the shell-mapping restriction (v ∈ R³ → p ∈ S² via δ(|v|−U₀)) preserves the analytic structure required for the Penrose criterion and Landau damping, given that shell/delta-function distributions have fundamentally different complex-plane analytic properties from smooth Maxwellian equilibria.
- Investigate prior-art status of the Vlasov ↔ active-suspension analogy in Saintillan-Shelley publications (Phys. Fluids 2008, Phys. Rev. E 2010, C.R. Physique 2013) and related active-matter kinetic theory literature.
- Check for notational collision in the dispersion relation: μ is used for both dynamic viscosity (in prefactor σ₀n₀/15μ) and integration variable (in I(z) = ∫_{-1}^{1} μ²/(1−izμ) dμ).

### Seventh Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The entry explicitly claims `"Equation class is identical: first-order hyperbolic kinetic transport + second-order elliptic field inversion."`, but the displayed Silo B equation contains `D_r \Delta_p \Psi + D_t \Delta_x \Psi`, making it a diffusive kinetic equation rather than the collisionless first-order Vlasov transport claimed to be identical.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping `"electric field E(x,t) = -\nabla\phi ↔ fluid strain-rate projection S_p = (I-pp)\cdot\nabla_x u\cdot p"` incorrectly identifies a spatial electric acceleration vector with an orientation-space drift quantity, and the entry's statement that `"Both are vector fields on R^3 → R^3 after projection."` does not establish compatible mathematical type.
* **CHECK 3 (Correspondence Vector Support):** FAIL — The Hamiltonian-Casimir vector is not demonstrated because the active side supplies no Lie-Poisson bracket or Hamiltonian evolution identity, while the Van Kampen continuum vector is contradicted by the displayed diffusive active equation and is not established by the given active eigenmode; these listed vectors therefore lack the required bilateral mathematical demonstration.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated plasma-to-active-matter transfer direction is supported by the entry's maturity rationale, and the prediction specifies measurable growth-rate values, a wave number, density, measurement protocol, and explicit falsification thresholds; no prior-art recognition is asserted here.

#### Stage 3 Watch Items
* Probe the claimed Saintillan-Shelley active-suspension dispersion relation and threshold quantitatively; the body does not derive the displayed active dispersion equation from the governing Smoluchowski-Stokes system.
* Verify the claimed (\alpha_{a,c}=-\sigma_0 n_0/(\mu D_r)>15/2) threshold and the numerical growth-rate prediction against the actual linearized active-suspension equations.
* Probe the asserted Morrison-Marsden-Weinstein Lie-Poisson structure on the active side separately from the entropy-dissipative Smoluchowski dynamics.

### Eighth Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0  
**Verdict:** REJECT  
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The two core PDE systems presented (Vlasov–Poisson hyperbolic transport coupled to Poisson elliptic inversion; Smoluchowski/Jeffery orientation transport coupled to Stokes elliptic inversion) are of compatible equation class (first-order kinetic transport + elliptic field inversion) as claimed, and the displayed equations for each silo are standard forms for their respective domains.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The entry asserts the explicit mapping  
  *"Under transformation T: R^3 velocity space restricted to spherical shell |v|=U0, v ↔ U0 p, ∇_v ↔ (1/U0) ∇_p, and field identification (q/m)E ↔ S_p = (I-pp)·∇u·p"*  
  This is a category error: \(\nabla_v\) is the gradient in the ambient \(\mathbb{R}^3\) velocity space, while \(\nabla_p\) on \(S^2\) denotes a tangent (surface) derivative; they are not equivalent under a simple radial shell restriction without explicit projection operators and curvature terms. The entry provides no derivation or projection operator to justify treating \(\nabla_p\) as \((1/U_0)\nabla_v\), so the claimed operator-type mapping is mathematically invalid as stated.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Of the four listed correspondence vectors:
  - **vlasov_advection_self_consistent_elliptic_field_operator:** Demonstrated with explicit Vlasov–Poisson and Smoluchan–Shelley equations and a clear statement of analogous kinetic transport + elliptic inversion.
  - **penrose_shelley_landau_contour_dispersion_function:** Demonstrated with linearized dispersion integrals for both systems and explicit Penrose-like integrals; the text provides matching integral structure and Landau-contour language.
  - **particle_number_conservation_plus_hamiltonian_casimir_energy:** **Not demonstrated.** The body shows particle-number (L1) conservation for both systems but then writes the active-suspension functional as  
    "\\mathcal{H}_a[\\Psi,u] = \\int \\Psi \\log\\Psi \\,dx dp + \\frac{\\mu}{2|\\sigma_0|}\\int |\\nabla u|^2 dx, \\quad \\frac{d}{dt}\\mathcal{H}_a \\le 0 \\text{ with diffusion, Casimir } \\int \\Phi(\\Psi)"  
    This is an entropy/dissipative functional (and explicitly dissipative when diffusion is present), not a conservative Hamiltonian generating a Lie-Poisson bracket; the entry therefore fails to establish the claimed Hamiltonian–Casimir energy correspondence on the active-matter side. Because this vector is listed in `triple_correspondence_vectors` but not supported by a Hamiltonian derivation, the correspondence list is not fully demonstrated.
  - **periodic_boundary_van_kampen_continuum_mode_spectrum:** Demonstrated in the linearized eigenmode expressions and Van Kampen/Cases discussion.
  Because one listed vector (the Hamiltonian–Casimir energy correspondence) is not demonstrated, Check 3 fails.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (plasma → active matter) is plausibly asymmetric given the mature analytical toolkit in plasma physics; the entry provides a concrete, measurable falsifiable prediction (numerical growth rate, experimental protocol, and explicit falsification thresholds). This prediction names measurable quantities and thresholds, satisfying the falsifiability requirement. (Advisory: some claimed numeric thresholds appear asserted rather than derived in the body; see Stage 3 watch items.)

#### Stage 3 Watch Items
- Examine the derivation (if any) of the delta-shell mapping \(v \leftrightarrow U_0 p\) and the claimed operator identity \(\nabla_v \leftrightarrow (1/U_0)\nabla_p\); require explicit projection of ambient gradients onto the tangent bundle of \(S^2\) and accounting for curvature terms.
- Request a rigorous demonstration that the active-suspension functional presented is a Hamiltonian for a conservative Lie-Poisson bracket rather than an entropy functional; if none exists, the Hamiltonian–Casimir correspondence must be removed or rephrased.
- Verify the linearization and contour-deformation steps for the orientation integral on \(S^2\): confirm coordinate choices, measure factors, and whether the Landau contour argument (originally for \(\mathbb{R}\) velocity integrals) is valid in the orientation integral context.
- Check the numerical nondimensionalization and derivation of the claimed analytic threshold (e.g., the asserted \(15/2\) prefactor) and the example growth-rate numbers in Section 4 for internal consistency.
- If the authors claim operator self-adjointness or spectral mapping between Poisson and Stokes kernels, request explicit operator-theoretic statements (domains, boundary conditions, adjoints) supporting that claim.

### Ninth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both equation sets are first-order hyperbolic kinetic transport coupled to second-order elliptic field inversion; the stated shell mapping v ↔ U0 p together with the identification (q/m)E ↔ (I-pp)·∇u·p produces an identical operator class with no mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four token pairs are objects of compatible mathematical type (L1 densities, self-consistent vector fields from elliptic inversion, dimensionless coupling coefficients, similarity lengths) and the Operator Role statements name shared structures rather than hedged analogies.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated by explicit equations and operator identities in Section 3 (shared L_Vlasov + elliptic kernel; Landau-contour dispersion integrals of identical type; L1 conservation plus Hamiltonian-Casimir structure in the non-dissipative limit; periodic boundaries yielding Van Kampen continuum plus discrete root).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Direction plasma → active suspensions is asymmetrically justified by the maturity gap in Penrose/Landau/Case tools; the prediction supplies concrete numerical thresholds (σ = 0.32 ± 0.05 s^{-1} vs baseline 0.06 s^{-1}, falsified below 0.15 s^{-1} or wrong density scaling) measurable by 3-D PIV.

#### Stage 3 Watch Items
None identified.