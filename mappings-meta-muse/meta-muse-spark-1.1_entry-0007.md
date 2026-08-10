---
sid_metadata:
  entry_id: "SID-0007"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Meta"
  model_family: "Muse"
  model_version: "Spark 1.1"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "lithium-metal-dendrite-electrodeposition"
  domain_b: "geological-stylolite-pressure-solution"
  structural_family: "stress-mediated-ATG-free-boundary-instability"
  triple_correspondence_vectors:
    - "shared_elastic_contribution_to_chemical_potential_operator"
    - "shared_quasistatic_laplacian_transport_governing_operator"
    - "shared_ATG_capillary_stabilized_dispersion_threshold"
    - "shared_elastic_surface_chemical_variational_functional"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities / timescale_separation_seconds_vs_megayears"
prior_discovery_metrics:
  structural_isomorphism_score: 8.6
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.4
  community_separation_score: 9.2
  representation_mismatch_score: 8.8
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±0.9"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_Butler_Volmer_vs_linear_dissolution_kinetics"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0007

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Electro-chemo-mechanical lithium-metal dendrite formation during electrodeposition in solid-state batteries, where compressive stack pressure and interfacial tension compete to morphologically stabilize a moving metal-electrolyte interface.
* **Silo B (Field 2):** Geological stylolite formation by stress-driven pressure-solution, where quartz/carbonate grains dissolve at stressed contacts and precipitate in pores, forming serrated dissolution seams.
* **Mathematical Isomorphism:** Both systems evolve by the same Asaro-Tiller-Grinfeld (ATG) free-boundary class under the restriction of quasi-static bulk equilibrium, where the interface normal velocity is driven by the shared_elastic_contribution_to_chemical_potential_operator, transport obeys the shared_quasistatic_laplacian_transport_governing_operator with Gibbs-Thomson curvature, linear stability obeys the identical shared_ATG_capillary_stabilized_dispersion_threshold, and dynamics derive from the same shared_elastic_surface_chemical_variational_functional.

## 2. DIAGNOSTIC VOCABULARY MATRIX
* **Electrochemical overpotential-shifted chemical potential** ↔ **Normal-stress-shifted dissolution chemical potential**
    * *Operator Role:* Scalar field mu: Omega -> R, C2, entering as variational derivative mu = delta F / delta h = mu0 + Omega * W_e(sigma) + Omega * gamma * kappa, where W_e is elastic strain energy density, gamma is isotropic surface energy, kappa is mean curvature, Omega is molar volume. Both mu_A and mu_B have type scalar potential.
* **Dendrite normal growth velocity** ↔ **Stylolite dissolution seam velocity**
    * *Operator Role:* Scalar normal speed v_n: Gamma -> R, entering linear kinetic law v_n = L * _jump, with mobility L_A for Butler-Volmer linearized kinetics and L_B = k_diss * Omega / (R T) for pressure solution, both type scalar rate, conserved via Rankine-Hugoniot jump condition.[mu]
* **Ionic flux / current density** ↔ **Grain-boundary solute diffusion flux**
    * *Operator Role:* Vector flux J = - M * grad_s mu: R3 -> R3, entering conservation law div_s J = - v_n / Omega on interface Gamma, with M_A = kappa_eff for electrolyte and M_B = D_gb * delta_gb * c0 / (R T) for fluid film. Both J_A and J_B have type tangent vector field on interface.
* **Elastic strain energy density** ↔ **Contact strain energy density**
    * *Operator Role:* Scalar density W_e = 0.5 sigma : C^{-1} : sigma : Omega -> R, entering both chemical potential and variational functional, with sigma in Sym(3) second-order tensor obeying div sigma = 0. Transformation: sigma_n,B = n. sigma_B. n reconciles tensor to scalar normal stress.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models Li metal as a linear elastic solid in contact with a binary electrolyte. Bulk equilibrium is elliptic: mechanical equilibrium and steady-state ion transport, with interface motion driven by the jump in chemo-mechanical potential including Monroe-Newman stress penalty and surface tension.

```math
\nabla \cdot \sigma_A = 0, \quad \sigma_A = \mathbb{C}_A : \varepsilon_A \text{ in } \Omega_A, \quad \nabla \cdot (\kappa_{eff} \nabla \phi_A) = 0 \text{ in } \Omega_{elyte}
```

