---
sid_metadata:
  entry_id: "SID-0035"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
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