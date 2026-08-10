---
sid_metadata:
  entry_id: "SID-0036"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "DeepSeek"
  model_family: "DeepSeek"
  model_version: "V4 Pro"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "polymer-melt-extrusion"
  domain_b: "3d-cell-migration-in-ecm"
  structural_family: "upper-convected-maxwell-viscoelastic-flows"
  triple_correspondence_vectors:
    - "upper_convected_stress_evolution_operator"
    - "momentum_balance_with_divergence_of_extra_stress"
    - "weissenberg_number_elastic_instability_onset_condition"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 8.5
  community_separation_score: 9.0
  representation_mismatch_score: 7.8
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.5
    uncertainty: "±1.2"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "incompatible_boundary_conditions"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0036

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Non‑isothermal viscoelastic polymer melt flow in planar extrusion dies, governed by the incompressible Navier–Stokes equations coupled to an Oldroyd‑B constitutive model for the extra‑stress tensor, exhibiting purely elastic instabilities (Pakdel–McKinley mechanism) at high Weissenberg numbers.
*   **Silo B (Field 2):** Three‑dimensional migration of a mesenchymal cell through a dense, fibrous collagen‑I extracellular matrix (ECM), commonly modeled as an upper‑convected Maxwell viscoelastic solid that undergoes large deformations due to cell‑exerted traction forces.
*   **Mathematical Isomorphism:** The coupled momentum–stress system describing the ECM deformation field u(x,t) and the viscoelastic extra‑stress tensor τ(x,t) under cell‑applied boundary traction is, after non‑dimensionalisation that absorbs the matrix stiffness and cell‑generated force scale, operator‑identical to the dimensionless Oldroyd‑B system for a polymer melt in a moving frame, with the cell body acting as a moving, force‑imposing boundary; both systems are described by the same upper‑convected derivative constitutive operator and exhibit an elastic instability governed by a critical Weissenberg number Wi_crit that depends on the local streamline curvature and the ratio of normal stress differences to shear stress.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Polymer extra‑stress tensor** τ^{(p)} ↔ **ECM viscoelastic stress** σ^{(ve)}
    *   *Operator Role:* Both are second‑rank symmetric tensors entering the momentum equation as ∇·τ (divergence), and both evolve according to the upper‑convected Maxwell operator: τ + λ τ^▽ = 2η D, where τ^▽ ≡ ∂τ/∂t + (v·∇)τ − (∇v)τ − τ(∇v)^T for Silo A, and identically for σ^{(ve)} with the ECM velocity field v = ∂u/∂t in Silo B. The mathematical type is real symmetric 3×3 tensor; the extra‑stress τ^{(p)} in A is non‑dimensionalized by η_p U/L, and σ^{(ve)} in B by G_0 (the plateau modulus), which are the same after the mapping η_p ↔ G_0 λ_ECM.
*   **Weissenberg number** Wi_A = λ_p γ̇ ↔ **Cell‑migration Weissenberg number** Wi_B = λ_ECM v_cell / R_cell
    *   *Operator Role:* Both appear as the coefficient of the nonlinear advective terms in the constitutive equation after the transformation to dimensionless variables, and control the onset of a purely elastic instability through the Pakdel–McKinley criterion: [τ_{nn} / (η_0 γ̇)] (1/R) ≥ M_crit, where R is the local radius of curvature of a streamline (Silo A) or of the cell‑induced flow trajectory (Silo B). Both numbers are dimensionless similarity parameters that govern the ratio of elastic normal stress to viscous shear stress.
*   **Die wall no‑slip condition** ↔ **ECM far‑field zero‑displacement condition**
    *   *Operator Role:* Both supply Dirichlet boundary conditions for the velocity field: v = 0 on stationary solid walls in A; u = 0 (or v = ∂u/∂t = 0) on the boundaries of the computational domain in B. In the moving reference frame attached to the migrating cell, the ECM far‑field condition becomes a flow with uniform velocity −v_cell, exactly matching the fixed‑wall condition in a laboratory frame for the extruder.

