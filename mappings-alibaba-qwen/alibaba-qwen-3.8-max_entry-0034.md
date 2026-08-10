---
sid_metadata:
  entry_id: "SID-0034"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "geocryology-frost-heave"
  domain_b: "lithium-metal-dendrite-electrodeposition"
  structural_family: "chemical-potential-driven-stefan-free-boundary"
  triple_correspondence_vectors:
    - "chemical_potential_divergence_mobility_transport_operator"
    - "capillary_kinetic_robin_interface_condition"
    - "stefan_faraday_normal_flux_accretion_law"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 8.1
  community_separation_score: 8.4
  representation_mismatch_score: 7.8
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±0.7"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0034

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Geocryology / frost-heave mechanics: ice segregation and ice-lens growth in freezing colloidal or porous media, driven by cryogenic suction through unfrozen water films.
*   **Silo B (Field 2):** Lithium-metal battery electrodeposition: dendritic or filamentary lithium advance through a porous separator/electrolyte, driven by electrochemical potential gradients and sustained by Faradaic accretion.
*   **Mathematical Isomorphism:** In the isothermal, dilute, quasi-steady, linearized-kinetics limit in which a single mobile species supplies a growing phase through a confining layer, both systems reduce to the same Stefan-type free-boundary problem: a dimensionless chemical-potential field satisfies the same divergence-form mobility transport operator, the interface obeys the same affine Robin-type capillary-kinetic condition, and the normal interface velocity is given by the same normal-flux accretion law, with cryogenic suction mapped to electrochemical overpotential after the explicit nondimensionalization displayed in Section 3.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   `cryogenic suction ψ` ↔ `Li-ion electrochemical potential μ̃`
    *   *Operator Role:* The mapped driving potentials are `Π_A = ψ_m - ψ` and `Π_B = μ̃ - μ̃_eq`. After nondimensionalization `u_A = Π_A / ΔΠ_A` and `u_B = Π_B / ΔΠ_B`, they are dimensionless scalar potentials entering the same divergence-form mobility operator displayed in Section 3.

*   `hydraulic conductivity K_w` ↔ `ionic mobility M_B = D c / (R T)`
    *   *Operator Role:* These are the positive mobility coefficients multiplying the potential gradient in the same flux-divergence operator. With `M_A = ρ_w K_w` for the frost-heave mass flux and `M_B = D c / (R T)` for the lithium flux, the two transport operators coincide after the scaling in Section 3.

*   `ice-lens velocity v_A` ↔ `lithium plating velocity v_B`
    *   *Operator Role:* Both are the normal free-boundary velocities in the same accretion identity `ρ_ph v_n = M ∂_n Π` and in the same Robin interface law `Π_i = R v_n + Γ κ`.

*   `frozen-fringe interfacial resistance R_f` ↔ `charge-transfer resistance R_ct`
    *   *Operator Role:* Both are the coefficients of `v_n` in the affine Robin interface condition, converting interface velocity into a potential drop at the accreting boundary.

*   `Gibbs-Thomson ice coefficient Γ_A = 2 γ_iw / ρ_i` ↔ `lithium capillary coefficient Γ_B = Ω_Li γ_Li`
    *   *Operator Role:* Both multiply curvature `κ` in the same interface condition and produce the hemispherical-tip critical potential `2 Γ / r` used in the falsifiable prediction.

*   `segregation potential drop ΔΠ_A` ↔ `applied electrochemical overpotential ΔΠ_B`
    *   *Operator Role:* Both are the boundary driving potential differences across the transport length `L`; they set the far-field boundary value for the same one-dimensional transport solution used in the threshold derivation.

## 3. CORE MATHEMATICAL PARALLELISM

In frost-heave mechanics, ice segregation is modeled by water migration through an unfrozen fringe toward an ice lens. Let `ψ` be the cryogenic water potential and let `ψ_m` be the local melting-equilibrium potential. Define the suction potential `Π_A = ψ_m - ψ`, which is positive when water is drawn toward the ice lens. In the quasi-steady frozen-fringe limit, the water potential satisfies a divergence-form transport equation. For locally constant hydraulic conductivity `K_w`, this is

```math
\nabla \cdot \left(K_w \nabla \psi\right) = 0,
\qquad
\Pi_A = \psi_m - \psi,
\qquad
\nabla \cdot \left(K_w \nabla \Pi_A\right) = 0.
```

