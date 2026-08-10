---
sid_metadata:
  entry_id: "SID-0011"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Microsoft"
  model_family: "Copilot"
  model_version: "1.2"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "electrodeposition-dendrite-growth"
  domain_b: "evaporative-colloidal-fingering-deposition"
  structural_family: "moving-boundary-flux-driven-instabilities"
  triple_correspondence_vectors:
    - "flux_limited_advection-diffusion_operator"
    - "normal_flux_to_interface_stefan_like_boundary_condition_with_kinetics"
    - "linear_dispersion_relation_with_curvature_stabilization_term"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.2
  vocabulary_divergence_score: 7.6
  expected_methodological_transfer_score: 7.9
  community_separation_score: 8.5
  representation_mismatch_score: 8.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.2"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0011

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** **Electrodeposition dendrite growth** in concentrated electrolytes (metal plating on a planar electrode) where ionic transport (diffusion + electromigration) supplies mass to a moving metal/electrolyte interface whose normal velocity is set by Faradaic reaction kinetics (Butler–Volmer type) and surface-energy (curvature) effects.
*   **Silo B (Field 2):** **Evaporative colloidal fingering deposition** (pattern formation at a receding contact line or drying front) where colloidal particles are transported by advection and diffusion toward a moving deposition front whose normal advance is set by adsorption/attachment kinetics and capillary/curvature-driven smoothing.
*   **Mathematical Isomorphism:** Under the quasi-electroneutral, thin-double-layer, and dilute-colloid limits, both systems reduce to a **flux-limited advection–diffusion operator** for a conserved scalar \(c\) supplying mass to a **moving boundary** whose normal velocity \(V_n\) is proportional to the **normal flux** \(J_n\) at the interface with a local kinetic law that includes a curvature-dependent term; linearizing about a flat front yields an identical **dispersion relation** of the form \(\sigma(k)=\alpha k - \beta k^2 - \gamma k^3\) (leading-order terms shown) where the destabilizing term is proportional to the steady flux and the stabilizing terms arise from diffusion and curvature — the correspondence holds after the explicit variable identifications and nondimensionalizations shown below.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Ion concentration \(c_i(\mathbf{x},t)\)** ↔ **colloid volume fraction \(c(\mathbf{x},t)\)**
  *   *Operator Role:* Both enter the same **advection–diffusion operator** \(\partial_t c + \nabla\cdot(\mathbf{u} c) = -\nabla\cdot \mathbf{J}\) with \(\mathbf{J}\) a diffusive (and electromigrative for ions) flux; both are scalar fields (conserved mass per unit volume) after nondimensionalization \(c\mapsto c/c_0\).
*   **Electromigration flux \(-\mu z c \nabla\phi\)** ↔ **advective capillary-driven drift \(c\,\mathbf{u}_{cap}\)**
  *   *Operator Role:* Both contribute a directed transport term that can be written as an effective advective flux \(\mathbf{U}_{\rm eff} c\); define \(\mathbf{U}_{\rm eff}^{(A)} = -\mu z \nabla\phi\), \(\mathbf{U}_{\rm eff}^{(B)}=\mathbf{u}_{cap}\); both are vector fields entering \(\nabla\cdot(\mathbf{U}_{\rm eff} c)\).
*   **Faradaic reaction current density \(j_F\)** ↔ **adsorption/attachment flux \(j_{ads}\)**
  *   *Operator Role:* Both set the **normal mass flux** into the moving interface and appear in the **Stefan-like boundary condition** \(V_n = \Omega j_n\) (with appropriate molecular/particle volume \(\Omega\)); both are scalar flux densities with kinetic dependence on local concentration and overpotential / local chemical potential.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A (Electrodeposition) — governing model (reduced, quasi-electroneutral limit).**  
