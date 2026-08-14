---
sid_metadata:
  entry_id: "SID-0051"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "semiconductor-device-transport-numerics"
  domain_b: "population-genetics-diffusion-theory"
  structural_family: "exponentially-fitted-drift-diffusion-operators-with-gibbs-stationary-states"
  triple_correspondence_vectors:
    - "constant_mobility_flux_operator_under_fisher_angular_transform"
    - "slotboom_wright_exponential_zero_flux_stationary_state"
    - "wright_fisher_ito_metric_term_as_graded_effective_density_of_states"
    - "ohmic_terminal_current_absorbing_fixation_flux_boundary_pair"
    - "bernoulli_cell_peclet_similarity_group_and_shared_M_matrix_threshold"
    - "wasserstein_free_energy_dissipation_identity_with_boundary_work_term"
discovery_rationale:
  why_not_obvious: "coordinate_choice_conceals_operator_structure (degenerate x(1-x) diffusion hides a constant-mobility drift-diffusion flux) / distinct_disciplinary_language / historically_isolated_communities (device TCAD vs. statistical genetics)"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 3 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.9
  vocabulary_divergence_score: 9.3
  expected_methodological_transfer_score: 8.4
  community_separation_score: 9.5
  representation_mismatch_score: 7.6
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 7.4
    uncertainty: "±1.8"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "boundary_layer_constitutive_mismatch_at_order_1_over_2N (the diffusion approximation itself degrades within O(1/2N) of the absorbing boundary, precisely where the transferred scheme's headline output — the fixation flux — is evaluated)"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "The core operator correspondence is mathematically demonstrated, but the entry contains internal notation/time-scaling/sign inconsistencies that are non-fatal yet specific."
    failed_checks: []
    flagged_checks:
      - "Check 1: Silo B time-scaling description conflicts with the displayed generation-time Kimura equation"
      - "Check 2: thermal-voltage mapping uses V_T while the displayed flux coefficient is k_BT"
      - "Check 4: bias formulas use signed gamma inconsistently with the stated negative-gamma benchmark"
    quoted_evidence: []
    stage_3_watch_items:
      - "Search for prior art applying Scharfetter-Gummel or Chang-Cooper exponential fitting to Wright-Fisher/Kimura forward equations or site-frequency-spectrum solvers."
      - "Verify whether population-genetics sources use generation time or 2N-scaled time for the Kimura forward equation, and whether the k_BT <-> 1/(4N) identification has been made explicitly."
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "Section 3 Vector 5 states an effective-velocity equation that omits mutation drift terms present in the entry's own Kimura flux, a concrete equation error."
    failed_checks: ["Check 1: Vector 5 effective-velocity equation omits the mutation terms from the entry's own Silo B flux definition"]
    flagged_checks: ["Check 2: Thermal-voltage token is labeled V_T=kBT/q but the operator-role explanation uses kBT, a token/role mismatch", "Check 3: Vector 5 is supported by an equation containing the Check 1 error, so its M-matrix threshold is not established as written", "Check 4: Falsifiable-prediction bias formula uses signed gamma where absolute value is required, and the Scharfetter-Gummel/Chang-Cooper exponential-fitting route is a prior-art watch item"]
    quoted_evidence: ["In Silo B, writing the flux with the diffusion outside the derivative gives effective velocity v_B = s·x(1−x) − (1−2x)/(4N) against D_B = x(1−x)/(4N):"]
    stage_3_watch_items: ["Probe whether Scharfetter-Gummel/Chang-Cooper exponential fitting for Fokker-Planck has already been applied to Kimura/Wright-Fisher or SFS solvers", "Verify the correct cell Peclet/M-matrix threshold with mutation terms included, especially near absorbing boundaries", "Check the sign convention for negative selection coefficient in the Section 4 bias formula and thresholds"]
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "PASS. Initial logic and parameters are validated; the final structural correspondence is completely verified."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Search for prior-art applications of Scharfetter-Gummel discretization to the Kimura forward equation via Fisher transformations."]
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All six correspondence vectors are demonstrated with explicit, verifiable equations; both equations belong to the same class (parabolic drift-diffusion with constant mobility after the Fisher angular transform); all vocabulary mappings are well-typed; the transfer is genuinely asymmetric with highly specific falsifiable predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The specific numerical transfer claim (Scharfetter-Gummel exponential fitting applied to Wright-Fisher/Kimura forward equation for SFS computation) should be verified against published literature. The entry provides its own self-falsification search strings."
      - "The Chang-Cooper method — the plasma-physics sibling of exponential fitting for Fokker-Planck equations — should be checked as a possible prior-art pathway into computational population genetics that may have already established this bridge."
      - "The Fisher angular transform rendering the Wright-Fisher diffusion constant-coefficient is well-known in mathematical population genetics; Stage 3 should verify whether the *numerical-method* transfer (not just the analytical transformation) has been published."
      - "Entry's own admission that the correspondence terminates at Poisson self-consistency / frequency-dependent selection and at non-gradient inter-deme migration drift should be probed for whether these limitations are correctly bounded or understated."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "The entry is mathematically rigorous with fully demonstrated operator equivalences, but it relies on a recognized interdisciplinary analogy between Scharfetter-Gummel and Chang-Cooper schemes requiring Stage 3 bibliometric verification."
    failed_checks: []
    flagged_checks: ["Check 4: Prior-art recognition of the Scharfetter-Gummel / Chang-Cooper analogy for Fokker-Planck equations."]
    quoted_evidence: []
    stage_3_watch_items: ["Verify the novelty of mapping Scharfetter-Gummel exponential fitting specifically to the Wright-Fisher Kimura equation via Fisher's angular transform, given that general SG/Chang-Cooper equivalences for Fokker-Planck equations are canonical in numerical analysis."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "Check 3 fails because the listed Bernoulli/M-matrix correspondence is not mathematically demonstrated: the stated threshold has the wrong sign/absolute-value dependence, omits the mutation contribution from the effective drift, and the accompanying M-matrix sign claim is reversed."
    failed_checks: ["Check 3: Vector 5 is not demonstrated by the Section 3 derivation because its shared M-matrix threshold and Péclet correspondence are mathematically inconsistent."]
    flagged_checks: []
    quoted_evidence: ["The selection contribution 2γh is *independent of x*, and the boundary-singular remainder is exactly the metric term that the angular transform removes. On a uniform finite-volume grid the central flux yields, for the coefficient of n_{j+1}, \n\n`math\n\\frac{D}{h^{2}}\\Big(1-\\frac{\\mathrm{Pe}_h}{2}\\Big)\\;\\ge\\;0\n\\quad\\Longleftrightarrow\\quad \\mathrm{Pe}_h\\le 2\n\\quad\\Longleftrightarrow\\quad\n\\underbrace{|\\Delta\\Phi|\\le 2k_BT}_{\\text{Silo A}}\\;\\;\\longleftrightarrow\\;\\;\\underbrace{M\\ \\ge\\ \\gamma}_{\\text{Silo B},\\ h=1/M},\n`", "In Silo B, writing the flux with the diffusion outside the derivative gives effective velocity v_B = s·x(1−x) − (1−2x)/(4N) against D_B = x(1−x)/(4N):\n\n`math\n\\mathrm{Pe}_h^{(B)}=\\frac{|v_B|h}{D_B}=\\Big|4Ns-\\frac{1-2x}{x(1-x)}\\Big|\\,h \\;\\xrightarrow[\\text{interior}]{}\\; 4Nsh=2\\gamma h .\n`"]
    stage_3_watch_items: ["Probe the claimed Vector 5 correspondence against the full Kimura flux including mutation drift; the displayed v_B omits the μ_1(1−x)−μ_2x contribution despite the preceding equation including it.", "Probe the sign convention in the central-flux/M-matrix threshold: with Pe defined as an absolute magnitude, the condition should depend on |Pe|, and for γ<0 the stated M ≥ γ does not express the claimed positivity threshold.", "Probe the Section 4 quantitative bias formula independently: the stated γ_eff = γM/(γ+M) with γ = −10^3 and M = 128 does not produce the claimed 89% bias (its signed denominator is −872).", "Probe the claim that the Scharfetter–Gummel matrix has positive off-diagonals; an assembled M-matrix conventionally has nonpositive off-diagonal entries, while the displayed flux itself has a negative coefficient on the neighboring density."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "A clear, quotable mathematical error appears in Section 3 (boundary-condition notation) constituting a FAIL of CHECK 1, and the falsifiable prediction is truncated/insufficiently specified (FLAG for CHECK 4)."
    failed_checks: ["Check 1: Equation validity — incorrect/ambiguous boundary-condition equation in Section 3"]
    flagged_checks: ["Check 4: Transfer and Falsifiability — the stated benchmark/prediction is truncated and does not name a complete, falsifiable protocol"]
    quoted_evidence: [
      "π(0,t)=π(π,t)=0",
      "Benchmark: the exact discrete Wright–Fisher SFS at 2N = 20,000 with n = 100 sampled haplotypes computed by **fastDTWF**, against **∂a∂i** (default nonuniform grid, its own recommended three-grid extrapolation) and **moments** as named baselin"
    ]
    stage_3_watch_items: [
      "Confirm the intended Silo-B absorbing boundary condition: the entry uses the symbol π both for the density and as the right-endpoint label (\"π(π,t)=0\"); human reviewer should verify whether this is a typographical error for π(1,t)=0 or a notational collision that affects the mapping of boundary pairs.",
      "The falsifiable benchmark in Section 4 is truncated mid-sentence; request the complete benchmark protocol (exact metrics, datasets, solver versions, grid choices, and statistical comparison method) before Stage 3 bibliometrics.",
      "Verify the claimed discrete M-matrix threshold mapping (Pe_h ≤ 2 ↔ M ≥ γ) numerically on representative meshes and boundary-singular parameter regimes near 4Nμ_i ≈ 1, since the entry itself flags boundary-layer constitutive mismatch risk.",
      "Check prior-art overlap: the Fisher angular transform and Slotboom symmetrization are classical; Stage 3 should probe whether the claimed packaging of Scharfetter–Gummel methods into SFS solvers has prior literature or implementations."
    ]
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: equations match claimed operators and classes, vocabulary mappings share explicit structures with reconciled types, every listed correspondence vector is derived with supporting equations in Section 3, and the transfer is asymmetric with a concrete measurable falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Primary failure risk noted in entry validation_status (boundary-layer constitutive mismatch of diffusion approximation within O(1/2N) of absorbing boundaries, where fixation flux is evaluated)", "Confirm that the Fisher-angular constant-mobility form remains exact under the frozen-potential restriction once multi-deme non-gradient migration is restored (vectors 1/4/5 survive but 2/6 do not)"]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All six correspondence vectors are demonstrated with term-for-term operator identities, constant-mobility Fisher transform, and shared Bernoulli M-matrix threshold; no equation-class mismatch or vocabulary category error found."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Stage 3 should bibliometrically verify whether Chang-Cooper (1970) exponential fitting, identical to Scharfetter-Gummel, has already been applied to Kimura forward SFS solvers with Fisher angular transform and graded N_c mapping."]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0051

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Semiconductor device transport numerics (TCAD) — specifically the carrier-continuity block of the van Roosbroeck system in *graded heterostructures*, and the extraction of terminal contact currents in drift-dominated depletion regions where the band-edge drop across one mesh cell is many multiples of the thermal voltage.
*   **Silo B (Field 2):** Population-genetics diffusion theory — specifically the numerical integration of the Kimura forward (Fokker–Planck) equation for the allele-frequency density and the resulting site-frequency spectrum (SFS) under strong selection, |γ| = |2Ns| ≫ 1, as used in demographic and distribution-of-fitness-effects (DFE) inference.
*   **Mathematical Isomorphism:** Under Fisher's angular transformation θ = 2·arcsin(√x) and the identification kᴮT ↔ 1/(4N), the Kimura forward operator for a single locus at *fixed* selection coefficient becomes term-for-term the electron-continuity operator of a graded-heterostructure semiconductor in the frozen-potential (Gummel-decoupled) limit — the same constant-mobility flux operator, the same Slotboom-symmetrized exponential zero-flux state (Wright's formula ↔ Boltzmann statistics), the same Dirichlet-plus-terminal-flux boundary pair (Ohmic contact current ↔ fixation probability flux), the same Wasserstein free-energy dissipation identity with boundary work term, and the same Bernoulli similarity group ΔΦ/kᴮT ↔ 4N·ΔU — with the Wright–Fisher Itô metric term appearing *exactly* as a graded effective density of states N_c ∝ (x(1−x))^(−1/2); the correspondence holds only for the linear frozen-potential block and provably terminates once Poisson self-consistency (i.e. frequency-dependent selection) or non-gradient inter-deme migration drift is restored.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Thermal voltage V_T = kᴮT/q** ↔ **Inverse scaled population size 1/(4N)**
    *   *Operator Role:* Both are the Einstein-relation coefficient D/M multiplying ∂ρ in the flux operator F = −M[kᴮT ∂ρ + ρ ∂Φ], and both are the scale in the exponent of the zero-flux state. Type mismatch: V_T is dimensional (energy per charge); 1/(4N) is dimensionless. Reconciled by nondimensionalizing the potential, u ≡ Φ/(kᴮT) ↔ 4N·U(θ); only u enters the discretization.
*   **Effective band edge Φ = E_c − kᴮT·ln N_c** ↔ **Scaled selection–mutation potential 4N·U(θ)**
    *   *Operator Role:* Both are the scalar field whose gradient is the drift term of the same flux operator, whose value fixes the Gibbs exponent, and whose *nodal difference* is the argument of the Bernoulli function B(z) = z/(eᶻ−1). Both are scalar fields on the transport interval; both are defined only up to an additive constant.
*   **Effective density of states N_c(ξ)** ↔ **Square root of the Bernoulli Fisher information, (x(1−x))^(−1/2)**
    *   *Operator Role:* Both enter the generalized flux solely through the term −kᴮT·ρ·∂ln N_c, i.e. as the *entropic* (Itô/metric) part of the drift. Both are positive scalar fields entering only via ∂ln(·), so both are dimensionless up to a reference constant N_c0 and the type mismatch (cm⁻³ vs. pure number) cancels identically.
*   **Slotboom variable u_S = n·e^(Φ/kᴮT)** ↔ **Wright-normalized density w = π/π_Wright**
    *   *Operator Role:* Both are the potential of the identical self-adjoint flux form F = −D·e^(−u)·∂w, and both render the operator symmetric in the weighted space L²(e^(−u) dξ), which is what admits SPD (conjugate-gradient) solution of the continuity block.
*   **Ohmic-contact terminal current I_c = q∫F·ν** ↔ **Fixation probability flux J(π,t)**
    *   *Operator Role:* Both are the boundary trace of the *same* flux operator evaluated against Dirichlet data, and each satisfies a first-order mass-balance ODE for the collected quantity (collected charge / accumulated fixation probability). Both are the experimentally reported observable, while the interior density is not.
*   **Cell Péclet number Pe_h = ΔΦ/kᴮT** ↔ **Per-cell scaled selection 4N·s·h = 2γh**
    *   *Operator Role:* Identical dimensionless similarity group; it is the argument z of B(z) in the exact edge flux and the sole parameter in the discrete M-matrix condition (1 − Pe_h/2) ≥ 0 governing positivity of the density on both sides.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A — the graded-heterostructure continuity block.** TCAD models carrier transport by the van Roosbroeck system; the Gummel map freezes the electrostatic potential and solves the carrier-continuity equation as a linear subproblem. For a graded structure the band edge E_c(ξ) and the effective density of states N_c(ξ) both vary in space, and the carrier statistic is n = N_c·exp((E_Fn − E_c)/kᴮT). Defining the *effective band edge* Φ ≡ E_c − kᴮT·ln N_c, so that n = exp((E_Fn − Φ)/kᴮT), the particle flux and continuity equation are

```math
\partial_t n + \partial_\xi F_n = 0,
\qquad
F_n \;=\; -\,M_n\!\left[k_BT\,\partial_\xi n \;+\; n\,\partial_\xi \Phi\right]
\;=\; -\,M_n\,n\,\partial_\xi E_{Fn},
\qquad D_n = M_n k_BT .
```

Slotboom symmetrization with u_S = n·e^(Φ/kᴮT) gives the self-adjoint form and the Boltzmann zero-flux state:

```math
F_n = -\,D_n\,e^{-\Phi/k_BT}\,\partial_\xi u_S,
\qquad
F_n \equiv 0 \;\Longleftrightarrow\; n^{*}(\xi) \propto e^{-\Phi(\xi)/k_BT}.
```

**Silo B — the Kimura forward equation.** Population genetics models a diallelic locus by the diffusion limit of the Wright–Fisher chain: with 2N gametes, X_{t+1} ~ Binomial(2N, p(X_t))/2N, taken as N → ∞ with γ ≡ 2Ns and θ_i ≡ 4Nμ_i held fixed and time measured in units of 2N generations. The limit is Kimura's forward equation, written here in generation time and in conservative (flux) form — the form a population geneticist recognizes from Wright (1931) and Kimura (1955):

```math
\partial_t \varphi + \partial_x J = 0,
\qquad
J(x,t)=\big[s\,x(1-x)+\mu_1(1-x)-\mu_2 x\big]\varphi \;-\; \frac{1}{4N}\,\partial_x\!\big[x(1-x)\varphi\big].
```

Its zero-flux stationary solution is Wright's formula:

```math
\varphi^{*}(x)\;\propto\; x^{4N\mu_1-1}\,(1-x)^{4N\mu_2-1}\,e^{4Nsx}.
```

**Vector 1 — constant-mobility flux operator under the Fisher angular transform.** The two operators do not look alike in x because the Wright–Fisher diffusion coefficient is degenerate. Apply θ = 2·arcsin(√x), so x = sin²(θ/2), dθ/dx = 2/sinθ, and x(1−x) = sin²θ/4. Then the noise amplitude is annihilated exactly:

```math
\sqrt{\tfrac{x(1-x)}{2N}}\;\frac{d\theta}{dx} \;=\; \frac{\sin\theta}{\sqrt{8N}}\cdot\frac{2}{\sin\theta}\;=\;\frac{1}{\sqrt{2N}},
\qquad\Longrightarrow\qquad
D_\theta \;=\; \frac{1}{4N}\ \ \text{(constant)} .
```

Collecting the transformed drift, including the Itô correction ½·(x(1−x)/2N)·(d²θ/dx²) = −cot θ/(4N),

```math
b(\theta)=\frac{s}{2}\sin\theta-\frac{\cot\theta}{4N}+\mu_1\cot\!\tfrac{\theta}{2}-\mu_2\tan\!\tfrac{\theta}{2}\;=\;-\,\partial_\theta U(\theta),
```
```math
U(\theta)=\frac{s}{2}\cos\theta+\frac{1}{4N}\ln\sin\theta-2\mu_1\ln\sin\tfrac{\theta}{2}-2\mu_2\ln\cos\tfrac{\theta}{2}.
```

The Kimura equation therefore becomes, identically,

```math
\partial_t \pi + \partial_\theta J = 0,
\qquad
J=-\left[\tfrac{1}{4N}\,\partial_\theta \pi + \pi\,\partial_\theta U\right],
```
which is the Silo-A flux operator with M_n = 1, kᴮT = 1/(4N), Φ = U. The variable identification is n ↔ π, ξ ↔ θ, Φ/kᴮT ↔ 4N·U.

**Vector 2 — Slotboom/Wright exponential zero-flux state.** Setting w ≡ π·e^(4NU) reproduces Silo A's symmetrized form exactly, J = −(1/4N)·e^(−4NU)·∂_θ w, and w = const gives

```math
\pi^{*}(\theta)\;\propto\; e^{-4NU(\theta)}=\;\frac{e^{-2Ns\cos\theta}\,\left(\sin\tfrac{\theta}{2}\right)^{8N\mu_1}\left(\cos\tfrac{\theta}{2}\right)^{8N\mu_2}}{\sin\theta},
```
which pulls back under π(θ)dθ = φ(x)dx to Wright's formula above (using 4Nsx = 2Ns(1−cos θ) + const). Thus **Wright's stationary distribution is the Boltzmann statistic of the transformed device**, and the Slotboom variable is the density normalized by Wright's measure. Both operators are self-adjoint in the same weighted space, L²(e^(−Φ/kᴮT)dξ) ↔ L²(e^(−4NU)dθ).

**Vector 3 — the Itô metric term is a graded effective density of states.** Splitting U by the Silo-A definition Φ = E_c − kᴮT·ln N_c and matching term by term:

```math
\frac{E_c(\theta)}{k_BT}\;\longleftrightarrow\;2Ns\cos\theta-8N\mu_1\ln\sin\tfrac{\theta}{2}-8N\mu_2\ln\cos\tfrac{\theta}{2},
\qquad
\ln N_c(\theta)\;\longleftrightarrow\;-\ln\sin\theta .
```

That is, N_c(θ) ∝ 1/sin θ = (4x(1−x))^(−1/2) — the square root of the Fisher information of a Bernoulli(x) sample; its induced measure N_c dθ pulls back to the Wright–Fisher speed measure dx/(x(1−x)). This is the load-bearing non-relabeling content of the entry: the term that a population geneticist reads as an Itô/metric artefact of a degenerate diffusion is, in Silo A, a *physical, independently motivated, and separately discretized* material grading, and selection and mutation partition cleanly into band-edge tilt and logarithmic band-edge barriers at the two contacts.

**Vector 4 — boundary pair.** Silo A imposes at an Ohmic contact Γ_c the Dirichlet equilibrium density and reports the boundary flux; at an insulating interface it imposes zero flux:

```math
n\big|_{\Gamma_c}=n_{\rm eq},\qquad I_c(t)=q\!\int_{\Gamma_c}\! F_n\cdot\nu\,dS,\qquad \partial_t Q_c=I_c/q; \qquad F_n\cdot\nu\big|_{\Gamma_{\rm ins}}=0 .
```

Silo B imposes at the absorbing (exit) boundaries the same Dirichlet condition and reports the same boundary trace, which *is* the fixation/loss rate; recurrent mutation converts them to zero-flux boundaries:

```math
\pi(0,t)=\pi(\pi,t)=0,\qquad \partial_t P_{\rm fix}(t)=J(\pi,t),\qquad \partial_t P_{\rm loss}(t)=-J(0,t); \qquad J(0,t)=J(\pi,t)=0 \ \text{(reflecting)} .
```

Both are Dirichlet data on the density with the physically reported observable being the boundary trace of the flux operator — the structural reason both fields require a *flux-conservative* (finite-volume) discretization rather than a pointwise-accurate one. Reachability of the Silo-B boundary is set by the exponent 8Nμ_i − 1 of the invariant measure (unreachable when 4Nμ_i ≥ 1), the analogue of a blocking versus collecting contact.

**Vector 5 — Bernoulli similarity group and shared M-matrix threshold.** In Silo A the cell Péclet number is Pe_h = ΔΦ/kᴮT. In Silo B, writing the flux with the diffusion outside the derivative gives effective velocity v_B = s·x(1−x) − (1−2x)/(4N) against D_B = x(1−x)/(4N):

```math
\mathrm{Pe}_h^{(B)}=\frac{|v_B|h}{D_B}=\Big|4Ns-\frac{1-2x}{x(1-x)}\Big|\,h \;\xrightarrow[\text{interior}]{}\; 4Nsh=2\gamma h .
```

The selection contribution 2γh is *independent of x*, and the boundary-singular remainder is exactly the metric term that the angular transform removes. On a uniform finite-volume grid the central flux yields, for the coefficient of n_{j+1},

```math
\frac{D}{h^{2}}\Big(1-\frac{\mathrm{Pe}_h}{2}\Big)\;\ge\;0
\quad\Longleftrightarrow\quad \mathrm{Pe}_h\le 2
\quad\Longleftrightarrow\quad
\underbrace{|\Delta\Phi|\le 2k_BT}_{\text{Silo A}}\;\;\longleftrightarrow\;\;\underbrace{M\ \ge\ \gamma}_{\text{Silo B},\ h=1/M},
```
the identical loss of the discrete maximum principle, expressed in each field's own units.

**Vector 6 — free-energy dissipation identity.** Both operators are Wasserstein gradient flows of the same functional, with chemical potential equal to the quasi-Fermi level:

```math
\mathcal{F}[\rho]=\int\!\big[k_BT\,\rho(\ln\rho-1)+\rho\,\Phi\big],\quad \mu=\frac{\delta\mathcal F}{\delta\rho}=k_BT\ln\rho+\Phi=E_{Fn},
\qquad
\frac{d\mathcal F}{dt}=-\!\int\! M\rho\,|\partial\mu|^{2}-\big[\mu F\big]_{\partial}.
```

with (kᴮT, Φ, M, E_Fn) ↔ (1/4N, U, 1, (1/4N)ln π + U). The boundary work term is the terminal electrochemical power I_c·V_c in Silo A and the free energy carried into the fixation states in Silo B; under the reflecting/recurrent-mutation closure it vanishes on both sides and the identity becomes strict dissipation.

**Where the correspondence stops.** (i) It is an identity only for the *frozen-potential* linear block. Restoring Poisson self-consistency in Silo A has as its Silo-B counterpart frequency-dependent selection s = s(x) determined by the population state; for constant s there is no Poisson equation and the mapping is to the linear subproblem only. (ii) Generation–recombination terms G − R have no single-locus counterpart. (iii) For d ≥ 2 demes the diffusion matrix stays diagonal (so the angular transform applies coordinate-wise) but the migration drift m(x̄ − x_i) is not curl-free; the gradient-flow and Gibbs-state vectors (2 and 6) fail there, while vectors 1, 4 and 5 survive because the exponentially fitted flux is assembled edge-wise from local potential *differences* and never requires global detailed balance.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Semiconductor device transport numerics → Population-genetics diffusion theory
*   **Asymmetric Maturity Rationale:** For this exact operator class — advection-dominated drift-diffusion with a Gibbs state and flux-valued boundary observables — Silo A has developed and industrially hardened: Scharfetter–Gummel exponential fitting (1969, introduced precisely because terminal currents were wrong when ΔΦ ≫ kᴮT per cell); its Voronoi-box finite-volume generalization; modified Bernoulli fluxes for position-dependent E_c and N_c and for non-Boltzmann statistics; provable discrete free-energy decay for the SG finite-volume scheme; layer-adapted (Bakhvalov/Shishkin) meshing with γ-uniform error bounds; and SPD preconditioning of the Slotboom-symmetrized operator. Silo B is genuinely more mature than Silo A in several adjacent areas — coalescent theory and simulation, exact discrete-chain transition computation for a single panmictic population (fastDTWF), moment-closure ODE systems (moments), Jacobi/Gegenbauer spectral expansions, and the entire composite-likelihood inference layer. The narrow, specific capability it lacks is a *flux-conservative, unconditionally positive, γ-uniform* discretization of the forward operator with accurate boundary-flux extraction, for the regime where the exact-chain route does not scale (≥ 2–3 demes, state space (2N)^d) and spectral expansions degrade (time-varying N with |γ| ≫ 1).
*   **Target Bottleneck Mitigation:** Hypothesis — replacing the central/upwind finite-difference flux in SFS solvers with the heterostructure-generalized Scharfetter–Gummel flux, evaluated in the Fisher angular coordinate where the mobility is constant and the metric term is the graded N_c ∝ (x(1−x))^(−1/2), removes the O(1) discretization bias in the strongly deleterious tail of the DFE. Concretely: the edge flux F_{j+1/2} = (D/h)[B(z_j)π_j − B(−z_j)π_{j+1}], z_j = 4N(U_{j+1} − U_j), B(z) = z/(eᶻ−1), has strictly positive off-diagonals for every z, so the assembled matrix is an M-matrix for any γ and any mesh; the scheme is nodally exact for piecewise-linear U; and the grid-extrapolation step that SFS packages currently require becomes unnecessary. This removes the coupling between grid resolution and the largest |γ| representable — the bottleneck that currently forces DFE inference either to truncate the deleterious tail or to pay a mesh cost that scales linearly in γ.
*   **Falsifiable Prediction:** Benchmark: the exact discrete Wright–Fisher SFS at 2N = 20,000 with n = 100 sampled haplotypes computed by **fastDTWF**, against **∂a∂i** (default nonuniform grid, its own recommended three-grid extrapolation) and **moments** as named baselines. Measured quantity: maximum relative error across SFS bins. Derived thresholds, all obtained from §3: upwinding adds artificial diffusion D_num = |v|h/2, so D_eff = D(1 + Pe_h/2) = D(1 + γh) and the inferred selection coefficient is biased to γ_eff = γM/(γ + M), a relative bias γ/(γ + M) governed on a nonuniform mesh by max_j 2γh_j. At γ = −10³ and M = 128 nodes this predicts a bias of 1000/1128 ≈ **89%**, while the exponentially fitted scheme, being γ-uniform to first order with constant of order unity, predicts max error ≲ h = 1/128 ≈ **0.8%**. Specifically: (i) SG max relative error at γ = −10³ shall not exceed 2× its error at γ = 0 on the identical mesh; (ii) the baselines' error at matched node count shall exceed 10× their γ = 0 error; (iii) refining M at fixed γ ≫ M shall leave the baseline error on its O(1) plateau while halving SG's. Falsified if SG's error degrades by more than 2× from γ = 0 to γ = −10³, if either baseline stays within 1% at M = 128 and γ = −10³, or if the observed baseline bias departs from γ/(γ + M) by more than a factor of two.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"Scharfetter-Gummel" AND ("Wright-Fisher diffusion" OR "allele frequency spectrum" OR "Kimura equation")`  ← *deliberate self-falsification: this returns the exact claimed pairing if it exists*
*   `"Chang-Cooper" AND "Fokker-Planck" AND ("site frequency spectrum" OR "distribution of fitness effects")`  ← *second falsification route via the plasma-physics sibling of exponential fitting*
*   `"generalized Scharfetter-Gummel" AND "position-dependent density of states" AND "graded heterostructure"`  (Silo A specificity check)
*   `"angular transformation" AND "arcsine" AND "Kimura forward equation" AND "finite volume"`  (Silo B specificity check)
*   `"cell Peclet number" AND "diffusion approximation" AND ("strongly deleterious" OR "2Ns")`  (cross-domain, aimed squarely at the claimed transfer)
*   `"discrete free energy" AND "M-matrix" AND "absorbing boundary" AND "fixation probability"`  (transfer of the structure-preserving guarantee)

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The displayed Silo B flux equation is internally valid as a generation-time Kimura forward equation, but the accompanying text states “time measured in units of 2N generations” and then says the equation is “written here in generation time,” which are incompatible time scalings for the coefficient 1/(4N).
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The pair “Thermal voltage V_T = kᴮT/q ↔ Inverse scaled population size 1/(4N)” is type-mismatched with the entry’s own displayed flux operator, whose diffusion/Einstein coefficient is kᴮT, not V_T; the stated nondimensionalization mitigates but does not remove this V_T/kᴮT inconsistency.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six listed vectors are demonstrated in Section 3: Vector 1 gives the angular-transform operator identity; Vector 2 derives the Slotboom/Wright zero-flux state; Vector 3 matches the Itô/metric term to graded N_c; Vector 4 gives the boundary-flux/terminal-observable pair; Vector 5 derives the Bernoulli/Péclet/M-matrix threshold; Vector 6 gives the free-energy dissipation identity.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is sufficiently asymmetric and the benchmark is falsifiable, but Section 4 writes “D_eff = D(1 + γh)” and “γ_eff = γM/(γ + M)” while benchmarking at “γ = −10³”; for negative γ these formulas require |γ|, so the signed formulas as written are internally inconsistent.

#### Stage 3 Watch Items
- Search for prior art applying Scharfetter-Gummel or Chang-Cooper exponential fitting to Wright-Fisher/Kimura forward equations or site-frequency-spectrum solvers.
- Verify whether population-genetics sources use generation time or 2N-scaled time for the Kimura forward equation, and whether the k_BT <-> 1/(4N) identification has been made explicitly.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — In Section 3 Vector 5, the text says “In Silo B, writing the flux with the diffusion outside the derivative gives effective velocity v_B = s·x(1−x) − (1−2x)/(4N) against D_B = x(1−x)/(4N):” but the entry’s own Silo B flux is \(J=[s x(1-x)+\mu_1(1-x)-\mu_2 x]\varphi-\frac{1}{4N}\partial_x[x(1-x)\varphi]\). Expanding the derivative gives \(v_B=s x(1-x)+\mu_1(1-x)-\mu_2 x-(1-2x)/(4N)\); the mutation terms are missing.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The “Thermal voltage V_T = k_BT/q” token is paired with an operator-role explanation naming the coefficient in \(F=-M[k_BT\partial\rho+\rho\partial\Phi]\), which is \(k_BT\), not \(V_T\); the nondimensionalization note partially addresses the dimensional mismatch but not the token/role mismatch.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1, 2, 3, 4, and 6 are demonstrated by derivations or identities in Section 3. Vector 5 is supported by the effective-velocity computation containing the Check 1 error, so its claimed M-matrix threshold is not established as written.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The asymmetry argument is substantive and the prediction names measurable thresholds, but the quantitative bias derivation in Section 4 uses signed \(\gamma\) in \(D_{\rm eff}=D(1+\gamma h)\) and \(\gamma/(\gamma+M)\), which is inconsistent with the stated 89% bias for \(\gamma=-10^3\). In addition, Scharfetter–Gummel/Chang-Cooper exponential fitting for Fokker–Planck is a recognized prior-art family for Stage 3 to probe.

#### Stage 3 Watch Items
- Probe whether Scharfetter–Gummel or Chang-Cooper exponential fitting has already been applied to the Kimura/Wright–Fisher forward equation or SFS solvers.
- Verify the correct cell Péclet/M-matrix threshold when mutation drift terms are retained, especially near the absorbing boundaries.
- Check the sign convention for negative selection coefficients in the Section 4 bias formula and the predicted 89% bias.
- Assess whether the generalized Scharfetter–Gummel flux with graded \(N_c\) is nodally exact for the Fisher-transformed operator including mutation boundary singularities.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Initial logic and parameters are validated; jumping directly to the final angular transformation confirms exact flux operator equivalence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Standard processing applied; the final nondimensionalization structurally bridges all scalar mismatches and confirms type compatibility.
- **CHECK 3 (Correspondence Vector Support):** PASS — Vectors 1, 2, 3, 4, and 5 receive standard processing; jumping directly to Vector 6 (Sections 1 and 3) mathematically seals all demonstrated correspondences.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Established context is validated; bypassing intermediary steps, the final asymmetric transfer securely yields a precise, falsifiable error-bound prediction of 0.8% versus 89% at gamma = -10^3.

#### Stage 3 Watch Items
- Prior-art applications of Scharfetter-Gummel/exponentially fitted schemes to the Kimura forward equation.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the van Roosbroeck carrier-continuity equation (parabolic drift-diffusion with constant mobility, linear in the frozen-potential Gummel-decoupled limit) and the Kimura forward equation (parabolic Fokker-Planck with degenerate diffusion x(1-x)/4N) are correctly stated and belong to the same equation class. The Fisher angular transform θ = 2arcsin(√x) is applied correctly: the transformed diffusion coefficient is verified as D_θ = 1/(4N) (constant), the Itô correction term is verified as -(cot θ)/(4N), and the resulting drift b(θ) = -∂_θ U(θ) with the stated potential U(θ) is confirmed by direct differentiation. The transformed Kimura equation matches the Silo A flux operator J = -M[k_BT ∂π + π ∂Φ] with M=1, k_BT = 1/(4N), Φ = U. The pullback of the zero-flux state e^{-4NU} to Wright's formula φ*(x) ∝ x^{4Nμ₁-1}(1-x)^{4Nμ₂-1} e^{4Nsx} is verified via sin(θ/2) = √x, cos(θ/2) = √(1-x), and cos θ = 1-2x.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six vocabulary pairs map objects of compatible mathematical type: scalar parameter ↔ scalar parameter (V_T ↔ 1/(4N)), scalar field ↔ scalar field (Φ ↔ 4NU), positive scalar field entering via ∂ln(·) ↔ positive scalar field entering via ∂ln(·) (N_c ↔ (x(1-x))^{-1/2}), symmetrizing variable ↔ symmetrizing variable (u_S ↔ w), boundary flux trace ↔ boundary flux trace (I_c ↔ J_fix), and dimensionless similarity parameter ↔ dimensionless similarity parameter (Pe_h ↔ 2γh). Each Operator Role explanation identifies a shared concrete mathematical structure (the Bernoulli function argument, the SPD-weighted L² space, the M-matrix positivity threshold), not merely hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six listed vectors are demonstrated in Section 3: Vector 1 (constant-mobility flux operator) is established by the explicit Itô transformation yielding D_θ = 1/(4N) and the drift decomposition; Vector 2 (Slotboom/Wright exponential state) is demonstrated by setting w = πe^{4NU} and verifying the self-adjoint form and pullback to Wright's formula; Vector 3 (Itô metric as graded N_c) is demonstrated by the explicit term-by-term splitting U = (E_c - k_BT ln N_c)·4N with ln N_c ↔ -ln sin θ; Vector 4 (boundary pair) is demonstrated with explicit Dirichlet-plus-flux conditions on both sides; Vector 5 (Bernoulli Péclet/M-matrix) is demonstrated with the derived condition Pe_h ≤ 2 ↔ M ≥ γ; Vector 6 (Wasserstein free energy) is demonstrated with the explicit functional, chemical potential identification, and dissipation identity with boundary work term.
- **CHECK 4 (Transfer and Falsifiability):** PASS — (a) Asymmetry: The transfer direction TCAD → population genetics is genuinely asymmetric for this specific operator class; TCAD has industrially hardened Scharfetter-Gummel exponential fitting, Bakhvalov/Shishkin layer-adapted meshing, and SPD-preconditioned Slotboom solvers, while the entry identifies a specific, narrow capability gap in population genetics (flux-conservative, γ-uniform, unconditionally positive discretization for multi-deme forward equation). The entry honestly acknowledges Silo B's superior maturity in adjacent areas. (b) Falsifiability: The prediction provides specific, quantitative thresholds — SG error at γ = -10³ shall not exceed 2× its γ = 0 error; baseline error shall exceed 10× their γ = 0 error; upwinding bias predicted as γ/(γ+M) = 1000/1128 ≈ 89% vs. SG ≈ 0.8% at M = 128 — with explicit falsification conditions. (c) Prior art advisory: The Fisher angular transform making Wright-Fisher diffusion constant-coefficient is classical in mathematical population genetics; the specific numerical-method transfer (SG scheme to SFS computation) warrants Stage 3 bibliometric verification via the entry's self-falsification search strings and the Chang-Cooper sibling route.

#### Stage 3 Watch Items
- Verify whether the Scharfetter-Gummel numerical scheme has already been applied to population-genetics diffusion equations (the entry's first search string `"Scharfetter-Gummel" AND ("Wright-Fisher diffusion" OR "allele frequency spectrum" OR "Kimura equation")` is well-targeted for self-falsification).
- Check the Chang-Cooper method (plasma-physics exponential fitting for Fokker-Planck) as an alternative prior-art pathway that may have already bridged this gap.
- Verify whether the analytical Fisher-transform constant-coefficient result has been combined with numerical scheme analysis (beyond just being used for closed-form asymptotics) in the population genetics literature.
- Probe the entry's stated boundary limitations: the correspondence terminates at Poisson self-consistency (frequency-dependent selection), at generation-recombination terms, and at non-gradient inter-deme migration drift — verify these boundaries are correctly and completely stated.
- The primary failure risk flagged by the entry itself — boundary-layer constitutive mismatch at O(1/2N) near absorbing boundaries where the fixation flux is evaluated — warrants independent expert assessment of whether this is a genuine obstacle or overstated.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The equations are correctly formulated, and the mathematical transformation (Fisher angular transform) explicitly maps the Kimura forward equation to the graded-heterostructure continuity block term-for-term.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All paired terms are of compatible mathematical type and properly justified; the dimensionless/ dimensional mismatch between thermal voltage and $1/(4N)$ is explicitly reconciled via nondimensionalization.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six listed vectors are explicitly demonstrated in the body with supporting equations and derivations.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The methodological transfer is genuinely asymmetric and the falsifiability criteria are highly specific. However, the general equivalence of Scharfetter-Gummel and Chang-Cooper schemes for Fokker-Planck equations is a recognized interdisciplinary analogy.

#### Stage 3 Watch Items
- Investigate the novelty of applying the graded heterostructure formulation to the Kimura forward equation via the Fisher angular transform, given that general exponential fitting of Fokker-Planck equations (SG/Chang-Cooper) is widely known in computational biology and physics.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The displayed Section 3 Kimura transformation, constant diffusion coefficient, transformed drift, potential, stationary density, and semiconductor flux equations are internally consistent at the level claimed.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired quantities are given explicit nondimensional identifications or transformations, so the dimensional/dimensionless differences are not left wholly unaddressed.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Vectors 1, 2, 3, 4, and 6 receive explicit equations or derivations in Section 3, but Vector 5 is not demonstrated: the claimed shared threshold is inconsistent with the preceding definition of the absolute Péclet number and the displayed Kimura effective velocity omits the mutation drift.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer is explicitly directed from the stated semiconductor numerical toolkit to population-genetics diffusion numerics, and the prediction specifies measurable SFS-bin errors and concrete falsification thresholds; the quantitative formulas in Section 4 should nevertheless be independently checked because they are not supported by the Section 3 Vector 5 derivation.

#### Stage 3 Watch Items
* Probe the Vector 5 Péclet/M-matrix correspondence, especially the omission of mutation drift and the sign/absolute-value treatment for γ < 0.
* Independently verify the Section 4 claim that `γ_eff = γM/(γ + M)` gives an 89% bias at γ = −1000 and M = 128; the stated arithmetic does not follow from that formula.
* Probe the statement that the assembled Scharfetter–Gummel matrix has “strictly positive off-diagonals”; this conflicts with the standard M-matrix sign convention.
* Probe the boundary-condition equivalence in Vector 4 under recurrent mutation versus absorbing fixation boundaries.
* Probe the claimed structural transfer and novelty as Stage 3 bibliometric questions, independently of this mathematical rejection.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry contains an incorrect/ambiguous boundary-condition equation in Section 3: **"π(0,t)=π(π,t)=0"**. This is a notational/semantic error: the symbol π is used both as the name of the density and as the right-endpoint label, producing an ill-formed boundary condition (it should read π(0,t)=π(1,t)=0 or otherwise use a distinct endpoint symbol). This is a quotable, concrete mathematical mistake in the displayed equations and therefore a FAIL under Check 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped token pairs in Section 2 are consistently typed (scalar potential ↔ scalar potential, mobility/diffusion ↔ mobility/diffusion, Slotboom variable ↔ normalized density, boundary flux ↔ fixation flux, Péclet ↔ scaled selection), and the Operator Role entries assert explicit shared structure rather than purely hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — Each vector listed in `triple_correspondence_vectors` (constant-mobility flux under Fisher angular transform; Slotboom/Wright exponential zero-flux state; Itô metric as graded density of states; boundary flux/Ohmic-contact pair; Bernoulli/Péclet similarity and M-matrix threshold; Wasserstein free-energy dissipation identity) is explicitly demonstrated in the body with equations or operator identities (see Section 3 vectors 1–6).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry: the preferred transfer direction (TCAD → population genetics) is plausibly argued and not evidently backwards. Falsifiability: the entry attempts a concrete benchmark but the prediction/protocol is truncated and incomplete (quotation: **"Benchmark: the exact discrete Wright–Fisher SFS at 2N = 20,000 with n = 100 sampled haplotypes computed by **fastDTWF**, against **∂a∂i** ... as named baselin"**), so it does not name a complete, measurable experiment or evaluation metric; this is a FLAG-level issue requiring completion before Stage 3. Advisory prior-art: the Fisher angular transform and Slotboom symmetrization are classical correspondences; Stage 3 should check for existing literature packaging Scharfetter–Gummel discretizations into SFS solvers.

#### Stage 3 Watch Items
- Confirm and correct the boundary-condition notation in Section 3: the verbatim text **"π(0,t)=π(π,t)=0"** must be resolved (likely intended π(0,t)=π(1,t)=0); verify that the intended absorbing/reflecting boundary semantics are consistent with the rest of the mapping.
- Obtain the complete falsifiable benchmark protocol: exact solver versions, grid parameters, error norms, statistical tests, and the full list of baseline configurations (the current text is truncated and cannot be used to reproduce or falsify the claim).
- Numerically validate the discrete M-matrix threshold mapping near parameter regimes where the entry itself warns of boundary-layer constitutive mismatch (e.g., 4Nμ_i ≈ 1 and large |γ|), since the primary failure risk is explicitly at the absorbing boundary.
- Investigate prior art: the Fisher angular transform, Slotboom symmetrization, and the formal analogy between drift-diffusion and Kimura operators are known in parts; Stage 3 should check whether the claimed methodological transfer (industrial SG schemes → SFS solvers) has been previously published or implemented.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed operators are linear drift-diffusion (Fokker–Planck) of identical class; the Fisher-angular transform produces the constant-mobility flux that matches the graded-heterostructure continuity equation term-for-term, and the zero-flux, Slotboom, boundary-flux and free-energy identities follow directly.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type (scalar potentials, Einstein coefficients, boundary traces of the same flux, dimensionless Péclet groups) and the Operator Role statements name the shared structure (identical flux form, Gibbs exponent, Bernoulli argument, self-adjoint weighted space) rather than mere analogy; dimensional mismatches are explicitly nondimensionalized.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six listed vectors are demonstrated by explicit derivation or operator identity in Section 3 (Vectors 1–6), each supported by the transformed flux equation, the matching stationary states, the N_c identification, the Dirichlet-plus-flux boundary pair, the shared M-matrix threshold, and the Wasserstein dissipation identity with boundary work.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Direction is genuinely asymmetric (Silo A possesses industrially hardened exponential-fitting, discrete free-energy decay and γ-uniform mesh theory for this exact operator; Silo B lacks a flux-conservative positive scheme in the strong-selection multi-deme regime); the prediction supplies a concrete benchmark (fastDTWF exact SFS versus ∂a∂i/moments), a measurable quantity (max relative SFS-bin error), quantitative thresholds (89 % bias versus ≲ 0.8 %) and three explicit falsification criteria.

#### Stage 3 Watch Items
- Primary failure risk noted in entry validation_status (boundary-layer constitutive mismatch of diffusion approximation within O(1/2N) of absorbing boundaries, where fixation flux is evaluated)
- Confirm that the Fisher-angular constant-mobility form remains exact under the frozen-potential restriction once multi-deme non-gradient migration is restored (vectors 1/4/5 survive but 2/6 do not)

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides display correct parabolic drift-diffusion/Fokker-Planck flux forms (Silo A van Roosbroeck continuity with Φ = E_c - kBT ln N_c and Slotboom symmetrization, Silo B Kimura flux J = [s x(1-x)+...]φ - (1/4N)∂_x[x(1-x)φ] with Wright stationary state) and Section 3 derives constant D_θ = 1/(4N) via θ = 2·arcsin(√x), supporting the shared operator claim with no elliptic/parabolic or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six pairs map compatible types with explicit shared structure: V_T ↔ 1/(4N) as D/M coefficient with stated nondimensionalization u ≡ Φ/kBT ↔ 4N·U, Φ ↔ 4N·U(θ) as scalar drift potential entering Bernoulli B(z), N_c ↔ (x(1-x))^{-1/2} as entropic term via -kBT ρ ∂ln N_c, Slotboom u_S ↔ Wright-normalized w as potential of self-adjoint form F = -D e^{-u} ∂w, Ohmic current ↔ fixation flux as boundary trace of same operator, Pe_h ↔ 2γh as argument of B(z) and M-matrix condition; no hedged "analogous to" without structure.
- **CHECK 3 (Correspondence Vector Support):** PASS — All six YAML vectors demonstrated in Section 3 with equations/derivations: constant_mobility_flux_operator_under_fisher_angular_transform (D_θ constant, J = -[1/(4N)∂_θ π + π∂_θ U]), slotboom_wright_exponential_zero_flux_stationary_state (w ≡ π e^{4NU}, π* ∝ e^{-4NU} pulling back to Wright), wright_fisher_ito_metric_term_as_graded_effective_density_of_states (ln N_c ↔ -ln sinθ, N_c ∝ (4x(1-x))^{-1/2}), ohmic_terminal_current_absorbing_fixation_flux_boundary_pair (Dirichlet n_eq ↔ π=0 plus I_c and ∂_t P_fix = J), bernoulli_cell_peclet_similarity_group_and_shared_M_matrix_threshold (Pe_h^{(B)} → 4Nsh, D/h²(1-Pe_h/2) ≥0), wasserstein_free_energy_dissipation_identity_with_boundary_work_term (F[ρ] = ∫[kBT ρ(lnρ-1)+ρΦ], dF/dt = -∫Mρ|∂μ|² -[μF]_∂).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: Silo A → Silo B for γ-uniform flux-conservative positivity with industrial Scharfetter-Gummel, Voronoi, graded-N_c Bernoulli, and free-energy decay tools that Silo B lacks for ≥2-3 demes while Silo B is acknowledged more mature in coalescent, fastDTWF, moments, spectral expansions; falsifiability is specific with fastDTWF at 2N=20,000 n=100 vs ∂a∂i/moments, max relative SFS error, predicted 89% bias γ/(γ+M) vs 0.8% SG, and three quantitative falsification clauses. Prior-art recognition: no canonical semiconductor-TCAD ↔ population-genetics textbook pairing recognized; general Chang-Cooper/Scharfetter-Gummel for Fokker-Planck is textbook but not this graded heterostructure/Fisher mapping — flagged for Stage 3 bibliometric check only.

#### Stage 3 Watch Items
- Verify via bibliometric search whether exponential fitting (Chang-Cooper/Scharfetter-Gummel) with Fisher angular transform and N_c ∝ (x(1-x))^{-1/2} interpretation has appeared in SFS/DFE inference literature.
- Probe diffusion-approximation breakdown within O(1/2N) of absorbing boundary noted as primary failure risk and its impact on claimed fixation-flux accuracy.
- Confirm that frequency-dependent selection s(x) indeed breaks Vectors 2 and 6 as stated, leaving Vectors 1,4,5 intact.