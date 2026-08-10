---
sid_metadata:
  entry_id: "SID-0033"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "elastohydrodynamic-lubrication-line-contact"
  domain_b: "subglacial-sheet-cavitation-hydrology"
  structural_family: "thin-film-cavitation-reynolds-operators"
  triple_correspondence_vectors:
    - "cubic_mobility_reynolds_potential_operator"
    - "reynolds_smooth_free_boundary_pair"
    - "dimensionless_cavitation_number_unit_threshold"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 8.0
  expected_methodological_transfer_score: 8.9
  community_separation_score: 8.3
  representation_mismatch_score: 6.8
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.1
    uncertainty: "±1.1"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "gap_closure_constitutive_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0033

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Elastohydrodynamic lubrication (EHL) line contacts in tribology, where a thin oil film separates rolling/sliding solids, generates high pressure through a Reynolds wedge, and cavitates when the local pressure reaches a cavitation threshold.
*   **Silo B (Field 2):** Subglacial distributed-sheet hydrology beneath sliding glaciers, where a millimetre-to-centimetre water sheet at the ice–bed interface is forced by basal sliding over rough topography and loses contact when the effective pressure (ice hydraulic potential minus water hydraulic potential) approaches zero.
*   **Mathematical Isomorphism:** In the one-dimensional, steady, isoviscous, source-free lubrication limit with a locally constant ice hydraulic potential and prescribed small-amplitude aperture, both systems reduce to the same cubic-mobility Reynolds operator driven by a moving-wall wedge term, satisfy the same smooth Reynolds cavitation boundary pair, and yield the same unit-threshold dimensionless cavitation number; outside that limit the nonlocal elastic gap law of EHL and the melt/creep closure terms of glaciology are distinct and are not claimed to be identical.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `P_A = p - p_c` ↔ `P_B = N = φ_i - φ_w`
    *   *Operator Role:* Nonnegative scalar field of pressure or effective pressure, measured in Pa, on which the Reynolds operator acts; it is clipped at zero at the free boundary and normalized by its mean value in the cavitation number. The explicit transformation is `P_A = p - p_c` in Silo A and `P_B = φ_i - φ_w` in Silo B, with a possible sign convention reversal of the along-bed coordinate so that the wedge source has the same sign in the two equations.
*   `p_c` ↔ `φ_i`
    *   *Operator Role:* Reference potential defining the gauge field that enters the cavitation complementarity; `p_c` is the cavitation pressure in EHL, while `φ_i` is the ice hydraulic potential in glaciology. The gauge fields are formed as `P_A = p - p_c` and `P_B = φ_i - φ_w`.
*   `h` ↔ `s`
    *   *Operator Role:* Aperture field of length dimension supplying the cubic mobility `h^3` or `s^3` and the wedge derivative `dh/dx` or `ds/dx` inside the shared Reynolds operator.
*   `U` ↔ `u_b`
    *   *Operator Role:* Tangential velocity of the moving solid boundary appearing in the wedge source term `6 η U dh/dx` in EHL and `6 μ_w u_b ds/dx` in the subglacial sheet equation.
*   `η` ↔ `μ_w`
    *   *Operator Role:* Dynamic viscosity entering the Poiseuille mobility and multiplying the wedge source; both have units Pa·s and enter the operator through the same algebraic position.
*   EHL cavitation front coordinate `x_c` ↔ basal zero-effective-pressure front coordinate `x_c`
    *   *Operator Role:* Free-boundary point at which the nonnegative field and its first derivative vanish, `P(x_c)=0` and `dP/dx(x_c)=0`, enforcing the smooth Reynolds cavitation condition.

## 3. CORE MATHEMATICAL PARALLELISM
In EHL line-contact theory, the film aperture `h(x)` and the gauge pressure `P_A(x)=p(x)-p_c` obey the steady one-dimensional Reynolds equation under the usual lubrication assumptions of negligible inertia, constant viscosity, and no normal squeeze. The governing equation is a quasilinear elliptic Reynolds operator with a moving-wall wedge source:

```math
L_h[P_A] \equiv \frac{d}{dx}\left(h^3\frac{dP_A}{dx}\right)=6\eta U\frac{dh}{dx}.
```

