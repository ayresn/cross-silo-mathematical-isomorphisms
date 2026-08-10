---
sid_metadata:
  entry_id: "SID-0039"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "DeepSeek"
  model_family: "DeepSeek"
  model_version: "V4 Pro"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "thermocapillary-thin-film-spreading"
  domain_b: "ferrofluid-thin-film-spreading"
  structural_family: "fourth-order-gradient-flow-with-forcing"
  triple_correspondence_vectors:
    - "shared_fourth-order_lubrication_operator_with_potential_forcing"
    - "dispersion_relation_for_spinodal_rupture_instability"
    - "contact_line_regularization_via_precursor_film_and_slip_length"
discovery_rationale:
  why_not_obvious: "distinct_physical_mechanisms_thermal_marangoni_vs_magnetic_kelvin_force / historically_isolated_research_communities_thermal_fluids_and_ferrohydrodynamics / mismatched_literature_terminology_despite_identical_governing_equation_class"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 8.1
  community_separation_score: 9.0
  representation_mismatch_score: 1.5
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 7.8
    uncertainty: "±1.8"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_magnetic_normal_stress_jump_vs_thermal_marangoni_stress_boundary_condition"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0039

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Thermocapillary-driven spreading and rupture of a thin viscous liquid film on a uniformly heated solid substrate, where a destabilizing Marangoni stress arises from surface tension gradients caused by temperature variations.
*   **Silo B (Field 2):** Spreading and pattern formation of a thin ferrofluid film on a solid substrate under an applied inhomogeneous, normal magnetic field, where the destabilizing magnetic normal stress arises from perturbations in the local field due to film thickness variations.
*   **Mathematical Isomorphism:** The dimensionless evolution equation for the film thickness \(h(\mathbf{x},t)\) in the long-wave (lubrication) approximation is structurally identical for both systems, taking the form \(\partial_t h = \nabla \cdot [M(h) \nabla (\nabla^2 h + \Phi)]\) with a mobility \(M(h)=h^3\), where the potential \(\Phi\) encodes the destabilizing driving force—temperature or magnetic potential—and the linear stability of a flat film exhibits a spinodal instability governed by a dispersion relation \(\omega = -k^2(k^2 - \Pi_0)\) with a control parameter \(\Pi_0\) that maps exactly between the thermal Marangoni number and the magnetic Bond number, while both regularize the moving contact line with identical Navier-slip and precursor-film conditions.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Thermocapillary Marangoni stress ↔ Magnetic Kelvin force potential
    *   *Operator Role:* The quantity \(\Phi\) enters the lubrication momentum balance as an in-plane gradient of a potential, i.e., the term \(\nabla\Phi\) in the pressure gradient. In Silo A, \(\Phi = \text{Ma}\cdot\theta(\mathbf{x})\) where Ma is the Marangoni number and \(\theta\) the dimensionless temperature; in Silo B, \(\Phi = \text{Bm}\cdot\phi(\mathbf{x})\) where Bm is the magnetic Bond number and \(\phi\) the dimensionless magnetic potential. Both are scalar potentials whose gradient drives flow, and they appear in the identical position in the thin-film equation after nondimensionalization. Both are of mathematical type `real scalar field over the substrate`.