```math
v_{n,A} = L_A \, [\mu_{elyte} - \mu_A], \quad \mu_A = \mu_A^0 + \Omega_A W_{e,A}(\sigma_A) - \Omega_A \gamma_A \kappa_A + F \eta_A, \quad W_{e,A} = \frac{1-\nu_A^2}{2E_A}\sigma_{A}^2 \text{ at interface}
```

Silo B models a stressed grain contact with a nanometer trapped fluid film. Bulk is identical elliptic elasticity for the solid and pore fluid, with solute transport confined to the grain boundary film, interface motion by dissolution, chemical potential defined by Raj (1982) and Schmittbuhl (2004) pressure-solution law recognized by structural geologists.

```math
\nabla \cdot \sigma_B = 0 \text{ in } \Omega_{solid}, \quad \nabla_s \cdot (D_{gb}\delta_{gb} c_0/(RT) \nabla_s \mu_B) = -v_{n,B}/\Omega_B \text{ on } \Gamma_{stylolite}
```

```math
v_{n,B} = L_B \, [\mu_{pore} - \mu_B], \quad \mu_B = \mu_B^0 + \Omega_B \sigma_{n,B} + \Omega_B W_{e,B}(\sigma_B) + \Omega_B \gamma_B \kappa_B, \quad L_B = k_{diss}\Omega_B/(RT)
```

Bridge: Identification is mu_A <-> mu_B, sigma_A <-> sigma_B via sigma_n,B = n. sigma_B. n, v_n,A <-> v_n,B, J_A = -kappa_eff grad phi_A <-> J_B = -M_B grad_s mu_B, Gamma_A = Li-electrolyte front <-> Gamma_B = dissolution seam, Omega_A <-> Omega_B, gamma_A <-> gamma_B. Under transformation h(x,t) = interface height, small-slope |grad h|<<1, quasi-static limit epsilon = (M gamma)/(L E L0^2) <<1, both reduce to same ATG free-boundary operator. Correspondence holds for linearized elasticity, isotropic gamma, and linearized kinetics; stops where Butler-Volmer exponential nonlinearity dominates far from equilibrium and where plastic creep in rocks dominates over elastic storage.

Demonstration of triple correspondence vectors:

Vector 1 - shared_elastic_contribution_to_chemical_potential_operator:
```math
\mu_A = \mu_A^0 + \Omega_A \frac{1-\nu_A^2}{2E_A}\sigma_{\infty,A}^2 (1 + 2 k \hat{h}_k) - \Omega_A \gamma_A k^2 \hat{h}_k \text{ for mode } h = \hat{h}_k e^{ikx}
```
```math
\mu_B = \mu_B^0 + \Omega_B \sigma_{\infty,B} + \Omega_B \frac{1-\nu_B^2}{2E_B}\sigma_{\infty,B}^2 (1 + 2 k \hat{h}_k) + \Omega_B \gamma_B k^2 \hat{h}_k
```

Vector 2 - shared_quasistatic_laplacian_transport_governing_operator with Gibbs-Thomson Robin boundary:
```math
\nabla^2 \mu_A = 0 \text{ in } \Omega_{elyte}, \quad M_A \partial_n \mu_A = v_{n,A}/\Omega_A, \quad \mu_A|_{\Gamma} = \mu_A^0 + \Omega_A \gamma_A \kappa_A \text{ Robin-Gibbs-Thomson}
```
```math
\nabla_s^2 \mu_B = v_{n,B}/(\Omega_B M_B) \text{ on } \Gamma_{stylolite}, \quad M_B \partial_n \mu_B = v_{n,B}/\Omega_B, \quad \mu_B|_{\Gamma} = \mu_B^0 + \Omega_B \sigma_{n,B} + \Omega_B \gamma_B \kappa_B
```