The Reynolds cavitation free boundary imposes a smooth transition to the cavitated region at `x=x_c`:

```math
P_A(x_c)=0,\qquad \frac{dP_A}{dx}(x_c)=0,\qquad P_A(x)>0\quad\text{for }x<x_c.
```

For a small-amplitude sinusoidal aperture, `h(x)=h_0+a\cos(kx)`, and a mean gauge pressure `p_m`, the first-order solution is

```math
P_A(x)=p_m+\frac{6\eta U a}{h_0^3 k}\sin(kx)+O(a^2),
```

so cavitation onset occurs when the pressure perturbation amplitude equals the mean gauge pressure. The corresponding dimensionless cavitation number is

```math
\Lambda_A\equiv\frac{6\eta U a}{h_0^3 k p_m},
\qquad
\Lambda_A=1
\quad\text{at cavitation onset.}
```

In subglacial hydrology, the relevant scalar potentials are the ice hydraulic potential `φ_i`, the water hydraulic potential `φ_w=p_w+ρ_w g z_b`, and the effective pressure potential `P_B=N=φ_i-φ_w`. A recognized distributed-sheet mass balance for a sliding ice mass over a hard bed can be written in one dimension as

```math
\frac{\partial s}{\partial t}
+
\frac{\partial}{\partial x}
\left[
-\frac{s^3}{12\mu_w}\frac{d\phi_w}{dx}
+
\frac{u_b s}{2}
\right]
=
\frac{m}{\rho_i}
-
C P_B^3,
```

where `s(x,t)` is the water-sheet aperture, `u_b` is basal sliding speed, `m` is meltwater input, and `C P_B^3` represents a creep-closure sink. In the steady, source-free, no-melt limit used for the operator comparison, this reduces to

```math
\frac{d}{dx}
\left[
-\frac{s^3}{12\mu_w}\frac{d\phi_w}{dx}
+
\frac{u_b s}{2}
\right]
=0,
```

or, equivalently,

```math
\frac{d}{dx}\left(s^3\frac{d\phi_w}{dx}\right)
=
6\mu_w u_b\frac{ds}{dx}.
```

With `φ_i` locally constant and with the along-bed coordinate chosen so that the wedge source has the same sign as in EHL, `P_B=φ_i-φ_w` satisfies

```math
L_s[P_B] \equiv \frac{d}{dx}\left(s^3\frac{dP_B}{dx}\right)
=
6\mu_w u_b\frac{ds}{dx}.
```

The basal zero-effective-pressure front satisfies the same smooth free-boundary pair:

```math
P_B(x_c)=0,\qquad \frac{dP_B}{dx}(x_c)=0,\qquad P_B(x)>0\quad\text{for }x<x_c.
```

For a small-amplitude sinusoidal sheet aperture, `s(x)=s_0+a\cos(kx)`, and a mean effective pressure `N_0`, the first-order effective-pressure perturbation has amplitude

```math
|P_B-N_0|_{\max}
=
\frac{6\mu_w u_b a}{s_0^3 k},
```

and, with the phase chosen so that the perturbation is sinusoidal,

```math
P_B(x)=N_0+\frac{6\mu_w u_b a}{s_0^3 k}\sin(kx)+O(a^2).
```

Thus the subglacial cavitation number is

```math
\Lambda_B\equiv\frac{6\mu_w u_b a}{s_0^3 k N_0},
\qquad
\Lambda_B=1
\quad\text{at zero-effective-pressure onset.}
```

The explicit bridge is the variable and parameter identification

```math
h \longleftrightarrow s,\qquad
P_A=p-p_c \longleftrightarrow P_B=N=\phi_i-\phi_w,
\qquad
\eta \longleftrightarrow \mu_w,
\qquad
U \longleftrightarrow u_b,
\qquad
p_m \longleftrightarrow N_0.
```

Under this map, the two Reynolds operators coincide:

```math
\frac{d}{dx}\left(H^3\frac{dP}{dx}\right)
=
6\mu V\frac{dH}{dx},
```

