---
sid_metadata:
  entry_id: "SID-0054"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
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