Transport in the electrolyte for a single dominant cation species (after electroneutrality and thin double layer reduction) can be written as an advection–diffusion–migration equation for the cation concentration \(c(\mathbf{x},t)\):
```math
\partial_t c + \nabla\cdot\big(\mathbf{U}_{\rm eff}^{(A)} c\big) = D\,\nabla^2 c,
```
where \(\mathbf{U}_{\rm eff}^{(A)} = -\mu z \nabla\phi\) is the electromigration-induced drift (mobility \(\mu\), valence \(z\)), \(D\) is the ionic diffusivity, and \(\phi\) solves a quasi-electroneutral potential equation (Poisson reduced to a constraint) consistent with current continuity. At the metal/electrolyte interface \(\Gamma(t)\) the normal mass balance (Stefan-like) and kinetic law (Butler–Volmer linearized form shown) read:
```math
V_n = \Omega\, j_n,\qquad
j_n = k_0\big(c|_{\Gamma} - c_{eq}(\phi|_{\Gamma})\big) - \kappa_m \mathcal{H},
```
where \(V_n\) is the interface normal velocity, \(\Omega\) is atomic volume, \(j_n\) is the normal ionic flux consumed by plating, \(k_0\) is an effective kinetic coefficient (linearized Faradaic response), \(c_{eq}\) is the local equilibrium concentration (function of local potential), \(\kappa_m\) is a curvature-mobility coupling, and \(\mathcal{H}\) is mean curvature (surface-energy contribution).

**Silo B (Evaporative colloidal fingering) — governing model (thin-front deposition limit).**  
Colloidal particle transport toward a drying/deposition front is governed by advection–diffusion of particle concentration \(c(\mathbf{x},t)\):
```math
\partial_t c + \nabla\cdot\big(\mathbf{U}_{\rm eff}^{(B)} c\big) = D_p\,\nabla^2 c,
```
where \(\mathbf{U}_{\rm eff}^{(B)}\) is the capillary/evaporation-driven drift field (e.g., radial capillary flow toward the contact line), and \(D_p\) is the particle diffusivity. The moving deposition front \(\Gamma(t)\) satisfies a mass-balance and adsorption-limited kinetic law:
```math
V_n = \Omega_p\, j_n^{(B)},\qquad
j_n^{(B)} = k_{ads}\big(c|_{\Gamma} - c_{sat}\big) - \kappa_p \mathcal{H},
```
with \(\Omega_p\) the particle volume per deposited unit area, \(k_{ads}\) an attachment rate, \(c_{sat}\) a saturation concentration at the front, and \(\kappa_p\) a curvature-dependent smoothing coefficient (capillary pressure effect).

**Explicit operator-level correspondence and nondimensionalization.**  
Define nondimensional concentration \(\tilde c = c/c_0\), length scale \(L\), time scale \(T=L/U_0\) with \(U_0\) a characteristic drift speed, and nondimensional curvature \(\tilde{\mathcal H}=L\mathcal H\). Under the identifications
```math
\mathbf{U}_{\rm eff}^{(A)} \leftrightarrow \mathbf{U}_{\rm eff}^{(B)},\quad
D \leftrightarrow D_p,\quad
\Omega\,k_0 \leftrightarrow \Omega_p\,k_{ads},\quad
c_{eq}(\phi)\leftrightarrow c_{sat},
```
the two transport equations become identical in nondimensional form:
```math
\partial_{\tilde t}\tilde c + \nabla_{\tilde x}\cdot(\tilde{\mathbf U}\,\tilde c) = \mathrm{Pe}^{-1}\nabla_{\tilde x}^2\tilde c,
```
with \(\mathrm{Pe}=U_0 L/D\). The interface condition in nondimensional variables is
```math
\tilde V_n = \Lambda\big(\tilde c|_{\Gamma}-\tilde c_*\big) - \Gamma_c\,\tilde{\mathcal H},
```
where \(\Lambda\) is a nondimensional kinetic Damköhler-like number and \(\Gamma_c\) is the nondimensional curvature coefficient. Both systems therefore share the same **flux-to-velocity operator** mapping \(j_n\mapsto V_n\) and the same advection–diffusion operator for the supplying scalar.