with `(H, μ, V, P) = (h, η, U, P_A)` for EHL and `(H, μ, V, P) = (s, μ_w, u_b, P_B)` for the subglacial sheet. The correspondence extends through the smooth cavitation boundary and the unit-threshold cavitation number. It stops where EHL’s nonlocal elastic deformation law for `h`, subglacial meltwater sources `m/ρ_i`, ice creep closure `C P_B^3`, channelization, temperature-dependent viscosity, or turbulent sheet flow become leading-order effects.

The three listed correspondence vectors are demonstrated as follows. First, the cubic-mobility Reynolds operator is displayed for both silos in the equations for `L_h[P_A]` and `L_s[P_B]`. Second, the smooth Reynolds free-boundary pair is displayed for both silos through `P_A(x_c)=0`, `dP_A/dx(x_c)=0` and `P_B(x_c)=0`, `dP_B/dx(x_c)=0`. Third, the dimensionless cavitation numbers `Λ_A` and `Λ_B` are derived from the same small-amplitude solution and both possess the unit onset threshold `Λ=1`.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Elastohydrodynamic lubrication → Subglacial sheet-cavitation hydrology
*   **Asymmetric Maturity Rationale:** EHL possesses a mature, highly deterministic computational toolkit for Reynolds-type cavitation: Jakobsson–Floberg–Olsson mass-conserving cavitation conditions, Elrod–Adams switch variables, active-set complementarity solvers, multigrid/multilevel Reynolds solvers, and load-conserving Newton methods for coupled nonlocal film-thickness laws. Glaciology is mature in ice-flow inversion, remote-sensing assimilation, and channelized hydrology, but distributed sheet models still often regularize zero effective pressure with ad hoc positive floors or switch heuristically between sheets and channels. The specific missing capability is a robust, mass-conserving, complementarity-based treatment of zero-effective-pressure patches in fast-sliding, rough-bed distributed sheets.
*   **Target Bottleneck Mitigation:** Importing EHL cavitation algorithms into subglacial sheet models should allow the effective-pressure field to be clipped at zero through a mathematically consistent free-boundary solver rather than by artificial regularization. This should eliminate nonphysical negative effective pressures, preserve water mass during cavity opening and closure, and produce a sharp, testable onset threshold for basal decoupling under increasing sliding speed.
*   **Falsifiable Prediction:** Consider a fast-sliding, hard-bed glacier reach approximated by a sinusoidal bed undulation of wavelength `λ=10 m`, amplitude `a=0.5 m`, distributed sheet thickness `s_0=1 mm`, mean effective pressure `N_0=1 kPa`, and water viscosity `μ_w=1.7×10^{-3} Pa·s`. With `k=2π/λ=0.628 m^{-1}`, the unit-threshold condition `Λ_B=1` gives a critical sliding speed

```math
u_c
=
\frac{N_0 s_0^3 k}{6\mu_w a}
=
\frac{(10^3)(10^{-9})(0.628)}{6(1.7\times10^{-3})(0.5)}
\approx
1.23\times10^{-4}\ \mathrm{m\,s^{-1}},
```

which is approximately `10.6 m/day`. At `u_b=2u_c`, the predicted zero-effective-pressure bed fraction is

```math
f
=
\frac{1}{\pi}\arccos\left(\frac{1}{\Lambda_B}\right)
=
\frac{1}{\pi}\arccos\left(\frac{1}{2}\right)
=
\frac{1}{3}.
```

The state-of-the-art baseline is a positive-effective-pressure distributed-sheet model without Reynolds complementarity, which predicts `f=0` for the same inputs. The measurable quantity is the fraction `f_obs` of the bed at zero effective pressure, inferred from borehole water-pressure records, ice-overburden estimates, and basal seismic or radar sensitivity to decoupled patches. The prediction is falsified if, with the measured input parameters inserted into the formula, `f_obs` remains indistinguishable from the baseline value `f=0` at `u_b=2u_c`, or if zero-effective-pressure patches appear at `u_b<u_c` in the absence of channel capture.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"elastohydrodynamic lubrication" AND "Reynolds cavitation" AND "multigrid"`
*   `"subglacial water sheet" AND "hydraulic potential" AND "effective pressure"`
*   `"basal sliding" AND "Reynolds equation" AND "cavitation" AND "subglacial hydrology"`
*   `"elastohydrodynamic cavitation" AND "subglacial sheet" AND "Reynolds operator"`