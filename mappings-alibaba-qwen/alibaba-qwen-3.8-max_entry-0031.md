---
sid_metadata:
  entry_id: "SID-0031"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "narrow-escape-diffusion-limited-reaction-kinetics"
  domain_b: "polycrystalline-photovoltaic-carrier-lifetime"
  structural_family: "robin-first-passage-capacity-operators"
  triple_correspondence_vectors:
    - "forward_fickian_bulk_first_order_killing_semigroup"
    - "global_probability_carrier_number_balance_law"
    - "robin_radiation_surface_recombination_flux_condition"
    - "adjoint_mean_lifetime_poisson_helmholtz_green_function"
    - "small_disk_capacity_damkohler_crossover_rate"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / different_observables / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 9.2
  vocabulary_divergence_score: 7.6
  expected_methodological_transfer_score: 8.3
  community_separation_score: 7.4
  representation_mismatch_score: 6.2
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 7.1
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "nonlinear_high_injection_or_trap_memory_breaking_first_order_robin_assumption"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0031

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Narrow-escape diffusion-limited reaction kinetics: Brownian reactants in a bounded microdomain with small, partially reactive boundary patches; observable is the reaction rate, survival probability, or mean first-passage/lifetime.
*   **Silo B (Field 2):** Polycrystalline photovoltaic carrier lifetime: low-injection excess minority carriers in a grain or flake with small, highly recombining surface patches; observable is the effective carrier lifetime extracted from transient photoluminescence or photoconductance decay.
*   **Mathematical Isomorphism:** In the linear low-injection limit with Fickian diffusion, first-order bulk loss, and localized Robin patches on a three-dimensional domain, the Silo A Smoluchowski survival problem and the Silo B minority-carrier continuity problem are the same self-adjoint diffusion-killing initial-boundary-value problem under the identification of radiation reactivity with surface recombination velocity, producing identical total-number balance, adjoint screened-Poisson lifetime Green’s functions, and leading-order small-disk capacity laws, provided drift, nonlinear Shockley-Read-Hall recombination, trap memory, and patch-patch interaction are negligible.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `c_A` ↔ `Δn`
    *   *Operator Role:* Dependent scalar number density with units m^{-3} acted on by the parabolic operator `∂_t - D∇² + λ`. `c_A` is the reactant concentration in Silo A; `Δn` is the excess minority-carrier density in Silo B.
*   `λ_A` ↔ `τ_b^{-1}`
    *   *Operator Role:* Bulk first-order killing rate with units s^{-1} in the operator `D∇² - λ`. `λ_A` is homogeneous reactant decay or bulk reaction loss; `τ_b^{-1}` is the bulk minority-carrier recombination rate.
*   `Q_A` ↔ `Q_B`
    *   *Operator Role:* Integrated scalar charge/probability/carrier number, `Q = ∫_Ω q dV`, whose time derivative is the negative sum of bulk and boundary sink integrals.
*   `κ` ↔ `S`
    *   *Operator Role:* Robin coefficient with units m s^{-1} in the boundary operator `D∂_n + κ` or `D∂_n + S`. `κ` is the radiation-boundary reactivity; `S` is the surface recombination velocity.
*   `u_A` ↔ `u_B`
    *   *Operator Role:* Adjoint mean lifetime field with units s solving the screened-Poisson problem `(D∇² - λ)u = -1` with the same Robin boundary operator.
*   `G_A` ↔ `G_B`
    *   *Operator Role:* Robin Green’s function of the screened-Poisson operator, satisfying `(D∇² - λ)G = -δ` and the same homogeneous Robin boundary condition; `u` is obtained by integrating `G` over the source coordinate.
*   `K_A` ↔ `K_B`
    *   *Operator Role:* Patch rate constant with units m^3 s^{-1} in the steady flux law `J = K c_∞` or `J = K Δn_∞`; in the diffusion-limited disk limit it becomes `4Da`.
*   `Da_A` ↔ `Da_B`
    *   *Operator Role:* Dimensionless Damköhler number `κa/D_A` or `Sa/D_n` controlling the crossover from reaction-limited area scaling to diffusion-limited capacity scaling.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models the concentration of diffusing reactants in a bounded domain `Ω` with volume `V`. The domain boundary contains `M` small circular reactive patches `Γ_a` of radius `a`; outside these patches the boundary is reflecting. The reactant concentration `c_A` obeys the Smoluchowski diffusion equation with optional bulk first-order loss, while the partially reactive patches impose a radiation, or Robin, boundary condition.