## 3. CORE MATHEMATICAL PARALLELISM
In polymer melt extrusion, the flow of an incompressible Oldroyd‑B fluid is described by conservation of mass and momentum together with an evolution equation for the extra‑stress tensor τ^{(p)}. The dimensionless equations read
```math
\nabla\cdot\mathbf{v}=0,\qquad 
Re\left(\frac{\partial\mathbf{v}}{\partial t}+\mathbf{v}\cdot\nabla\mathbf{v}\right)=-\nabla p+\nabla\cdot\boldsymbol{\tau}^{(p)},
```
```math
\boldsymbol{\tau}^{(p)}+Wi\left(\frac{\partial\boldsymbol{\tau}^{(p)}}{\partial t}+\mathbf{v}\cdot\nabla\boldsymbol{\tau}^{(p)}-\nabla\mathbf{v}\cdot\boldsymbol{\tau}^{(p)}-\boldsymbol{\tau}^{(p)}\cdot(\nabla\mathbf{v})^T\right)=2\mathbf{D},
```
where Re = ρUL/η_0, Wi = λ_p U/L, and D = (∇v + (∇v)^T)/2.

In the cell‑migration community, a widely adopted large‑deformation constitutive model for a cross‑linked collagen ECM treats the gel as an upper‑convected Maxwell (UCM) solid. Expressing the elastic stress σ^{(ve)} directly in terms of the displacement field u via the deformation gradient tensor F = I + ∇u, one writes a finite‑strain viscoelastic model whose rate form, linearised for small increments, yields the identical operator structure. The momentum balance (neglecting inertial terms) and the stress evolution in a frame moving with the migrating cell at velocity v_cell become
```math
\nabla\cdot\mathbf{v}=0,\qquad 
\mathbf{0} = -\nabla p + \nabla\cdot\boldsymbol{\sigma}^{(ve)},
```
```math
\boldsymbol{\sigma}^{(ve)}+Wi_B\left(\frac{\partial\boldsymbol{\sigma}^{(ve)}}{\partial t}+\mathbf{v}\cdot\nabla\boldsymbol{\sigma}^{(ve)}-\nabla\mathbf{v}\cdot\boldsymbol{\sigma}^{(ve)}-\boldsymbol{\sigma}^{(ve)}\cdot(\nabla\mathbf{v})^T\right)=2\;\frac{\eta_{ECM}}{G_0\lambda_{ECM}}\mathbf{D},
```
where Wi_B = λ_ECM v_cell / R_cell is defined using the matrix relaxation time λ_ECM, the cell speed v_cell, and a characteristic cell radius R_cell. The right‑hand side viscosity η_ECM is related to the plateau modulus by η_ECM = G_0 λ_ECM, so that the coefficient reduces to 2, exactly mirroring the Oldroyd‑B form in Silo A. The formal correspondence is established by the variable identification
```math
\mathbf{x}_A\leftrightarrow\mathbf{x}_B,\quad
\mathbf{v}_A\leftrightarrow\mathbf{v}_B,\quad
\boldsymbol{\tau}^{(p)}_A\leftrightarrow\boldsymbol{\sigma}^{(ve)}_B,\quad
Wi_A\leftrightarrow Wi_B,
```
and by interpreting the zero‑displacement far‑field condition in the cell problem as a uniform inflow with velocity −v_cell e_z in the co‑moving frame. The two systems share not only the differential operator of the constitutive equation but also the momentum balance (Stokes flow for typical cell migration, a finite‑Re but often Stokes‑dominated limit in extrusion) and the boundary‑driven flow geometry. The correspondence extends as far as the constitutive assumptions remain in the UCM limit without the solvent viscosity term (Oldroyd‑B includes a solvent, but in many extrusion models the solvent viscosity is neglected, reducing to UCM, exactly matching the standard solid‑ECM model).