*   Spreading coefficient \(S\) ↔ Magnetic pressure jump \(\mu_0 M H\)
    *   *Operator Role:* The constant part of the potential that sets the reference pressure level and enters the boundary condition at the contact line as a Young-type equilibrium condition. In Silo A, \(S = \sigma_{SV} - \sigma_{SL} - \sigma_{LV}\); in Silo B, the magnetic contribution \(P_{\text{mag}} = \mu_0 \int_0^H M(H') dH'\) modifies the effective spreading coefficient. Both are scalars that shift the chemical potential.
*   Thermal diffusion equation ↔ Maxwell equations in the magnetostatic limit
    *   *Operator Role:* Auxiliary field equations that determine the potential \(\Phi\) from the instantaneous film shape. In Silo A, the temperature field satisfies the Laplace equation \(\nabla^2 \theta = 0\) in the substrate and film; in Silo B, the magnetic scalar potential satisfies \(\nabla^2 \phi_m = 0\) outside the ferrofluid. Both are scalar harmonic functions coupled to the free surface by a mixed boundary condition (conductive/convective vs. permeable magnetic). Both are of type `scalar harmonic field`.

## 3. CORE MATHEMATICAL PARALLELISM
In Silo A, a thin incompressible liquid film of thickness \(h(x,y,t)\) on a heated solid is described by the long-wave lubrication equation, derived by integrating the Stokes equations with a tangential Marangoni stress at the free surface \(z = h\). With a constant substrate temperature and a prescribed heat flux from the liquid–gas interface, the film evolution is given by:
```math
\partial_t h = \nabla \cdot \left[ \frac{h^3}{3\mu} \nabla \left( \gamma \nabla^2 h + \frac{\partial \sigma}{\partial T} \Delta T \, \theta(\mathbf{x}) \right) \right],
```
where \(\gamma\) is surface tension, \(\mu\) the viscosity, \(\Delta T\) the temperature scale, and \(\theta\) solves \(\nabla^2\theta = 0\) with a convective boundary condition at the free surface. Nondimensionalizing with a characteristic film thickness \(h_0\), the equation becomes:
```math
\frac{\partial H}{\partial \tau} = \nabla \cdot \left[ H^3 \nabla \left( \nabla^2 H + \text{Ma}\, \Theta \right) \right], \qquad \text{(1)}
```
with Ma the Marangoni number.

In Silo B, a thin layer of an isothermal ferrofluid with constant magnetization \(M\) subjected to a normal applied magnetic field \(\mathbf{H} = -\nabla\phi_m\) evolves according to the ferrohydrodynamic lubrication equations. The magnetic normal stress at the interface provides a destabilizing pressure term that depends linearly on the local film thickness for a uniform applied field gradient. The long-wave equation reads:
```math
\partial_t h = \nabla \cdot \left[ \frac{h^3}{3\eta} \nabla \left( \gamma \nabla^2 h - \mu_0 M \frac{\partial \phi_m}{\partial z}\bigg|_{z=h} \right) \right],
```
where \(\phi_m\) satisfies \(\nabla^2\phi_m = 0\) in the space above the film and appropriate jump conditions. After nondimensionalization using the same thickness scale, the equation takes the identical structural form:
```math
\frac{\partial H}{\partial \tau} = \nabla \cdot \left[ H^3 \nabla \left( \nabla^2 H - \text{Bm}\, \Phi \right) \right], \qquad \text{(2)}
```
with the magnetic Bond number Bm and the dimensionless magnetic potential \(\Phi(\mathbf{x}) = -\partial_z \phi_m\big|_{\text{interface}}\) that, to first order, is a linear functional of the film thickness perturbation.

Under the mapping \(\text{Ma}\,\Theta \leftrightarrow -\text{Bm}\,\Phi\), equations (1) and (2) are operator-identical: both are of the class \(\partial_t H = \nabla\cdot[H^3\nabla(\nabla^2 H + \Psi)]\) with a forcing potential \(\Psi\) obtained from a harmonic field. The correspondence holds as long as the Boussinesq approximation for the temperature field (constant material properties) and the linear magnetization limit \(\mathbf{M}=M\hat{\mathbf{H}}\) for the ferrofluid are valid; these constitute the only constitutive restrictions.

*Linear stability of a flat film.* For a uniform base state \(H=1\) and a constant potential \(\Psi_0\), the normal-mode perturbation \(\propto e^{\omega t + i\mathbf{k}\cdot\mathbf{x}}\) yields the identical dispersion relation:
```math
\omega = -k^2\left( k^2 - \Pi_0 \right), \qquad k = |\mathbf{k}|,
```
where the control parameter is \(\Pi_0 = -\partial\Psi/\partial H\) evaluated at \(H=1\). In Silo A, \(\Pi_0 = \text{Ma}\), and in Silo B, \(\Pi_0 = \text{Bm}\). The critical wavenumber \(k_c = \sqrt{\Pi_0}\) and the fastest-growing mode \(k_m = \sqrt{\Pi_0/2}\) are identical, establishing a complete one-to-one mapping of the linear spinodal instability.

*Contact line regularization.* In both systems, the spreading of a liquid film with a moving contact line requires a regularization to avoid a stress singularity. The standard approach in Silo A introduces a microscopic precursor film of thickness \(b\) and a Navier slip length \(\ell_s\), leading to a mobility function \(M(H) = H^3 + b^3\) and a slip-modified curvature term. Silo B employs exactly the same regularization by postulating a thin prewetting layer and a magnetic-slip length of identical functional form. The boundary condition at the apparent contact line, where \(H = b\) and the flux vanishes, is mathematically indistinguishable, giving the same dynamic contact angle relation.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Thermocapillary thin films (Silo A) → Ferrofluid thin films (Silo B)
*   **Asymmetric Maturity Rationale:** The thermocapillary community has developed highly accurate, adaptive finite-element and spectral schemes for solving the 4th-order lubrication equation with harmonic-coupling and moving contact lines, as well as rigorous branching analysis for the secondary instabilities leading to droplet arrays (the “fingering” and “polygon” patterns). Ferrofluid thin-film research still predominantly relies on lubrication-theory simulations with simple finite differences and has not systematically mapped the bifurcation structure of the pattern formation. Silo B’s mature tools are in magnetic field computation and suspension rheology, not in the numerical bifurcation analysis of nonlinear free-surface instabilities.
*   **Target Bottleneck Mitigation:** Transferring the arc-length continuation and branch-tracking algorithms from thermocapillary film studies to the ferrofluid problem will allow the first complete numerical bifurcation diagram of Rosensweig instability in a confined thin film, pinpointing the threshold Bm for secondary transitions from hexagons to labyrinthine patterns and the hysteretic regimes.
*   **Falsifiable Prediction:** For a ferrofluid film of thickness \(h_0 = 100\ \mu\mathrm{m}\), magnetic susceptibility \(\chi = 3\), and surface tension \(\gamma = 0.03\ \mathrm{N/m}\), the normalized secondary bifurcation from hexagonal to square-planform patterns will occur at a magnetic Bond number \(\text{Bm}_{\text{hex→sq}} = 1.65 \pm 0.05\) and will be supercritical, replicating the known Marangoni-number scaling \(\text{Ma}_{\text{hex→sq}} \approx 1.65\) reported in the thermocapillary literature (Boos & Thess, 1999). Falsification would occur if the computed critical Bm lies outside the range \(1.4\)–\(1.9\) after accounting for fully nonlinear magnetic field coupling.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"thermocapillary thin film" AND "lubrication equation" AND "Marangoni instability" AND "bifurcation diagram"`
*   `"ferrofluid thin film" AND "Rosensweig instability" AND "lubrication approximation" AND "pattern formation"`
*   `("thermocapillary" OR "Marangoni") AND ("ferrofluid" OR "magnetic liquid") AND ("thin film" OR "lubrication") AND ("isomorphism" OR "mapping" OR "analogy")`