The ice-lens interface condition combines interfacial hydraulic resistance with Gibbs-Thomson curvature depression of the freezing potential. With normal velocity `v_A` and interface curvature `κ`,

```math
\Pi_{A,i} = R_f v_A + \Gamma_A \kappa,
\qquad
\Gamma_A = \frac{2 \gamma_{iw}}{\rho_i}.
```

The Stefan mass-balance condition equates ice accretion to the incoming water mass flux. With the normal `n` oriented so that positive flux is toward the growing ice phase,

```math
\rho_i v_A = \rho_w K_w \, \partial_n \Pi_A.
```

In lithium-metal electrodeposition, the relevant driving field is the electrochemical potential of lithium in the electrolyte or solid-ion conductor,

```math
\tilde{\mu} = \mu^0 + R T \ln\left(\frac{c}{c_{\mathrm{ref}}}\right) + F \phi.
```

Define the local overpotential potential `Π_B = μ̃ - μ̃_eq`, where `μ̃_eq` is the equilibrium electrochemical potential of lithium metal. In a dilute, isothermal, electroneutral transport layer of thickness `L`, the quasi-steady flux is written in terms of the mobility `M_B = D c / (R T)` as

```math
\nabla \cdot \left(M_B \nabla \tilde{\mu}\right) = 0,
\qquad
\Pi_B = \tilde{\mu} - \tilde{\mu}_{eq},
\qquad
\nabla \cdot \left(M_B \nabla \Pi_B\right) = 0.
```

At the lithium/electrolyte interface, linearized Butler-Volmer kinetics plus capillarity give

```math
\Pi_{B,i} = R_{ct} v_B + \Gamma_B \kappa,
\qquad
\Gamma_B = \Omega_{Li} \gamma_{Li},
```

where `v_B` is the normal plating velocity, `R_ct` is the linearized charge-transfer resistance expressed as an overpotential per unit velocity, and `Ω_Li` is the molar volume of lithium metal. Faradaic accretion gives the moving-boundary condition

```math
\frac{1}{\Omega_{Li}} v_B
=
M_B \, \partial_n \Pi_B,
\qquad
v_B
=
\Omega_{Li} M_B \, \partial_n \Pi_B
=
\frac{\Omega_{Li}}{F} i_n.
```

The explicit bridge is obtained by scaling the spatial coordinate and the two driving potentials:

```math
\hat{x} = \frac{x}{L},
\qquad
u_A = \frac{\Pi_A}{\Delta \Pi_A},
\qquad
u_B = \frac{\Pi_B}{\Delta \Pi_B},
```

and by introducing reference mobilities `K_w^0` and `M_B^0`:

```math
\hat{M}_A = \frac{K_w}{K_w^0},
\qquad
\hat{M}_B = \frac{M_B}{M_B^0}.
```

Under this transformation, both transport equations become

```math
\nabla_{\hat{x}} \cdot \left(\hat{M} \, \nabla_{\hat{x}} u\right) = 0.
```

The correspondence extends through the following three demonstrated vectors.

**Vector 1: chemical_potential_divergence_mobility_transport_operator.**  
For Silo A,

```math
\mathcal{L}_A[\Pi_A]
=
\nabla \cdot \left(K_w \nabla \Pi_A\right)
=
0.
```

For Silo B,

```math
\mathcal{L}_B[\Pi_B]
=
\nabla \cdot \left(M_B \nabla \Pi_B\right)
=
0.
```

After the nondimensionalization above, the two operators are identical in form:

```math
\mathcal{L}[u]
=
\nabla_{\hat{x}} \cdot \left(\hat{M} \nabla_{\hat{x}} u\right)
=
0.
```

**Vector 2: capillary_kinetic_robin_interface_condition.**  
For Silo A,

```math
\Pi_{A,i} = R_f v_A + \Gamma_A \kappa.
```

For Silo B,

```math
\Pi_{B,i} = R_{ct} v_B + \Gamma_B \kappa.
```

Both are the same affine Robin-type free-boundary condition,

```math
\Pi_i = R v_n + \Gamma \kappa,
```

with the parameter identifications

