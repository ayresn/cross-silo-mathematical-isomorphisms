---
sid_metadata:
  entry_id: "SID-0057"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "Xiaomi"
  model_family: "MiMo"
  model_version: "V2.5 Pro"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "epitaxial-step-flow-dynamics"
  domain_b: "vehicular-traffic-flow-theory"
  structural_family: "scalar-nonlinear-conservation-laws"
  triple_correspondence_vectors:
    - "scalar_conservation_law_operator_with_concave_constitutive_flux"
    - "rankine_hugoniot_shock_jump_condition_at_step_bunch_and_jam_front"
    - "lax_entropy_condition_selecting_physically_realizable_shocks"
discovery_rationale:
  why_not_obvious: "surface_physics_and_traffic_engineering_share_zero_publication_overlap_use_entirely_disjoint_terminologies_and_neither_community_frames_step_bunching_or_traffic_congestion_in_the_others_mathematical_language"
prior_discovery_metrics:
  structural_isomorphism_score: 8.5
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 7.8
  community_separation_score: 9.5
  representation_mismatch_score: 7.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.8
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_saturating_vs_zero_flux_at_packing_limit"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "Check 1 fails: the displayed second-derivative formula for the BCF flux in Correspondence 1 does not equal the derivative of the f(rho) stated immediately above it and is dimensionally inconsistent by one power of length."
    failed_checks: ["Check 1: BCF-side f''(rho) formula in Section 3, Correspondence 1"]
    flagged_checks: ["Check 4c: domain pairing shares its underlying framework with Whitham kinematic-wave theory, which originates in traffic flow and is applied across multiple transport domains"]
    quoted_evidence: ['-8F\Omega x_s^3\,\frac{\tanh\xi\;\mathrm{sech}^2\!\xi}{\xi^3} < 0, with \xi = \frac{1}{2x_s\rho} > 0 (Section 3, Correspondence 1)']
    stage_3_watch_items: ["Before resubmission, verify the corrected BCF second-derivative formula against the f(rho) given in Section 3 (see Check 1 finding).", "Search specifically for prior use of conservation-law / shock / kinematic-wave language applied to step bunching in the surface-physics literature -- the entry's own Section 5 strings (e.g. 'kinematic wave' AND ('step bunch' OR 'vicinal surface')) already target this, and Whitham's kinematic-wave theory (originating in Lighthill & Whitham 1955 traffic-flow papers) is a plausible common ancestor.", "Independently verify the canonical BCF step-velocity closure (tanh vs. coth form, numerical prefactor) against standard epitaxy references -- this review checked only internal/dimensional self-consistency, not fidelity to the literature's standard BCF derivation."]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a mathematically incorrect BCF second-derivative display and an internally inconsistent Lax-entropy shock labeling that contradicts its own concave-flux claim."
    failed_checks: ["Check 1: displayed BCF second derivative is not the derivative of the displayed flux", "Check 3: lax_entropy_condition_selecting_physically_realizable_shocks is not coherently demonstrated because the Lax inequality conflicts with the stated high/low state labels"]
    flagged_checks: []
    quoted_evidence:
      - |
        f''(\rho) = \frac{d^2}{d\rho^2}\!\left[2F\Omega x_s\,\rho\,\tanh\!\left(\frac{1}{2x_s\rho}\right)\right] = -8F\Omega x_s^3\,\frac{\tanh\xi\;\mathrm{sech}^2\!\xi}{\xi^3}\;<\;0, \quad \xi = \frac{1}{2x_s\rho} > 0
      - |
        Both fluxes are therefore concave on their entire domain, ensuring the characteristic speed c(ρ) = f′(ρ) is strictly decreasing
      - |
        where ρ_L is the density behind the shock (tight step spacing / congested traffic) and ρ_R is the density ahead (wide terraces / free-flowing traffic).
      - |
        f'(\rho_L) > s > f'(\rho_R)
    stage_3_watch_items: ["Verify whether the BCF step-density conservation law and concave-flux/kinematic-shock framing already appear in epitaxy or surface-physics literature.", "Verify whether traffic-engineering Godunov/CTM/data-assimilation methods have previously been proposed for step-flow or crystal-growth control.", "Check the correct left/right state convention for Lax-entropy shocks in traffic and step-flow descriptions, since the entry's labels are internally inconsistent.", "Assess whether the symmetric no-Ehrlich-Schwoebel BCF continuum model used here actually supports spontaneous step bunching or only shock propagation from imposed gradients."]
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "Section 3 contains a false second-derivative equation for the BCF flux and applies the Lax entropy inequality in a direction inconsistent with the entry's own stated high-density-left/low-density-right shock configuration under a globally concave flux."
    failed_checks:
      - "Check 1: Incorrect BCF flux second derivative; Lax entropy condition incompatible with the stated density assignment for a concave flux."
      - "Check 3: The lax_entropy_condition vector is not demonstrated because the displayed inequality cannot hold for the asserted high-density-left/low-density-right shock orientation."
    flagged_checks: []
    quoted_evidence:
      - |
        f''(\rho) = \frac{d^2}{d\rho^2}\!\left[2F\Omega x_s\,\rho\,\tanh\!\left(\frac{1}{2x_s\rho}\right)\right] = -8F\Omega x_s^3\,\frac{\tanh\xi\;\mathrm{sech}^2\!\xi}{\xi^3}\;<\;0, \quad \xi = \frac{1}{2x_s\rho} > 0
      - |
        where ρ_L is the density behind the shock (tight step spacing / congested traffic) and ρ_R is the density ahead (wide terraces / free-flowing traffic).
      - |
        f'(\rho_L) > s > f'(\rho_R)
      - |
        In epitaxy, this selects the stable step-bunch front: faster characteristics from the wide-terrace side and slower characteristics from the tight-step side both converge on the bunch boundary.
    stage_3_watch_items:
      - "Recheck the BCF f'' derivation: the sign is correct, but the displayed formula appears algebraically wrong, so determine whether this is a typographical error."
      - "Search the kinematic-wave/step-bunching literature, including the entry's own search string 'kinematic wave' AND ('step bunch' OR 'vicinal surface'), before accepting novelty."
      - "Verify the physically correct density orientation for step-bunch and jam-front shocks under concave flux; the current left/right assignment appears reversed."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a mathematically and dimensionally incorrect algebraic derivation for the second derivative (concavity) of the BCF step flux."
    failed_checks: ["Check 1: Equation Validity"]
    flagged_checks: []
    quoted_evidence: ["f''(\\rho) = \\frac{d^2}{d\\rho^2}\\!\\left[2F\\Omega x_s\\,\\rho\\,\\tanh\\!\\left(\\frac{1}{2x_s\\rho}\\right)\\right] = -8F\\Omega x_s^3\\,\\frac{\\tanh\\xi\\;\\mathrm{sech}^2\\!\\xi}{\\xi^3}\\;<\\;0, \\quad \\xi = \\frac{1}{2x_s\\rho} > 0"]
    stage_3_watch_items: ["None identified."]
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "FLAG"
    verdict_rationale: "Two genuine but non-fatal mathematical errors: an incorrect second-derivative formula for the BCF flux (correct sign, wrong prefactors) and an inconsistent L/R state labeling in the Lax entropy condition that contradicts the stated concave-flux structure."
    failed_checks: []
    flagged_checks: ["Check 1: BCF second-derivative formula has incorrect prefactors (x_s^3/ξ^3 instead of x_s^2·ξ^3)", "Check 3: Lax entropy condition state labeling is inconsistent with concave flux — entry assigns ρ_L to the high-density state but Lax-compliant shocks for concave flux require ρ_L < ρ_R"]
    quoted_evidence: ["f''(\\rho) = \\frac{d^2}{d\\rho^2}\\!\\left[2F\\Omega x_s\\,\\rho\\,\\tanh\\!\\left(\\frac{1}{2x_s\\rho}\\right)\\right] = -8F\\Omega x_s^3\\,\\frac{\\tanh\\xi\\;\\mathrm{sech}^2\\!\\xi}{\\xi^3}\\;<\\;0", "\\rho_L is the density behind the shock (tight step spacing / congested traffic) and \\rho_R is the density ahead (wide terraces / free-flowing traffic)"]
    stage_3_watch_items: ["Verify whether the specific domain pairing (epitaxial step-flow ↔ vehicular traffic flow) has been previously published; the underlying scalar-conservation-law framework (LWR, RH, Lax) is textbook PDE theory", "Check whether the BCF step-velocity formula v_n = FΩx_s[tanh(l_n/(2x_s)) + tanh(l_{n+1}/(2x_s))] matches the standard BCF normalization convention used in the surface-physics literature", "Verify whether step bunching actually occurs in the symmetric (no ES barrier) BCF model, or whether it requires an asymmetry that would break the concave-flux correspondence"]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a mathematically incorrect second derivative for the BCF flux and applies the Lax shock condition with the density ordering appropriate to a convex, not concave, flux, so its claimed shock correspondence is not supported."
    failed_checks: ["Check 1: The displayed BCF flux second derivative is incorrect, and the stated high-density-to-low-density Lax shock configuration is incompatible with a concave flux.", "Check 3: The Rankine-Hugoniot/Lax shock correspondence is not valid as demonstrated because the stated Lax inequality cannot hold for the specified density ordering and concave flux."]
    flagged_checks: []
    quoted_evidence: ["f''(\\rho) = \\frac{d^2}{d\\rho^2}\\!\\left[2F\\Omega x_s\\,\\rho\\,\\tanh\\!\\left(\\frac{1}{2x_s\\rho}\\right)\\right] = -8F\\Omega x_s^3\\,\\frac{\\tanh\\xi\\;\\mathrm{sech}^2\\!\\xi}{\\xi^3}\\;<\\;0, \\quad \\xi = \\frac{1}{2x_s\\rho} > 0", "f'(\\u03c1_L) > s > f'(\\u03c1_R)"]
    stage_3_watch_items: ["Probe the claimed cross-domain step-bunch/traffic-jam shock correspondence after correcting the density ordering required by entropy admissibility for a concave flux.", "Probe whether the BCF continuum step-density model and its numerical conservation-law treatment are already established in the step-bunching literature."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "PASS"
    verdict_rationale: "The entry consistently demonstrates a symbol-for-symbol operator-level isomorphism: both sides are scalar first-order hyperbolic conservation laws with concave fluxes, Rankine–Hugoniot shock propagation, and Lax entropy selection, and the methodological-transfer claim is asymmetric and falsifiable as stated."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify prior-art on conservation-law framings of BCF; the entry states: \"Both systems are governed by a scalar, nonlinear, first-order hyperbolic conservation law of identical operator form, ∂ρ/∂t + ∂f(ρ)/∂x = 0, in which a conserved density ρ (step density / vehicle density) advects with a constitutive velocity v(ρ) that produces a globally concave flux function f(ρ) = ρv(ρ); shock solutions satisfying the Rankine-Hugoniot jump condition and selected by the Lax entropy inequality correspond physically to step-bunch fronts in Silo A and to traffic-jam fronts in Silo B.\""
      - "Confirm numerical stability and accuracy claims in Section 4: the falsifiable prediction gives explicit thresholds (20% accuracy at Θ = 50 ML; 50× speedup) that Stage 3 should test against KMC baselines."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: identical scalar hyperbolic conservation-law operator with demonstrated concave fluxes, type-compatible vocabulary mappings, full support for every listed correspondence vector by explicit equations, and a genuinely asymmetric transfer with a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Constitutive high-density mismatch (BCF saturation versus traffic gridlock) and its effect on two-branch phenomena; whether the continuum BCF reduction already appears in the epitaxy literature under conservation-law language."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "PASS"
    verdict_rationale: "All three claimed vectors are demonstrated with matching first-order hyperbolic conservation laws, concave fluxes with explicit second-derivative calculations, and compatible scalar-field vocabulary; transfer is asymmetric and falsifiable with quantitative thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Constitutive high-density mismatch disclosed in Section 1 and Section 3 scope limitation (BCF flux saturates to ΩF vs traffic flux to 0) - verify Stage 3 does not treat this as breaking the shared operator structure, which it does not.", "General kinematic-wave textbook context - scalar conservation law analogies across sedimentation, chromatography, and traffic are textbook, but specific epitaxy ↔ LWR pairing is not canonical; confirm novelty via bibliometric search strings provided."]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0057

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Epitaxial crystal-growth dynamics — specifically the Burton-Cabrera-Frank (BCF) continuum model of step-flow on vicinal surfaces, where steps are ledges on a slightly misoriented crystal face and the observable phenomenon is **step bunching**: the spontaneous clustering of steps into dense bands separated by wide, atomically flat terraces during growth or sublimation.
*   **Silo B (Field 2):** Vehicular traffic-flow theory — specifically the Lighthill-Whitham-Richards (LWR) macroscopic model of highway traffic, where the observable phenomenon is **traffic congestion**: the spontaneous formation of stop-and-go waves and jam fronts from initially uniform traffic.
*   **Mathematical Isomorphism:** Both systems are governed by a scalar, nonlinear, first-order hyperbolic conservation law of identical operator form, ∂ρ/∂t + ∂f(ρ)/∂x = 0, in which a conserved density ρ (step density / vehicle density) advects with a constitutive velocity v(ρ) that produces a globally concave flux function f(ρ) = ρv(ρ); shock solutions satisfying the Rankine-Hugoniot jump condition and selected by the Lax entropy inequality correspond physically to step-bunch fronts in Silo A and to traffic-jam fronts in Silo B, and the correspondence holds under the identification of step density with vehicle density and step flux with traffic flow, with the caveat that the BCF flux saturates at high density (no gridlock analogue) rather than returning to zero.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Step density ρ_s (steps m⁻¹)** ↔ **Vehicle density ρ_v (veh m⁻¹)**
    *   *Operator Role:* Conserved scalar density field in the conservation law ∂ρ/∂t + ∂f(ρ)/∂x = 0. Both are intensive, non-negative densities whose spatial gradient drives wave propagation. Identical mathematical type: scalar field ρ: ℝ × ℝ → ℝ₊.