**Linear stability (dispersion relation) — demonstrated on both sides.**  
Linearize a flat front at \(y=0\) with small perturbation \(h(x,t)=\hat h e^{ikx+\sigma t}\). For both systems (identical nondimensional operator and boundary condition above) the standard linearization (mass conservation + diffusion-limited supply + curvature term) yields, to leading orders,
```math
\sigma(k) = \Lambda\,\tilde J_0\,|k| - \mathrm{Pe}^{-1} k^2 - \Gamma_c |k|^3 + \mathcal{O}(k^4),
```
where \(\tilde J_0\) is the steady normal flux into the flat front (nondimensional), the \(|k|\) destabilizing term arises from the nonlocal coupling of front perturbations to the far-field flux (Mullins–Sekerka type kernel in both derivations), the \(k^2\) term is diffusion-limited smoothing, and the \(|k|^3\) term is curvature-capillary stabilization mapped from surface-energy in electrodeposition to capillary pressure in colloidal fronts. The same functional form and origin of each term are derived independently in the electrodeposition linearization (electromigration-diffusion + Butler–Volmer linear kinetics + curvature) and in the colloidal deposition linearization (capillary-driven advection + adsorption kinetics + capillary curvature), satisfying the Triple-Correspondence Rule: **(1)** governing operator, **(2)** boundary kinetic flux-to-velocity law with curvature, **(3)** linear dispersion relation with identical term structure.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** **Electrodeposition (Silo A)** → **Colloidal fingering deposition (Silo B)**
*   **Asymmetric Maturity Rationale:** The electrodeposition community has developed mature, quantitative linear-stability control strategies and time-dependent current-shaping protocols (pulsed currents, waveform engineering) grounded in operator-level models (Nernst–Planck + Butler–Volmer reductions) and fast spectral solvers for the Mullins–Sekerka kernel; they also possess experimentally validated in-situ diagnostics (electrochemical impedance spectroscopy, high-speed optical/electrochemical imaging) and control-theoretic pulse-design tools. The colloidal deposition community has precise experimental control of evaporation and flow but lacks a widely adopted operator-level pulse/flux-shaping methodology that maps a time-dependent supply flux to suppression of fingering instabilities via the same dispersion-kernel manipulation.
*   **Target Bottleneck Mitigation:** **Hypothesis:** Applying electrodeposition-style **flux-shaping protocols** (time-periodic modulation of the supply drift \(\mathbf{U}_{\rm eff}\) or the effective normal attachment rate \(k_{ads}(t)\)) designed by spectral optimization of the linear operator will reduce the maximum linear growth rate \(\max_k \sigma(k)\) for colloidal fingering below zero for a class of experimentally relevant Peclet numbers \(\mathrm{Pe}\in[10^1,10^3]\), thereby preventing fingering and producing uniform deposition fronts at higher mean flux than steady protocols allow. The transfer requires adapting pulse-design algorithms (spectral optimization, adjoint-based control) from electrodeposition to the colloidal advection–diffusion operator with the same kernel structure.
*   **Falsifiable Prediction:** For a planar drying front experiment with measured nondimensional parameters \(\mathrm{Pe}\) and \(\Gamma_c\), let the steady-state nondimensional flux be \(\tilde J_0\) and the steady maximal linear growth rate be \(\sigma_{\max}^{\rm steady}=\max_k \sigma_{\rm steady}(k)>0\). There exists a time-periodic modulation \(k_{ads}(t)=\bar k_{ads}\big(1+\epsilon\sin(2\pi f t)\big)\) with amplitude \(\epsilon\in(0,1)\) and frequency \(f\) such that the time-averaged maximal Floquet exponent \(\sigma_{\max}^{\rm pulsed}\) satisfies
```math
\sigma_{\max}^{\rm pulsed}(\epsilon,f;\mathrm{Pe},\Gamma_c,\tilde J_0) \le 0,
```
and the **quantitative** falsification test is: using the same experimental geometry and mean flux \(\bar k_{ads}\), the pulsed protocol must reduce the measured spectral power of front perturbations at the previously dominant wavenumber \(k^*\) by at least **90%** relative to steady deposition within three characteristic diffusion times \(T_D=L^2/D_p\). If repeated experiments at the same \(\mathrm{Pe}\), \(\Gamma_c\), and \(\tilde J_0\) fail to achieve \(\sigma_{\max}^{\rm pulsed}\le 0\) or do not reduce spectral power by ≥90%, the hypothesis is falsified. The inequality for \(\sigma_{\max}^{\rm pulsed}\) is computable from the linearized operator and the Floquet analysis derived from the equations above; no external numeric constants are assumed.
  
## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"electrodeposition dendrite linear stability" AND "Butler–Volmer" AND "Mullins–Sekerka"`
*   `"colloidal deposition fingering" AND "adsorption-limited deposition" AND "linear stability"`
*   `"pulsed current control" AND "morphological stability" AND "flux-shaping" `