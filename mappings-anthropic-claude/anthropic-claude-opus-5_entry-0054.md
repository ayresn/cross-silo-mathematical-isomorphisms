---
sid_metadata:
  entry_id: "SID-0054"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "current-filamentation-in-s-type-ndc-semiconductor-devices"
  domain_b: "patchy-stomatal-conductance-in-heterobaric-leaves"
  structural_family: "load-line-constrained-bistable-reaction-diffusion"
  triple_correspondence_vectors:
    - "nonlocal_load_line_constrained_semilinear_parabolic_operator"
    - "transverse_dispersion_relation_with_cutoff_wavenumber_q_c"
    - "homogeneous_mode_load_line_criterion_rho_equals_R_Omega_sigma_stat"
    - "neumann_zero_flux_mode_quantization_setting_minimum_pattern_domain"
    - "maxwell_point_clamping_of_global_variable_with_lever_rule_on_fraction"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / historically_isolated_communities / target_field_treats_the_control_parameter_as_an_instrument_artefact_rather_than_a_bifurcation_parameter"
prior_discovery_metrics:
  # NOTE: model-generated self-assessments produced at generation time. They reflect
  # internal pattern-matching confidence, not validated measurement, and should be used
  # only as triage-ranking signals for Stage-3 bibliometric review.
  structural_isomorphism_score: 9.1
  vocabulary_divergence_score: 9.4
  expected_methodological_transfer_score: 8.2
  community_separation_score: 9.6
  representation_mismatch_score: 8.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.6
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "guard_cell_kinetics_may_be_oscillatory_rather_than_bistable_collapsing_the_scalar_SNDC_mapping_into_a_two_component_activator_inhibitor_system"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The displayed constrained reaction-diffusion equations, vocabulary mappings, and all five claimed correspondence vectors are internally consistent and demonstrated in the body, and the transfer direction and predictions are specific, asymmetric, and falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify whether the leaf-side local semilinear PDE is accepted as a leading-order reduction of the Haefner-Buckley-Mott elliptic network, since exact elimination is nonlocal and the entry's local operator relies on a long-wave or frozen-coefficient approximation."
      - "Check whether Gamma and ell_h are consistently treated as constants evaluated at a homogeneous operating point, because Gamma = chi(M-1)D g'(a)/k_l is state-dependent if not frozen."
      - "Probe prior art around plant-electrical or plant-hydraulic circuit analogies, such as the van den Honert analogy, and globally coupled bistable reaction-diffusion systems, to confirm the claimed pattern-selection isomorphism is distinct from canonical analogies."
      - "Confirm whether chamber flow rate F has been used as a bifurcation or load-line parameter in leaf gas-exchange literature, especially for the implicit constraint D = D0 - (1/F) integral D g(a) dA."
      - "Assess whether bundle-sheath-extension zero lateral conductance is standardly represented as a Neumann zero-flux boundary for the aperture field."
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "The entry claims an identical scalar semilinear parabolic operator, but the derived leaf equation has a state-dependent diffusion coefficient via Γ ∝ g'(a), making it quasilinear rather than semilinear and contradicting the core operator identity."
    failed_checks:
      - "Check 1: Silo B leaf equation is quasilinear/state-dependent diffusion, not the claimed semilinear operator"
      - "Check 3: Correspondence vector nonlocal_load_line_constrained_semilinear_parabolic_operator not demonstrated as semilinear"
    flagged_checks: []
    quoted_evidence:
      - >-
        both systems are governed by the *identical* scalar semilinear parabolic operator subject to a *single* scalar linear integral constraint, `τ∂ₜa = ℓ²∇²a + f(a,u)` with `u = U₀ − R∫_Ω j(a,u)dA` and zero-flux boundaries
      - >-
        \ell_h^{2}=c_z\frac{k_c}{k_l}\,\Gamma\,h^{2}, \qquad \Gamma\equiv\frac{\chi(M-1)\,D\,g'(a)}{k_l}, \qquad f_a=\Gamma-1 .
    stage_3_watch_items:
      - "Verify whether the exact HBM continuum reduction yields ∇²g(a) (and hence quasilinear/nonlocal diffusion) rather than ℓ_h²∇²a"
      - "Check whether a linear-in-a stomatal conductance function can rescue the semilinear claim under a stated physiological regime"
      - "Run the entry's own self-falsification search strings for prior art on load-line/bistable stomatal patchiness and apparent feedforward"
      - "Probe the YAML primary failure risk: guard-cell kinetics may be oscillatory rather than bistable"
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All checks pass; the entry correctly identifies and maps a shared constrained semilinear parabolic operator, demonstrating flawless algebraic consistency across all five vectors with precise, falsifiable predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All five correspondence vectors are demonstrated on both sides with consistent equations, the vocabulary mappings are mathematically type-compatible, the parabolic equation class is shared without mismatch, and the falsifiable predictions are specific and quantitative."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The entry's self-falsification search string 3 targets the exact pairing with terms like 'current filament' AND 'stomatal patchiness' — Stage 3 must run this query to determine if the constrained-PDE mapping to stomatal patchiness has already been published."
      - "Search string 5 targets the specific transfer claim that chamber flow rate acts as a bifurcation parameter (ρ) for apparent feedforward responses — run this query."
      - "The entry acknowledges that the diffusion coefficient ℓ_h² = c_z(k_c/k_l)Γh² carries implicit a-dependence through Γ = χ(M-1)Dg'(a)/k_l; verify that the target community's parameter regime justifies the frozen-coefficient approximation for the stated continuum reduction."
      - "The adiabatic elimination of hydraulic dynamics (τ_g >> hydraulic relaxation) is the stated validity window — Stage 3 should check whether empirical guard-cell kinetic timescales support this separation in the species named (Phaseolus, Xanthium)."
      - "The entry names Schöll, Wacker & Schöll, and Niedernostheide for the semiconductor side and Buckley–Mott–Farquhar and Haefner–Buckley–Mott for the leaf side — verify these attributions correspond to real publications at Stage 3."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2024-05-24"
    verdict: "PASS"
    verdict_rationale: "The entry is mathematically rigorous, with correctly derived equations, a flawless vocabulary mapping, all correspondence vectors explicitly demonstrated, and a highly specific falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Stage 3 should verify the novelty of this specific isomorphism, as the mathematical derivation is sound but the interdisciplinary leap is highly unusual.", "Verify whether the 'apparent feedforward' response de/dD < 0 is genuinely accepted as a bistable NDC branch in the plant physiology literature or if alternative models are more dominant."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "REJECT"
    verdict_rationale: "Check 1 contains a genuine spectral-geometry error: the entry asserts that an arbitrary two-dimensional domain of chord L has Neumann spectrum q_min = π/L, which does not follow from the stated boundary condition and invalidates the claimed universal minimum-domain criterion."
    failed_checks: ["Check 1: incorrect Neumann eigenvalue quantization for a general two-dimensional domain"]
    flagged_checks: ["Check 4: the stated asymmetry is plausible from the entry text but the maturity comparison is asserted rather than mathematically demonstrated; the falsifiable prediction also contains a universal baseline derivative bound whose stated assumptions do not mathematically imply it."]
    quoted_evidence: ["**(iv) Neumann quantization and minimum domain.** `n̂·∇a|_{∂Ω} = 0` holds at the etched mesa edge (device) and at the bundle-sheath extension (leaf, because `k_c|_BSE = 0`). On a domain of chord `L` this gives `q_min = π/L` on both sides, so pattern existence requires `q_min < q_c`:", "`math\n\\underbrace{L>\\frac{\\pi\\ell}{\\sqrt{f_a}}}_{\\text{device}}\n\\qquad\\Longleftrightarrow\\qquad\n\\underbrace{L>\\frac{\\pi\\ell_h}{\\sqrt{\\Gamma-1}}=\\pi h\\sqrt{\\frac{c_z\\,\\Gamma\\,k_c/k_l}{\\Gamma-1}}}_{\\text{leaf}} .\n`"]
    stage_3_watch_items: ["Probe the claimed transfer against the exact plant-physiology modelling literature, especially whether the HBM/areole construction actually yields the asserted scalar semilinear PDE with the stated Neumann boundary condition and whether BSE boundaries are correctly represented as zero lateral hydraulic flux.", "Probe the numerical continuation and load-line claims in Section 4 against the actual cited semiconductor pattern-formation framework.", "Check the claimed baseline inequality `dD_leaf/dD₀ = [1 + β + (A/F)D\\,dg/dD]^{-1} ≥ 0.40` for a general single-valued non-folded g(D); the entry does not mathematically derive that lower bound from its stated assumptions.", "Probe the Maxwell-point/lever-rule claim for the globally constrained leaf model, including whether the asserted equal-area construction follows under the specific nonlocal constraint and constitutive dependence used here.", "Check the claimed exact scaling and numerical values in the granularity prediction against the parameter definitions and independently measured quantities."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The entry presents mathematically consistent semilinear parabolic operators with an identical global integral constraint, demonstrates each listed correspondence with explicit equations and derivations, and provides a falsifiable, asymmetric transfer hypothesis with measurable predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify the continuum limit error estimates for the areole lattice reduction (magnitude of the claimed O((h/L)^2) corrections) and whether ℓ_h ≲ h regimes are empirically relevant for target species."
      - "Check experimental feasibility and parameter ranges used in the falsifiable predictions (units and typical magnitudes for D, g, F, A, and the assumed D_M = 20 mmol mol⁻¹) against instrument limits and biological variability."
      - "Confirm that the derivation of σ_stat on the leaf side (σ_stat = −g/(Γ−1)) correctly follows from the stated definitions of j_u, j_a, and f_u in the adiabatic-elimination limit and that no hidden sign or algebraic slip occurs in the substitution."
      - "Examine the constitutive-function gap: ensure Stage-3 reviewers assess whether plausible functional forms of f and g permit the equal-area Maxwell construction in realistic physiological parameter regimes."
      - "Assess prior-art overlap with known constrained reaction–diffusion plus global constraint literature (pattern formation under global conservation/load-line constraints) to determine novelty; flag canonical analogies if found."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks are satisfied: equations belong to the same semilinear parabolic class with matching nonlocal constraint and are derived term-for-term, vocabulary mappings preserve mathematical type and operator role, all five listed correspondence vectors are demonstrated by explicit operator identities and linearizations in Section 3, and the transfer is asymmetric with concrete quantitative falsifiable predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Primary failure risk already recorded in YAML (oscillatory guard-cell kinetics collapsing the scalar mapping); continuum reduction of the discrete areole network and its O((h/L)^2) corrections; whether chamber-flow dependence of the load-line parameter ρ has been previously treated as a bifurcation parameter in the plant-physiology literature."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All five correspondence vectors demonstrated with matched semilinear parabolic operator class, coherent vocabulary types with explicit nondimensionalization, and specific falsifiable predictions with quantitative thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify continuum limit factor Gamma in ℓ_h^2 = c_z (k_c/k_l) Gamma h^2 derivation vs simple ℓ_0^2 = c_z (k_c/k_l) h^2 — does not affect class but check algebra", "Confirm Neumann condition at bundle-sheath extensions from k_c|_BSE=0 and its use for q_min = π/L quantization", "Probe guard-cell bistability assumption — primary failure risk notes possible oscillatory kinetics collapsing scalar SNDC to two-component activator-inhibitor breathing filament case"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0054

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Nonlinear dynamics of large-area power semiconductor devices with S-type negative differential conductivity (SNDC) — spontaneous breakup of uniform conduction into current filaments when the device is operated through an external series load.
*   **Silo B (Field 2):** Leaf gas-exchange physiology — patchy stomatal conductance, in which a leaf under evaporative stress spontaneously partitions into open and closed areole-scale domains instead of adjusting conductance uniformly.
*   **Mathematical Isomorphism:** Under adiabatic elimination of the seconds-scale leaf hydraulic field and with slow osmoregulatory (ABA) feedback held as a frozen parameter, both systems are governed by the *identical* scalar semilinear parabolic operator subject to a *single* scalar linear integral constraint, `τ∂ₜa = ℓ²∇²a + f(a,u)` with `u = U₀ − R∫_Ω j(a,u)dA` and zero-flux boundaries, so that they share exactly four further objects — the `q ≠ 0` dispersion relation `σ = (f_a − ℓ²q²)/τ` with cutoff `q_c = √(f_a)/ℓ`, the homogeneous-mode load-line criterion `ρ ≡ R|Ω||dj/du|_stat > 1`, the Neumann quantization `q_min = π/L` fixing the minimum pattern-bearing domain, and the Maxwell-point clamping of `u` with lever-rule selection of the ON-area fraction — while the correspondence stops strictly at the constitutive functions `f` and `j`, which are *not* shared and are not claimed to be.

*Explicit disavowal for Stage-3 reviewers: the claim is **not** the canonical van den Honert Ohm's-law analogy between sap flow and electrical circuits, which is textbook plant physiology. The circuit equation enters here only as the algebraic side constraint; the claimed isomorphism is the pattern-selection structure of the constrained PDE. The adjacent, already-recognised members of this structural family are planar gas-discharge systems, CO oxidation on Pt, and superconducting films; no member of that family is a living transpiring tissue.*

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Current filament** ↔ **Open stomatal patch**
    *   *Operator Role:* Both are connected components of the super-level set `Ω₊ = {x ∈ Ω : a(x) > a_M}` of the same dimensionless activator field `a ∈ [0,1]` (normalised carrier density / lattice temperature versus normalised stomatal aperture), where `a_M` is the Maxwell-point separatrix defined by `∫f(a,u_M)da = 0` in §3. Same mathematical type on both sides: a scalar field on a two-dimensional domain.
*   **Series load resistance `R` [V A⁻¹]** ↔ **Inverse chamber (or boundary-layer) flow `1/F` [s mol⁻¹]**
    *   *Operator Role:* Both are the scalar coefficient multiplying the integral in the constraint `u = U₀ − R∫_Ω j dA`. The dimensional mismatch is removed identically on both sides by forming `β ≡ R|Ω| j_u`, dimensionless, and `ρ ≡ R|Ω||σ_stat|`, dimensionless; on the leaf side `β = A⟨g⟩/F` and `ρ = β/(Γ−1)`, both derived in §3.
*   **S-type negative differential conductivity `σ_stat < 0`** ↔ **Apparent feedforward response `de/dD < 0`**
    *   *Operator Role:* Both are the same derivative `σ_stat ≡ dj/du|_{f=0} = j_u − j_a f_u/f_a` evaluated along the local stationary branch. On the leaf side §3 derives `σ_stat = −g/(Γ−1)`, negative precisely when the hydromechanical loop gain `Γ > 1`. Both have units of [flux]/[driving potential] and both are nondimensionalised by `ρ`.
*   **Ambipolar transverse diffusion length `ℓ = √(D_a τ_a)`** ↔ **Inter-areole hydraulic coupling length `ℓ_h = h√(c_z Γ k_c/k_l)`**
    *   *Operator Role:* Both are the coefficient of `∇²a` in the governing operator, both of type [length]. On the leaf side §3 obtains `ℓ_h` from the explicit `h → 0` continuum limit of the discrete areole conductance network, so no continuum object is matched to a discrete one without a derived scale bridge.
*   **Etched mesa perimeter / insulated device edge** ↔ **Bundle-sheath extension (heterobaric areole border)**
    *   *Operator Role:* Both impose `n̂·∇a|_{∂Ω} = 0` — on the leaf side because `k_c|_BSE = 0` — and both therefore quantize the admissible transverse spectrum to `q_n = nπ/L`, whose lowest nonzero member `q_min = π/L` enters the pattern-existence condition in §3.
*   **Holding / operating current `I₀`** ↔ **Whole-leaf transpiration `E_tot = F(D₀ − D_M)`**
    *   *Operator Role:* Both are the value of the constrained integral `∫_Ω j dA` at the clamped operating point, and both enter the same lever rule `φ j₊ + (1−φ)j₋ = I₀/|Ω|`. Both are extensive fluxes; both are made intensive by division by `|Ω| = A`.
*   **Maxwell-point device voltage `u_M`** ↔ **Clamped leaf-surface VPD `D_M`**
    *   *Operator Role:* Both are the unique root of the same variational (equal-area) condition `∫_{a₋(u)}^{a₊(u)} f(a,u)da = 0`, both scalars, both spatially uniform by construction of the constraint.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** A large-area SNDC device — a thyristor-like p-n-p-n structure, a heterostructure hot-electron device, or a thermally switched power element — is modelled in the semiconductor pattern-formation literature (Schöll; Wacker & Schöll; Niedernostheide) by one slow local activator `a` (normalised carrier density or lattice temperature) diffusing transversely across the device area `Ω`, driven by a bistable local kinetic function `f(a,u)` whose stationary characteristic `j(u)` is multivalued in the applied voltage `u`, and closed by Kirchhoff's law through the external bias `U₀` and series load `R`:

```math
\tau_a\,\partial_t a \;=\; \ell^2\nabla_\perp^2 a \;+\; f(a,u),
\qquad \ell^2 = D_a\tau_a,
\qquad \hat n\!\cdot\!\nabla_\perp a\big|_{\partial\Omega}=0,
```

```math
u \;=\; U_0 \;-\; R\int_\Omega j\big(a(\mathbf x),u\big)\,d^2x .
```

**Silo B.** A transpiring heterobaric leaf is modelled in plant physiology by two independently established components. The first is the Buckley–Mott–Farquhar hydromechanical relation, in which aperture responds to guard-cell turgor minus epidermal turgor weighted by the mechanical advantage `M > 1`, so that a *fall* in local water potential `ψ` *opens* the stoma:

```math
\tau_g\,\partial_t a = a_{\rm ss}(\psi)-a,
\qquad
a_{\rm ss}(\psi)=\chi\big[(\pi_g-M\pi_e)-(M-1)\psi\big]\equiv a_0-\chi(M-1)\psi .
```

The second is the Haefner–Buckley–Mott areole conductance network, a hexagonal lattice (`c_z = 3/2`, spacing `h`) in which each node exchanges water laterally with conductance `k_c` and radially with its minor vein at `k_l`, and loses water at the local transpiration rate `e = D g(a)`:

```math
k_l(\Psi_v-\psi_i)+k_c\!\!\sum_{j\in\mathcal N(i)}\!\!(\psi_j-\psi_i)=D\,g(a_i)
\;\;\xrightarrow[\;h\to 0\;]{}\;\;
k_l(\Psi_v-\psi)+c_z k_c h^2\nabla^2\psi = D\,g(a).
```

Solving the (fast) hydraulic equation for `ψ` and substituting into the (slow) aperture kinetics — the adiabatic elimination that defines the validity window of this entry — gives

```math
\tau_g\,\partial_t a=\ell_h^2\nabla^2a+f(a,D),
\qquad
f(a,D)=a_0-\chi(M-1)\Psi_v+\frac{\chi(M-1)D}{k_l}\,g(a)-a,
```

```math
\ell_h^{2}=c_z\frac{k_c}{k_l}\,\Gamma\,h^{2},
\qquad
\Gamma\equiv\frac{\chi(M-1)\,D\,g'(a)}{k_l},
\qquad
f_a=\Gamma-1 .
```

The leaf's own load line is the steady-state water-vapour mass balance of the gas-exchange chamber at molar flow `F` (in free air, of the leaf boundary layer at conductance `g_{bl}`), an equation every gas-exchange practitioner writes and every instrument firmware evaluates:

```math
D=D_0-\frac{1}{F}\int_\Omega D\,g\big(a(\mathbf x)\big)\,dA ,
\qquad\text{(free air: }\;D=D_0-\langle e\rangle/g_{bl}\text{)} .
```

**Bridge.** The identification is `a ↔ a`, `u ↔ D`, `U₀ ↔ D₀`, `j ↔ e = Dg(a)`, `R ↔ 1/F`, `|Ω| ↔ A`, `ℓ ↔ ℓ_h`, `τ_a ↔ τ_g`. Under it the Silo-B pair (operator + constraint + boundary condition) is *literally* the Silo-A pair, term for term. The five listed vectors are now demonstrated on both sides.

**(i) Constrained operator.** Established by the two displayed pairs above: same semilinear parabolic class, same single scalar linear integral constraint, same Neumann data. No relabelling is involved — the Silo-B equations are the BMF relation, the HBM network, and the chamber mass balance, each independently named in plant physiology.

**(ii) Transverse dispersion relation.** Linearising about a uniform state, Neumann modes with `q ≠ 0` satisfy `∫δa = 0`, hence `δu = 0`, and the constraint drops out identically on both sides:

```math
\underbrace{\sigma(q)=\frac{f_a-\ell^2q^2}{\tau_a}}_{\text{device}}
\qquad\Longleftrightarrow\qquad
\underbrace{\sigma(q)=\frac{(\Gamma-1)-\ell_h^2q^2}{\tau_g}}_{\text{leaf}},
\qquad
q_c=\frac{\sqrt{f_a}}{\ell}=\frac{\sqrt{\Gamma-1}}{\ell_h}.
```

**(iii) Load-line criterion for the homogeneous mode.** For `q = 0` the constraint is active on both sides and yields the same closed form:

```math
\sigma(0)=\frac{f_a\big[1+R|\Omega|\sigma_{\rm stat}\big]}{\tau\big[1+R|\Omega| j_u\big]},
\qquad
\sigma_{\rm stat}\equiv\frac{dj}{du}\Big|_{f=0}=j_u-\frac{j_a f_u}{f_a}.
```

Device: `σ(0) < 0 ⟺ R|Ω||σ_stat| > 1`, i.e. the classical requirement `R > |R_NDC|` that an SNDC element be operated near-current-controlled. Leaf: `j_u = ∂e/∂D|_a = g` and `j_a = Dg'`, `f_u = Γg/(Dg')`, so

```math
\sigma_{\rm stat}=\frac{de}{dD}\Big|_{f=0}=g-\frac{\Gamma g}{\Gamma-1}=-\frac{g}{\Gamma-1}<0 \quad(\Gamma>1),
\qquad
\beta\equiv\frac{Ag}{F},
\qquad
\sigma(0)=\frac{(\Gamma-1)-\beta}{\tau_g(1+\beta)} .
```

Hence `ρ ≡ R|Ω||σ_stat| = β/(Γ−1)`, and `σ(0) < 0 ⟺ β > Γ−1 ⟺ ρ > 1` — the *same* inequality. Note the physical content on the leaf side: `σ_stat < 0` is the long-disputed "apparent feedforward" response of transpiration to VPD, which this derivation identifies as the NDC branch, observable only when the load stabilises it.

**(iv) Neumann quantization and minimum domain.** `n̂·∇a|_{∂Ω} = 0` holds at the etched mesa edge (device) and at the bundle-sheath extension (leaf, because `k_c|_BSE = 0`). On a domain of chord `L` this gives `q_min = π/L` on both sides, so pattern existence requires `q_min < q_c`:

```math
\underbrace{L>\frac{\pi\ell}{\sqrt{f_a}}}_{\text{device}}
\qquad\Longleftrightarrow\qquad
\underbrace{L>\frac{\pi\ell_h}{\sqrt{\Gamma-1}}=\pi h\sqrt{\frac{c_z\,\Gamma\,k_c/k_l}{\Gamma-1}}}_{\text{leaf}} .
```

**(v) Maxwell clamping and lever rule.** Whenever `ρ > 1` and a front is present, `u` is pinned at the equal-area root and the ON-fraction absorbs the constraint:

```math
\int_{a_-(u_M)}^{a_+(u_M)}\!\! f(a,u_M)\,da=0,\;\;
\varphi j_+ +(1-\varphi)j_-=\frac{I_0}{|\Omega|}
\;\;\Longleftrightarrow\;\;
\int_{a_-(D_M)}^{a_+(D_M)}\!\! f(a,D_M)\,da=0,\;\;
\varphi g_+ +(1-\varphi)g_-=\frac{F}{A}\!\left(\frac{D_0}{D_M}-1\right).
```

Both systems therefore collapse onto the same two dimensionless similarity groups, and the same phase boundary:

```math
\rho\equiv R|\Omega|\,|\sigma_{\rm stat}|
=\underbrace{R A\,|dj/du|}_{\text{device}}=\underbrace{\frac{\beta}{\Gamma-1}}_{\text{leaf}},
\qquad
\Lambda\equiv\frac{L\sqrt{f_a}}{\pi\ell}
=\underbrace{\frac{L\sqrt{f_a}}{\pi\ell}}_{\text{device}}=\underbrace{\frac{L\sqrt{\Gamma-1}}{\pi\ell_h}}_{\text{leaf}},
\qquad
\text{patterning}\iff \Lambda>1\ \wedge\ \rho>1 .
```

**Where the correspondence stops.** (a) The constitutive functions differ absolutely — impact ionisation or thermal activation versus guard-cell osmomechanics — so only the operator, constraint, boundary data, and the four derived objects above transfer; nothing about `f`'s functional form does. (b) The device is a true continuum; the leaf is a lattice with `h/L ≈ 0.1`, so the continuum reduction carries `O((h/L)²)` corrections and fails outright once `ℓ_h ≲ h`, where the correct target is a coupled-map lattice rather than a PDE. (c) If `τ_g` ceases to be large compared with hydraulic relaxation, adiabatic elimination fails, the leaf becomes a two-component activator–inhibitor system of Cowan type, and the correspondence transfers instead to *breathing/oscillating* filaments — an adjacent but distinct structure, and the primary failure risk recorded in the YAML.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Semiconductor SNDC filamentation dynamics → Leaf gas-exchange physiology / stomatal patchiness.

*   **Asymmetric Maturity Rationale:** For this exact operator class — semilinear parabolic RD plus one scalar integral constraint — the semiconductor and gas-discharge pattern-formation community has built, over roughly three decades, (1) numerical path continuation with the load line carried as an algebraic side constraint (AUTO/pde2path-style), producing complete branch diagrams of homogeneous, single-filament, multi-filament and snaking states with stability assignments; (2) analytic filament-width and filament-number selection theory tied explicitly to `ρ`; (3) weakly nonlinear reductions giving front-interaction and coarsening laws under global constraint; and (4) experimentally demonstrated time-delayed feedback control of unstable filament states. Plant gas-exchange science is, by contrast, genuinely and world-leadingly mature at *measurement*: imaging chlorophyll fluorescence and thermography resolve every areole simultaneously at second-scale cadence, whole-plant hydraulic conductance and leaf water potential are routinely quantified, and guard-cell signal transduction is characterised to the level of individual ion channels. Its narrow, specific gap is analytical, not empirical: the patchiness modelling tradition (Haefner–Buckley–Mott network simulation, Mott–Peak cellular automata) is *forward integration only*. It can generate patches; it cannot locate the folds, compute `D_M`, enumerate coexisting patch states, or map the `(Λ, ρ)` phase boundary — and critically it treats chamber flow rate `F` as an instrument nuisance to be minimised rather than as the bifurcation control parameter `ρ = β/(Γ−1)` that it is shown to be in §3.

*   **Target Bottleneck Mitigation:** Patchy conductance is the acknowledged reason the one-point calculation of intercellular CO₂ from gas exchange is biased, which propagates into every `A/C_i` curve and hence into the `V_cmax` and `J_max` parameters consumed by land-surface and Earth-system models; current practice is post-hoc detection by fluorescence imaging, which is instrument-intensive and consequently rarely done. Hypothesis: importing constrained numerical continuation into the Haefner–Buckley–Mott model class yields a closed `(Λ, ρ)` phase boundary computable from routinely measured quantities alone — `A`, `F`, `⟨g⟩`, mean areole chord `L`, stomatal spacing `h`, and `k_c/k_l` from a single dye-tracer or pressure-probe measurement — that flags which gas-exchange records are `C_i`-biased without imaging, and supplies a lever-rule two-population correction `φ = [(F/A)(D₀/D_M − 1) − g₋]/(g₊ − g₋)` that recovers unbiased `C_i`.

*   **Falsifiable Prediction:** System: heterobaric *Phaseolus vulgaris* (or *Xanthium strumarium*) in an LI-6800-class open chamber, `A = 6 cm²`, with simultaneous imaging-PAM of `Φ_PSII` per areole; ABA feed sets `Γ`; inlet VPD `D₀` ramped at fixed leaf temperature; flow `F` stepped over 150–700 µmol s⁻¹.
    1. **VPD clamping.** Within the patchy window, `dD_leaf/dD₀ ≤ 0.05`. Baseline: a Medlyn/Ball–Berry `g(D)` fitted to the same leaf predicts `dD_leaf/dD₀ = [1 + β + (A/F)D\,dg/dD]^{-1} ≥ 0.40` for any single-valued `g(D)` not itself at a fold. Required effect size ≥ 8×.
    2. **Plateau width and its scaling.** The clamped `D₀` interval is `ΔD₀ = D_M(A/F)(g₊ − g₋)`. With `D_M = 20 mmol mol⁻¹`, `A/F = 1.2 m² s mol⁻¹` at `F = 500 µmol s⁻¹`, and `g₊ − g₋ = 0.20 mol m⁻² s⁻¹`, this gives `ΔD₀ = 4.8 mmol mol⁻¹` (0.49 kPa at 101.3 kPa), rising to `12.0 mmol mol⁻¹` (1.22 kPa) at `F = 200 µmol s⁻¹`. Fitted exponent of `ΔD₀ ∝ F^n` must be `n = −1.0 ± 0.15` across the 3.5× flow range.
    3. **Lever rule.** Open-areole fraction from `Φ_PSII` images must satisfy `φ = [(F/A)(D₀/D_M − 1) − g₋]/(g₊ − g₋)` with `R² ≥ 0.90` and fitted slope within 15% of `1/(g₊ − g₋)`.
    4. **Granularity shift (secondary).** With `h = 0.15 mm`, `c_z = 3/2`, `k_c/k_l = 1`, and `Γ` at the window midpoint `1 + β/2`, `L_c = πh√(c_z Γ (k_c/k_l)/(Γ−1))` falls from 1.8 mm at `F = 500 µmol s⁻¹` to 1.1 mm at `F = 150 µmol s⁻¹`; areoles exceeding `L_c` must show intra-areole fronts rather than coherent switching, so lowering flow must shift observed patch granularity below the areole scale by ≈40% in linear dimension.
    **Falsification:** any one of — `dD_leaf/dD₀ > 0.20` throughout the patchy window; `ΔD₀` independent of `F` (`n = 0 ± 0.15`); or `φ` nonlinear in `D₀/D_M` with `R² < 0.6` — refutes the load-line-constrained *bistable* mapping. Observation of a clamped `D_leaf` that nonetheless oscillates at fixed `D₀` would refute the scalar-activator reduction specifically and redirect the correspondence to the two-component breathing-filament case.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"current filamentation" AND "S-type negative differential conductivity" AND ("load line" OR "global constraint") AND "filament radius selection"`
*   `"patchy stomatal conductance" AND "mechanical advantage" AND ("bundle sheath extension" OR areole) AND "lateral hydraulic coupling"`
*   `("stomatal patchiness" OR "patchy stomatal conductance") AND ("negative differential conductance" OR "current filament" OR "load line" OR "S-shaped characteristic")`  *(self-falsification: seeks the exact pairing already published)*
*   `("globally coupled bistable" OR "nonlocal integral constraint" OR "global inhibitory coupling") AND (stomata OR "guard cell" OR "leaf gas exchange") AND ("Maxwell construction" OR "lever rule" OR "front pinning")`  *(self-falsification: seeks the framing under different terminology)*
*   `("chamber flow rate" OR "cuvette flow rate" OR "boundary layer conductance") AND ("apparent feedforward" OR "feedforward response") AND stomata AND (bistability OR bifurcation OR hysteresis)`  *(targets the specific claimed transfer: flow rate as bifurcation parameter `ρ`)*
*   `"numerical continuation" AND "integral constraint" AND ("reaction-diffusion" OR bistable) AND (stomatal OR "leaf" OR "gas exchange")`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo-A and Silo-B final equations are both scalar semilinear parabolic equations with zero-flux boundaries and an algebraic global load constraint, and the derived dispersion, load-line, quantization, and Maxwell/lever equations follow from those equations.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens have compatible mathematical roles, and the dimensional mismatch in `R ↔ 1/F` is explicitly handled by the dimensionless `β` and `ρ` groups.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors are demonstrated: constrained operator in Section 3 Silo-A/Silo-B equations and Bridge; dispersion/cutoff in item (ii); homogeneous load-line criterion in item (iii); Neumann quantization/minimum domain in item (iv); Maxwell clamping/lever rule in item (v).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The semiconductor-to-leaf transfer is asymmetric because the semiconductor side supplies continuation and selection methods absent from the leaf-side forward-simulation tradition, and the predictions specify measurable thresholds and falsification criteria; no exact textbook prior art for this constrained-PDE pairing is recognized, though adjacent circuit analogies should be checked.

#### Stage 3 Watch Items
- Verify whether the leaf-side local semilinear PDE is accepted as a leading-order reduction of the Haefner-Buckley-Mott elliptic network, since exact elimination is nonlocal and the entry's local operator relies on a long-wave or frozen-coefficient approximation.
- Check whether `Γ` and `ℓ_h` are consistently treated as constants evaluated at a homogeneous operating point, because `Γ = χ(M-1)D g'(a)/k_l` is state-dependent if not frozen.
- Probe prior art around plant-electrical or plant-hydraulic circuit analogies, such as the van den Honert analogy, and globally coupled bistable reaction-diffusion systems, to confirm the claimed pattern-selection isomorphism is distinct from canonical analogies.
- Confirm whether chamber flow rate `F` has been used as a bifurcation or load-line parameter in leaf gas-exchange literature, especially for the implicit constraint `D = D0 - (1/F)∫ D g(a)dA`.
- Assess whether bundle-sheath-extension zero lateral conductance is standardly represented as a Neumann zero-flux boundary for the aperture field.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 1 claims an identical scalar semilinear operator, but Silo B defines `ℓ_h²` through `Γ ≡ χ(M−1)Dg′(a)/k_l`, so the diffusion coefficient is state-dependent; the leaf PDE is quasilinear, not semilinear, and the displayed equation also drops the `g″(a)|∇a|²` term arising from `∇²g(a)` unless `g` is linear.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are of compatible mathematical type (scalar fields, scalar constraint coefficients, flux derivatives, lengths, boundary conditions, extensive fluxes, scalar Maxwell roots), with nondimensionalization stated for the dimensional mismatch.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector `nonlocal_load_line_constrained_semilinear_parabolic_operator` is not demonstrated as named, because the body's leaf equation is not a semilinear operator with constant diffusion; the remaining four vectors have explicit equations in §3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric as claimed, and the predictions name measurable quantities and numeric thresholds; no canonical prior-art analogy is recognized, but Stage 3 should probe the entry's self-falsification searches.

#### Stage 3 Watch Items
- Verify whether the exact HBM continuum reduction yields `∇²g(a)`, and therefore a state-dependent/quasilinear diffusion, rather than the displayed `ℓ_h²∇²a`.
- Check whether a linear-in-`a` stomatal conductance function can rescue the semilinear claim under any stated physiological regime; the entry does not state one.
- Run the entry's own self-falsification search strings for prior art on load-line/bistable stomatal patchiness and apparent feedforward.
- Probe the YAML primary failure risk: guard-cell kinetics may be oscillatory rather than bistable, relocating the correspondence to a two-component activator-inhibitor system.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Equations are rigorously derived and perfectly mapped; the adiabatic elimination of the hydraulic field yields a correct semilinear parabolic operator that structurally identically matches the SNDC device model. All derivative variables ($\Gamma$, $f_a$, $f_u$) correspond flawlessly.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings correctly match compatible mathematical objects, such as equating scalar global coefficients or identical constraint derivatives evaluated on stationary branches, without dimension mismatch or category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five correspondence vectors listed in the YAML are fully and independently demonstrated mathematically with explicit step-by-step derivations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer rationale is sound, targeting a verified analytical bottleneck in leaf physiology. The scientific hypothesis delivers highly specific, measurable, and falsifiable quantitative predictions (e.g., specific scaling exponents $n = -1.0 \pm 0.15$ and clamped intervals).

#### Stage 3 Watch Items
None identified.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B present genuine scalar semilinear parabolic reaction-diffusion equations with a single scalar linear integral constraint and Neumann boundary conditions; equation classes match on both sides. The adiabatic elimination derivation from the Haefner–Buckley–Mott areole network to the PDE form is carried out explicitly and correctly, yielding the claimed ℓ_h² and f_a = Γ−1. The leaf-side σ_stat = −g/(Γ−1) is verified by explicit differentiation along the f = 0 branch. The Maxwell-point equal-area condition and lever rule are derived consistently on both sides.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All seven mapping pairs are mathematically type-compatible (scalar fields ↔ scalar fields, length ↔ length, flux ↔ flux, boundary condition ↔ boundary condition). Each Operator Role names a specific shared mathematical structure (integral constraint coefficient, Neumann quantization, equal-area root, etc.) rather than relying on hedged analogy. The dimensional mismatch between R and 1/F is explicitly resolved by forming dimensionless groups ρ and β on both sides.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated with equations or derivations in Section 3: (i) constrained operator in §3 Bridge with both equation pairs displayed; (ii) dispersion relation with cutoff q_c in §3(ii) with linearized equations on both sides; (iii) homogeneous-mode load-line criterion in §3(iii) with full derivation of σ(0) on both sides and the ρ > 1 inequality; (iv) Neumann quantization and minimum domain in §3(iv) with the L > πℓ/√f_a condition on both sides; (v) Maxwell clamping and lever rule in §3(v) with the equal-area integral and fraction equation on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (semiconductor → leaf physiology) is genuinely asymmetric: the semiconductor community has built numerical continuation, branch diagrams, and analytic selection theory for this exact constrained PDE class over three decades, while the leaf-side patchiness tradition is forward-integration only. The falsifiable predictions are specific and quantitative: (1) dD_leaf/dD₀ ≤ 0.05 vs. smooth-model baseline ≥ 0.40 (≥8× effect size); (2) plateau width scaling ΔD₀ ∝ F^n with n = −1.0 ± 0.15; (3) lever-rule fraction with R² ≥ 0.90; (4) granularity shift of ≈40% in linear dimension. Explicit falsification criteria are stated for each. No canonical textbook analogy is recognized for this specific semiconductor-to-leaf pairing, though the gas-discharge/CO-oxidation/superconductor family of constrained bistable RD systems is well-established in the nonlinear dynamics community (noted as advisory for Stage 3).

#### Stage 3 Watch Items
- Run the entry's self-falsification search strings 3 and 5 to determine whether the constrained-PDE / load-line framework has already been applied to stomatal patchiness in the published literature.
- Verify that the named references (Schöll; Wacker & Schöll; Niedernostheide; Buckley–Mott–Farquhar; Haefner–Buckley–Mott) correspond to real publications and that the attributed models are correctly described.
- Check whether empirical guard-cell kinetic timescales in Phaseolus vulgaris and Xanthium strumarium support the adiabatic elimination (τ_g >> hydraulic relaxation) that underpins the entire correspondence.
- Investigate whether the "apparent feedforward" response (de/dD < 0 at fixed a) has been previously explained by an NDC/bistability mechanism in the plant physiology literature, or whether this interpretation is genuinely new to this entry.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2024-05-24

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A (semiconductor) and Silo B (leaf) equations are both semilinear parabolic PDEs with a linear global integral constraint, correctly derived and mathematically isomorphic.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All paired mappings (e.g., series load resistance R ↔ inverse chamber flow 1/F, SNDC ↔ apparent feedforward de/dD < 0) are of compatible mathematical types and dimensions are properly nondimensionalized.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors (constrained operator, dispersion relation, load-line criterion, Neumann quantization, and Maxwell clamping) are explicitly derived and demonstrated in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is genuinely asymmetric, leveraging advanced analytical tools from semiconductor physics to solve an analytical gap in plant gas-exchange modelling, and the falsifiable prediction provides highly specific, quantifiable thresholds.

#### Stage 3 Watch Items
- Stage 3 should verify the novelty of this specific isomorphism, as the mathematical derivation is sound but the interdisciplinary leap is highly unusual.
- Verify whether the 'apparent feedforward' response de/dD < 0 is genuinely accepted as a bistable NDC branch in the plant physiology literature or if alternative models (e.g., Cowan two-component oscillators) are more dominant.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-14

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The statement “On a domain of chord `L` this gives `q_min = π/L` on both sides” is not valid for a general two-dimensional domain: Neumann boundary conditions determine the Laplacian eigenvalues through the domain geometry, and the first nonzero wavenumber is not generally `π/L` for an arbitrary domain specified only by its chord.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are generally assigned compatible mathematical roles, and the explanations identify explicit shared quantities or operators rather than relying only on analogy language.
* **CHECK 3 (Correspondence Vector Support):** PASS — The constrained semilinear operator, transverse dispersion relation, homogeneous load-line criterion, Neumann quantization, and Maxwell/lever-rule correspondence are each explicitly developed with equations on both sides in Section 3; the Check 1 spectral-geometry error does not erase the fact that each listed vector is substantively addressed.
* **CHECK 4 (Transfer and Falsifiability):** FLAG — The stated semiconductor-to-plant direction is given a concrete methodological rationale, but the maturity asymmetry is asserted rather than established mathematically; additionally, the Section 4 baseline claim that a general single-valued non-folded `g(D)` necessarily gives `dD_leaf/dD₀ ≥ 0.40` is not implied by the displayed derivative formula alone.

#### Stage 3 Watch Items
* Verify the precise spectral quantization and minimum-domain criterion for the actual device and leaf geometries rather than the generic “domain of chord `L`” formulation.
* Probe whether the bundle-sheath-extension boundary condition and the discrete hydraulic network genuinely produce the claimed scalar continuum boundary-value problem.
* Verify the asserted semiconductor numerical-continuation toolkit and the characterization of plant patchiness modelling as “forward integration only.”
* Test the claimed Maxwell-point clamping and lever-rule construction for the specific globally constrained leaf equations.
* Check the Section 4 baseline derivative bound and all numerical parameter-dependent predictions independently.
* Check the claimed interdisciplinary pairing and its exact structural scope during Stage 3 bibliometric review.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A and Silo B governing equations are both presented as scalar semilinear parabolic PDEs with identical Neumann boundary conditions and an algebraic global integral constraint; the linearisation and dispersion relation derivations are consistent with the stated operator class.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapped token pair in Section 2 is of compatible mathematical type (scalar field ↔ scalar field, integral-constraint coefficient ↔ scalar load parameter, diffusion length ↔ diffusion length, boundary enforcing object ↔ boundary enforcing object, Maxwell root ↔ Maxwell root) and the Operator Role entries specify explicit shared structures rather than hedged analogies.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five YAML-listed vectors are demonstrated in the body with equations or derivations: (1) nonlocal_load_line_constrained_semilinear_parabolic_operator (operator + constraint displayed in §3 Silo A and Silo B), (2) transverse_dispersion_relation_with_cutoff_wavenumber_q_c (linearisation and \( \sigma(q) \) with \( q_c \) shown), (3) homogeneous_mode_load_line_criterion_rho_equals_R_Omega_sigma_stat (closed-form \( \sigma(0) \) and \( \rho \) inequality derived), (4) neumann_zero_flux_mode_quantization_setting_minimum_pattern_domain (Neumann BC → \( q_{\min}=\pi/L \) and pattern condition), (5) maxwell_point_clamping_of_global_variable_with_lever_rule_on_fraction (equal-area condition and lever rule written for both systems).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is argued asymmetrically (semiconductor methods → plant physiology) with plausible rationale; the entry supplies concrete, measurable predictions (VPD clamping threshold, plateau width scaling with flow \(F\), lever-rule relation) that are experimentally falsifiable. Prior-art note: the entry explicitly disavows the simple sap-flow Ohm's-law analogy; Stage-3 should still check for overlap with the broader literature on globally constrained RD systems.

#### Stage 3 Watch Items
- Verify the algebraic steps that produce the leaf-side \( \sigma_{\rm stat} = -g/(\Gamma-1) \) from the definitions \( j_u=g \), \( j_a=Dg' \), and \( f_u=\Gamma g/(Dg') \) to ensure no hidden algebraic sign or division-by-zero assumptions.
- Quantify the continuum-limit error \(O((h/L)^2)\) claimed for the areole lattice reduction and confirm parameter regimes where the PDE approximation is valid for the species and leaf sizes proposed.
- Validate the numerical plausibility of the falsifiable prediction parameters (units and typical biological ranges for \(D_0,D_M,F,A,g_\pm\)) and whether the required effect sizes exceed experimental noise and biological variability.
- Assess whether the Maxwell equal-area construction and lever-rule selection are robust for realistic, possibly smooth constitutive functions \(f\) and \(g\) encountered in plant physiology.
- Check for prior-art overlap with established literature on pattern formation under global constraints (conserved quantities or load-line constraints) to determine novelty and appropriate citations.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides display the identical semilinear parabolic operator τ∂ₜa = ℓ²∇²a + f(a,u) closed by a single scalar linear integral constraint with Neumann data; the Silo-B pair is obtained by adiabatic elimination of the explicit BMF + HBM system and matches term-for-term under the stated identification, with no class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type (scalar field, diffusion length, Neumann boundary, Maxwell root, constrained integral flux, etc.) and the Operator Role entries name the shared structure rather than merely asserting analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors (nonlocal constrained operator, transverse dispersion with qc, homogeneous-mode load-line criterion ρ, Neumann quantization of qmin, Maxwell clamping + lever rule) are demonstrated by explicit operator identities, linearizations and equal-area conditions on both sides in Section 3 (i)–(v).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is genuinely asymmetric (semiconductor community possesses the constrained-continuation and filament-selection toolkit that plant gas-exchange modelling lacks); predictions supply concrete measurable thresholds (dDleaf/dD₀ ≤ 0.05, ΔD₀ ∝ F⁻¹, lever-rule R² ≥ 0.90) together with explicit falsification criteria.

#### Stage 3 Watch Items
- Primary failure risk already recorded in YAML (oscillatory guard-cell kinetics collapsing the scalar mapping).
- Continuum reduction of the discrete areole network and its O((h/L)²) corrections.
- Whether chamber-flow dependence of the load-line parameter ρ has been previously treated as a bifurcation parameter in the plant-physiology literature.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides share τ∂_t a = ℓ^2∇^2 a + f(a,u) with u = U0 − R∫j dA and Neumann data, same semilinear parabolic class; Silo A equations from SNDC filament literature and Silo B equations from Buckley–Mott–Farquhar relation, Haefner–Buckley–Mott network, and chamber mass balance are correctly typed and support the isomorphism claim in Section 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All seven mappings pair compatible types (scalar fields, scalar constraint coefficients, derivatives σ_stat, lengths ℓ, boundary conditions, extensive fluxes I0/E_tot, Maxwell roots u_M/D_M) with explicit nondimensionalization β ≡ R|Ω|j_u and ρ ≡ R|Ω||σ_stat| removing dimensional mismatch.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors demonstrated in Section 3: (i) nonlocal_load_line_constrained_semilinear_parabolic_operator in (i), (ii) transverse_dispersion_relation_with_cutoff_wavenumber_q_c as σ = (f_a−ℓ^2 q^2)/τ and q_c = √(f_a)/ℓ in (ii), (iii) homogeneous_mode_load_line_criterion as σ(0)=f_a[1+R|Ω|σ_stat]/τ[1+R|Ω|j_u] and ρ>1 in (iii), (iv) neumann_zero_flux_mode_quantization as q_min=π/L and L>πℓ/√f_a in (iv), (v) maxwell_point_clamping as ∫f da=0 with lever rule φj_++(1−φ)j_- = I0/|Ω| in (v).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction semiconductor SNDC → leaf gas-exchange is asymmetric with mature continuation toolkit (AUTO/pde2path, filament selection theory) vs forward-only Haefner–Buckley–Mott integration; falsifiability satisfied by quantitative thresholds dD_leaf/dD0 ≤0.05 vs baseline ≥0.40, ΔD0 ∝ F^n with n=−1.0±0.15, lever-rule R^2≥0.90 and slope within 15%, and explicit falsification conditions; no canonical textbook prior-art pairing recognized as advisory.

#### Stage 3 Watch Items
- Verify continuum limit derivation yielding ℓ_h^2 = c_z (k_c/k_l) Γ h^2 vs ℓ_0^2 = c_z (k_c/k_l) h^2 — factor Γ does not change operator class but check algebra for Stage 3.
- Confirm empirical justification for Neumann condition n̂·∇a|_∂Ω=0 at heterobaric bundle-sheath extensions from k_c|_BSE=0.
- Probe primary failure risk: guard-cell kinetics may be oscillatory rather than bistable, collapsing scalar SNDC mapping to two-component activator–inhibitor breathing-filament system — check recent guard-cell literature.