*   **Step velocity v_s (m s⁻¹)** ↔ **Macroscopic velocity v_v (m s⁻¹)**
    *   *Operator Role:* Constitutive velocity in the closure f(ρ) = ρ·v(ρ). Both are monotonically decreasing functions of density — v_s through the BCF terrace-width-dependent adatom capture rate, v_v through the empirical speed-density relationship — and both satisfy v(0) = v_max (maximum step speed / free-flow speed). The derivative v′(ρ) < 0 for all ρ > 0 is what generates the concavity of f.
*   **Step flux J_s = ρ_s v_s (steps s⁻¹)** ↔ **Traffic flow q_v = ρ_v v_v (veh s⁻¹)**
    *   *Operator Role:* The nonlinear flux function f(ρ) in the conservation law. Both are concave functions of ρ (demonstrated below), ensuring that characteristic speed f′(ρ) is strictly decreasing, which produces compression-wave steepening into shocks and expansion-wave broadening into rarefactions.
*   **Step bunch** ↔ **Traffic jam (stop-and-go wave)**
    *   *Operator Role:* A traveling shock solution of the conservation law, separating a high-density region (tightly packed steps / congested traffic) from a low-density region (wide terraces / free-flowing traffic), propagating at the Rankine-Hugoniot speed s = [f(ρ_L) − f(ρ_R)]/(ρ_L − ρ_R).