```math
\frac{\partial c_A}{\partial t}
=
D_A \nabla^2 c_A - \lambda_A c_A,
\qquad x\in\Omega
```

```math
D_A \frac{\partial c_A}{\partial n} + \kappa(\mathbf{s}) c_A = 0,
\qquad \mathbf{s}\in\partial\Omega
```

Silo B models low-injection excess minority carriers in a passivated semiconductor grain or flake. The excess minority-carrier density `Δn` obeys the minority-carrier continuity equation with bulk Shockley-Read-Hall lifetime `τ_b`, and small recombination-active surface patches are represented by a local surface recombination velocity `S`. This equation and boundary condition are standard in semiconductor device physics and photovoltaic lifetime analysis.

```math
\frac{\partial \Delta n}{\partial t}
=
D_n \nabla^2 \Delta n - \frac{\Delta n}{\tau_b},
\qquad x\in\Omega
```

```math
D_n \frac{\partial \Delta n}{\partial n} + S(\mathbf{s})\Delta n = 0,
\qquad \mathbf{s}\in\partial\Omega
```

The operator identification is explicit and local:

```math
D_A = D_n,
\qquad
\lambda_A = \tau_b^{-1},
\qquad
\kappa = S,
\qquad
c_A \leftrightarrow \Delta n.
```

Under this identification the forward parabolic semigroups coincide. Integrating the forward equations over `Ω` gives the same global balance law for total reactant number `Q_A` and total excess carrier number `Q_B`:

```math
Q_A(t)=\int_\Omega c_A\,dV,
\qquad
\frac{dQ_A}{dt}
=
-\lambda_A Q_A
-
\int_{\partial\Omega}\kappa c_A\,dA
```

```math
Q_B(t)=\int_\Omega \Delta n\,dV,
\qquad
\frac{dQ_B}{dt}
=
-\frac{Q_B}{\tau_b}
-
\int_{\partial\Omega}S\Delta n\,dA
```

The adjoint mean-lifetime fields are also identical in form. In Silo A, the mean time to bulk decay or boundary absorption, starting from position `x`, satisfies the backward screened-Poisson problem with radiation boundary condition. In Silo B, the corresponding mean carrier lifetime before bulk or surface recombination satisfies the same adjoint problem with surface recombination velocity.

```math
D_A \nabla^2 u_A - \lambda_A u_A = -1,
\qquad
D_A \frac{\partial u_A}{\partial n} + \kappa u_A = 0
```

```math
D_n \nabla^2 u_B - \frac{u_B}{\tau_b} = -1,
\qquad
D_n \frac{\partial u_B}{\partial n} + S u_B = 0
```

The associated Robin Green’s functions obey the same screened-Poisson operator and boundary operator:

```math
\left(D_A\nabla^2-\lambda_A\right)G_A(x,y)=-\delta(x-y),
\qquad
D_A\frac{\partial G_A}{\partial n_y}+\kappa(y)G_A=0,
\qquad
u_A(x)=\int_\Omega G_A(x,y)\,dy
```

```math
\left(D_n\nabla^2-\tau_b^{-1}\right)G_B(x,y)=-\delta(x-y),
\qquad
D_n\frac{\partial G_B}{\partial n_y}+S(y)G_B=0,
\qquad
u_B(x)=\int_\Omega G_B(x,y)\,dy
```

The correspondence extends to the small-patch capacity law. For a single small circular absorbing or recombining disk of radius `a` on an otherwise reflecting boundary, the steady diffusion-limited flux from a far-field concentration `c_∞` or excess carrier density `Δn_∞` is governed by the microdisk capacity `4Da`. With finite surface reactivity, reaction and diffusion resistances add to leading order. In Silo A:

```math
J_A = K_A(a,\kappa)c_\infty,
\qquad
\frac{1}{K_A(a,\kappa)}
\simeq
\frac{1}{\pi a^2\kappa}
+
\frac{1}{4D_A a}
```

```math
\mathrm{Da}_A = \frac{\kappa a}{D_A},
\qquad
K_A \xrightarrow[\kappa\to\infty]{} 4D_A a
```

