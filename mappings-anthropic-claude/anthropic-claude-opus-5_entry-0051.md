---
sid_metadata:
  entry_id: "SID-0051"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
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