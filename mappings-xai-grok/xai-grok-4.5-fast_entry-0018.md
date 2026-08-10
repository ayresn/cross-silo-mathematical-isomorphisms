---
sid_metadata:
  entry_id: "SID-0018"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "xAI"
  model_family: "Grok"
  model_version: "4.5 Fast"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "semiconductor-drift-diffusion-transport"
  domain_b: "electrolyte-poisson-nernst-planck-transport"
  structural_family: "self-consistent-drift-diffusion-poisson-systems"
  triple_correspondence_vectors:
    - "shared_drift_diffusion_flux_operator"
    - "shared_poisson_self-consistent_electrostatic_coupling"
    - "shared_mixed_dirichlet_neumann_electrostatic_boundary_structure"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_device-physics_versus_soft-matter-electrokinetics_communities / incompatible_primary_ontologies_of_band-structure_carriers_versus_solvated_ions"
prior_discovery_metrics:
  structural_isomorphism_score: 9.1
  vocabulary_divergence_score: 8.7
  expected_methodological_transfer_score: 8.4
  community_separation_score: 9.0
  representation_mismatch_score: 7.8
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.6
    uncertainty: "±1.1"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "constitutive_law_mismatch_in_mobility_or_activity_coefficients"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0018

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Microelectronic device physics — continuum drift-diffusion transport of electrons and holes self-consistently coupled to the electrostatic potential inside semiconductor structures.
* **Silo B (Field 2):** Soft-matter electrokinetics / electrochemical transport — continuum Nernst–Planck transport of multiple ionic species self-consistently coupled to the electrostatic potential inside electrolytes and charged soft interfaces.
* **Mathematical Isomorphism:** Both systems are governed by an identical self-consistent parabolic–elliptic operator structure in which species fluxes of drift-diffusion form are divergence-coupled to a Poisson equation for the electrostatic potential, sharing the same flux operator, the same Poisson coupling, and the same mixed Dirichlet–Neumann electrostatic boundary structure (under the standard continuum-limit nondimensionalization that maps carrier densities to ion concentrations and band-edge potentials to electrochemical potentials).

## 2. DIAGNOSTIC VOCABULARY MATRIX
* Electron/hole density \(n,p\) ↔ Ionic number densities \(c_i\)
    * *Operator Role:* Both enter the identical divergence-form continuity equation as the conserved scalar densities whose fluxes are of drift-diffusion type; the explicit nondimensionalization \(n,p \mapsto c_i\) (scaled by reference doping or bulk concentration) places both objects in the same function space \(L^\infty\cap H^1\).
* Electrostatic potential \(\psi\) ↔ Electrostatic potential \(\phi\)
    * *Operator Role:* Both are the solution of the identical Poisson operator \(-\nabla\cdot(\varepsilon\nabla\cdot)=\) space charge; the mapping is the identity after nondimensionalization by thermal voltage \(kT/q\).
* Drift-diffusion flux \(\mathbf{J}_n = q\mu_n n\mathbf{E}+qD_n\nabla n\) ↔ Nernst–Planck flux \(\mathbf{J}_i = -D_i\nabla c_i - z_i\mu_i c_i\nabla\phi\)
    * *Operator Role:* Both realize the same first-order differential flux operator (gradient of chemical potential plus electrophoretic drift); Einstein relation \(D=\mu kT/q\) supplies the exact coefficient identification.

