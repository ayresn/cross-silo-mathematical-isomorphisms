---
sid_metadata:
  entry_id: "SID-0035"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "petroleum-reservoir-fractional-flow"
  domain_b: "gravity-thickening-sedimentation"
  structural_family: "scalar-hyperbolic-conservation-shocks"
  triple_correspondence_vectors:
    - "nondimensional_scalar_conservation_operator"
    - "rankine_hugoniot_shock_speed_velocity_scaling"
    - "welge_kynch_entropy_tangent_shock_selection"
    - "integral_phase_volume_conservation_law"
    - "flux_nonconvexity_shape_parameter_mapping"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_design_codes"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 8.2
  expected_methodological_transfer_score: 7.9
  community_separation_score: 7.5
  representation_mismatch_score: 6.3
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.4
    uncertainty: "±1.4"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "constitutive_flux_and_regularization_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "FLAG"
    verdict_rationale: "All four checks pass their mathematical-consistency criteria on independently re-derived equations, type-compatible vocabulary mappings, and fully demonstrated correspondence vectors; the sole issue is Check 4c's mandatory advisory flag for a recognizable prior-art example class."
    failed_checks: []
    flagged_checks: ["Check 4c: prior-art recognition -- the Buckley-Leverett/Kynch-sedimentation pairing instantiates the broader nonconvex scalar-conservation-law example class"]
    quoted_evidence: []
    stage_3_watch_items: ["Confirm whether the specific Buckley-Leverett to Kynch-sedimentation correspondence, beyond the general nonconvex-conservation-law framing it shares with traffic flow, has prior published treatment in sedimentation-consolidation or multiphase-porous-media literature.", "Check precision of the Corey relative-permeability label in Section 3: the entry fixes the Corey exponent at 2 (quadratic S^2/(1-S)^2 form) rather than leaving it as a free parameter.", "Check the Section 4 numerical-diffusion estimate D_num = (v_inf * delta_z / 2) * max|g prime| against the truncation-error term for a first-order flux-vector-splitting scheme specifically, since the formula used is a generic leading-order upwind-type approximation."]
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "FLAG"
    verdict_rationale: "The entry is mathematically coherent overall, but it contains a nonfatal overgeneralization in the entropy-condition discussion and triggers an advisory prior-art flag."
    failed_checks: []
    flagged_checks:
      - "Check 3: Vector 3 overgeneralizes the tangent condition as reducing to Lax/Oleinik for convex fluxes; the specific Welge/Kynch tangent equations are valid, but the explanatory claim is not."
      - "Check 4: Prior-art advisory only—Buckley-Leverett and Kynch sedimentation are already linked in standard scalar conservation-law treatments."
    quoted_evidence: []
    stage_3_watch_items:
      - "Prior-art search for Buckley-Leverett ↔ Kynch scalar conservation-law analogy, e.g. LeVeque finite-volume/textbook treatments and thickener design literature."
      - "Human reviewer should consider tightening or correcting the sentence 'Where the flux is locally convex, this tangent condition reduces to the standard Lax/Oleinik characteristic-entrainment requirement.'"
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "FLAG"
    verdict_rationale: "All mathematical derivations are rigorously correct and the hypothesis is falsifiable, but the domain pairing is flagged as canonical prior art found in standard graduate conservation-law textbooks."
    failed_checks: []
    flagged_checks: ["Check 4: Canonical prior art recognized (scalar conservation law textbook examples)"]
    quoted_evidence: []
    stage_3_watch_items: ["Prior-Art Recognition: The Buckley-Leverett and Kynch sedimentation models are routinely taught together as canonical examples of non-convex scalar hyperbolic conservation laws (e.g., in LeVeque's *Numerical Methods for Conservation Laws*). Stage 3 should verify if the engineering transfer proposed is genuinely novel."]
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "All five correspondence vectors are demonstrated with correct equations and derivations, both equations belong to the same class (scalar hyperbolic conservation law), all vocabulary mappings are type-compatible, and the transfer is asymmetric with a concrete falsifiable prediction."
    failed_checks: []
    flagged_checks: ["Check 4c: prior-art advisory — Buckley-Leverett ↔ Kynch correspondence is a recognized interdisciplinary analogy"]
    quoted_evidence: []
    stage_3_watch_items: ["The Buckley-Leverett / Kynch / scalar-conservation-law correspondence is a well-known analogy in petroleum engineering and mineral-processing textbooks (e.g., Lake's Enhanced Oil Recovery; Bustos, Concha & Bürger's Sedimentation and Thickening). Stage 3 should verify whether the specific nonconvexity parameter mapping (M ↔ n), the Welge/Kynch entropy tangent parallel, and the front-tracking methodological transfer proposal constitute genuinely novel contributions beyond the canonical conservation-law isomorphism.", "Verify that the Richardson-Zaki flux convention g(φ)=φ(1−φ)^n used here (as opposed to the alternative g(φ)=φ(1−phi)^{n-1} convention) matches the specific sedimentation references the entry would cite, and that n values are consistent."]
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "FLAG"
    verdict_rationale: "All four mathematical checks pass with no fatal flaws — equations are correctly attributed and derived, vocabulary mappings are type-coherent with named shared structure, all five correspondence vectors are demonstrated, and the falsifiable prediction is specific and numerically consistent — but prior-art recognition of the Buckley-Leverett ↔ Kynch sedimentation pairing as a known scalar-conservation-law isomorphism triggers an advisory FLAG for Stage 3 novelty review."
    failed_checks: []
    flagged_checks: ["Check 4: Recognized prior art — the Buckley-Leverett ↔ Kynch sedimentation correspondence as instances of the same scalar hyperbolic conservation law, together with the proposed transfer of entropy-correct Riemann solvers / front-tracking / Godunov schemes into sedimentation modeling, are both established in the mathematical sedimentation literature (Bürger, Diehl, Karlsen, Towers, Berres; CENTPACK).", "Check 4: Asymmetry rationale may be weakened because the academic sedimentation literature already contains high-resolution shock-capturing methods for Kynch-type equations, so the claimed gap between the two fields' toolkits may be an industrial-practice gap rather than a disciplinary-knowledge gap."]
    quoted_evidence: []
    stage_3_watch_items: ["Prior-art / novelty: Determine whether the Buckley-Leverett ↔ Kynch sedimentation operator-class isomorphism is already explicit in graduate textbooks or widely-cited reviews on scalar conservation laws (e.g., LeVeque, Dafermos) and in the Bürger/Diehl/Karlsen/Towers sedimentation-theory corpus; if so, the entry's novelty claim narrows to the specific industrial-transfer framing.", "Asymmetry direction: Probe whether industrial thickener control genuinely lacks reservoir-grade shock-capturing methods, or whether the academic sedimentation community (CENTPACK, Bürger et al. 1998+) has already developed and disseminated front-tracking/entropy-solution methods to the target practitioner community; the transfer may be academic-sedimentation-theory → industrial-thickener-practice rather than petroleum → sedimentation.", "Constitutive equivalence: The entry self-reports constitutive_equivalence_confidence as 'low' and primary_failure_risk as 'constitutive_flux_and_regularization_mismatch'; Stage 3 should assess whether operator-class equivalence alone is a defensible 'isomorphism' given that the two constitutive fluxes (Corey fractional flow vs Richardson-Zaki hindered settling) share only the abstract conservation-law shell, not any specific flux geometry.", "Welge tangent scope: The entry correctly scopes the tangent construction to the capillary-free / compression-free limit; verify that the claimed 'Welge ↔ Kynch' tangent-construction identity is not already a named result in the sedimentation-theory literature (Bürger & Karlsen explicitly invoke Oleinik/entropy conditions for Kynch shocks).", "Falsifiability baseline fairness: The 'first-order flux-vector-splitting' baseline label is imprecise for a scalar law (flux-vector splitting is a system-scale technique); Stage 3 may wish to confirm the intended baseline is standard first-order upwind and that the predicted 12 mm → 5 mm interface-thickness reduction is not an artifact of comparing against an unfairly diffusive reference scheme."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "FLAG"
    verdict_rationale: "The governing scalar-conservation-law correspondence and the first four vectors are mathematically supported, but the fifth vector asserts a parameter-to-parameter flux-shape mapping without deriving an actual relation between M and n."
    failed_checks: []
    flagged_checks: ["Check 3: flux_nonconvexity_shape_parameter_mapping is only partially demonstrated; the body derives separate curvature/inflection conditions for M and n but does not establish a mathematical mapping between the two parameters."]
    quoted_evidence: []
    stage_3_watch_items: ["Check 4: verify the asserted first-order flux-vector-splitting numerical-diffusion coefficient and the conversion of D_num/U_B into a 10%-90% shock-thickness estimate; these quantitative baseline claims are not derived from a specified discretization in the entry.", "Check 3: determine whether the intended M ↔ n correspondence requires an explicit parameter transformation rather than merely showing that both parameters affect their respective flux curvature.", "Check 4c: the Buckley-Leverett ↔ Kynch/sedimentation scalar-conservation-law analogy is a recognizable interdisciplinary correspondence; probe the published record for prior formulations of this mathematical bridge."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "The entry consistently demonstrates an operator-level isomorphism between two scalar hyperbolic conservation laws, provides explicit equations for each claimed correspondence, and supplies a concrete, falsifiable transfer experiment."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify that the constitutive closures f_w(S) and g(φ) are treated only as distinct constitutive inputs in Stage 3 bibliometrics and that no implicit claim of physical equivalence is assumed when proposing numerical transfer."
      - "Examine the entry's statement about regularization: confirm whether capillary-pressure diffusion (Silo A) and compressive-yield diffusion (Silo B) can be matched by a single parabolic regularization in practice; the entry explicitly excludes mapping these without separate matched regularizations."
      - "Check the numerical constants and units in the falsifiable prediction (grid spacing, v_∞, computed σ and U_B) for transcription or unit-conversion errors when reproducing the benchmark experiment."
      - "Confirm that the mapping of flux-shape parameters (M ↔ n) is presented as a control-parameter analogy rather than a claim of parametric identity; probe whether the Stage 3 reviewer finds this mapping sufficiently justified for methodological transfer."
      - "Assess prior-art overlap with canonical textbook analogies between Buckley-Leverett and Kynch theory (if any) as an advisory watch item for Stage 3; the entry's novelty claim should be checked against established interdisciplinary literature."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: equations are valid scalar hyperbolic conservation laws of matching class, vocabulary mappings are type-compatible with explicit shared structure, all five listed vectors are fully demonstrated by equations and derivations, and the transfer is asymmetric with a concrete falsifiable numerical prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Bibliometric probe for prior mathematical treatments that already equate Buckley-Leverett fractional-flow and Kynch sedimentation as instances of the same nonconvex scalar conservation law (including shared Rankine-Hugoniot and tangent entropy constructions)."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "Entry demonstrates consistent scalar-hyperbolic operator equivalence across five vectors with correctly typed Buckley-Leverett and Kynch equations, compatible vocabulary mappings, and a specific thresholded falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Bibliometric check should probe Bürger-type sedimentation literature and conservation-law textbooks for prior co-citation of Buckley-Leverett and Kynch as scalar conservation laws with Welge/Kynch tangent constructions; pairing is not canonical textbook identity like Black-Scholes↔heat but is within same operator class and may have specialized prior art."]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0035

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Petroleum reservoir fractional-flow analysis of one-dimensional, immiscible waterflooding, where the water saturation front propagates through a porous medium under a prescribed total Darcy velocity.
*   **Silo B (Field 2):** Mineral-processing gravity thickening and batch sedimentation, where a solids volume fraction profile evolves under hindered settling in a quiescent column.
*   **Mathematical Isomorphism:** In the capillary-free, compression-free, one-dimensional limit and after explicit nondimensionalization, both systems are instances of the scalar hyperbolic conservation-law operator `C_F[u] = ∂_τ u + ∂_ξ F(u) = 0`, so their characteristic speeds, Rankine-Hugoniot shock speeds, Welge/Kynch entropy tangent selections, integral volume balances, and flux-nonconvexity control parameters are the same mathematical structures, with the domain-specific fluxes `f_w(S_w)` and `g(φ_s)` supplying only constitutive closure.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `S_w` ↔ `φ_s`
    *   *Operator Role:* Both are the conserved scalar state `u` in the operator `C_F[u] = ∂_τ u + ∂_ξ F(u) = 0`. Both are dimensionless volume fractions in `[0,1]`. The identification is `u = S_w = φ_s` after the scalings `τ_A = v_t t / (ϕ_p L)` and `τ_B = v_∞ t / L`, with `ξ = x/L` and `ζ = z/L`.
*   `f_w(S_w)` ↔ `g(φ_s)`
    *   *Operator Role:* Both are the nonlinear flux `F(u)` entering the same conservation-law operator. Their derivatives `f_w'(S_w)` and `g'(φ_s)` are the characteristic speeds in `dξ/dτ = F'(u)`. The fluxes are not symbol relabelings: `f_w` is Corey relative-permeability fractional flow, while `g` is Richardson-Zaki hindered-settling flux.
*   `v_t / ϕ_p` ↔ `v_∞`
    *   *Operator Role:* Both are the dimensional velocity scales converting a dimensionless Rankine-Hugoniot speed `σ = [F]/[u]` into a physical discontinuity speed: `U_A = (v_t/ϕ_p) σ_f` for the waterflood front and `U_B = v_∞ σ_g` for the sedimentation concentration jump.
*   `S_f` ↔ `φ_j`
    *   *Operator Role:* Both are entropy-selected shock states determined by the same tangent condition `F'(u^*) = (F(u^*) - F(u_0))/(u^* - u_0)`. In Silo A this is the Welge front saturation `S_f`; in Silo B this is the Kynch jump concentration `φ_j`.
*   `M` ↔ `n`
    *   *Operator Role:* Both are dimensionless flux-shape parameters controlling loss of convexity and therefore admissible shock structure. `M` enters the fractional-flow curvature condition `f_w''(S)=0`; `n` enters the hindered-settling curvature condition `g''(φ_s)=0`, whose inflection point is `φ_s = 2/(n+1)`.

## 3. CORE MATHEMATICAL PARALLELISM

Silo A models waterflooding with the Buckley-Leverett fractional-flow equation. For one-dimensional, incompressible, homogeneous flow with capillary pressure neglected, water saturation `S_w(x,t)` satisfies

```math
\varphi_p \frac{\partial S_w}{\partial t}
+
v_t \frac{\partial f_w(S_w)}{\partial x}
= 0,
```

where `ϕ_p` is porosity and `v_t` is the imposed total Darcy velocity. With Corey endpoint relative permeabilities and no residual saturations, the fractional-flow curve is

```math
f_w(S_w)
=
\frac{M S_w^2}{M S_w^2 + (1-S_w)^2},
\qquad
M = \frac{\mu_o}{\mu_w}.
```

Introducing the dimensionless coordinate `ξ = x/L` and dimensionless time `τ_A = v_t t / (ϕ_p L)` gives

```math
\frac{\partial S_w}{\partial \tau_A}
+
\frac{\partial f_w(S_w)}{\partial \xi}
= 0.
```

Silo B models gravity thickening in the hindered-settling regime with Kynch’s solids continuity equation. For a batch column with vertical coordinate `z` taken positive downward, the solids volume fraction `φ_s(z,t)` obeys

```math
\frac{\partial \phi_s}{\partial t}
+
v_\infty \frac{\partial g(\phi_s)}{\partial z}
= 0,
\qquad
g(\phi_s) = \phi_s(1-\phi_s)^n,
```

where `v_∞` is the isolated-particle terminal settling velocity and `n` is the Richardson-Zaki hindered-settling exponent. With `ζ = z/L` and `τ_B = v_∞ t / L`,

```math
\frac{\partial \phi_s}{\partial \tau_B}
+
\frac{\partial g(\phi_s)}{\partial \zeta}
= 0.
```

The bridge is the identification

```math
u = S_w = \phi_s,
\qquad
\tau_A = \tau_B = \tau,
\qquad
\xi = \zeta,
\qquad
F(u) =
\begin{cases}
f_w(u), & \text{Silo A},\\
g(u), & \text{Silo B}.
\end{cases}
```

Under this identification, both systems are governed by

```math
C_F[u] \equiv \frac{\partial u}{\partial \tau}
+
\frac{\partial F(u)}{\partial \xi}
= 0.
```

The equivalence is an operator-class equivalence for scalar hyperbolic conservation laws, not an assertion that `f_w` and `g` are identical constitutive laws. The mapping holds for shock speed, entropy selection, characteristic structure, and integral conservation in the absence of regularization. It stops where Silo A adds capillary-pressure diffusion or Silo B adds compressive-yield diffusion, unless those diffusive terms are separately mapped as matched parabolic regularizations, which is not claimed here.

### Demonstrated vector 1: `nondimensional_scalar_conservation_operator`

Silo A nondimensional equation:

```math
\frac{\partial S_w}{\partial \tau_A}
+
\frac{\partial f_w(S_w)}{\partial \xi}
= 0.
```

Silo B nondimensional equation:

```math
\frac{\partial \phi_s}{\partial \tau_B}
+
\frac{\partial g(\phi_s)}{\partial \zeta}
= 0.
```

With `u = S_w = φ_s`, `τ_A = τ_B = τ`, and `ξ = ζ`, both become

```math
\frac{\partial u}{\partial \tau}
+
\frac{\partial F(u)}{\partial \xi}
= 0.
```

The associated characteristic equations are identical in form:

```math
\frac{d\xi}{d\tau} = f_w'(S_w)
```

for Silo A, and

```math
\frac{d\zeta}{d\tau} = g'(\phi_s)
```

for Silo B.

### Demonstrated vector 2: `rankine_hugoniot_shock_speed_velocity_scaling`

Let a discontinuity connect left state `u_L` to right state `u_R`. For any scalar conservation law `∂_τ u + ∂_ξ F(u)=0`, the dimensionless shock speed is

```math
\sigma
=
\frac{d\xi_s}{d\tau}
=
\frac{F(u_R)-F(u_L)}{u_R-u_L}.
```

For Silo A, the dimensional waterflood shock speed is therefore

```math
U_A
=
\frac{d x_s}{dt}
=
\frac{v_t}{\varphi_p}
\frac{f_w(S_R)-f_w(S_L)}{S_R-S_L}.
```

For Silo B, the dimensional sedimentation concentration-jump speed is

```math
U_B
=
\frac{d z_s}{dt}
=
v_\infty
\frac{g(\phi_R)-g(\phi_L)}{\phi_R-\phi_L}.
```

Both are the same Rankine-Hugoniot jump condition scaled by the respective velocity factor identified in the vocabulary matrix.

### Demonstrated vector 3: `welge_kynch_entropy_tangent_shock_selection`

For nonconvex fluxes, the physically admissible shock state is selected by a tangent construction. In Silo A, the Welge front saturation `S_f` from initial water saturation `S_{wi}` satisfies

```math
f_w'(S_f)
=
\frac{f_w(S_f)-f_w(S_{wi})}{S_f-S_{wi}}.
```

In Silo B, the Kynch jump concentration `φ_j` from initial solids fraction `φ_0` satisfies

```math
g'(\phi_j)
=
\frac{g(\phi_j)-g(\phi_0)}{\phi_j-\phi_0}.
```

Both are the same entropy-admissibility condition written for their respective fluxes:

```math
F'(u^*)
=
\frac{F(u^*)-F(u_0)}{u^*-u_0}.
```

Where the flux is locally convex, this tangent condition reduces to the standard Lax/Oleinik characteristic-entrainment requirement. For a shock with `u_L > u_R`,

```math
F'(u_L) > \sigma > F'(u_R),
```

with the inequalities reversed when the state ordering is reversed.

### Demonstrated vector 4: `integral_phase_volume_conservation_law`

Integrating the nondimensional conservation law over an interval `[a,b]` gives

```math
\frac{d}{d\tau}
\int_a^b u(\xi,\tau)\,d\xi
=
F(u(a,\tau)) - F(u(b,\tau)).
```

In dimensional Silo A variables, the conserved water volume in a core of cross-sectional area `A` is

```math
V_w = A \varphi_p L \int_a^b S_w(\xi,\tau)\,d\xi,
```

and its balance is

```math
\frac{dV_w}{dt}
=
A v_t
\left[
f_w(S_w(a,t)) - f_w(S_w(b,t))
\right].
```

In dimensional Silo B variables, the conserved solids volume is

```math
V_s = A L \int_a^b \phi_s(\zeta,\tau)\,d\zeta,
```

with balance

```math
\frac{dV_s}{dt}
=
A v_\infty
\left[
g(\phi_s(a,t)) - g(\phi_s(b,t))
\right].
```

The conserved extensive quantity differs physically—water volume versus solids volume—but the operator-level balance law is identical.

### Demonstrated vector 5: `flux_nonconvexity_shape_parameter_mapping`

Silo A fractional-flow curvature is controlled by the mobility ratio `M`. Differentiating

```math
f_w(S)
=
\frac{M S^2}{M S^2 + (1-S)^2}
```

gives

```math
f_w'(S)
=
\frac{2 M S(1-S)}
{\left[M S^2 + (1-S)^2\right]^2}.
```

The inflection condition is

```math
f_w''(S)=0
\quad\Longleftrightarrow\quad
2(M+1)S^3 - 3(M+1)S^2 + 1 = 0.
```

Silo B hindered-settling curvature is controlled by the Richardson-Zaki exponent `n`. Since

```math
g(\phi) = \phi(1-\phi)^n,
```

its first derivative is

```math
g'(\phi)
=
(1-\phi)^{n-1}
\left[
1-(n+1)\phi
\right],
```

and its second derivative is

```math
g''(\phi)
=
n(1-\phi)^{n-2}
\left[
(n+1)\phi - 2
\right].
```

Thus the Silo B inflection point is

```math
\phi_* = \frac{2}{n+1}.
```

In both silos, a dimensionless constitutive parameter—`M` in fractional flow, `n` in hindered settling—controls flux nonconvexity, which in controls which shocks are entropy-admissible.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** petroleum-reservoir-fractional-flow → gravity-thickening-sedimentation
*   **Asymmetric Maturity Rationale:** Petroleum reservoir simulation has developed a mature operational toolkit for nonconvex scalar fractional-flow problems: Welge tangent analysis, high-resolution Godunov schemes, front tracking, Riemann-problem solvers, and streamline-based shock propagation under heterogeneous boundary conditions. Gravity thickening possesses mature steady-state flux analysis, batch settling tests, and compressive rheology characterization, but industrial thickener control still frequently relies on low-order transient solvers or graphical Kynch constructions that are less robust when feed concentration shocks, flocculant changes, or underflow drawdown perturbations create moving nonconvex discontinuities. The target field is not generally immature; it specifically lacks reservoir-grade dynamic front tracking for transient nonconvex concentration jumps.
*   **Target Bottleneck Mitigation:** Importing reservoir-style front-tracking and entropy-correct Riemann solvers into Kynch sedimentation modeling will reduce artificial numerical diffusion of concentration jumps, improve prediction of interface arrival times, and enable feed-forward thickener control. The hypothesis is that the persistent bottleneck of spurious interface smearing in low-order thickener simulators is primarily numerical, not physical, in the hindered-settling regime, and can be removed by shock-capturing methods already standard in fractional-flow reservoir simulation.
*   **Falsifiable Prediction:** Consider a 1.00 m batch settling column initialized with a sharp step between clear supernatant and a monodisperse hindered-settling suspension:

```math
\phi_L = 0,
\qquad
\phi_R = 0.20,
\qquad
n = 4,
\qquad
v_\infty = 1.00 \times 10^{-4}\ \mathrm{m\,s^{-1}},
\qquad
N = 100,
\qquad
\Delta z = \frac{1.00\ \mathrm{m}}{100} = 1.00 \times 10^{-2}\ \mathrm{m}.
```

The dimensionless Rankine-Hugoniot speed of the concentration jump is

```math
\sigma
=
\frac{g(\phi_R)-g(\phi_L)}{\phi_R-\phi_L}
=
(1-0.20)^4
=
0.4096.
```

The physical shock speed is therefore

```math
U_B = v_\infty \sigma
=
4.096 \times 10^{-5}\ \mathrm{m\,s^{-1}}.
```

If the initial interface is at `z=0` and a concentration sensor is placed at `z=0.500 m`, the exact hyperbolic arrival time is

```math
t_{0.5}
=
\frac{0.500\ \mathrm{m}}{U_B}
=
1.2207 \times 10^4\ \mathrm{s}.
```

A reservoir-style front-tracking implementation must predict this arrival time within one half grid cell:

```math
\epsilon_t
=
\frac{0.5\,\Delta z}{U_B}
=
122\ \mathrm{s},
```

and must produce a measured 10%-90% interface thickness no larger than

```math
\delta_{\mathrm{FT}}
\le
0.5\,\Delta z
=
5.0 \times 10^{-3}\ \mathrm{m}.
```

The named state-of-the-art baseline is a first-order flux-vector-splitting Kynch thickener simulator on the same `N=100` grid. Its leading numerical diffusion coefficient is

```math
D_{\mathrm{num}}
=
\frac{v_\infty \Delta z}{2}
\max_{\phi\in[0,0.20]} |g'(\phi)|.
```

For `g(φ)=φ(1-φ)^4`, `g'(0)=1` and `g'(φ)≥0` on `[0,0.20]`, so

```math
D_{\mathrm{num}}
=
\frac{(1.00\times10^{-4})(1.00\times10^{-2})}{2}
=
5.0 \times 10^{-7}\ \mathrm{m^2\,s^{-1}}.
```

The corresponding numerical shock thickness estimate is

```math
\delta_{\mathrm{FO}}
\approx
\frac{D_{\mathrm{num}}}{U_B}
=
1.22 \times 10^{-2}\ \mathrm{m}.
```

Therefore the falsifiable prediction is: in ultrasonic or optical concentration profiling of the benchmark column, front tracking must reduce the measured 10%-90% interface thickness from at least `12 mm` for the first-order baseline to no more than `5 mm`, and must reduce arrival-time error to no more than `122 s`. The hypothesis is falsified if front tracking yields interface thickness greater than `5 mm`, arrival-time error greater than `122 s`, or fails to outperform the first-order Kynch baseline by at least a factor of two in interface thickness on the same grid.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Buckley-Leverett" AND "fractional flow" AND "Welge tangent"`
*   `"Kynch" AND "batch sedimentation" AND "Rankine-Hugoniot" AND "hindered settling"`
*   `"Buckley-Leverett" AND "Kynch" AND "gravity thickening" AND "front tracking"`
*   `"fractional flow" AND "sedimentation" AND "scalar conservation law" AND "entropy condition"`
*   `"thickener control" AND "shock capturing" AND "Kynch theory"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A's φ_p∂S_w/∂t + v_t∂f_w/∂x=0 and Silo B's ∂φ_s/∂t + v_∞∂g/∂z=0 are both correctly-stated first-order nonlinear scalar hyperbolic conservation laws of the same class; their nondimensionalized forms were independently re-derived by symbolic chain-rule substitution and match the entry's ∂u/∂τ+∂F(u)/∂ξ=0 exactly, with f_w and g kept as distinct constitutive closures rather than being asserted identical.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — every pairing (S_w↔φ_s, f_w↔g, v_t/φ_p↔v_∞, S_f↔φ_j, M↔n) matches compatible mathematical types (state variable, flux, velocity scale, shock state, and dimensionless shape parameter respectively on both sides), and each Operator Role names a specific shared equation rather than relying on hedged language alone.
- **CHECK 3 (Correspondence Vector Support):** PASS — all five YAML-listed vectors are demonstrated in Section 3 with matched equations on both sides (nondimensional_scalar_conservation_operator, rankine_hugoniot_shock_speed_velocity_scaling, welge_kynch_entropy_tangent_shock_selection, integral_phase_volume_conservation_law, flux_nonconvexity_shape_parameter_mapping). The f_w', f_w'' inflection cubic 2(M+1)S³−3(M+1)S²+1=0, g', g'', and inflection point φ*=2/(n+1) were independently re-derived symbolically and match the entry exactly.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — (a) asymmetry is field-specific rather than generic (petroleum's front-tracking/Riemann-solver toolkit vs. thickener control's reliance on low-order transient solvers for nonconvex concentration jumps specifically) and shows no sign of being backwards; (b) the falsifiable prediction names concrete measurable thresholds (≤5 mm interface thickness, ≤122 s arrival-time error, ≥2x improvement over the first-order baseline), and every intermediate number (σ=0.4096, U_B=4.096×10⁻⁵ m/s, t≈12207 s, D_num=5.0×10⁻⁷ m²/s, δ_FO≈12.2 mm) was independently recomputed and matches the entry exactly; (c) however, this domain pairing is recognizable as an instance of the broader "nonconvex scalar conservation law" example class that recurs alongside traffic flow in applied-PDE pedagogy and sedimentation-modeling literature — flagged here as advisory only, per protocol, not as grounds for rejection.

#### Stage 3 Watch Items
- Confirm whether the specific Buckley-Leverett ↔ Kynch-sedimentation correspondence, beyond the general nonconvex-conservation-law framing it shares with traffic flow, has prior published treatment in sedimentation-consolidation or multiphase-porous-media literature.
- Check precision of the "Corey relative-permeability" label in Section 3: the entry fixes the Corey exponent at 2 (quadratic S²/(1−S)² form) rather than leaving it as a free parameter.
- Check the Section 4 numerical-diffusion estimate against the truncation-error term for a first-order flux-vector-splitting scheme specifically, since the formula used is a generic leading-order upwind-type approximation.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed Buckley-Leverett and Kynch conservation equations, nondimensionalizations, Rankine-Hugoniot speeds, integral balances, and curvature expressions are mathematically valid and support the scalar hyperbolic operator-class mapping claimed in Section 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are type-compatible scalar states, scalar fluxes, velocity scales, shock states, and dimensionless shape parameters; no category errors or unmotivated dimensional mappings are identified.
- **CHECK 3 (Correspondence Vector Support):** FLAG — All five listed vectors are demonstrated by equations in Section 3, but the supporting explanation for vector 3 contains the incorrect statement "Where the flux is locally convex, this tangent condition reduces to the standard Lax/Oleinik characteristic-entrainment requirement." A tangent equality F'(u*)=σ does not reduce to strict Lax inequalities F'(u_L)>σ>F'(u_R); these are different admissibility statements. The specific Welge and Kynch tangent equations are otherwise valid, so this is a nonfatal overgeneralization.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is asymmetric in the required direction and the prediction is specific and falsifiable. However, I recognize this domain pairing as a canonical scalar hyperbolic conservation-law analogy (Buckley-Leverett ↔ Kynch), which triggers an advisory prior-art FLAG for Stage 3 bibliometric review.

#### Stage 3 Watch Items
- Prior-art probe: Buckley-Leverett and Kynch sedimentation as scalar conservation laws, including finite-volume textbook treatments (e.g., LeVeque) and gravity-thickening/Kynch design literature.
- Have a human reviewer examine and, if needed, correct the sentence in vector 3: "Where the flux is locally convex, this tangent condition reduces to the standard Lax/Oleinik characteristic-entrainment requirement."
- Bibliometric check for existing explicit mappings between Welge tangent and Kynch tangent in thickener design.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the Buckley-Leverett and Kynch models are correctly formulated, explicitly nondimensionalized, and accurately mapped to the scalar hyperbolic conservation law operator without any equation-class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All terms in the vocabulary matrix correctly map mathematically equivalent state variables, fluxes, velocities, and dimensionless parameters with precisely defined shared mathematical roles.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed correspondence vectors (`nondimensional_scalar_conservation_operator`, `rankine_hugoniot_shock_speed_velocity_scaling`, `welge_kynch_entropy_tangent_shock_selection`, `integral_phase_volume_conservation_law`, and `flux_nonconvexity_shape_parameter_mapping`) are explicitly demonstrated with correct equations and derivations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer rationale specifies a valid asymmetric direction and provides a highly rigorous, measurable, and falsifiable prediction; however, the domain pairing is flagged as canonical prior art (standard graduate textbook examples of scalar non-convex conservation laws, e.g., LeVeque's *Numerical Methods for Conservation Laws*).

#### Stage 3 Watch Items
- Prior-Art Recognition: The isomorphism between the Buckley-Leverett fractional flow equation and Kynch's batch sedimentation model is a canonical analogy for non-convex scalar hyperbolic conservation laws, prominently featured in standard applied mathematics texts such as LeVeque's *Numerical Methods for Conservation Laws* or Dafermos's *Hyperbolic Conservation Laws in Continuum Physics*. Stage 3 should evaluate whether the proposed numerical transfer (high-resolution front tracking for industrial Kynch thickener control) represents a novel operational application despite the underlying mathematical pairing being heavily documented in the mathematical physics literature.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the Buckley-Leverett fractional-flow equation and the Kynch sedimentation equation are genuine scalar hyperbolic conservation laws from their stated domains; all derivatives ($f_w'$, $f_w''$, $g'$, $g''$), inflection conditions, and numerical values in the falsifiable prediction (Rankine-Hugoniot speed, arrival time, diffusion coefficient, interface thickness) are algebraically correct.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five paired mappings ($S_w \leftrightarrow \phi_s$, $f_w \leftrightarrow g$, $v_t/\phi_p \leftrightarrow v_\infty$, $S_f \leftrightarrow \phi_j$, $M \leftrightarrow n$) are between objects of compatible mathematical type, and each Operator Role explanation identifies a specific shared structure rather than hedging.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated with explicit equations and derivations: vector 1 (nondimensional operator, Section 3 main derivation), vector 2 (Rankine-Hugoniot speed with velocity scaling, Demonstrated vector 2), vector 3 (Welge/Kynch tangent condition, Demonstrated vector 3), vector 4 (integral conservation balance, Demonstrated vector 4), vector 5 (flux curvature analysis via $f_w''$ and $g''$, Demonstrated vector 5).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (petroleum → sedimentation) is genuinely asymmetric: the rationale correctly identifies that reservoir simulation has mature high-resolution Godunov/front-tracking tools for nonconvex scalar conservation laws while industrial thickener simulators still use low-order methods. The prediction is concrete and falsifiable with specific thresholds (interface thickness ≤ 5 mm, arrival-time error ≤ 122 s, factor-of-two improvement over first-order baseline). Advisory: the Buckley-Leverett ↔ Kynch conservation-law correspondence is a recognized interdisciplinary analogy in petroleum and mineral-processing textbooks; Stage 3 should verify novelty of the specific parameter mapping and methodological transfer proposal.

#### Stage 3 Watch Items
- The Buckley-Leverett / Kynch / scalar-hyperbolic-conservation-law isomorphism is a well-known canonical analogy (e.g., Lake, *Enhanced Oil Recovery*; Bustos, Concha & Bürger, *Sedimentation and Thickening*; LeVeque, *Numerical Methods for Conservation Laws*). Stage 3 should determine whether the entry's specific contributions — the nonconvexity parameter mapping ($M \leftrightarrow n$), the systematic entropy-tangent parallel, and the proposed asymmetric methodological transfer of front-tracking techniques — go beyond what is already established in these sources.
- The entry uses the Richardson-Zaki convention $g(\phi) = \phi(1-\phi)^n$ rather than the alternative $g(\phi) = \phi(1-\phi)^{n-1}$. Stage 3 should confirm that the cited literature uses the same convention and that $n$ values are consistent with the stated domain.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the Buckley-Leverett equation `ϕ_p ∂S_w/∂t + v_t ∂f_w(S_w)/∂x = 0` and the Kynch equation `∂φ_s/∂t + v_∞ ∂g(φ_s)/∂z = 0` are genuinely first-order quasilinear hyperbolic scalar conservation laws from their stated domains, the nondimensionalizations to `∂u/∂τ + ∂F(u)/∂ξ = 0` are algebraically correct, and the Corey flux `f_w = M S²/(M S² + (1-S)²)`, Richardson-Zaki flux `g = φ(1-φ)^n`, and the inflection conditions `2(M+1)S³ - 3(M+1)S² + 1 = 0` and `φ_* = 2/(n+1)` were independently re-derived and verified; no equation-class mismatch, no misattribution.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each of the five pairs maps objects of compatible mathematical type (`S_w ↔ φ_s` both dimensionless conserved scalars in [0,1]; `f_w ↔ g` both constitutive fluxes `F(u)`; `v_t/ϕ_p ↔ v_∞` both dimensional velocity scales; `S_f ↔ φ_j` both entropy-selected shock states; `M ↔ n` both dimensionless flux-shape parameters), and every Operator Role specifies a named shared mathematical structure (the operator `C_F[u]`, the characteristic equation `dξ/dτ = F'(u)`, the Rankine-Hugoniot scaling, the tangent condition `F'(u*) = (F(u*)-F(u_0))/(u*-u_0)`, and the curvature condition `F''=0`) rather than relying on hedged analogy language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated in the body with equations or derivations: vector 1 (`nondimensional_scalar_conservation_operator`) is shown in Section 3 / Demonstrated vector 1 via both nondimensional equations collapsing to `∂u/∂τ + ∂F(u)/∂ξ = 0`; vector 2 (`rankine_hugoniot_shock_speed_velocity_scaling`) is shown via the RH jump `σ = [F]/[u]` and both dimensional speeds `U_A`, `U_B`; vector 3 (`welge_kynch_entropy_tangent_shock_selection`) is shown via both tangent equations and the unified `F'(u*) = (F(u*)-F(u_0))/(u*-u_0)` plus the Lax/Oleinik inequality; vector 4 (`integral_phase_volume_conservation_law`) is shown via the integrated balance for both silos; vector 5 (`flux_nonconvexity_shape_parameter_mapping`) is shown via the derived inflection conditions for both fluxes. No vector is merely named.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The falsifiable prediction is genuinely specific and internally consistent (verified: `σ = 0.4096`, `U_B = 4.096×10⁻⁵ m/s`, `t_0.5 = 1.2207×10⁴ s`, `ε_t = 122 s`, `D_num = 5.0×10⁻⁷ m²/s`, `δ_FO ≈ 1.22×10⁻² m` all recompute correctly), and the asymmetry direction (petroleum → thickening) is defensible within the entry's own industrial-practice framing. However, (c) prior-art is recognized: the Buckley-Leverett ↔ Kynch sedimentation correspondence as a shared scalar hyperbolic conservation law, and the specific transfer of entropy-correct Riemann solvers / Godunov / front-tracking schemes to sedimentation, are both established in the mathematical sedimentation literature (Bürger, Diehl, Karlsen, Towers, Berres; CENTPACK), which confirms Kynch sedimentation is routinely treated as a scalar conservation law with entropy solutions 【turn0search6】【turn0search8】. This is advisory only and not grounds for REJECT.

#### Stage 3 Watch Items
- Prior-art / novelty: Whether the Buckley-Leverett ↔ Kynch operator-class isomorphism and the proposed front-tracking transfer are already explicit in conservation-law textbooks (LeVeque, Dafermos) and the Bürger/Diehl/Karlsen/Towers sedimentation corpus; if so, the entry's novelty narrows to its industrial-transfer framing.
- Asymmetry: Whether the claimed gap is a disciplinary-knowledge gap or merely an industrial-adoption gap, given that the academic sedimentation community already publishes high-resolution shock-capturing schemes for Kynch equations; the true transfer direction may be academic-sedimentation-theory → industrial-thickener-practice rather than petroleum → sedimentation.
- Constitutive equivalence: The entry self-reports `constitutive_equivalence_confidence: "low"` and `primary_failure_risk: "constitutive_flux_and_regularization_mismatch"`; Stage 3 should judge whether operator-class equivalence alone supports an "isomorphism" label when the two fluxes share only the abstract conservation-law shell.
- Welch tangent scope: Verify the "Welge ↔ Kynch" tangent-construction identity is not already a named result in sedimentation theory (Bürger & Karlsen invoke Oleinik entropy conditions for Kynch shocks).
- Falsifiability baseline fairness: The "first-order flux-vector-splitting" baseline label is imprecise for a scalar law (flux-vector splitting is a system-scale technique); confirm the intended baseline is standard first-order upwind and that the predicted 12 mm → 5 mm improvement is not inflated by an unfairly diffusive reference scheme.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-15

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The Section 3 equations are mutually consistent scalar first-order hyperbolic conservation laws, and the nondimensionalization, Rankine-Hugoniot scaling, tangent conditions, and displayed curvature derivatives are internally consistent.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapping pairs compatible mathematical objects and identifies their shared role in the scalar conservation-law operator rather than merely asserting a verbal analogy.
* **CHECK 3 (Correspondence Vector Support):** FLAG — `nondimensional_scalar_conservation_operator`, `rankine_hugoniot_shock_speed_velocity_scaling`, `welge_kynch_entropy_tangent_shock_selection`, and `integral_phase_volume_conservation_law` are demonstrated in Section 3, but `flux_nonconvexity_shape_parameter_mapping` is only partially established: Section 3 derives separate curvature conditions for `M` and `n` but does not derive an actual mathematical mapping between the two parameters.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated petroleum-reservoir-to-sedimentation transfer is given a concrete asymmetric rationale, and the prediction specifies measurable arrival-time and interface-thickness thresholds with explicit failure criteria; no prior-art recognition is used as a rejection.

#### Stage 3 Watch Items
* Verify the quantitative numerical-diffusion and shock-thickness claims in Section 4 against the particular first-order flux-vector-splitting discretization, since no discrete scheme is specified sufficiently to derive those quantities internally.
* Probe whether the claimed `M ↔ n` correspondence requires an explicit parameter transformation rather than the demonstrated fact that each parameter controls curvature of its own flux.
* Probe the published record for prior formulations of the Buckley-Leverett/Kynch-sedimentation scalar-conservation-law correspondence.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B are presented as one-dimensional, capillary-free (Silo A) and compression-free (Silo B) scalar hyperbolic conservation laws and the entry gives the correct nondimensional forms `∂_τ u + ∂_ξ F(u) = 0` for each silo, so the claimed shared governing operator class is consistent.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired mapping (`S_w ↔ φ_s`, `f_w ↔ g`, `v_t/ϕ_p ↔ v_∞`, `S_f ↔ φ_j`, `M ↔ n`) maps objects of compatible mathematical type (scalar conserved variable, flux function, dimensional velocity scale, entropy-selected shock state, flux-shape parameter) and the Operator Role entries specify explicit shared structures rather than hedged analogies.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed correspondence vectors are demonstrated in the body with equations or derivations: `nondimensional_scalar_conservation_operator` (Section 3 nondimensional forms and unified operator), `rankine_hugoniot_shock_speed_velocity_scaling` (Rankine-Hugoniot formula and dimensional scalings), `welge_kynch_entropy_tangent_shock_selection` (tangent condition equations for Welge and Kynch), `integral_phase_volume_conservation_law` (integrated balance laws and dimensional conserved volumes), and `flux_nonconvexity_shape_parameter_mapping` (derivatives, inflection condition, and explicit `φ_* = 2/(n+1)`), each supported by explicit equations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric (reservoir numerical toolset → thickening simulators) and the entry supplies a concrete, measurable falsifiable prediction (numerical values for shock speed, arrival time, allowable arrival-time error, and interface thickness reduction) rather than a non-specific claim; prior-art recognition is noted as advisory for Stage 3 review.

#### Stage 3 Watch Items
- Verify that the Stage 3 bibliometric review checks for existing literature explicitly connecting Buckley-Leverett fractional flow and Kynch hindered-settling beyond textbook analogies.
- Confirm that the entry's exclusion of matched parabolic regularizations is appropriate and that any proposed numerical transfer does not implicitly rely on unproven equivalence of diffusive regularizations.
- Recompute the numerical benchmark constants (σ, U_B, t_{0.5}, D_num, δ_FO) to ensure no transcription or unit-conversion mistakes before experimental replication.
- Scrutinize the practical mapping of the flux-shape control parameters (`M ↔ n`) in proposed numerical experiments to ensure the analogy is used only to guide numerical method transfer and not to assert physical parameter equivalence.
- Check whether reservoir-grade Riemann solvers/front-tracking implementations require additional domain-specific modifications (e.g., handling of compressive rheology or polydispersity) before being applied to industrial thickener models.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are genuine first-order scalar hyperbolic conservation laws of matching class (Buckley-Leverett fractional-flow and Kynch hindered-settling continuity), and after the stated nondimensionalization they become identical operator instances supporting the claimed structural correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired mapping identifies objects of identical mathematical type (conserved volume-fraction state, nonlinear flux, velocity scale, entropy-selected shock state, dimensionless shape parameter) with an explicit shared operator or algebraic structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors (nondimensional_scalar_conservation_operator, rankine_hugoniot_shock_speed_velocity_scaling, welge_kynch_entropy_tangent_shock_selection, integral_phase_volume_conservation_law, flux_nonconvexity_shape_parameter_mapping) are demonstrated by explicit equations and derivations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by reservoir-grade front-tracking and Riemann-solver maturity versus the target field’s reliance on lower-order or graphical methods for transient nonconvex jumps; the prediction supplies concrete numerical thresholds (arrival-time error ≤122 s, 10–90 % thickness ≤5 mm versus baseline ≈12 mm) that can be measured and can fail.

#### Stage 3 Watch Items
- Bibliometric probe for prior mathematical treatments that already equate Buckley-Leverett fractional-flow and Kynch sedimentation as instances of the same nonconvex scalar conservation law (including shared Rankine-Hugoniot and tangent entropy constructions).

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A equation `varphi_p ∂S_w/∂t + v_t ∂f_w/∂x =0` with `f_w=M S_w^2/(M S_w^2+(1-S_w)^2)` and Silo B equation `∂φ_s/∂t + v_∞ ∂g/∂z=0` with `g=φ_s(1-φ_s)^n` are correctly typed as first-order scalar hyperbolic conservation laws and collapse after stated nondimensionalization to shared operator `C_F[u]=∂_τ u+∂_ξ F(u)=0`; no class mismatch and regularizing diffusive terms are explicitly excluded.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings pair compatible mathematical types: `S_w↔φ_s` scalar state `u∈[0,1]`, `f_w↔g` nonlinear flux `F(u)` with characteristic speed `F'(u)`, `v_t/φ_p↔v_∞` dimensional velocity scale for `U=scale·σ`, `S_f↔φ_j` entropy-selected shock state via tangent condition, `M↔n` dimensionless flux-shape parameter controlling `F''=0`; operator roles name shared structure, not hedged similarity.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors demonstrated in body: `nondimensional_scalar_conservation_operator` via Section 3 nondimensional forms and identification `u=S_w=φ_s`; `rankine_hugoniot_shock_speed_velocity_scaling` via `σ=(F_R-F_L)/(u_R-u_L)` with `U_A=(v_t/φ_p)σ_f` and `U_B=v_∞σ_g`; `welge_kynch_entropy_tangent_shock_selection` via `f_w'(S_f)=(f_w(S_f)-f_w(S_wi))/(S_f-S_wi)`, `g'(φ_j)=(g(φ_j)-g(φ_0))/(φ_j-φ_0)`, general form `F'(u*)=(F(u*)-F(u0))/(u*-u0)` and Lax condition `F'(u_L)>σ>F'(u_R)`; `integral_phase_volume_conservation_law` via `d/dτ∫u dξ=F(a)-F(b)` and dimensional `V_w` and `V_s` balances; `flux_nonconvexity_shape_parameter_mapping` via `f_w''=0 ⇔ 2(M+1)S^3-3(M+1)S^2+1=0` and `g''=n(1-φ)^{n-2}[(n+1)φ-2]` with `φ_*=2/(n+1)`.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuinely directional: petroleum reservoir toolkit (Welge analysis, Godunov, front-tracking, Riemann solvers) → thickener transient control lacking reservoir-grade front tracking, with rationale that target is not generally immature but specifically lacks dynamic shock-capturing; falsifiability satisfied by specific measurable thresholds for a 1.00 m column with `φ_L=0, φ_R=0.20, n=4, v_∞=1e-4 m/s, N=100`: `σ=0.4096`, `U_B=4.096e-5 m/s`, `t_0.5=1.2207e4 s`, required `ε_t=122 s` arrival error and `δ_FT≤5.0e-3 m` vs baseline `D_num=5.0e-7 m2/s`, `δ_FO≈1.22e-2 m`, falsified if thickness >5 mm, error >122 s, or <2× improvement. No canonical textbook identity recognized as grounds for flag.

#### Stage 3 Watch Items
- Verify bibliometric novelty of Buckley-Leverett ↔ Kynch pairing against sedimentation references (Bürger, Wendland, Concha) and conservation-law texts (e.g., LeVeque) that treat both as examples of scalar hyperbolic laws; check for prior explicit Welge tangent ↔ Kynch tangent equivalence.
- Confirm that batch-settling experiments cited for falsifiability (ultrasonic/optical concentration profiling) exist for monodisperse `n=4` case and that `g'(φ)` maximum used for `D_num` bound is valid on `[0,0.20]`.