In Silo B, the same capacity law gives the recombination flux to a small high-velocity patch:

```math
J_{\mathrm{rec},B}=K_B(a,S)\Delta n_\infty,
\qquad
\frac{1}{K_B(a,S)}
\simeq
\frac{1}{\pi a^2 S}
+
\frac{1}{4D_n a}
```

```math
\mathrm{Da}_B = \frac{S a}{D_n},
\qquad
K_B \xrightarrow[S\to\infty]{} 4D_n a
```

For `M` well-separated patches, `a` much smaller than the grain length scale, and weak total sink capacity, the effective lifetime in Silo B is the inverse sum of bulk and patch rates:

```math
\tau_{\mathrm{eff},B}^{-1}
\simeq
\tau_b^{-1}
+
\frac{M K_B(a,S)}{V}
```

```math
\tau_{\mathrm{eff},B}^{-1}
\xrightarrow[S\gg D_n/a]{}
\tau_b^{-1}
+
\frac{4D_n M a}{V}
```

The mapping stops where the linear first-order Robin assumptions fail: strong electric-field drift, high-injection nonlinear recombination, trap-mediated memory kernels, non-Fickian transport, large patches, or closely spaced patches whose diffusion fields strongly overlap.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** narrow-escape-diffusion-limited-reaction-kinetics → polycrystalline-photovoltaic-carrier-lifetime
*   **Asymmetric Maturity Rationale:** Chemical physics and narrow-escape theory possess mature matched-asymptotic tools, boundary homogenization formulas, Brownian simulation methods, and capacity-based rate laws for sparse small Robin/Dirichlet patches on complex boundaries. Photovoltaic lifetime analysis is mature in drift-diffusion device simulation, transient optical measurement, and bulk SRH parameter extraction, but it lacks compact, geometry-aware capacity models for sparsely distributed nanoscale recombination patches; common practice either homogenizes the patches into an area-averaged surface recombination velocity or resolves them with expensive three-dimensional meshes.
*   **Target Bottleneck Mitigation:** Importing the narrow-escape capacity formula lets a photovoltaic practitioner predict the effective lifetime directly from patch radius, patch count, diffusivity, and bulk lifetime without fitting an effective surface recombination velocity. The specific hypothesis is that nanoscale recombination patches in passivated polycrystalline absorbers act as diffusion-limited capacity sinks, so the patch contribution to recombination scales with patch radius, not patch area, once the local surface reactivity exceeds the diffusion-supply limit.
*   **Falsifiable Prediction:** Prepare a benchmark sample with a known grain volume `V`, independently measured `D_n` and `τ_b`, and `M` engineered circular recombination patches of radius `a` on an otherwise passivated surface. Measure the effective lifetime `τ_eff` by time-resolved photoluminescence or microwave photoconductance decay. Define `Da_B = Sa/D_n`. The capacity model predicts that for `Da_B = 10`,

```math
K_B(Da_B=10)
=
\left(
\frac{1}{10\pi D_n a}
+
\frac{1}{4D_n a}
\right)^{-1}
=
3.55\,D_n a
```

whereas the state-of-the-art area-averaged surface-recombination model predicts

```math
K_{\mathrm{area}}
=
\pi a^2 S
=
10\pi D_n a
=
31.4\,D_n a
```

Thus the capacity model predicts a patch recombination rate smaller by a factor

```math
\frac{31.4}{3.55} \approx 8.9
```

at `Da_B = 10`, and a scaling exponent

```math
\frac{d\ln(\tau_{\mathrm{eff}}^{-1}-\tau_b^{-1})}{d\ln a} \approx 1
```

instead of the area-model exponent `2`. The prediction is falsified if, for independently characterized `D_n`, `a`, and `S` with `Da_B > 10`, the extracted patch rate exceeds `7.1 D_n a` (twice the capacity prediction) or the measured log-log slope versus patch radius exceeds `1.5` while the patches remain small and well separated.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"narrow escape" AND "radiation boundary" AND "microdisk electrode"`
*   `"surface recombination velocity" AND "grain boundary" AND "minority carrier lifetime"`
*   `"mean first passage time" AND "surface recombination velocity" AND "grain boundary"`
*   `"narrow escape" AND "minority carrier lifetime" AND "Robin boundary"`
*   `"diffusion-limited recombination" AND "small absorbing patch" AND "photovoltaic lifetime"`