*   **Terrace width l = 1/ρ_s (m)** ↔ **Mean headway h = 1/ρ_v (m veh⁻¹)**
    *   *Operator Role:* Reciprocal of the conserved density, entering the constitutive velocity as the primary argument. In BCF, v_s depends on l through the tanh function; in traffic, v_v depends on h through the fundamental diagram. Both are monotonically increasing in their respective arguments, and both produce the same concave flux structure.

## 3. CORE MATHEMATICAL PARALLELISM

### Silo A — Epitaxial step-flow dynamics

On a vicinal crystal surface, adatoms deposited at rate F diffuse on terraces (lateral diffusion coefficient Dₛ, lifetime τₛ before desorption) and attach to step edges. In the quasi-steady approximation for the adatom diffusion field, the Burton-Cabrera-Frank (BCF) theory yields the velocity of step n as a function of the adjacent terrace widths lₙ (upstep) and lₙ₊₁ (downstep). For the symmetric case (no Ehrlich-Schwoebel barrier):

```math
v_n = F\Omega x_s\!\left[\tanh\!\left(\frac{l_n}{2x_s}\right) + \tanh\!\left(\frac{l_{n+1}}{2x_s}\right)\right]
```

where Ω is the atomic area and x_s = √(Dₛ τₛ) is the adatom diffusion length. Taking the continuum limit with step density ρ(x,t) = 1/l(x,t) and assuming slowly varying step spacing (lₙ ≈ lₙ₊₁ ≈ 1/ρ), the step current is J = ρv, giving the **step-density conservation law**:

```math
\frac{\partial \rho}{\partial t} + \frac{\partial}{\partial x}\!\left[\rho \cdot 2F\Omega x_s\,\tanh\!\left(\frac{1}{2x_s\rho}\right)\right] = 0
```

### Silo B — Lighthill-Whitham-Richards traffic model

On a single-lane road, vehicles obey a conservation law derived independently by Lighthill & Whitham (1955) and Richards (1956). With vehicle density ρ and a speed-density relationship v(ρ), the **vehicle-density conservation law** is:

```math
\frac{\partial \rho}{\partial t} + \frac{\partial}{\partial x}\!\Big[\rho\, v(\rho)\Big] = 0
```

The Greenshields constitutive model v(ρ) = v_f(1 − ρ/ρ_{jam}) yields the quadratic flux:

```math
f_{\text{traffic}}(\rho) = v_f\,\rho\!\left(1 - \frac{\rho}{\rho_{\text{jam}}}\right)
```

### Explicit operator-level correspondence

Both systems share the **identical conservation-law operator** ∂/∂t + ∂/∂x[f(·)] acting on a scalar density field. Under the variable identification:

| Epitaxy (BCF) | Traffic (LWR) |
|---|---|
| ρ (step density) | ρ (vehicle density) |
| f(ρ) = 2FΩxₛ · ρ tanh(1/(2xₛρ)) | f(ρ) = v_f ρ(1 − ρ/ρ_jam) |
| v_max = 2FΩxₛ | v_max = v_f |
| ρ → ∞ : f → ΩF (saturation) | ρ → ρ_jam : f → 0 (gridlock) |

**Correspondence 1 — Scalar conservation law with concave flux.**
The constitutive flux f(ρ) is globally concave in ρ for both systems. For the BCF flux:

```math
f''(\rho) = \frac{d^2}{d\rho^2}\!\left[2F\Omega x_s\,\rho\,\tanh\!\left(\frac{1}{2x_s\rho}\right)\right] = -8F\Omega x_s^3\,\frac{\tanh\xi\;\mathrm{sech}^2\!\xi}{\xi^3}\;<\;0, \quad \xi = \frac{1}{2x_s\rho} > 0
```

For the Greenshields traffic flux:

```math
f''(\rho) = -\frac{2v_f}{\rho_{\text{jam}}} < 0
```

Both fluxes are therefore concave on their entire domain, ensuring the characteristic speed c(ρ) = f′(ρ) is strictly decreasing, which is the structural prerequisite for shock formation via compression and rarefaction-fan formation via expansion.

**Correspondence 2 — Rankine-Hugoniot shock-jump condition.**
Discontinuous solutions (step bunches / traffic jams) in both systems propagate as shocks whose speed s is determined by the jump condition obtained from integrating the conservation law across the discontinuity:

```math
s\,(\rho_L - \rho_R) = f(\rho_L) - f(\rho_R)
```

where ρ_L is the density behind the shock (tight step spacing / congested traffic) and ρ_R is the density ahead (wide terraces / free-flowing traffic). This is not an analogy but the identical weak-solution condition for any scalar conservation law, applied to the domain-specific flux function on each side.

**Correspondence 3 — Lax entropy condition for shock selection.**
Among all weak solutions satisfying the Rankine-Hugoniot condition, the physically realizable shock is selected by the Lax entropy inequality, which requires that characteristics impinge on the shock from both sides:

```math
f'(\rho_L) > s > f'(\rho_R)
```

In epitaxy, this selects the stable step-bunch front: faster characteristics from the wide-terrace side and slower characteristics from the tight-step side both converge on the bunch boundary. In traffic, this selects the observable jam front: vehicles enter the jam from the free-flow side (fast characteristics) and exit from the congested side (slow characteristics). The mathematical condition is symbol-for-symbol identical and plays the same physical role in both domains.