```math
(\Pi, R, \Gamma, v_n)_A
=
(\Pi_A, R_f, \Gamma_A, v_A),
\qquad
(\Pi, R, \Gamma, v_n)_B
=
(\Pi_B, R_{ct}, \Gamma_B, v_B).
```

**Vector 3: stefan_faraday_normal_flux_accretion_law.**  
For Silo A,

```math
\rho_i v_A
=
\rho_w K_w \, \partial_n \Pi_A.
```

For Silo B,

```math
\frac{1}{\Omega_{Li}} v_B
=
M_B \, \partial_n \Pi_B.
```

Both are the same normal-flux-to-velocity Stefan-type law,

```math
\rho_{\mathrm{ph}} v_n
=
M \, \partial_n \Pi,
```

with

```math
(\rho_{\mathrm{ph}}, M)_A
=
(\rho_i, \rho_w K_w),
\qquad
(\rho_{\mathrm{ph}}, M)_B
=
\left(\frac{1}{\Omega_{Li}}, \frac{D c}{R T}\right).
```

The correspondence stops where the constitutive physics diverges: frost heave may require a heat equation, disjoining-pressure films, and strong saturation-dependent permeability; lithium electrodeposition may require migration in non-dilute electrolytes, double-layer charging, convection, mechanical fracture, and electron tunneling. Those effects add operators not present in the minimal mapping above.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Geocryology / frost-heave mechanics → Lithium-metal battery dendrite electrodeposition.

*   **Asymmetric Maturity Rationale:** Frost-heave mechanics possesses a mature suite of ice-segregation criteria, frozen-fringe film-flow models, interfacial resistance laws, and curvature-dependent critical suction rules for confined porous media. Lithium-battery modeling is mature in porous-electrode transport, Newman-style continuum models, and phase-field dendrite simulations, but it lacks a compact, pore-scale free-boundary inception criterion that directly links separator pore curvature, interfacial kinetic resistance, and critical electrochemical driving force without resolving nanometer-scale double layers or running full phase-field simulations.

*   **Target Bottleneck Mitigation:** Importing the frost-heave segregation-potential criterion provides a reduced-order dendrite-inception rule for porous separators. The hypothesis is that dendrite penetration through a separator pore is governed at onset by the same capillary-kinetic Robin condition that controls ice-lens nucleation in a freezing pore. This rule can replace purely concentration-depletion criteria in separator design screens and can identify pore radii and interfacial resistances for which dendrite inception is suppressed at practical charging currents.

*   **Falsifiable Prediction:** Prepare cells with identical separator thickness `L`, porosity, tortuosity, electrolyte, and electrode chemistry, but with controlled cylindrical pore radii `r` and `2r`. At a fixed small plating velocity `v_0`, measure the additional overpotential beyond a planar-reference cell required to sustain plating. From the interface law with hemispherical tip curvature `κ = 2 / r`, the radius-dependent overpotential component is

```math
\eta_{\mathrm{rad}}(r)
=
\frac{2 \Gamma_B}{F r}
=
\frac{2 \Omega_{Li} \gamma_{Li}}{F r}.
```

Therefore,

```math
\frac{\eta_{\mathrm{rad}}(r)}{\eta_{\mathrm{rad}}(2r)}
=
2,
\qquad
\eta_{\mathrm{rad}}(r)
-
\eta_{\mathrm{rad}}(2r)
=
\frac{\Omega_{Li} \gamma_{Li}}{F r}.
```

The state-of-the-art Sand-time / Newman porous-electrode baseline, when held at fixed electrolyte and transport parameters, predicts no such pore-radius-dependent overpotential increment; its predicted radius-dependent component is zero, or equivalently a ratio of one after experimental noise is included. The prediction is falsified if the measured radius-dependent overpotential increment is statistically indistinguishable from zero, or if the measured scaling exponent in `η_rad ∝ r^{-α}` is not close to `α = 1` under conditions where the capillary term dominates the kinetic term.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"cryogenic suction" AND "ice segregation" AND "Stefan condition"`
*   `"electrochemical potential" AND "Butler-Volmer" AND "moving boundary" AND "lithium dendrite"`
*   `"frost heave" AND "lithium dendrite" AND "segregation potential"`
*   `"Gibbs-Thomson" AND "cryogenic suction" AND "Nernst-Planck"`
*   `"separator pore radius" AND "critical overpotential" AND "lithium plating"`