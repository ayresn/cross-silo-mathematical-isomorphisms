---
sid_metadata:
  entry_id: "SID-0021"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "OpenAI"
  model_family: "GPT"
  model_version: "5.6 Luna"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "reactive-infiltration-instability-in-porous-geochemistry"
  domain_b: "autothermal-reactive-transport-in-porous-catalysts"
  structural_family: "advection-diffusion-reaction-front-instabilities"
  triple_correspondence_vectors:
    - "Darcy-advection-diffusion-reaction_operator"
    - "mixed_Dirichlet-Neumann_inlet-outlet_flux_boundary_pair"
    - "Peclet-Damkohler_instability_parameter_pair"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / different_constitutive_ontologies"
prior_discovery_metrics:
  structural_isomorphism_score: 8.1
  vocabulary_divergence_score: 8.8
  expected_methodological_transfer_score: 8.4
  community_separation_score: 8.7
  representation_mismatch_score: 7.9
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.6
    uncertainty: "±1.4"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0021

## 1. CROSS-SILO SYSTEM DEFINITION

* **Silo A (Field 1):** Reactive-infiltration instability in porous geochemistry, specifically chemically reactive fluid penetration through a porous rock matrix where dissolution changes permeability and destabilizes the advancing reaction front.
* **Silo B (Field 2):** Autothermal reactive transport in porous catalytic media, specifically spatially distributed exothermic conversion where reactant transport and temperature-dependent reaction rates generate localized reaction fronts and thermal localization.
* **Mathematical Isomorphism:** After nondimensionalization and restriction to a one-dimensional homogeneous Darcy medium with a single mobile reactant, both systems possess the same linearized advection-diffusion-reaction operator, the same mixed inlet concentration/flux boundary structure, and the same controlling Peclet-Damkohler parameter combination governing front localization; the correspondence does not extend to the nonlinear constitutive laws linking permeability to mineral dissolution or reaction rate to temperature. 

## 2. DIAGNOSTIC VOCABULARY MATRIX

* **Reactive-infiltration transport operator** ↔ **reactant transport operator**

  * *Operator Role:* Both act on a scalar mobile-species field (c(x,t)) through the dimensional operator (D\partial_{xx}-u\partial_x) plus a local sink/source term (R), with (c) having units of concentration in both silos; no tensor-to-scalar or dimensional-to-dimensionless identification is required before the nondimensionalization in Section 3.

* **Mineral-dissolution reaction rate** ↔ **catalytic conversion rate**

  * *Operator Role:* Both enter as local nonlinear reaction terms (R(c,\chi)) in the same scalar balance law, while the auxiliary state (\chi) differs physically: porosity/permeability evolution in Silo A and temperature-dependent catalytic activity in Silo B. The structural identification is therefore at the reaction-operator level rather than a constitutive identity.

* **Infiltration front** ↔ **reaction/thermal front**

  * *Operator Role:* Both are represented by a steep spatial gradient of the transported scalar and are localized by competition between advection, diffusion, and reaction. The common dimensionless localization parameters are the Peclet number (Pe=uL/D) and Damkohler number (Da=kL/u).

## 3. CORE MATHEMATICAL PARALLELISM

In Silo A, a minimal reactive-infiltration model for a mobile aqueous reactant (c_A) in a homogeneous porous column is the conservation equation coupled to Darcy transport. With constant porosity and permeability during the short-time front calculation, the mobile concentration satisfies

```math
\phi \frac{\partial c_A}{\partial t}
+
u_A\frac{\partial c_A}{\partial x}
=
D_A\frac{\partial^2 c_A}{\partial x^2}
-
k_A c_A ,
\qquad
u_A=-\frac{K_A}{\mu_A}\frac{\partial p_A}{\partial x}.
```

The corresponding inlet/outlet conditions can be written as a prescribed inlet concentration and convective-dispersive outlet flux:

```math
c_A(0,t)=c_{A,0},
\qquad
-D_A\frac{\partial c_A}{\partial x}(L,t)=0 .
```

Thus the demonstrated Silo-A operator is the advection-diffusion-reaction operator

```math
\mathcal L_A
=
D_A\partial_{xx}
-
u_A\partial_x
-
k_A .
```

In Silo B, the independently recognizable porous-catalyst model is the one-dimensional reactant balance for an exothermic catalytic medium,

```math
\varepsilon \frac{\partial c_B}{\partial t}
+
u_B\frac{\partial c_B}{\partial x}
=
D_B\frac{\partial^2 c_B}{\partial x^2}
-
k_B(T)c_B ,
```

with the temperature field coupled through the heat balance

```math
\rho C_p\frac{\partial T}{\partial t}
+
\rho C_p u_T\frac{\partial T}{\partial x}
=
\lambda\frac{\partial^2T}{\partial x^2}
+
(-\Delta H)k_B(T)c_B .
```

For the reactant field, an independently recognizable inlet/outlet specification is

```math
c_B(0,t)=c_{B,0},
\qquad
-D_B\frac{\partial c_B}{\partial x}(L,t)=0 .
```

Consequently, the reactant-sector operator is

```math
\mathcal L_B
=
D_B\partial_{xx}
-
u_B\partial_x
-
k_B(T).
```