Vector 3 - shared_ATG_capillary_stabilized_dispersion_threshold Type II:
```math
\omega_A(k) = L_A M_A k^2 \left[ \frac{(1-\nu_A^2)\sigma_{\infty,A}^2}{E_A} - \gamma_A k \right], \quad k_{c,A} = \frac{(1-\nu_A^2)\sigma_{\infty,A}^2}{E_A \gamma_A}, \quad \lambda_{c,A}=2\pi/k_{c,A}
```
```math
\omega_B(k) = L_B M_B k^2 \left[ \frac{(1-\nu_B^2)\sigma_{\infty,B}^2}{E_B} - \gamma_B k \right], \quad k_{c,B} = \frac{(1-\nu_B^2)\sigma_{\infty,B}^2}{E_B \gamma_B}, \quad \lambda_{c,B}=2\pi/k_{c,B}
```

Vector 4 - shared_elastic_surface_chemical_variational_functional:
```math
\mathcal{F}_A[h] = \int_{\Omega_A} W_{e,A}(\varepsilon) dV + \int_{\Gamma_A} \gamma_A \sqrt{1+|\nabla h|^2} dS + \int_{\Omega_A} f_{chem}(c_A) dV, \quad \mu_A = \delta \mathcal{F}_A / \delta h
```
```math
\mathcal{F}_B[h] = \int_{\Omega_B} W_{e,B}(\varepsilon) dV + \int_{\Gamma_B} \gamma_B \sqrt{1+|\nabla h|^2} dS + \int_{\Gamma_B} \sigma_{n,B} h dS, \quad \mu_B = \delta \mathcal{F}_B / \delta h
```

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
* **Preferred Transfer Direction:** lithium-metal-dendrite-electrodeposition → geological-stylolite-pressure-solution
* **Asymmetric Maturity Rationale:** Source field (battery electro-chemo-mechanics) has mature 3D coupled phase-field solvers with adaptive mesh refinement, Jacobian-free Newton-Krylov with block preconditioning for Cahn-Hilliard + Butler-Volmer + finite-strain elasticity, history-variable irreversibility enforcement, and MOOSE/FEniCS implementations validated against in-situ TEM. Target field (stylolite geomorphology) is mature at field mapping and statistical roughness analysis (Fourier, Hurst exponents) but lacks 3D finite-deformation coupled dissolution-elastic solvers; existing models are 2D lattice-spring or rigid-grain approximations with prescribed diffusion, no implicit coupling or AMR.
* **Target Bottleneck Mitigation:** Importing source field's variational phase-field fracture formalism (Francfort-Marigo with spectral split) replacing explicit interface tracking will resolve persistent inability to simulate interacting non-planar stylolite anastomosis and teeth coalescence in 3D, by treating dissolution seam as diffusive damage variable d with degradation g(d) multiplying W_e and coupling mu(d) through double-well potential, enabling stable large-step implicit solves for million-grain ensembles.
* **Falsifiable Prediction:** Using battery-derived phase-field code with limestone parameters E_B=30 GPa, nu_B=0.25, gamma_B=0.27 J/m2, Omega_B=3.69e-5 m3/mol, D_gb*delta_gb=1e-14 m3/s, at effective stress sigma_infty,B=50 MPa, the model predicts mean stylolite wavelength lambda_B = 2pi*E_B*gamma_B/((1-nu_B^2)*sigma_infty,B^2) = 1.02 mm +/-0.15 mm and scaling lambda_B proportional to sigma_infty,B^-2 with exponent -2.00 +/-0.10. Baseline to beat is Ebner et al. 2009 mechanical buckling model predicting lambda proportional to sigma^-1 and lambda ~2.5 mm at same conditions. Measurement on 20 Indiana limestone samples via micro-CT with 10 micron voxel will show lambda in 0.9-1.3 mm range and power-law exponent -2 within 95% CI. Falsified if mean lambda differs >40% from 1.02 mm or exponent confidence interval excludes -2 and includes -1, or if clay content >5 wt% fails to reduce effective M_B by 30% and increase lambda by >15% as predicted by diffusive transport term.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
* `"lithium dendrite" AND "Asaro-Tiller-Grinfeld" AND "phase-field chemo-mechanical"`
* `"stylolite" AND "pressure solution" AND "Mullins-Sekerka dispersion relation"`
* `"lithium dendrite" AND "stylolite" AND "elastic chemical potential"`
* `"pressure solution" AND "Butler-Volmer" AND "Gibbs-Thomson boundary condition"`
* `"stylolite wavelength scaling" AND "surface energy" AND "effective stress squared"`