To demonstrate the conserved quantity underpinning the elastic instability, we note that for both systems a first integral of the steady two‑dimensional creeping flow equations exists when the streamlines align with the coordinate axes, giving the normal stress difference N_1 = τ_{xx} - τ_{yy} = 2 Wi τ_{xy}² along a streamline. This relation is derived by integrating the constitutive equation along a streamline for both A and B, and its breakdown due to streamline curvature is the origin of the Pakdel–McKinley purely elastic instability:
```math
\frac{N_1}{\eta_0\dot{\gamma}}\;\frac{1}{R} \ge M_{crit},
```
where R is the local radius of curvature and M_{crit} is a numerically determined threshold. For Silo A, M_{crit} ≈ 3–5 for planar contraction flows; for Silo B, we hypothesise an analogous threshold for the onset of fluctuating traction forces when the cell‑induced flow curvature exceeds a critical value, measurable via time‑resolved traction force microscopy.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Polymer‑Melt Extrusion (Silo A) → 3D Cell Migration in ECM (Silo B)
*   **Asymmetric Maturity Rationale:** The computational rheology community has developed highly optimised, stabilised finite‑element and finite‑volume codes (e.g., log‑conformation representation, discrete elastic‑viscous split stress, adaptive mesh refinement) specifically for the high‑Weissenberg‑number problem. These methods can stably integrate the upper‑convected Maxwell equations beyond Wi ≈ 1, where the hyperbolic nature of the stress equation causes severe numerical breakdown. In contrast, the cell‑migration modelling community typically solves quasi‑static linear elastic or poroelastic equations using standard structural mechanics solvers; fully coupled large‑deformation viscoelastic simulations with a UCM‑type rate formulation remain rare, and when attempted they often fail at moderate Wi_B due to the same stress‑gradient singularities known from polymer CFD. The target field is genuinely mature in static ECM mechanics but lacks a robust numerical toolkit for the highly nonlinear, high‑Wi regime where elastic instabilities are expected to dominate dynamic cell traction.
*   **Target Bottleneck Mitigation:** We hypothesise that importing the log‑conformation tensor formulation and the associated streamline‑upwind Petrov–Galerkin (SUPG) stabilisation, standard in Silo A since the early 2000s, will enable the first stable, mesh‑converged simulations of a polarised cell migrating in a UCM‑modelled ECM at Wi_B > 1. This will directly resolve the traction‑force fluctuations that currently cannot be computed with the available linear‑elastic or small‑strain‑only toolkits, unlocking a quantitative comparison with time‑lapse traction force microscopy data that to date lacks a predictive computational counterpart in the high‑strain regime.
*   **Falsifiable Prediction:** For a spindle‑shaped mesenchymal cell (major axis 50 µm, speed 0.1 µm/s) embedded in a 2 mg/mL collagen‑I gel (λ_ECM ≈ 5 s, plateau modulus G₀ ≈ 10 Pa), the mapped Weissenberg number is Wi_B ≈ (5 s × 0.1 µm/s)/(25 µm) = 0.02, well below the instability threshold. If the gel is cross‑linked to increase λ_ECM to 100 s, or the cell is stimulated to migrate at 2 µm/s, Wi_B reaches ≈ (100 × 2)/25 = 8. Our prediction states that in such a regime, the time‑averaged autocorrelation of the traction‑force dipole moment measured by 3D traction force microscopy will exhibit a secondary peak at a characteristic elastic oscillation period of ≈ 2π λ_ECM / √(Wi_B² − Wi_{crit}²) with Wi_{crit} ≈ 3.0 derived from Pakdel–McKinley for the cell‑induced flow curvature extracted from the numerical velocity field. The prediction is falsified if no such secondary peak appears above Wi_B = 3 in at least 15 independent cell trajectories, or if the measured dominant frequency does not scale with λ_ECM^{-1} as the gel relaxation time is varied by temperature. The baseline is the current literature consensus that cell traction stresses are aperiodic and dominated by actin‑myosin pulsatility; our hypothesis asserts that above a measurable Wi_B, purely elastic ECM instabilities become the dominant driver of force fluctuations, replacing the myosin‑driven signal with a matrix‑driven one.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"upper-convected Maxwell" AND "extracellular matrix" AND "cell migration" AND "viscoelastic"`
*   `"Pakdel-McKinley" AND "traction force microscopy" AND "collagen"`
*   `"log-conformation representation" AND "cell mechanics" OR "ECM"`