The structural bridge is obtained by defining

```math
\xi=\frac{x}{L},
\qquad
\tau=\frac{u_0t}{L},
\qquad
\hat c=\frac{c}{c_0},
```

and, for each silo,

```math
Pe=\frac{u_0L}{D},
\qquad
Da=\frac{k_0L}{u_0}.
```

The nondimensional linearized reactant equations then become

```math
\frac{\partial \hat c_A}{\partial \tau}
+
\frac{\partial \hat c_A}{\partial \xi}
=
\frac{1}{Pe_A}\frac{\partial^2\hat c_A}{\partial \xi^2}
-
Da_A\hat c_A ,
```

and

```math
\frac{\partial \hat c_B}{\partial \tau}
+
\frac{\partial \hat c_B}{\partial \xi}
=
\frac{1}{Pe_B}\frac{\partial^2\hat c_B}{\partial \xi^2}
-
Da_B\hat c_B .
```

Under the explicit restriction

```math
Pe_A=Pe_B=Pe,
\qquad
Da_A=Da_B=Da,
```

the operators coincide:

```math
\mathcal L_A^\ast
=
\mathcal L_B^\ast
=
\frac{1}{Pe}\partial_{\xi\xi}
-
\partial_\xi
-
Da .
```

This establishes the first correspondence vector, **Darcy-advection-diffusion-reaction operator**, without claiming that the full nonlinear physical systems are identical.

The second correspondence vector, **mixed Dirichlet-Neumann inlet-outlet flux boundary pair**, follows directly from

```math
\hat c_A(0,\tau)=1,
\qquad
\partial_\xi\hat c_A(1,\tau)=0,
```

and

```math
\hat c_B(0,\tau)=1,
\qquad
\partial_\xi\hat c_B(1,\tau)=0.
```

The third correspondence vector, **Peclet-Damkohler instability parameter pair**, follows because the spatial eigenvalues of either common operator satisfy

```math
\frac{1}{Pe}\lambda^2-\lambda-Da=0,
```

or

```math
\lambda_{\pm}
=
\frac{Pe}{2}
\left(
1\pm\sqrt{1+\frac{4Da}{Pe}}
\right).
```

Thus the front localization length is controlled by the same two dimensionless groups in both silos. In particular, the ratio

```math
\Lambda=\frac{Da}{Pe}
=
\frac{kD}{u^2}
```

is identical under the mapping and determines the relative importance of reaction localization to advective transport.

The correspondence stops at this operator level. Silo A modifies permeability through a geological constitutive law, whereas Silo B couples reaction to temperature through an Arrhenius-type law,

```math
k_B(T)=k_{B,0}
\exp\!\left[
-\frac{E_a}{R}
\left(
\frac{1}{T}-\frac{1}{T_0}
\right)
\right].
```

Therefore the candidate claims a shared transport/front operator and parameter structure, not a complete constitutive equivalence.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

* **Preferred Transfer Direction:** Autothermal reactive-transport in porous catalysts → reactive-infiltration instability in porous geochemistry

* **Asymmetric Maturity Rationale:** The source field has comparatively mature continuation, parameter-sweep, stiffness-aware time integration, and front-localization analysis for coupled advection-diffusion-reaction systems, particularly when sharp reaction zones coexist with slowly varying transported fields. The target field is mature in reactive-transport formulation and geological constitutive modeling but has a narrower operational toolkit for systematically continuing front solutions across (Pe)-(Da) parameter space while retaining the geological permeability feedback. The proposed transfer is therefore specifically the numerical continuation and bifurcation-analysis machinery, not generic finite-element transport software.

* **Target Bottleneck Mitigation:** The testable hypothesis is that continuation of the geological front solutions using the source-field parameterization in ((Pe,Da)), rather than independent dimensional parameter sweeps, will identify a reproducible localization transition associated with the dimensionless ratio (\Lambda=Da/Pe). A successful transfer should collapse geometrically similar simulations onto the same nondimensional front-localization curve when (Pe) and (Da) are held fixed, despite changes in (L), (u), (D), and (k).

* **Falsifiable Prediction:** For a geometrically similar reactive-infiltration benchmark satisfying the restricted scalar model in Section 3, two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (\hat c(\xi)) below (1%) after convergence. The baseline is an independently resolved dimensional finite-volume solution of the same scalar benchmark. The hypothesis is falsified if either case differs by (1%) or more after grid refinement, or if simulations having identical (Pe) and (Da) do not collapse. This prediction is deliberately restricted to the demonstrated common operator and does not assert collapse once permeability evolution or temperature coupling becomes dynamically important.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"reactive infiltration instability" AND "Damkohler" AND "Peclet" AND "continuation"`
* `"autothermal reactor" AND "advection diffusion reaction" AND "Peclet" AND "Damkohler" AND "bifurcation"`
* `"reactive infiltration" AND "autothermal" AND "Peclet Damkohler" AND "porous"`
* `"mineral dissolution" AND "catalytic reactor" AND "front localization" AND "advection diffusion reaction"`
* `"reactive infiltration" AND "autothermal reactive transport" AND "operator equivalence"`