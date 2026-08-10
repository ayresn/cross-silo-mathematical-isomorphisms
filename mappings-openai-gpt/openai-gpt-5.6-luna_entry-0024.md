---
sid_metadata:
  entry_id: "SID-0024"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "OpenAI"
  model_family: "GPT"
  model_version: "5.6 Luna"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "dendritic-metal-solidification"
  domain_b: "ice-lens-growth-in-frost-heave"
  structural_family: "moving-phase-boundary-and-capillary-regularized-free-boundary-growth"
  triple_correspondence_vectors:
    - "Gibbs-Thomson-curvature-corrected-interface-temperature"
    - "Stefan-latent-heat-interface-balance"
    - "diffusion-field-similarity-parameter"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / porous-soil-versus-metallurgical-ontology"
prior_discovery_metrics:
  structural_isomorphism_score: 8.1
  vocabulary_divergence_score: 8.8
  expected_methodological_transfer_score: 8.5
  community_separation_score: 8.7
  representation_mismatch_score: 7.9
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.4
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0024

## 1. CROSS-SILO SYSTEM DEFINITION

* **Silo A (Field 1):** Dendritic metal solidification, specifically diffusion-controlled growth of a solid-liquid interface with capillary/Gibbs-Thomson regularization.
* **Silo B (Field 2):** Ice-lens growth during frost heave, specifically the local advance of an ice-water interface supplied by diffusive heat/mass transport in a porous soil matrix.
* **Mathematical Isomorphism:** Under a local sharp-interface reduction in which the interfacial temperature is represented by a curvature-corrected Gibbs-Thomson condition, the latent-heat/phase-change balance is represented by a Stefan condition, and transport is nondimensionalized by the same diffusion-field similarity parameter, both systems possess the same moving-boundary operator structure even though their constitutive closures and physical driving fields differ.

## 2. DIAGNOSTIC VOCABULARY MATRIX

* **Gibbs-Thomson temperature** ↔ **ice-interface equilibrium temperature**

  * *Operator Role:* Both are scalar interfacial boundary fields entering a curvature-dependent Dirichlet condition for the temperature/diffusion field. The shared mathematical type is a scalar boundary value, with curvature supplying the geometric correction.

* **Stefan condition** ↔ **ice-lens latent-heat balance**

  * *Operator Role:* Both impose a normal-velocity boundary constraint equating latent-energy consumption to the jump in normal conductive heat flux. The shared mathematical type is a scalar flux-balance condition on the moving interface.

* **thermal diffusion length** ↔ **frost-heave thermal diffusion length**

  * *Operator Role:* Both normalize the diffusion equation through a moving-interface similarity variable, producing the dimensionless ratio of interface velocity to diffusive transport.

## 3. CORE MATHEMATICAL PARALLELISM

In dendritic solidification, the temperature field in each phase is commonly represented by a diffusion equation, while the interface is advanced through a Stefan balance. A curvature-dependent Gibbs-Thomson relation supplies capillary regularization of the otherwise ill-posed sharp-interface growth problem:

```math
\frac{\partial T}{\partial t}
=
\alpha \nabla^2 T,
\qquad
T_i=T_m-\Gamma\kappa-\beta V_n,
\qquad
\rho L V_n
=
k_s\partial_nT_s-k_l\partial_nT_l .
```

Here (T_i) is the interfacial temperature, (T_m) the planar equilibrium melting temperature, (\Gamma) the Gibbs-Thomson capillary coefficient, (\kappa) interface curvature, (V_n) normal interface velocity, (L) latent heat per unit mass, and (k_s,k_l) the thermal conductivities of solid and liquid. The first equation establishes the transport operator; the second establishes curvature regularization; and the third establishes the phase-change flux balance.

For frost-heave ice-lens growth, the local temperature field in the unfrozen/frozen regions can likewise be reduced to diffusion with a moving ice-water interface. The interfacial equilibrium temperature is curvature-sensitive at the scale where capillary effects are retained, while latent heat released or absorbed at the advancing interface produces a Stefan-type flux condition:

```math
\frac{\partial T_f}{\partial t}
=
\alpha_f\nabla^2T_f,
\qquad
T_i=T_m-\Gamma_i\kappa,
\qquad
\rho_i L_i V_n
=
k_f\partial_nT_f-k_u\partial_nT_u .
```

