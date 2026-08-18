---
sid_metadata:
  entry_id: "SID-0053"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "applied-superconductivity-magnet-quench-protection"
  domain_b: "clinical-neurophysiology-cortical-spreading-depolarization"
  structural_family: "bistable-semilinear-parabolic-ignition-fronts"
  triple_correspondence_vectors:
    - "shared_bistable_parabolic_operator_with_unit_restoring_slope_after_affine_nondimensionalization"
    - "maxwell_equal_area_stall_condition_minimum_propagating_current_vs_sd_abort_threshold"
    - "unstable_stationary_nucleus_first_integral_mpz_vs_critical_initiation_half_length"
    - "shared_L2_gradient_flow_lyapunov_functional_and_mountain_pass_content_mqe_vs_threshold_kcl_moles"
    - "generation_to_clearance_capacity_ratio_with_unit_threshold_stekly_number_vs_pump_reserve"
    - "diffusion_free_core_path_independent_dose_integral_miits_vs_depolarization_duration"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / historically_isolated_communities / structure_visible_only_after_nondimensionalization"
prior_discovery_metrics:
  structural_isomorphism_score: 8.6
  vocabulary_divergence_score: 9.4
  expected_methodological_transfer_score: 7.8
  community_separation_score: 9.6
  representation_mismatch_score: 6.8
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.4
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "source_term_nonautonomy — the Silo B source depends on slow variables (ATP availability, [Na⁺]ᵢ, glutamate, cell swelling) that are frozen in the single-field reduction; the bistable reduction is valid only on the fast ionic timescale"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-06-22"
    verdict: "REJECT"
    verdict_rationale: "The entry claims the Silo A current-sharing point θ_A=1-I/I_c0 is an interior unstable zero of the shared source, but its own displayed Silo A source gives ĝ_A(θ_A)=-θ_A, so the claimed shared bistable root structure is not supported."
    failed_checks:
      - "Check 1: Bridge/V1 asserts ĝ(θ)=0 with θ_A=1-I/I_c0, but the displayed Silo A source yields ĝ_A(θ_A)=-θ_A."
      - "Check 2: The T_cs ↔ [K+]_{e,θ} mapping identifies T_cs as the interior unstable zero, which the Silo A equation contradicts."
    flagged_checks:
      - "Check 3: Vector 1 (shared bistable operator) is only partially supported; the operator form is shown, but the Silo A interior unstable zero is not the stated θ_A."
    quoted_evidence:
      - |
        Both are the interior unstable zero $\theta$ of the shared source, $\hat g(\theta)=0$, $\hat g'(\theta)>0$, separating the two basins of $\tau\partial_t u=\lambda^2\partial_x^2u+\hat g(u)$. $T_{cs}$ is a real scalar in K; $[\mathrm{K^+}]_{e,\theta}$ is a real scalar in mol m⁻³. The affine maps $u=(T-T_{op})/(T_c-T_{op})$ and $w=(K-K_{rest})/(K_r-K_{rest})$ carry both to the same dimensionless $\theta\in(0,u_+)$, giving $\theta_A=1-I/I_{c0}$ and $\theta_B=(K_\theta-K_{rest})/(K_r-K_{rest})$.
      - |
        $\hat g_A(u)=\alpha_S\,\varphi_A(u)-u$
      - |
        $\varphi_A(u)=
        \begin{cases}
        0,&u<\theta_A\\[3pt]
        \Bigl(\tfrac{u-\theta_A}{1-\theta_A}\Bigr)^{2},&\theta_A\le u\le 1\\[5pt]
        1,&u>1
        \end{cases}$
      - |
        $\hat g(0)=\hat g(\theta)=\hat g(u_+)=0,\quad \hat g'(0)=-1,\quad \hat g'(u_+)<0,$
      - |
        with $(\tau,\lambda,\theta,u_+)=(CA/hP,\ \sqrt{kA/hP},\ 1-I/I_{c0},\ \alpha_S)$ for Silo A
    stage_3_watch_items:
      - "Verify whether a separate Silo A interior unstable root (distinct from the current-sharing switch-on point θ_A) is defined in the literature and whether it maps to the SD threshold root."
      - "Probe prior art for direct quench-protection ↔ spreading-depolarization analogies, and for use of Nagumo/equal-area/critical-nucleus bistable-front theory in both domains."
      - "Check whether the Silo B pump-reserve ratio Π alone can determine the sign of the equal-area integral, given the displayed dependence on K_r, K_p, K_{rest}, and K_+."
      - "Assess whether the V6 dose-integral correspondence survives the slow-variable source nonautonomy identified in the entry's failure risk."
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "The shared-operator Bridge asserts a three-root bistable source with θ_A=1-I/I_c0 as the interior unstable zero, but the Silo A piecewise source gives ĝ_A(θ_A)=-θ_A≠0; this is a fatal internal contradiction."
    failed_checks:
      - "Check 1: Bridge equation falsely claims ĝ(θ)=0 for Silo A with θ=1-I/I_c0."
      - "Check 2: Vocabulary matrix maps T_cs to the interior unstable zero ĝ(θ)=0, which is false for Silo A."
    flagged_checks:
      - "Check 3: Vector 3 (unstable stationary nucleus first integral) is not demonstrated for Silo A by the shared first integral; Silo A uses a step-source idealization with cooling neglected."
    quoted_evidence:
      - "Both systems are now instances of ... \\hat g(0)=\\hat g(\\theta)=\\hat g(u_+)=0,\\quad \\hat g'(0)=-1,\\quad \\hat g'(u_+)<0, with (\\tau,\\lambda,\\theta,u_+)=(CA/hP,\\ \\sqrt{kA/hP},\\ 1-I/I_{c0},\\ \\alpha_S) for Silo A"
      - "\\varphi_A(u)= \\begin{cases} 0,&u<\\theta_A ... \\end{cases} \\qquad \\theta_A=1-\\tfrac{I}{I_{c0}}"
      - "\\hat g_A(u)=\\alpha_S\\,\\varphi_A(u)-u"
      - "Both are the interior unstable zero $\\theta$ of the shared source, $\\hat g(\\theta)=0$, $\\hat g'(\\theta)>0$"
    stage_3_watch_items:
      - "Probe whether redefining θ_A as the actual unstable root of α_S φ_A - u, rather than 1-I/I_c0, restores the shared three-root structure."
      - "Check the V3 Silo A MPZ derivation against the full stationary Wilson equation with cooling; the step-source idealization may not be the same first-integral nucleus."
      - "Verify the V6 Silo A adiabatic equation C dT/dt=ρ_m J_m^2 against the earlier source term G=ρ_m J_m^2 A_m/A; possible missing matrix-fraction factor."
      - "Prior-art watch: bistable reaction-diffusion ignition-front analogies between superconducting quench and cortical spreading depolarization (Wilson/Dresner and Tuckwell-Miura); determine if the pairing is canonical."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a fatal mathematical contradiction in Section 3 regarding the condition for the upper root's existence in Silo B, claiming it exists when generation exceeds clearance at infinity."
    failed_checks: ["Check 1: Equation Validity"]
    flagged_checks: ["Check 4: Transfer and Falsifiability"]
    quoted_evidence: ["In Silo B, since $J_{rel}-J_{pump}\\to j_0+j_r-j_p$ as $K\\to\\infty$, the upper root exists iff\n\n```math\n\\Pi\\equiv\\frac{j_0+j_r}{j_p}>1 .\n```"]
    stage_3_watch_items: ["The bistable traveling wave equation (often formulated as FitzHugh-Nagumo or Schlögl) is a textbook canonical model for both excitable biological media and superconducting normal zones; verify if the specific interdisciplinary transfer of metrology ($E_{MQE}$, MIITs) is genuinely novel despite this established structural analogy."]
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "The vocabulary mapping and Bridge V1 identify θ_A = 1 − I/I_{c0} as the interior unstable zero of the shared source with ĝ(θ)=0, but the entry's own Silo A derivation gives ĝ_A(θ_A) = −θ_A ≠ 0; the abstract three-zero bistable structure is valid for both systems, all six correspondence vectors are demonstrated with correct mathematics, and the computational content of V2–V6 is unaffected, but the specific identification of θ for Silo A is a quotable mathematical misidentification."
    failed_checks: []
    flagged_checks:
      - "Check 2: Vocabulary mapping T_cs ↔ [K⁺]_{e,θ} and Bridge V1 claim both are the interior unstable zero θ of the shared source with ĝ(θ)=0, ĝ′(θ)>0, but ĝ_A(θ_A) = −θ_A ≠ 0 for Silo A; the actual interior zero of ĝ_A lies at θ̂ ∈ (θ_A, 1) satisfying α_S((θ̂−θ_A)/(1−θ_A))² = θ̂, which depends on both θ_A and α_S"
    quoted_evidence:
      - "Bridge V1: 'ĝ(0)=ĝ(θ)=ĝ(u₊)=0' with '(τ,λ,θ,u₊)=(CA/hP, √(kA/hP), 1−I/I_{c0}, α_S) for Silo A'"
      - "Silo A derivation: 'ĝ_A(u) = α_S φ_A(u) − u' and 'φ_A(u) = 0, u < θ_A' — therefore ĝ_A(θ_A) = α_S·0 − θ_A = −θ_A ≠ 0"
      - "Vocabulary matrix: 'Both are the interior unstable zero θ of the shared source, ĝ(θ)=0, ĝ′(θ)>0 ... giving θ_A = 1−I/I_{c0}'"
    stage_3_watch_items:
      - "The specific cross-domain pairing (superconductor quench ↔ cortical spreading depolarization via shared bistable parabolic operator) should be checked against published interdisciplinary analogies; individually, the Grafstein-Tuckwell-Miura SD model and the Wilson/Stekly quench model are canonical in their fields, and bistable reaction-diffusion reductions of SD have appeared in the work of Dahlem, Miura, and others"
      - "The falsifiable prediction of a logarithmic law L*(v_SD) = λ_tail ln(B/τc) with experimentally testable quantitative claims should be checked against existing SD threshold/initiation data and against the bistable RD front-interaction literature"
      - "The V5 claim that for Silo A 'the upper root always exists and α_S=1 marks its position' should be verified: for the piecewise source as written, the upper root u₊=α_S lies in the valid region u>1 only when α_S>1, which is functionally the same existence criterion as Silo B's Π>1; the stated distinction between 'position' and 'existence' may be imprecise"
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The entry demonstrates internally consistent mathematics with correctly derived nondimensionalizations, matched equation classes, and fully supported correspondence vectors."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify the novelty of the specific domain pairing (magnet quench protection ↔ cortical spreading depolarization). While the interdisciplinary transfer of metrology is novel, the shared mathematical structure (bistable semilinear parabolic reaction-diffusion equations, Maxwell equal-area, mountain-pass) is a canonical framework in mathematical physics and biology."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a fatal vocabulary/equilibrium error: it identifies the superconducting current-sharing threshold with an interior unstable zero of the nondimensional source, but the displayed Silo A equation has nonzero source at that threshold."
    failed_checks: ["Check 2: The mapping T_cs ↔ SD initiation threshold incorrectly identifies T_cs with the unstable zero theta of the shared source.", "Check 1: The claimed shared bistable operator has the stated Silo A condition g_hat(theta)=0, but the displayed Silo A source gives g_hat(theta)=-theta, so the asserted root structure is internally inconsistent."]
    flagged_checks: []
    quoted_evidence: ["**Current-sharing temperature $T_{cs}$** ↔ **SD initiation threshold $[\\mathrm{K^+}]_{e,\\theta}$**\\n    *   *Operator Role:* Both are the interior unstable zero $\\theta$ of the shared source, $\\hat g(\\theta)=0$, $\\hat g'(\\theta)>0$, separating the two basins of $\\tau\\partial_t u=\\lambda^2\\partial_x^2u+\\hat g(u)$.", "`math\\n\\\\varphi_A(u)=\\n\\\\begin{cases}\\n0,&u<\\\\theta_A\\\\\\\\[3pt]\\n\\\\Bigl(\\\\tfrac{u-\\\\theta_A}{1-\\\\theta_A}\\\\Bigr)^{2},&\\\\theta_A\\\\le u\\\\le 1\\\\\\\\[5pt]\\n1,&u>1\\n\\\\end{cases}\\n\\\\qquad \\\\theta_A=1-\\\\tfrac{I}{I_{c0}}\\n`", "Note $\\hat g_A(0)=0$, $\\hat g_A'(0)=-1$, and the upper root is $u_+=\\alpha_S$, which is a fully resistive self-sustaining state iff $\\alpha_S>1$ — the classical Stekly cryostability criterion recovered as a statement about root position.", "`math\\n\\\\tau\\\\,\\\\partial_t u=\\\\lambda^{2}\\\\,\\\\partial_x^{2}u+\\\\hat g(u),\\n\\\\qquad\\n\\\\hat g(0)=\\\\hat g(\\\\theta)=\\\\hat g(u_+)=0,\\\\quad \\\\hat g'(0)=-1,\\\\quad \\\\hat g'(u_+)<0,\\n`"]
    stage_3_watch_items: ["If the entry is otherwise retained after the equilibrium/root error is addressed, verify the stronger Section 1 claim that the two systems have an exact operator identification while Section 1 simultaneously states that their constitutive source shapes differ."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The entry presents internally consistent semilinear bistable parabolic operators on both sides, type-consistent vocabulary mappings, and provides explicit equations/derivations supporting each listed correspondence vector; the proposed methodological transfer is asymmetric and names measurable outcomes."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify prior-art overlap with classical Nagumo / Grafstein reductions and Wilson MPZ/MQE literature (look for canonical mappings and earlier explicit reductions)."
      - "Check empirical feasibility and existing experimental protocols in SD literature for constructing an energy–duration (E_{MQE}-equivalent) calibration and a tissue-calibrated Γ_B mapping."
      - "Confirm assumptions behind the flux-factorization in V6 for realistic pump dynamics (the entry notes failure when m depends on K)."
      - "Examine the step-source and adiabatic idealizations used in Silo A closed-form derivations for applicability to modern composite conductor geometries and nonuniform J_m(T)."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency of the shared bistable parabolic structure, type-compatible mappings, fully demonstrated vectors, and a specific measurable falsifiable prediction under genuine asymmetry."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Constitutive source forms differ (piecewise-quadratic vs Hill) and are explicitly excluded from the claimed identity; confirm that the operator-level claims do not silently rely on source-shape identity.", "V6 dose-integral correspondence holds only under flux factorization and fails when m depends on K; verify that this limitation is respected in any transfer of the MIITs concept.", "Single-field reduction freezes slow variables (ATP, [Na+]i, glutamate, swelling); probe whether the bistable operator remains predictive once those variables are restored."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All six correspondence vectors are demonstrated with a shared semilinear bistable parabolic operator, Maxwell equal-area, first-integral nucleus, L2 gradient-flow Lyapunov and mountain-pass content, unit-threshold capacity ratio, and conditional dose integral; vocabulary types are compatible and transfer prediction is quantitatively falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Generic bistable reaction-diffusion (Nagumo / Allen-Cahn) structure is textbook; Stage 3 should bibliometrically verify novelty of specific MPZ/MQE/MIITs ↔ SD threshold/duration mapping via the provided search strings", "Entry's own primary_failure_risk notes source_term_nonautonomy — Silo B source depends on slow variables ATP, Na_i, glutamate, swelling frozen in single-field reduction; Stage 3 should probe validity of fast-ionic-timescale reduction for predicted L* ~ log(1/v_SD) law"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0053

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Applied superconductivity — magnet stability and quench protection engineering. A localized thermal disturbance in a composite superconductor either decays back to the cryogenic operating point or ignites a self-sustaining normal zone that propagates along the conductor at the normal-zone propagation velocity.
*   **Silo B (Field 2):** Clinical and experimental neurophysiology — cortical spreading depolarization (SD) in injured cortex. A focal ionic disturbance either is reabsorbed by Na⁺/K⁺-ATPase clearance and astrocytic buffering or ignites a self-sustaining depolarized zone that propagates across cortex at 1.5–7 mm min⁻¹.
*   **Mathematical Isomorphism:** Under the affine rescalings $u=(T-T_{op})/(T_c-T_{op})$ and $w=(K-K_{rest})/(K_r-K_{rest})$ followed by division by each system's linear restoring slope at its own rest state, the Wilson normal-zone equation and the Grafstein–Tuckwell–Miura extracellular-potassium equation become the *same* semilinear bistable parabolic operator $\tau\partial_t u=\lambda^{2}\partial_x^{2}u+\hat g(u)$ with $\hat g(0)=0,\ \hat g'(0)=-1$, so that their traveling-front solvability relation, Maxwell equal-area stall condition, unstable stationary nucleus and its first integral, $L^2$-gradient-flow Lyapunov functional and mountain-pass content, and unit-threshold generation-to-clearance capacity ratio coincide term by term — exactly for the operator and its stationary and traveling-wave structure, only in the flux-factorized diffusion-free core limit for the dose integral, and not at all at the level of constitutive source form (piecewise-quadratic current sharing versus Hill-type release and pump) or slow-variable coupling.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Current-sharing temperature $T_{cs}$** ↔ **SD initiation threshold $[\mathrm{K^+}]_{e,\theta}$**
    *   *Operator Role:* Both are the interior unstable zero $\theta$ of the shared source, $\hat g(\theta)=0$, $\hat g'(\theta)>0$, separating the two basins of $\tau\partial_t u=\lambda^2\partial_x^2u+\hat g(u)$. $T_{cs}$ is a real scalar in K; $[\mathrm{K^+}]_{e,\theta}$ is a real scalar in mol m⁻³. The affine maps $u=(T-T_{op})/(T_c-T_{op})$ and $w=(K-K_{rest})/(K_r-K_{rest})$ carry both to the same dimensionless $\theta\in(0,u_+)$, giving $\theta_A=1-I/I_{c0}$ and $\theta_B=(K_\theta-K_{rest})/(K_r-K_{rest})$.
*   **Stekly cryostability parameter $\alpha_S$** ↔ **Pump-reserve ratio $\Pi$**
    *   *Operator Role:* Both are the dimensionless ratio (peak generation capacity)/(clearance capacity at the reference excursion) multiplying the generation term in the nondimensional source; both are dimensionless reals whose unit crossing marks loss of the self-sustaining upper state. $\alpha_S=\rho_m J_m^2A_m/(hP(T_c-T_{op}))$; $\Pi=(j_0+j_r)/j_p$.
*   **Minimum propagating zone half-length $\ell_{MPZ}$** ↔ **Critical initiation half-length $\ell^{*}$**
    *   *Operator Role:* Both are the half-width of the unstable stationary solution $U_c$ of $\lambda^2U''+\hat g(U)=0$, obtained from the identical first integral $\tfrac{\lambda^2}{2}U'^2+\hat G(U)=0$. Both are lengths in m; no rescaling needed beyond $\lambda_A=\sqrt{kA/hP}$ versus $\lambda_B=\sqrt{D_K^{*}\alpha/r}$.
*   **Minimum quench energy $E_{MQE}$** ↔ **Threshold KCl content $Q^{*}$**
    *   *Operator Role:* Both are the stored-extensive-quantity content of the same mountain-pass profile $U_c$ of the shared Lyapunov functional $F$. Types differ (J versus mol) and are reconciled by identifying the densities conjugate to the diffusing potential — i.e. the coefficients of $\partial_t$ in each PDE: $C\,(T-T_{op})\ \leftrightarrow\ \alpha\,(K-K_{rest})$, in J m⁻³ and mol m⁻³ respectively. The shared dimensionless invariant is the nucleus content $\mathcal{Q}=\lambda^{-1}\!\int U_c\,d\xi$.
*   **Minimum propagating current $I_p$ / cold-end recovery** ↔ **SD abort (stall) threshold**
    *   *Operator Role:* Both are the Maxwell equal-area condition $\int_0^{u_+}\hat g(u)\,du=0$, i.e. the vanishing of the numerator in the traveling-wave solvability relation $\tau c\int U'^2 d\xi=\int_0^{u_+}\hat g\,du$. Both are codimension-one surfaces in the respective parameter spaces $(I,h)$ and $(j_0,j_r,j_p,K_p)$.
*   **Normal-zone propagation velocity (NZPV)** ↔ **SD front velocity $v_{SD}$**
    *   *Operator Role:* Both are the eigenvalue $c$ of the same traveling-wave operator $\lambda^2U''+\tau cU'+\hat g(U)=0$ with $U(-\infty)=u_+$, $U(+\infty)=0$. Both in m s⁻¹.
*   **Quench integral (MIITs) $\Gamma_A$** ↔ **Cumulative depolarization duration $\Gamma_B$**
    *   *Operator Role:* Both are the path-independent first integral of the diffusion-free core dynamics, $\int(\text{normalized drive})\,dt=$ state function of the peak excursion. Types are reconciled by normalizing each drive to its reference value ($J_m^2\!\to\!(J_m/J_{op})^2$; ATP availability $m$ already dimensionless), after which both integrals carry units of s.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** A composite superconductor operating at $T_{op}$ carries transport current $I$; a mechanical or flux-jump disturbance heats a short length above the current-sharing temperature $T_{cs}$, at which current begins to commutate into the normal matrix and Joule generation switches on. Magnet engineers model the resulting one-dimensional competition between generation, axial conduction and cryogen cooling with the Wilson normal-zone equation:

```math
C\,\partial_t T \;=\; k\,\partial_x^{2}T \;+\; G(T;I)\;-\;\frac{hP}{A}\bigl(T-T_{op}\bigr),
\qquad
G(T;I)=\frac{\rho_m\,I_m(T)^{2}}{A\,A_m}
```

```math
I_m(T)=
\begin{cases}
0, & T<T_{cs}\\[4pt]
I\,\dfrac{T-T_{cs}}{T_c-T_{cs}}, & T_{cs}\le T\le T_c\\[6pt]
I, & T>T_c
\end{cases}
\qquad
T_{cs}=T_{op}+\bigl(T_c-T_{op}\bigr)\Bigl(1-\tfrac{I}{I_{c0}}\Bigr)
```

Setting $u=(T-T_{op})/(T_c-T_{op})$, $\tau_A=CA/hP$, $\lambda_A=\sqrt{kA/hP}$ and dividing through by $(hP/A)(T_c-T_{op})$:

```math
\tau_A\,\partial_t u=\lambda_A^{2}\,\partial_x^{2}u+\hat g_A(u),
\qquad
\hat g_A(u)=\alpha_S\,\varphi_A(u)-u,
\qquad
\alpha_S=\frac{\rho_m J_m^{2}A_m}{hP\,(T_c-T_{op})}
```

```math
\varphi_A(u)=
\begin{cases}
0,&u<\theta_A\\[3pt]
\Bigl(\tfrac{u-\theta_A}{1-\theta_A}\Bigr)^{2},&\theta_A\le u\le 1\\[5pt]
1,&u>1
\end{cases}
\qquad \theta_A=1-\tfrac{I}{I_{c0}}
```

Note $\hat g_A(0)=0$, $\hat g_A'(0)=-1$, and the upper root is $u_+=\alpha_S$, which is a fully resistive self-sustaining state iff $\alpha_S>1$ — the classical Stekly cryostability criterion recovered as a statement about root position.

**Silo B.** The Grafstein potassium hypothesis, formalized by Tuckwell and Miura and expressed in Nicholson's extracellular-space variables, models SD as autocatalytic K⁺ release into a tortuous extracellular volume fraction $\alpha$ opposed by Na⁺/K⁺-ATPase uptake:

```math
\partial_t K = D_K^{*}\,\partial_x^{2}K+\frac{1}{\alpha}\Bigl[J_{rel}(K)-J_{pump}(K)\Bigr],
\qquad D_K^{*}=\frac{D_K}{\lambda_t^{2}}
```

```math
J_{rel}(K)=j_0+j_r\frac{K^{2}}{K_r^{2}+K^{2}},
\qquad
J_{pump}(K)=j_p\frac{K^{2}}{K_p^{2}+K^{2}}
```

With $r\equiv\bigl(J_{pump}'-J_{rel}'\bigr)\big|_{K_{rest}}>0$, $\Delta K\equiv K_r-K_{rest}$, $w=(K-K_{rest})/\Delta K$, $\tau_B=\alpha/r$, $\lambda_B=\sqrt{D_K^{*}\alpha/r}$:

```math
\tau_B\,\partial_t w=\lambda_B^{2}\,\partial_x^{2}w+\hat g_B(w),
\qquad
\hat g_B(w)=\frac{J_{rel}-J_{pump}}{r\,\Delta K}\Big|_{K=K_{rest}+w\Delta K}
```

so that $\hat g_B(0)=0$ and $\hat g_B'(0)=-1$ by construction.

**Bridge (V1 — shared operator).** Both systems are now instances of

```math
\tau\,\partial_t u=\lambda^{2}\,\partial_x^{2}u+\hat g(u),
\qquad
\hat g(0)=\hat g(\theta)=\hat g(u_+)=0,\quad \hat g'(0)=-1,\quad \hat g'(u_+)<0,
```

with $(\tau,\lambda,\theta,u_+)=(CA/hP,\ \sqrt{kA/hP},\ 1-I/I_{c0},\ \alpha_S)$ for Silo A and $(\alpha/r,\ \sqrt{D_K^{*}\alpha/r},\ \theta_B,\ w_+)$ for Silo B. The identification is exact; only the constitutive shape of $\hat g$ between its roots differs.

**V2 — Maxwell equal-area stall condition.** Setting $u(x,t)=U(\xi)$, $\xi=x-ct$, $U(-\infty)=u_+$, $U(+\infty)=0$ gives $\lambda^2U''+\tau cU'+\hat g(U)=0$. Multiplying by $U'$ and integrating over $\mathbb{R}$ annihilates the boundary terms:

```math
\tau c\int_{-\infty}^{\infty}\!U'^{2}\,d\xi=\int_{0}^{u_+}\hat g(u)\,du
\qquad\Longrightarrow\qquad
\operatorname{sign}(c)=\operatorname{sign}\!\int_{0}^{u_+}\hat g(u)\,du .
```

*Silo A closed form.* With $u_+=\alpha_S$ and $\int_{\theta_A}^{1}\varphi_A\,du=(1-\theta_A)/3$:

```math
\int_0^{\alpha_S}\!\hat g_A\,du=\alpha_S\Bigl[\tfrac{1-\theta_A}{3}+\alpha_S-1\Bigr]-\tfrac{\alpha_S^{2}}{2}=0
\;\Longleftrightarrow\;
\alpha_S=\tfrac{4+2\theta_A}{3}.
```

Writing $i=I/I_{c0}$, $\alpha_S=\alpha_0 i^{2}$ with $\alpha_0=\rho_m I_{c0}^{2}/(A_m hP(T_c-T_{op}))$ and $\theta_A=1-i$, the minimum propagating current solves

```math
\alpha_0 i_p^{2}+\tfrac{2}{3}i_p-2=0
\qquad\Longrightarrow\qquad
i_p=\frac{-\tfrac{2}{3}+\sqrt{\tfrac{4}{9}+8\alpha_0}}{2\alpha_0},
```

which is the cold-end recovery / minimum-propagating-current criterion in closed form.

*Silo B closed form.* The same condition, written in the neurophysiologist's variables and evaluated with the Hill-2 forms above ($\Delta=K_+-K_{rest}$):

```math
\int_{K_{rest}}^{K_+}\!\bigl[J_{rel}-J_{pump}\bigr]dK
=(j_0+j_r-j_p)\Delta
-j_rK_r\Bigl[\arctan\tfrac{K}{K_r}\Bigr]_{K_{rest}}^{K_+}
+j_pK_p\Bigl[\arctan\tfrac{K}{K_p}\Bigr]_{K_{rest}}^{K_+}=0 .
```

This is the SD abort threshold: pharmacological or metabolic manipulations that drive this integral through zero reverse the sign of $v_{SD}$, exactly as reducing $I$ through $I_p$ reverses NZPV. In the step-source adiabatic limit the Silo A branch reproduces Wilson's $v=(J_m/C)\sqrt{\rho_m k/(T_t-T_{op})}$ with $T_t=(T_c+T_{cs})/2$; in the cubic reduction $\hat g=a\,u(u-\theta)(1-u)$ the Silo B branch reproduces the Nagumo speed $c=(\lambda/\tau)\sqrt{a/2}\,(1-2\theta)$.

**V3 — Unstable stationary nucleus.** Stationary solutions of $\lambda^2U''+\hat g(U)=0$ decaying to $0$ obey the first integral

```math
\tfrac{\lambda^{2}}{2}\,U'^{2}+\hat G(U)=0,\qquad \hat G(U)=\int_0^{U}\hat g(s)\,ds,
```

so the nucleus peak $u_p$ is fixed by $\hat G(u_p)=0$ — a second, *local* equal-area condition distinct from the global one in V2.

*Silo A.* Taking the step-source idealization $G=G_{max}=\rho_mJ_m^2A_m/A$ inside the zone and neglecting cooling there, $kT''=-G_{max}$ with $T(\pm\ell)=T_{op}$ gives $T(x)=T_{op}+\tfrac{G_{max}}{2k}(\ell^{2}-x^{2})$, and imposing $T(0)=T_c$:

```math
\ell_{MPZ}=\sqrt{\frac{2kA\,(T_c-T_{op})}{\rho_m J_m^{2}A_m}}
\;\xrightarrow{\;A_m/A\to1\;}\;
\Bigl[\tfrac{2k(T_c-T_{op})}{\rho_m J_m^{2}}\Bigr]^{1/2},
```

Wilson's standard MPZ estimate.

*Silo B.* The same quadrature, with the half-width measured to half-peak to avoid the logarithmic tail divergence:

```math
\ell^{*}=\lambda_B\!\int_{w_p/2}^{w_p}\frac{dw}{\sqrt{-2\hat G_B(w)}},
\qquad \hat G_B(w_p)=0,
\qquad \lambda_B=\sqrt{D_K^{*}\alpha/r}.
```

Linearization about the two stable roots gives the tail decay lengths $\lambda_-=\lambda$ and $\lambda_+=\lambda/\sqrt{|\hat g'(u_+)|}$ on both sides; write $\lambda_{tail}=\max(\lambda_-,\lambda_+)$.

**V4 — Shared Lyapunov functional and mountain-pass content.** Both PDEs are $L^2$ gradient flows. In Silo A variables (constant $k$; for temperature-dependent $C$ the flow is gradient in the $C$-weighted metric):

```math
F_A[T]=\int\Bigl[\tfrac{k}{2}(\partial_xT)^{2}-\!\int_{T_{op}}^{T}\!\Bigl(G(s;I)-\tfrac{hP}{A}(s-T_{op})\Bigr)ds\Bigr]dx,
\qquad C\,\partial_tT=-\frac{\delta F_A}{\delta T}.
```

In Silo B variables:

```math
F_B[K]=\int\Bigl[\tfrac{D_K^{*}\alpha}{2}(\partial_xK)^{2}-\!\int_{K_{rest}}^{K}\!\bigl(J_{rel}(s)-J_{pump}(s)\bigr)ds\Bigr]dx,
\qquad \alpha\,\partial_tK=-\frac{\delta F_B}{\delta K}.
```

In both cases $dF/dt=-\!\int\!\rho_{\!*}(\partial_t\cdot)^{2}dx\le0$ with $\rho_{\!*}\in\{C,\alpha\}$, so $U_c$ is the mountain-pass saddle separating the rest basin from the propagating branch. The *operationally measured* threshold in each field is not $\Delta F$ but the stored-quantity content of $U_c$ — the enthalpy and the ion content respectively:

```math
E_{MQE}=A\!\int\!\Bigl[\int_{T_{op}}^{U_c(x)}\!C\,dT\Bigr]dx
\qquad\longleftrightarrow\qquad
Q^{*}=\alpha\!\int\bigl(K_c(x)-K_{rest}\bigr)\,dV,
```

$Q^{*}$ being precisely the threshold number of moles of KCl in a focal microinjection. The two integrands are the densities conjugate to the diffusing potential in each PDE, which is what makes the type reconciliation $C(T-T_{op})\leftrightarrow\alpha(K-K_{rest})$ forced rather than chosen.

**V5 — Generation-to-clearance capacity ratio, unit threshold.** In Silo A, $\alpha_S=\rho_mJ_m^{2}A_m/(hP(T_c-T_{op}))$ is exactly the nondimensional upper root $u_+$, and $\alpha_S\le1$ places that root below the normal transition: no self-sustaining resistive zone. In Silo B, since $J_{rel}-J_{pump}\to j_0+j_r-j_p$ as $K\to\infty$, the upper root exists iff

```math
\Pi\equiv\frac{j_0+j_r}{j_p}>1 .
```

Both parameters are (peak generation capacity)/(clearance capacity at the reference excursion), both have threshold exactly unity in their own nondimensionalization, and both control the sign of the V2 integral. **Where the correspondence stops:** Silo A's removal term is linear (Newton cooling), so the upper root always exists and $\alpha_S=1$ marks its *position*; Silo B's removal saturates, so $\Pi=1$ marks its *existence*. The dimensionless statement "no self-sustaining upper state below unity" is shared; the mechanism producing it is not.

**V6 — Diffusion-free core dose integral (holds only under flux factorization).** At the core of a fully developed zone, diffusion is negligible and the local balance is a separable ODE on both sides.

*Silo A:* $C(T)\,dT/dt=\rho_m(T)J_m(t)^{2}$, hence

```math
\Gamma_A=\int_0^{t_f}\!\Bigl(\tfrac{J_m(t)}{J_{op}}\Bigr)^{2}dt
=\frac{1}{J_{op}^{2}}\int_{T_{op}}^{T_{hot}}\frac{C(T)}{\rho_m(T)}\,dT ,
```

the MIITs / quench-integral hot-spot criterion: a path-independent state function of the peak temperature.

*Silo B:* under the pump-limited factorization $\alpha\,dK/dt=-m(t)\,J_{pump}(K)$, with $m(t)\in[0,1]$ the ATP availability,

```math
\Gamma_B=\int_0^{t_f}\!m(t)\,dt=\alpha\!\int_{K_{rest}}^{K_{hi}}\frac{dK}{J_{pump}(K)} ,
```

so the clinically recorded depolarization duration is likewise a path-independent state function of the peak ionic excursion. The correspondence requires the flux to factorize into (time-dependent drive) × (function of state) on both sides; it fails where $m$ itself depends on $K$.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Applied superconductivity / magnet quench protection → experimental and clinical cortical spreading depolarization.

*   **Asymmetric Maturity Rationale:** For this exact operator class, superconductivity has built, over roughly sixty years, an *instrumented metrology and protection-decision* stack on top of the bistable ignition PDE: Wilson–Dresner MPZ/MQE theory; the calibrated heater-pulse protocol that measures minimum quench energy as a two-dimensional map over pulse energy and pulse duration on instrumented short samples; the Stekly and cold-end-recovery criteria used as quantitative design rules rather than descriptions; the MIITs hot-spot integral tied to a hard design limit; and detection architectures specified as threshold voltage plus validation window with an explicitly budgeted false-trigger rate. The SD field is genuinely mature elsewhere — multi-ion biophysical models with explicit Na⁺/K⁺/Cl⁻/glutamate dynamics and cell swelling (Kager–Wadman–Somjen, Hübel–Ullah), bifurcation analysis of SD wave models, and standardized clinical ECoG detection of DC shifts under COSBID recommendations — and it is *not* less sophisticated at PDE analysis, which is the shared asset here, not the transferable one. The narrow, specific capability it lacks: no calibrated stimulus-energy threshold metrology (an $E_{MQE}$-equivalent energy–duration map), no tissue-calibrated $\Gamma_B$ converting recorded depolarization duration into a predicted peak local excursion, and consequently no protection-decision architecture with a quantified false-positive budget. SD "threshold" is still reported as a preparation-specific KCl volume or stimulation charge.

*   **Target Bottleneck Mitigation:** Hypothesis — the operational bottleneck in SD research and neurocritical monitoring is that propagate-versus-abort cannot presently be predicted for a given focal depolarization in a given cortex, because the threshold is treated as a fixed injected volume rather than as the mountain-pass content $Q^{*}$ of a nucleus whose size depends on how close the tissue sits to the equal-area stall condition. Importing the MQE energy–duration ladder protocol (V4), the equal-area stall criterion (V2) and the $\Gamma$ dose integral (V6) replaces that fixed volume with a two-parameter criterion in $(\lambda_{tail},v_{SD})$, both independently measurable at the bedside or bench from the K⁺ front profile and the propagation delay between adjacent electrodes.

*   **Falsifiable Prediction:** In urethane-anesthetized rat neocortex with an open cranial window, K⁺-selective microelectrode plus intrinsic-optical-signal imaging, and SD induced by focal KCl microinjection through a calibrated micropipette of controlled radius, grade $v_{SD}$ over at least a 4-fold range (nominally 6 → 1.5 mm min⁻¹) across ≥5 conditions by superfusion with graded low-dose ouabain or graded hypoxia. Near the stall condition the critical nucleus is two interacting fronts whose stationarity requires $\tau c=B\,e^{-L^{*}/\lambda_{tail}}$, so $L^{*}=\lambda_{tail}\ln\!\bigl(B/\tau c\bigr)$ and, independent of the unknown prefactor, $L^{*}(v_1)-L^{*}(v_2)=\lambda_{tail}\ln(v_2/v_1)$. **Prediction:** the minimum initiation half-length regressed on $\ln(1/v_{SD})$ is linear with $R^{2}\ge0.9$ and slope equal, within 25%, to $\lambda_{tail}$ measured independently from the exponential leading edge of the $[\mathrm{K^+}]_e$ front; a 4-fold speed reduction must raise $L^{*}$ by $\lambda_{tail}\ln4=1.386\,\lambda_{tail}$, i.e. 0.28–0.83 mm for the reported $\lambda_{tail}\approx0.2$–0.6 mm. The named baseline it must beat is the speed-independent fixed-critical-volume (fixed threshold charge) criterion in standard use for SD induction, which predicts slope zero. **Falsified if** the regression slope is statistically indistinguishable from zero, or differs from the independently measured $\lambda_{tail}$ by more than 25%, or if $L^{*}$ varies with $v_{SD}$ non-logarithmically (e.g. as a power law) over the tested range. **Corollary, conditional on the cubic reduction $\hat g=a\,u(u-\theta)(1-u)$ only:** stall ($c=0$) occurs at $\int_0^1\hat g=0\Leftrightarrow\theta=1/2$, predicting that SD aborts when the measured threshold $[\mathrm{K^+}]_{e,\theta}$ reaches the midpoint of the rest-to-plateau excursion — 29–31 mM for $K_{rest}=3$ mM and a 55–60 mM plateau. Falsified if abort is observed with $\theta$ outside 0.40–0.60 in tissue where the source is verified single-field and cubic-like.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"minimum propagating zone" AND "minimum quench energy" AND ("cold end recovery" OR "minimum propagating current") AND "equal area"`
*   `"spreading depolarization" AND ("Tuckwell-Miura" OR "extracellular potassium reaction-diffusion") AND ("critical nucleus" OR "threshold initiation volume") AND "front velocity"`
*   `("spreading depolarization" OR "spreading depression") AND ("quench propagation" OR "normal zone propagation" OR "minimum quench energy" OR "Stekly")` — deliberate self-falsification of the pairing claim
*   `("MIITs" OR "quench integral" OR "hot spot temperature") AND ("depolarization duration" OR "cumulative depolarization" OR "neurocritical care")` — self-falsification of the V6 transfer claim
*   `"critical nucleus" AND "logarithmic" AND "front interaction" AND "bistable reaction-diffusion" AND ("spreading depolarization" OR "cortical")` — tests whether the predicted log law has already been applied target-side

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-06-22

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The bridge states “$\hat g(0)=\hat g(\theta)=\hat g(u_+)=0$” and assigns Silo A “$\theta=1-I/I_{c0}$,” but the displayed Silo A source “$\hat g_A(u)=\alpha_S\,\varphi_A(u)-u$” with “$\varphi_A(\theta_A)=0$” gives “$\hat g_A(\theta_A)=-\theta_A$,” so the claimed shared zero at $\theta_A$ is not modeled by the Silo A equation.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The pair “Current-sharing temperature $T_{cs}$ ↔ SD initiation threshold $[\mathrm{K^+}]_{e,\theta}$” states “Both are the interior unstable zero $\theta$ of the shared source,” but $T_{cs}$ maps to the Silo A switch-on point $\theta_A$ in $\varphi_A$, not to a root of $\hat g_A$.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors V2–V6 are supported by derivations in Section 3 (V2 equal-area condition, V3 stationary nucleus, V4 Lyapunov/content, V5 capacity ratio, V6 dose integral). Vector 1, “shared_bistable_parabolic_operator_with_unit_restoring_slope_after_affine_nondimensionalization,” is only partially supported: the nondimensional parabolic operator is demonstrated, but the Silo A interior unstable zero required for bistability is not correctly established because $\theta_A$ is not a source root.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is specifically asymmetric (quench-protection metrology and protection-decision stack → SD threshold metrology), and the prediction names measurable quantitative criteria (regression slope within 25% of independently measured $\lambda_{tail}$, $R^2\ge0.9$, specified falsification conditions). Prior-art advisory: general bistable-front equal-area/critical-nucleus theory is well developed; Stage 3 should check whether this specific domain pairing has been published.

#### Stage 3 Watch Items
- Verify whether a separate Silo A interior unstable root (distinct from the current-sharing switch-on point $\theta_A$) is defined in the quench literature and whether it maps to the SD threshold root.
- Probe prior art for direct quench-protection ↔ cortical spreading depolarization analogies, and for explicit use of Nagumo/equal-area/critical-nucleus bistable-front theory in both domains.
- Check whether the Silo B pump-reserve ratio $\Pi$ alone can determine the sign of the equal-area integral, or whether the additional Hill-function parameters shown in the entry are required.
- Assess whether the V6 dose-integral correspondence survives the slow-variable source nonautonomy noted in the entry’s primary failure risk.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The Bridge claims both systems are instances of
  ```
  τ ∂_t u = λ² ∂_x² u + ĝ(u),  ĝ(0)=ĝ(θ)=ĝ(u_+)=0
  ```
  with `θ=1-I/I_c0` for Silo A. But from the Silo A definitions,
  ```
  ĝ_A(u)=α_S φ_A(u)-u,
  φ_A(u)=0 for u<θ_A,  θ_A=1-I/I_c0,
  ```
  so at `u=θ_A` one has `φ_A(θ_A)=0` and therefore `ĝ_A(θ_A)=-θ_A≠0`. Thus the claimed shared three-root operator is false for Silo A.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping “Current-sharing temperature `T_cs` ↔ SD initiation threshold” states: “Both are the interior unstable zero `θ` of the shared source, `ĝ(θ)=0`, `ĝ'(θ)>0`.” This is false for Silo A: `T_cs` is the switch-on threshold of the generation term, not a zero of `ĝ_A`.
- **CHECK 3 (Correspondence Vector Support):** FLAG — The vector `unstable_stationary_nucleus_first_integral_mpz_vs_critical_initiation_half_length` is not demonstrated for Silo A by the shared first integral. Silo A uses a step-source idealization with cooling neglected (`kT''=-G_max`, finite Dirichlet boundaries), while Silo B uses the full stationary equation `λ²U''+ĝ(U)=0`. The other five listed vectors have body derivations, subject to the V1 root error.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetry rationale is specific and directional, and the falsifiable prediction names measurable quantities, thresholds, and explicit falsification conditions. No prior-art recognition requiring rejection; see Stage 3 watch items.

#### Stage 3 Watch Items
- Probe whether redefining `θ_A` as the actual unstable root of `α_S φ_A - u`, rather than `1-I/I_c0`, restores the shared three-root structure.
- Check the V3 Silo A MPZ derivation against the full stationary Wilson equation with cooling; the step-source idealization may not be the same first-integral nucleus.
- Verify the V6 Silo A adiabatic equation `C dT/dt=ρ_m J_m^2` against the earlier source term `G=ρ_m J_m^2 A_m/A`; possible missing matrix-fraction factor.
- Prior-art watch: bistable reaction-diffusion ignition-front analogies between superconducting quench and cortical spreading depolarization, especially Wilson/Dresner quench theory and Tuckwell-Miura extracellular K⁺ models.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The claim about the existence of the upper root in Silo B is mathematically backward; if $\Pi > 1$, peak generation ($j_0+j_r$) strictly exceeds maximum clearance ($j_p$) as $K \to \infty$, meaning the source term remains positive and no upper stable equilibrium can form. Error text: "In Silo B, since $J_{rel}-J_{pump}\to j_0+j_r-j_p$ as $K\to\infty$, the upper root exists iff \n\n```math\n\Pi\equiv\frac{j_0+j_r}{j_p}>1 .\n```"
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All vocabulary pairs map objects of compatible mathematical types and explicitly describe identical structural roles within the shared bistable framework.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six vectors listed in the metadata are rigorously demonstrated in the text via explicit derivations, integrations, and operator identities.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The methodological transfer is genuinely asymmetric and the specific experimental predictions are highly falsifiable, but as an advisory prior-art note, the mapping of both fields to the generic bistable traveling wave equation is well-established in nonlinear dynamics textbooks.

#### Stage 3 Watch Items
- The bistable traveling wave equation (frequently studied via the FitzHugh-Nagumo or Schlögl models) is a canonical mechanism for both excitable biological tissues and propagating superconducting normal zones; Stage 3 should evaluate whether the specific proposed transfer of engineering metrology (MIITs, $E_{MQE}$ protocols) offers novel value beyond the well-known mathematical homology.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the Wilson normal-zone equation and the Grafstein–Tuckwell–Miura extracellular-potassium equation are genuine semilinear parabolic PDEs from their stated domains. The nondimensionalization to the shared form τ∂_t u = λ²∂_x² u + ĝ(u) with ĝ(0)=0, ĝ′(0)=−1 is correctly performed on both sides. The traveling-wave solvability relation, equal-area condition, first integral, gradient-flow Lyapunov functionals, and diffusion-free core dose integrals are all derived with correct equations. The piecewise quadratic current-sharing source and the Hill-function release/pump source are correctly reduced.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The vocabulary mapping T_cs ↔ [K⁺]_{e,θ} and Bridge V1 claim both quantities are the interior unstable zero θ of the shared source with ĝ(θ)=0. For Silo A, the entry's own derivation defines ĝ_A(u) = α_S φ_A(u) − u with φ_A(u)=0 for u < θ_A, giving ĝ_A(θ_A) = −θ_A ≠ 0. The actual interior unstable zero of ĝ_A exists at a point θ̂ ∈ (θ_A, 1) satisfying α_S((θ̂−θ_A)/(1−θ_A))² = θ̂, which depends on both θ_A and α_S and is not simply 1−I/I_{c0}. For Silo B, the identification is correct: K_θ is a genuine root of ĝ_B. The abstract three-zero bistable structure is valid for both systems, and all other vocabulary mappings (Stekly ↔ pump reserve, MPZ ↔ critical half-length, MQE ↔ threshold KCl, NZPV ↔ v_SD, MIITs ↔ depolarization duration) are between compatible mathematical types with correct dimensional reconciliations.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six listed vectors are independently demonstrated with equations and/or derivations in Section 3: V1 (shared operator, Bridge section), V2 (Maxwell equal-area with closed-form Silo A cold-end recovery and Silo B SD abort integral), V3 (unstable stationary nucleus with Wilson MPZ formula and quadrature for SD critical half-length), V4 (explicit Lyapunov functionals F_A, F_B with gradient flow structure and mountain-pass content integrals E_MQE, Q*), V5 (Stekly α_S and pump-reserve Π with unit threshold), V6 (MIITs quench integral and cumulative depolarization duration as path-independent state functions under flux factorization).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (superconductivity → SD) is genuinely asymmetric: the entry identifies a specific, narrow capability gap in SD research (no calibrated stimulus-energy threshold metrology, no E_MQE-equivalent energy–duration map, no protection-decision architecture with quantified false-positive budget) that superconductivity has developed over sixty years for the same operator class, while acknowledging SD's maturity in multi-ion biophysical modeling and PDE analysis. The falsifiable prediction is quantitatively specific: a logarithmic law L*(v_SD) = λ_tail ln(B/τc) predicting linearity of minimum initiation half-length against ln(1/v_SD) with R² ≥ 0.9, slope equal to independently measured λ_tail within 25%, beating a zero-slope null hypothesis, with explicit falsification conditions including non-logarithmic (e.g., power-law) dependence. Prior art advisory: the individual models are canonical in their fields and bistable RD reductions of SD have appeared in the computational neuroscience literature; the specific structural isomorphism with MQE/MIITS transfer should be verified at Stage 3.

#### Stage 3 Watch Items
- The cross-domain pairing should be checked for prior publication; the Grafstein–Tuckwell–Miura SD model, the Wilson/Stekly quench framework, and bistable reaction-diffusion models of SD are individually well-established.
- The falsifiable prediction (logarithmic law for critical nucleus half-length) should be checked against existing SD initiation threshold data and the front-interaction literature for bistable RD systems.
- The V5 qualitative claim distinguishing Silo A ("position") from Silo B ("existence") at the unit threshold should be verified against standard Stekly-parameter presentations.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the Wilson normal-zone equation and the Grafstein–Tuckwell–Miura extracellular-potassium equation are correctly nondimensionalized into the same bistable semilinear parabolic operator class.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mapped pairs are of compatible mathematical types and are tied together by explicit structural identifications rather than hedged assertions.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six listed correspondence vectors (V1 through V6) are explicitly derived and demonstrated with equations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is strictly asymmetric (focusing on the metrology and protection-decision stack absent in SD), and the falsifiable prediction provides specific regression criteria, thresholds, and explicit falsification conditions.

#### Stage 3 Watch Items
- Verify the novelty of the specific domain pairing (magnet quench protection ↔ cortical spreading depolarization). While the interdisciplinary transfer of metrology is novel, the shared mathematical structure (bistable semilinear parabolic reaction-diffusion equations, Maxwell equal-area, mountain-pass) is a canonical framework in mathematical physics and biology.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The Silo A source does not have the claimed unstable root at $\theta_A$: the displayed piecewise $\varphi_A$ gives $\hat g_A(\theta_A)=\alpha_S\varphi_A(\theta_A)-\theta_A=-\theta_A$, contradicting the later shared-operator assertion $\hat g(\theta)=0$.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping **“Current-sharing temperature $T_{cs}$ ↔ SD initiation threshold $[\mathrm{K^+}]_{e,\theta}$”** is explicitly assigned the role of an interior unstable zero, but the Silo A equation makes $T_{cs}$ merely the onset point of the piecewise Joule-generation term, not an equilibrium/unstable zero of $\hat g_A$.
* **CHECK 3 (Correspondence Vector Support):** PASS — The six listed vectors are each addressed in Sections 2–3 and supported by equations or derivations: the normalized parabolic form (V1), Maxwell stall condition (V2), stationary-nucleus first integral (V3), Lyapunov functional (V4), generation/clearance ratio (V5), and diffusion-free integral (V6).
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction is explicitly argued as asymmetric, and the prediction supplies measurable variables, a quantitative logarithmic slope, an $R^2$ threshold, a fourfold-speed test, and explicit falsification criteria. No prior-art determination is made at Stage 2.

#### Stage 3 Watch Items
* Probe the Section 1 assertion that the identification is “exact” and “coincide[s] term by term” despite the entry itself stating that the two constitutive shapes of $\hat g$ differ.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B are reduced to the same semilinear bistable parabolic form \(\tau\partial_t u=\lambda^{2}\partial_x^{2}u+\hat g(u)\) with \(\hat g(0)=0,\ \hat g'(0)=-1\); the Wilson normal-zone PDE and the Grafstein–Tuckwell–Miura potassium PDE are correctly cast as parabolic reaction–diffusion problems and the operator classes match.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token in Section 2 maps objects of the same mathematical type (scalar thresholds, dimensionless ratios, length scales, extensive nucleus content, eigenvalue front speed, path-independent integrals); the Operator Role entries specify shared mathematical structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — Every vector listed in `triple_correspondence_vectors` is demonstrated in the body: V1 (shared operator) in Bridge (V1); V2 (Maxwell equal-area) in V2 with closed-form evaluations for both silos; V3 (unstable stationary nucleus and first integral) in V3 with MPZ and \(\ell^{*}\) expressions; V4 (L² gradient flow, Lyapunov, mountain-pass content) in V4 with explicit functionals and MQE/Q* integrals; V5 (generation/clearance unit threshold) in V5; V6 (diffusion-free core dose integral) in V6. Each listed correspondence is supported by an equation, operator identity, or derivation.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric (superconductivity offers calibrated metrology and instrumented decision stacks not present in SD practice), and the proposal names concrete, measurable outcomes (an energy–duration MQE-style calibration map and a tissue-calibrated \(\Gamma_B\) converting depolarization duration to peak excursion), which are falsifiable by experiment or protocol development; prior-art analogies (Nagumo reductions, Grafstein–Tuckwell, Wilson MPZ theory) are present as background but do not invalidate the internal mathematical claims.

#### Stage 3 Watch Items
- Verify prior-art overlap with classical Nagumo / Grafstein reductions and Wilson MPZ/MQE literature (look for canonical mappings and earlier explicit reductions).
- Check empirical feasibility and existing experimental protocols in SD literature for constructing an energy–duration (E_{MQE}-equivalent) calibration and a tissue-calibrated \(\Gamma_B\) mapping.
- Confirm assumptions behind the flux-factorization in V6 for realistic pump dynamics (the entry notes failure where ATP availability \(m\) depends on \(K\)).
- Inspect the step-source and adiabatic idealizations used in Silo A closed-form derivations for applicability to modern composite conductor geometries and nonuniform \(J_m(T)\).

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both systems reduce to the identical semilinear bistable parabolic operator after the stated affine nondimensionalizations; the displayed Wilson and Grafstein–Tuckwell–Miura equations are of matching class and support the claimed structural correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type and the Operator Role statements identify shared zeros, first integrals, mountain-pass content or unit-threshold ratios rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six listed vectors are demonstrated by explicit operator reduction (V1), traveling-wave solvability and Maxwell condition (V2), first-integral nucleus (V3), Lyapunov functional and mountain-pass content (V4), unit-threshold capacity ratio (V5), and path-independent core integrals under flux factorization (V6).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric toward the instrumented metrology gap in SD; the prediction supplies a concrete linear relation L*(v_SD) versus ln(1/v_SD) with quantitative slope and R^{2} criteria that can be falsified by experiment.

#### Stage 3 Watch Items
- Constitutive source forms differ (piecewise-quadratic vs Hill) and are explicitly excluded from the claimed identity; confirm that the operator-level claims do not silently rely on source-shape identity.
- V6 dose-integral correspondence holds only under flux factorization and fails when m depends on K; verify that this limitation is respected in any transfer of the MIITs concept.
- Single-field reduction freezes slow variables (ATP, [Na+]i, glutamate, swelling); probe whether the bistable operator remains predictive once those variables are restored.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A Wilson equation `C ∂_t T = k ∂_x^2 T + G(T;I) - hP/A(T-T_op)` and Silo B Tuckwell-Miura `∂_t K = D_K* ∂_x^2 K + 1/α[J_rel-J_pump]` reduce after stated affine rescalings to the same semilinear bistable parabolic operator `τ ∂_t u = λ^2 ∂_x^2 u + ĝ(u)` with `ĝ(0)=0, ĝ'(0)=-1`; both parabolic, no class mismatch, and together support the Section 1 operator identity.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All seven mappings pair compatible mathematical types: scalar unstable zeros (T_cs ↔ [K+]_θ), dimensionless capacity ratios (α_S ↔ Π), lengths (ℓ_Mpz ↔ ℓ*), extensive contents with explicit conjugate-density reconciliation C(T-Top) ↔ α(K-Krest) and shared dimensionless invariant (E_MQE ↔ Q*), codimension-one Maxwell surfaces (I_p ↔ abort threshold), front eigenvalues (NZPV ↔ v_SD), and dose integrals normalized to seconds (MIITs ↔ depolarization duration); each Operator Role names shared structure (common zero, equal-area integral, first integral, Lyapunov functional).
- **CHECK 3 (Correspondence Vector Support):** PASS — All six vectors listed in YAML are demonstrated in body: shared_bistable_parabolic_operator_with_unit_restoring_slope_after_affine_nondimensionalization in Bridge V1, maxwell_equal_area_stall_condition_minimum_propagating_current_vs_sd_abort_threshold in V2 with solvability `τc∫U'^2 = ∫_0^{u+}ĝ du` and closed forms for both silos, unstable_stationary_nucleus_first_integral_mpz_vs_critical_initiation_half_length in V3 via `λ^2/2 U'^2 + Ĝ(U)=0`, shared_L2_gradient_flow_lyapunov_functional_and_mountain_pass_content_mqe_vs_threshold_kcl_moles in V4 via F_A and F_B gradient flows, generation_to_clearance_capacity_ratio_with_unit_threshold_stekly_number_vs_pump_reserve in V5 via `Π=(j0+jr)/jp>1`, diffusion_free_core_path_independent_dose_integral_miits_vs_depolarization_duration in V6 via `Γ_A=∫(Jm/Jop)^2 dt` and `Γ_B=∫m(t)dt`.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: source provides 60-year instrumented MPZ/MQE metrology, heater-pulse energy-duration map, Stekly/cold-end-recovery design rules, MIITs limit, and voltage-plus-validation-window detection with false-trigger budget, while target lacks calibrated energy-duration threshold and is mature elsewhere (multi-ion models, bifurcation analysis, COSBID ECoG), not backwards. Falsifiability is quantitative: prediction that L* regressed on ln(1/v_SD) is linear with R^2≥0.9 and slope within 25% of independently measured λ_tail, ΔL*=λ_tail ln4=0.28–0.83 mm for 4-fold speed reduction, and conditional cubic corollary θ=1/2 → 29–31 mM abort, with explicit falsification if slope≈0 or non-logarithmic. No canonical textbook pairing recognized for this specific domain pair.

#### Stage 3 Watch Items
- Generic bistable RD framework is textbook (Nagumo/Allen-Cahn); verify via bibliometric search that detailed MPZ/MQE/MIITs ↔ critical KCl volume / depolarization duration mapping has not been published.
- Probe entry's stated primary failure risk: source_term_nonautonomy — Silo B source depends on slow variables (ATP availability, [Na+]_i, glutamate, cell swelling) frozen in single-field reduction; test whether single-field reduction remains valid over the 4-fold v_SD grading needed for log law.
- Verify V6 flux-factorization condition holds for experimental conditions proposed (pump-limited factorization α dK/dt = -m(t) J_pump(K)).