**Scope and limitation of the correspondence.** The operator equivalence holds exactly for the local, symmetric (no Ehrlich-Schwoebel barrier) BCF model. The constitutive laws differ in their high-density behavior: the BCF flux saturates at f → ΩF (every deposited atom is immediately captured; no "gridlock" state), while the traffic flux vanishes at ρ = ρ_jam (standstill). Consequently, the two-branch (free-flow / congested) structure of the traffic fundamental diagram and phenomena such as the capacity drop have no direct BCF analogue. The correspondence is strongest for the basic single-flux concave conservation law and its immediate shock/rarefaction structure.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Vehicular traffic-flow engineering → Epitaxial growth modeling.
*   **Asymmetric Maturity Rationale:** Traffic engineering has accumulated four decades of mature methodology for solving scalar conservation laws in real-time operational settings: Godunov-type exact Riemann solvers, the cell-transmission model (CTM), ENO/WENO high-resolution schemes, front-tracking methods, and — critically — real-time data assimilation frameworks that fuse sparse loop-detector data with conservation-law models for live state estimation (e.g., the Kalman-filter-based freeway surveillance systems deployed at traffic management centers worldwide). Epitaxial growth modeling, by contrast, relies on kinetic Monte Carlo (KMC) for atomistic accuracy or on step-tracking ODE codes for continuum dynamics; both are computationally expensive and neither supports real-time process monitoring. The epitaxy community does not currently employ Godunov-type schemes, Riemann solvers, or data-assimilation frameworks for step dynamics, even though the governing equation admits them directly.
*   **Target Bottleneck Mitigation:** Current MBE (molecular beam epitaxy) process control relies on post-growth ex-situ characterization (STM, AFM) or indirect real-time indicators (RHEED oscillation damping) that cannot resolve step-bunch morphology during growth. Importing the traffic community's real-time conservation-law data-assimilation pipeline — specifically, a Godunov-type observer that assimilates sparse, real-time RHEED specular-beam intensity measurements to reconstruct the full step-density field ρ(x,t) — would enable closed-loop feedback control of growth parameters (flux F, substrate temperature T) to suppress step bunching in situ. The Godunov solver exploits the exact Riemann problem for the BCF flux to propagate step-density information at wave-characteristic speeds, enabling prediction of bunch evolution on the timescale of a single RHEED frame (~1 s), which is impossible with KMC or phase-field approaches.
*   **Falsifiable Prediction:** For the Si(001) vicinal surface grown by MBE at T = 650 °C with diffusion length x_s = 50 nm (independently calibrated from step-velocity measurements), a Godunov-type front-tracking scheme using the BCF-derived fundamental diagram f(ρ) = 2FΩx_s ρ tanh(1/(2x_sρ)) will reproduce the transient step-bunch coarsening trajectory — specifically, the mean inter-bunch spacing L_b(Θ) as a function of deposited coverage Θ — as predicted by kinetic Monte Carlo (KMC) simulations to within 20 % at Θ = 50 monolayers (ML) for deposition fluxes F ∈ [0.1, 2.0] ML/s, while achieving a wall-clock computational speedup of at least 50× over the KMC baseline. The prediction is falsified if (a) the L_b discrepancy exceeds 30 % at any Θ ∈ [10, 100] ML for any F in the stated range, (b) the speedup is less than 10×, or (c) the Godunov scheme predicts a qualitatively different coarsening regime (e.g., steady-state bunch spacing where KMC shows continuous logarithmic coarsening).

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"step bunching" AND "conservation law" AND "Burton-Cabrera-Frank"` — verifies whether the conservation-law framing of BCF step dynamics is already established within the epitaxy literature.
*   `"Lighthill-Whitham-Richards" AND "crystal growth" OR "epitaxial"` — directly tests whether the cross-domain mapping has been previously published.
*   `"step dynamics" AND "Godunov" OR "Riemann solver" AND "surface"` — checks whether conservation-law numerical methods from traffic or compressible-flow communities have already been applied to step-flow.
*   `"kinematic wave" AND ("step bunch" OR "vicinal surface")` — targets the specific physical mechanism (kinematic wave steepening) claimed as shared.
*   `"fundamental diagram" AND "step velocity" AND "terrace width"` — searches for the specific constitutive-law parallel (fundamental diagram as a concept applied to step dynamics).

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — In Section 3, Correspondence 1, the entry states "f''(\rho) = ... = -8F\Omega x_s^3\,\frac{\tanh\xi\;\mathrm{sech}^2\!\xi}{\xi^3} < 0"; this is not the second derivative of the f(ρ) = 2FΩx_sρ tanh(1/(2x_sρ)) given two lines above it. Direct differentiation gives f''(ρ) = -8FΩx_s²ξ³sech²(ξ)tanh(ξ) — x_s squared with ξ³ in the numerator, not x_s cubed with ξ³ in the denominator — and the entry's version is dimensionally inconsistent by one power of length given the units its own v_n = FΩx_s[tanh(l_n/2x_s)+tanh(l_{n+1}/2x_s)] equation requires of F. (The Silo B / Greenshields concavity calculation in the same section, f''(ρ) = −2v_f/ρ_jam, is correct.)
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five Section 2 mappings pair objects of compatible mathematical type (scalar density↔scalar density, constitutive velocity↔constitutive velocity, flux↔flux, shock↔shock, reciprocal-density spacing↔reciprocal-density spacing), and each Operator Role names a specific shared structure — an explicit shared PDE, a shared monotonicity/boundary condition, or a shared closed-form shock speed — rather than hedged similarity language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with explicit equations in Section 3: concave-flux conservation law (Correspondence 1 — the governing PDEs and the Greenshields-side concavity proof are valid even though the BCF-side derivative computation contains the error identified in Check 1), the Rankine-Hugoniot jump condition (Correspondence 2), and the Lax entropy condition (Correspondence 3).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (4a) is genuine: the named toolkit (Godunov/Riemann solvers, CTM, ENO/WENO, Kalman-filter data assimilation) is specific to real-time traffic operations, and no comparably mature real-time counterpart is described or plausible for step-flow control, so the direction is not reversible with comparable benefit. Falsifiability (4b) is satisfied with unusual specificity — the prediction names a measurable quantity (L_b(Θ)), explicit thresholds (20%/30% discrepancy, 10×/50× speedup), a bounded parameter range, and a distinct qualitative failure mode, not the template non-prediction pattern. Prior art (4c, advisory only): the shared mathematical skeleton here (scalar conservation law, concave flux, kinematic shocks) is the same one Whitham's kinematic-wave theory — which originates in Lighthill & Whitham's 1955 traffic-flow papers — applies across traffic, flood waves, and chromatography; I have moderate but not certain recollection that step-bunching has likewise been treated with conservation-law/kinematic-wave methods in the surface-science literature, which would bear on novelty without invalidating the mathematics.

#### Stage 3 Watch Items
- The Check 1 formula error needs correction and re-verification before resubmission — confirm the corrected f''(ρ) against the f(ρ) actually stated in Section 3.
- Search specifically for step-bunching literature already using conservation-law, shock-wave, or kinematic-wave framing (the entry's own Section 5 strings target exactly this; Whitham's traffic-originated kinematic-wave theory is a plausible common ancestor worth tracing).
- Independently verify the canonical BCF step-velocity closure (tanh vs. coth, and the numerical prefactor) against standard epitaxy references — this review checked only the formula's internal and dimensional self-consistency, not its fidelity to the standard BCF derivation.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — the displayed formula `f''(\rho) = \frac{d^2}{d\rho^2}[2F\Omega x_s\,\rho\,\tanh(1/(2x_s\rho))] = -8F\Omega x_s^3\,\frac{\tanh\xi\,\mathrm{sech}^2\!\xi}{\xi^3} < 0` is not the second derivative of the displayed BCF flux; the ξ-dependence is inverted relative to differentiating the stated flux with respect to ρ.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — the paired terms are mathematically compatible objects: densities map to densities, velocities to velocities, fluxes to fluxes, reciprocal lengths to reciprocal lengths, and shock-like solutions to shock-like solutions.
- **CHECK 3 (Correspondence Vector Support):** FAIL — `rankine_hugoniot_shock_jump_condition_at_step_bunch_and_jam_front` is demonstrated in Section 3, but `scalar_conservation_law_operator_with_concave_constitutive_flux` is not validly demonstrated because its concavity derivation is the erroneous second-derivative display, and `lax_entropy_condition_selecting_physically_realizable_shocks` is not coherently demonstrated because the entry labels ρ_L as high-density/congested while also asserting a concave flux and then imposing `f'(\rho_L) > s > f'(\rho_R)`, which would require ρ_L to be the lower-density/fast-characteristic side.
- **CHECK 4 (Transfer and Falsifiability):** PASS — the proposed transfer direction is plausibly asymmetric, and the prediction names measurable quantities, thresholds, and falsification conditions; no prior-art recognition is strong enough here to constitute a flag, though related literature should be checked at Stage 3.

#### Stage 3 Watch Items
- Verify whether the BCF step-density conservation law and concave-flux/kinematic-shock framing already appear in epitaxy or surface-physics literature.
- Verify whether traffic-engineering Godunov/CTM/data-assimilation methods have previously been proposed for step-flow or crystal-growth control.
- Check the correct left/right state convention for Lax-entropy shocks in traffic and step-flow descriptions, since the entry's labels are internally inconsistent.
- Assess whether the symmetric no-Ehrlich-Schwoebel BCF continuum model used here actually supports spontaneous step bunching or only shock propagation from imposed gradients.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed BCF second derivative is algebraically false: differentiating \(f(\rho)=2F\Omega x_s \rho \tanh(1/(2x_s\rho))\) gives \(f''(\rho)=-8F\Omega x_s^2 \xi^3 \tanh\xi\,\mathrm{sech}^2\xi\), not the displayed \(-8F\Omega x_s^3 \tanh\xi\,\mathrm{sech}^2\xi/\xi^3\); moreover, since the entry proves \(f''<0\), \(f'\) is strictly decreasing, so if \(\rho_L>\rho_R\) as asserted, then \(f'(\rho_L)<f'(\rho_R)\), making the displayed Lax inequality \(f'(\rho_L)>s>f'(\rho_R)\) impossible for the stated high-density-left/low-density-right shock.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are type-compatible scalar densities, velocities, fluxes, shock objects, and reciprocal length quantities; no category errors appear in Section 2.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The scalar conservation-law operator and Rankine-Hugoniot jump condition are supported by displayed equations, but the listed vector `lax_entropy_condition_selecting_physically_realizable_shocks` is not demonstrated: the body's own concavity claim and density assignment contradict the displayed entropy inequality.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The traffic-to-epitaxy direction is asymmetric by the entry's stated maturity rationale, and the prediction supplies measurable falsification thresholds (20%/30% \(L_b\) discrepancy, 50×/10× speedup, coarsening regime); prior-art note: the entry's own search string `"kinematic wave" AND ("step bunch" OR "vicinal surface")` should be run by Stage 3.

#### Stage 3 Watch Items
- Recheck the BCF \(f''\) formula; the sign is correct but the algebraic form is wrong.
- Probe existing kinematic-wave/BCF step-bunching literature for novelty.
- Verify the correct left/right density state assignment for entropy-admissible shocks in a concave scalar conservation law; the entry's stated high-density-behind/low-density-ahead orientation appears reversed.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The evaluation of the second derivative of the BCF flux $f(\rho)$ is algebraically and dimensionally incorrect. The entry claims: `f''(\rho) = \frac{d^2}{d\rho^2}\!\left[2F\Omega x_s\,\rho\,\tanh\!\left(\frac{1}{2x_s\rho}\right)\right] = -8F\Omega x_s^3\,\frac{\tanh\xi\;\mathrm{sech}^2\!\xi}{\xi^3}\;<\;0, \quad \xi = \frac{1}{2x_s\rho} > 0`. Because $\rho$ is inversely proportional to $\xi$, the $1/\rho^3$ generated by the second derivative requires $\xi^3$ in the *numerator*, not the denominator. Furthermore, the dimensional scaling is wrong ($x_s^2$ instead of $x_s^3$). The correct evaluation is $f''(\rho) = -8F\Omega x_s^2 \xi^3 \tanh(\xi)\mathrm{sech}^2(\xi)$.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mappings pair mathematically compatible objects (e.g., scalar density to scalar density, nonlinear flux to nonlinear flux, reciprocal of density to reciprocal of density) and explicitly state their shared structural role in the scalar conservation law.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three stated vectors (scalar conservation law with concave flux, Rankine-Hugoniot shock-jump condition, Lax entropy condition) are explicitly demonstrated in the body of Section 3 with equations and physical justifications.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric, porting traffic-flow engineering tools (Riemann solvers, Godunov schemes, real-time data assimilation) to epitaxial step-growth modeling, which traditionally relies on KMC or ODE codes. The hypothesis provides specific, falsifiable thresholds for inter-bunch spacing prediction errors and computational speedups.

#### Stage 3 Watch Items
None identified.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The governing conservation laws are correctly stated and properly paired (both first-order hyperbolic, same operator class). However, the displayed second-derivative formula for the BCF flux is incorrect: the entry writes `f''(ρ) = -8FΩx_s³ tanh(ξ) sech²(ξ) / ξ³`, but direct calculation yields `f''(ρ) = -8FΩx_s² ξ³ sech²(ξ) tanh(ξ)` — the entry has x_s³ and ξ⁻³ where the correct result has x_s² and ξ³. The sign is correct (both negative), so the concavity conclusion holds, but the specific prefactors are wrong by orders of magnitude (numerical verification at x_s=1, ρ=1 gives f''≈−0.36, while the entry's formula gives ≈−23.3).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five paired mappings connect objects of compatible mathematical type: scalar density ↔ scalar density, constitutive velocity ↔ constitutive velocity, flux function ↔ flux function, shock solution ↔ shock solution, reciprocal density ↔ reciprocal density. No category errors or hedged assertions without shared structure.
- **CHECK 3 (Correspondence Vector Support):** FLAG — All three listed vectors (scalar conservation law with concave flux, Rankine-Hugoniot, Lax entropy) are demonstrated in the body with equations and physical interpretation. However, the Lax entropy condition (Correspondence 3) contains an internal inconsistency: the entry states `ρ_L is the density behind the shock (tight step spacing / congested traffic)` i.e. ρ_L is the high-density state, but for a concave flux (f''<0, f' decreasing), the Lax-compliant shock requires ρ_L < ρ_R. With ρ_L > ρ_R as described, f'(ρ_L) < f'(ρ_R), making `f'(ρ_L) > s > f'(ρ_R)` unsatisfiable. The physical description ("faster characteristics from the wide-terrace side…slower from the tight-step side…both converge") is correct and contradicts the L/R labeling — the labels should be swapped. The formula itself is standard and correct; the error is in the physical state assignment.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (traffic → epitaxy) is genuinely asymmetric: traffic engineering possesses decades of mature Godunov/CTM/data-assimilation methodology that the epitaxy community does not employ for step dynamics. The falsifiable prediction is specific and measurable: it names a system (Si(001), T=650°C, x_s=50nm), a quantitative metric (mean inter-bunch spacing L_b within 20% at Θ=50 ML), a parameter range (F∈[0.1,2.0] ML/s), a speedup threshold (≥50×), and three explicit falsification criteria. No prior-art recognition triggered — the mathematical framework is textbook PDE theory but this specific domain pairing does not appear canonical in graduate-level references I can recall.

#### Stage 3 Watch Items
- Verify whether the specific domain pairing (epitaxial step-flow ↔ vehicular traffic flow) has been previously published. The underlying scalar-conservation-law, Rankine-Hugoniot, and Lax entropy framework is standard textbook PDE theory; the novelty claim rests entirely on the cross-domain application.
- Check whether the BCF step-velocity formula `v_n = FΩx_s[tanh(l_n/(2x_s)) + tanh(l_{n+1}/(2x_s))]` matches the normalization convention in the standard surface-physics BCF literature (some references include a factor of 1/2 or use coth instead of tanh).
- Verify whether step bunching actually occurs in the symmetric (no Ehrlich-Schwoebel barrier) BCF model — the entry restricts its correspondence to this case, but step bunching in experiments and KMC simulations typically requires an asymmetry (ES barrier or similar) that may modify the flux function's concavity structure.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The displayed BCF second derivative is mathematically wrong: the entry gives “(f''(\rho)=\cdots=-8F\Omega x_s^3,\tfrac{\tanh\xi,\mathrm{sech}^2\xi}{\xi^3})” for (f(\rho)=2F\Omega x_s\rho\tanh(1/(2x_s\rho))), whereas direct differentiation gives a factor proportional to (x_s^2\xi^3), not (x_s^3/\xi^3); additionally, the claimed Lax shock condition “(f'(\rho_L)>s>f'(\rho_R))” is incompatible with the stated concave flux when (\rho_L) is explicitly the high-density side and (\rho_R) the low-density side.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The principal mappings pair scalar density fields, constitutive velocities, fluxes, reciprocal length scales, and traveling discontinuities with compatible mathematical types and explicit operator roles.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Correspondence 1 is supported by the conservation-law equations, and the Rankine-Hugoniot formula is explicitly given, but Correspondence 2/3 as a claimed physically admissible shock correspondence is not demonstrated correctly because the stated density ordering and Lax inequality are incompatible with the concavity asserted in Correspondence 1.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed traffic-to-epitaxy transfer is stated asymmetrically, and the prediction specifies measurable coarsening error, speedup, coverage/flux ranges, and falsification criteria rather than merely asserting that the method may work.

#### Stage 3 Watch Items
* Probe the claimed shock correspondence against the correct entropy-admissibility ordering for a concave scalar flux.
* Probe whether the BCF step-density conservation-law formulation and traffic-style numerical treatment are already established in the step-bunching literature.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The entry presents the same scalar conservation-law operator \(\partial_t + \partial_x[f(\cdot)]\) on both sides and supplies domain-specific concave flux functions (BCF: \(f(\rho)=2F\Omega x_s\,\rho\tanh(1/(2x_s\rho))\); LWR: \(f(\rho)=v_f\rho(1-\rho/\rho_{\text{jam}})\)), both of which are first-order hyperbolic conservation laws and thus of the same equation class.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapped token is of compatible mathematical type (e.g., **Step density ρ_s ↔ Vehicle density ρ_v** are both scalar conserved densities; **Step flux J_s ↔ Traffic flow q_v** are both nonlinear flux functions), and the Operator Role entries specify explicit shared structures rather than hedged analogies.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed correspondence vectors are demonstrated in the body:  
  - **scalar_conservation_law_operator_with_concave_constitutive_flux** — shown in Section 1 and Section 3 with explicit flux formulas and concavity arguments;  
  - **rankine_hugoniot_shock_jump_condition_at_step_bunch_and_jam_front** — derived and quoted in Correspondence 2 with the jump condition \(s(\rho_L-\rho_R)=f(\rho_L)-f(\rho_R)\);  
  - **lax_entropy_condition_selecting_physically_realizable_shocks** — stated and applied in Correspondence 3 with \(f'(\rho_L)>s>f'(\rho_R)\).
- **CHECK 4 (Transfer and Falsifiability):** PASS — (a) The transfer direction (traffic → epitaxy) is plausibly asymmetric and justified by the entry's argument about mature traffic numerical/data-assimilation toolchains; (b) The prediction in Section 4 is falsifiable and specific (numerical thresholds for L_b discrepancy and computational speedup are provided); (c) Prior-art recognition is advisory only — Stage 3 should probe whether the conservation-law framing of BCF is already established.

#### Stage 3 Watch Items
- Verify whether the conservation-law framing of BCF and application of Godunov-type solvers to step-flow have prior literature (the entry itself highlights this as a verification string).
- Test the numerical claim: run the proposed Godunov-type scheme against KMC for the specified Si(001) parameters and check the stated accuracy (≤20% at Θ = 50 ML) and speedup (≥50×).
- Confirm the algebraic sign and domain of the BCF flux second derivative used to assert global concavity (the entry gives an explicit formula for \(f''(\rho)\) that Stage 3 should re-derive numerically for representative parameter values).

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are first-order scalar hyperbolic conservation laws of identical operator form with globally concave fluxes; the Rankine-Hugoniot and Lax conditions are the standard weak-solution apparatus for that class and are correctly attributed.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of identical mathematical type (scalar density fields, constitutive velocities, flux functions, shock solutions, reciprocal lengths) and the Operator Role statements name the shared structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (scalar conservation law with concave constitutive flux; Rankine-Hugoniot shock-jump condition; Lax entropy condition) are derived and displayed with explicit equations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction from traffic numerics/data-assimilation to epitaxy is asymmetrically justified by maturity differences; the prediction supplies concrete quantitative thresholds (L_b discrepancy, wall-clock speedup, qualitative coarsening regime) that can be falsified by direct comparison with KMC.

#### Stage 3 Watch Items
- Constitutive high-density mismatch (BCF saturation versus traffic gridlock) and its effect on two-branch phenomena
- Whether the continuum BCF reduction already appears in the epitaxy literature under conservation-law language

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B display genuine first-order hyperbolic scalar conservation laws ∂ρ/∂t + ∂f(ρ)/∂x = 0 with domain-correct BCF step-velocity v_n = FΩx_s[tanh(l_n/2x_s)+tanh(l_{n+1}/2x_s)] and LWR flux f= v_f ρ(1-ρ/ρ_jam); no class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five mappings pair compatible mathematical types (scalar density ↔ scalar density, constitutive velocity ↔ constitutive velocity, concave flux ↔ concave flux, shock ↔ shock, reciprocal length ↔ reciprocal length) with shared operator roles specified, no category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three YAML vectors demonstrated: (1) scalar_conservation_law_operator_with_concave_constitutive_flux via f''<0 derivations in Section 3, (2) rankine_hugoniot_shock_jump_condition_at_step_bunch_and_jam_front via s(ρ_L-ρ_R)=f(ρ_L)-f(ρ_R) in Section 3, (3) lax_entropy_condition_selecting_physically_realizable_shocks via f'(ρ_L)>s>f'(ρ_R) in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer traffic→epitaxy is genuinely asymmetric (Godunov/CTM/WENO/data-assimilation mature in traffic, absent in epitaxy per Section 4); prediction is falsifiable with specific measurable L_b(Θ) within 20% at Θ=50 ML, speedup ≥50×, and explicit falsification criteria (30% discrepancy, <10× speedup, wrong coarsening regime). No canonical prior-art pairing recognized.

#### Stage 3 Watch Items
- Verify bibliometric novelty of epitaxy ↔ LWR pairing; general kinematic-wave analogies are textbook but this specific cross-silo mapping is not a standard textbook example.
- Probe the disclosed high-density constitutive difference (saturation vs zero-flux) to ensure Stage 3 reviewers treat it as a limitation, not a structural break, as correctly scoped in the entry.
- Confirm no existing literature already applies Godunov-type Riemann solvers to BCF step dynamics as suggested by search string 3.