The subscripts (f,u,i) denote the relevant frozen/unfrozen phases and ice interface. This representation deliberately isolates the local phase-boundary physics from the additional poromechanical and hydraulic laws governing macroscopic frost heave.

The first correspondence is therefore the curvature-corrected interfacial condition:

```math
T_i-T_m=-\Gamma\kappa-\beta V_n
\quad\longleftrightarrow\quad
T_i-T_m=-\Gamma_i\kappa
```

The correspondence extends only to the capillary sharp-interface limit; the kinetic term (\beta V_n) has no demonstrated universal counterpart in the frost-heave formulation above and is therefore not included as a correspondence vector.

The second correspondence is the Stefan interface operator. Dividing each flux balance by its latent-heat coefficient gives the common normal-velocity form:

```math
V_n
=
\frac{k_s\partial_nT_s-k_l\partial_nT_l}{\rho L}
\quad\longleftrightarrow\quad
V_n
=
\frac{k_f\partial_nT_f-k_u\partial_nT_u}{\rho_iL_i}.
```

Thus the interface velocity is determined by a jump in normal diffusive flux divided by the latent phase-change scale in both systems.

The third correspondence follows from nondimensionalizing the diffusion equation with a characteristic interface speed (V) and length (R). Defining

```math
\xi=\frac{x}{R},
\qquad
\tau=\frac{Vt}{R},
\qquad
Pe=\frac{VR}{\alpha},
```

the transport equation becomes

```math
\frac{\partial T}{\partial \tau}
=
\frac{1}{Pe}\nabla_\xi^2T
```

for both the metal-solidification and local frost-heave temperature fields, with

```math
Pe_m=\frac{V_mR_m}{\alpha_m}
\quad\longleftrightarrow\quad
Pe_f=\frac{V_fR_f}{\alpha_f}.
```

The shared structural quantity is therefore not equality of the dimensional thermal properties but equality of the nondimensional transport operator at matched (Pe). The mapping stops there: soil permeability, unfrozen-water retention, pore pressure, and mechanical stress have no demonstrated counterpart in the metal-solidification equations displayed above and are not claimed to be isomorphic.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

* **Preferred Transfer Direction:** Dendritic-metal-solidification → ice-lens-growth-in-frost-heave
* **Asymmetric Maturity Rationale:** Metal solidification has a mature family of curvature-regularized moving-boundary solvers, including phase-field/sharp-interface formulations and adaptive interface-resolution strategies designed specifically to resolve curvature-dependent growth and latent-heat transport. The target frost-heave problem is mature in poromechanics and soil-water transport, but the local morphology of an advancing ice interface is less systematically resolved as a capillary-regularized moving boundary. The proposed transfer is therefore narrow: import moving-interface resolution and curvature regularization, not the metallurgical constitutive model.
* **Target Bottleneck Mitigation:** A curvature-regularized adaptive moving-interface solver should reduce the dependence of predicted ice-lens morphology on the numerical interface thickness or mesh scale while retaining the existing frost-heave hydraulic and mechanical closures outside the local phase boundary.
* **Falsifiable Prediction:** For a one-dimensional-to-axisymmetric ice-lens-growth benchmark in which (Pe_f=1) is imposed by nondimensional matching, the imported curvature-regularized moving-interface method should produce a converged nondimensional interface velocity (V_nR/\alpha_f) whose change under halving the interface-resolution length is below (1%), while the named baseline—an unregularized fixed-grid enthalpy/Stefan discretization at the same nominal mesh resolution—should exhibit a change exceeding (5%). The hypothesis is falsified if the baseline also remains below (1%), or if the transferred method fails to achieve the (1%) convergence criterion.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"dendritic solidification" AND "ice lens" AND "Gibbs-Thomson" AND "Stefan"`
* `"frost heave" AND "curvature" AND "moving boundary" AND "phase field"`
* `"ice lens growth" AND "adaptive mesh" AND "Stefan problem" AND "solidification"`
* `"ice lens" AND "dendritic growth" AND "Gibbs-Thomson" AND "phase-field"`