## 3. CORE MATHEMATICAL PARALLELISM
In semiconductor device physics the continuum transport of electrons and holes is described by the drift-diffusion continuity equations closed by Poisson’s equation for the electrostatic potential:
```math
\frac{\partial n}{\partial t}=\frac{1}{q}\nabla\cdot\mathbf{J}_n-R,\qquad
\mathbf{J}_n=q\mu_n n\mathbf{E}+qD_n\nabla n,
```
```math
\frac{\partial p}{\partial t}=-\frac{1}{q}\nabla\cdot\mathbf{J}_p-R,\qquad
\mathbf{J}_p=q\mu_p p\mathbf{E}-qD_p\nabla p,
```
```math
\nabla\cdot(\varepsilon\nabla\psi)=q(n-p-C),
```
where \(\mathbf{E}=-\nabla\psi\) and \(R\) is a recombination term. The electrostatic boundary conditions are mixed: Dirichlet (applied contact voltages) on ohmic or Schottky contacts and homogeneous Neumann (or Robin) on insulating surfaces.

In electrolyte and soft-matter electrokinetics the continuum transport of ionic species is described by the Poisson–Nernst–Planck system:
```math
\frac{\partial c_i}{\partial t}=-\nabla\cdot\mathbf{J}_i,\qquad
\mathbf{J}_i=-D_i\nabla c_i-z_i\mu_i c_i\nabla\phi,
```
```math
-\nabla\cdot(\varepsilon\nabla\phi)=\rho_f+\sum_i z_i e c_i,
```
with the same mixed Dirichlet–Neumann structure for \(\phi\) (fixed potential on electrodes, no-flux or prescribed surface charge on insulating or charged walls).  

Under the standard nondimensionalization that scales potentials by the thermal voltage \(kT/e\), lengths by a macroscopic device or channel length, and densities by a reference concentration (doping level or bulk electrolyte concentration), the flux operators become identical:
```math
\mathbf{J}\propto -(\nabla u+u\nabla\psi)
```
for each carrier/ionic density \(u\), the Poisson operators coincide, and the boundary-condition pairs map onto each other. The correspondence therefore holds at the level of the full differential operator (continuity + self-consistent Poisson) and its boundary structure; it stops when generation–recombination kinetics or concentration-dependent activity coefficients are retained without further constitutive mapping.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
* **Preferred Transfer Direction:** Semiconductor-drift-diffusion-transport → Electrolyte-poisson-nernst-planck-transport
* **Asymmetric Maturity Rationale:** Semiconductor device physics possesses a decades-mature suite of positivity-preserving finite-volume and finite-element discretizations (Scharfetter–Gummel exponential fitting, Slotboom variables, adaptive anisotropic meshing, and industrial TCAD solvers) specifically engineered for the drift-diffusion–Poisson operator under extreme density gradients and boundary layers. Soft-matter electrokinetics and electrochemical continuum modeling are mature in constitutive theory and asymptotic analysis yet lack comparably robust, industrially hardened numerical infrastructure for the identical operator when multiple ionic species, large Debye-layer contrasts, and moving free boundaries are present.
* **Target Bottleneck Mitigation:** Importation of the Scharfetter–Gummel flux discretization together with density-aware anisotropic mesh adaptation directly into multi-ion Poisson–Nernst–Planck solvers for porous-electrode battery models is predicted to eliminate the well-documented oscillations and loss of positivity that currently force researchers to employ artificially elevated permittivities or excessively fine uniform meshes.
* **Falsifiable Prediction:** On the standard Newman porous-electrode benchmark (1 M LiPF₆ in a 50 µm separator, applied current 1–5 mA cm⁻²), a Scharfetter–Gummel / anisotropic-adaptation PNP solver must reduce the discrete maximum principle violation (negative concentration cells) to zero while simultaneously lowering the L² error in the steady-state concentration profile by at least a factor of four relative to a conventional second-order finite-volume baseline at identical degrees of freedom; failure to achieve both the zero-violation and the four-fold error reduction on this benchmark falsifies the claimed transfer advantage.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
* `"Scharfetter-Gummel" AND "Poisson-Nernst-Planck" AND "electrolyte"`
* `"drift-diffusion" AND "Nernst-Planck" AND "self-consistent Poisson" AND semiconductor`
* `"device simulation methods" AND "Poisson-Nernst-Planck" AND battery OR electrokinetic`