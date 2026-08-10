---
sid_metadata:
  entry_id: "SID-0032"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "ultrathin-polymer-film-dewetting"
  domain_b: "lithium-intercalation-phase-separation"
  structural_family: "conserved-gradient-flow-spinodal"
  triple_correspondence_vectors:
    - "degenerate_mobility_conserved_gradient_flow_operator"
    - "energy_dissipation_H_minus_one_metric"
    - "neutral_substrate_no_flux_boundary_pair"
    - "spinodal_fastest_mode_wavelength_selector"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.8
  vocabulary_divergence_score: 8.4
  expected_methodological_transfer_score: 8.2
  community_separation_score: 8.1
  representation_mismatch_score: 6.7
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.4
    uncertainty: "±0.9"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "electrochemical_surface_flux_or_chemo_mechanical_coupling_breaking_closed_gradient_flow"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0032

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Ultrathin polymer-film dewetting: capillary- and disjoining-pressure-driven lubrication flow of a nanometric liquid film on a neutral substrate, with film thickness conserved except at negligible evaporation.
*   **Silo B (Field 2):** Lithium-intercalation phase separation: spinodal decomposition of lithium site fraction in a closed or potentiostatically equilibrated intercalation particle, modeled by a regular-solution free energy and concentration-dependent chemical diffusion.
*   **Mathematical Isomorphism:** Under nondimensionalization of film thickness and lithium site fraction to dimensionless conserved scalars, and restricted to isothermal, closed, non-reactive, small-slope dynamics without elastic or hydrodynamic memory terms, both systems are H^{-1} gradient flows of a local free energy with square-gradient penalty, sharing the same conserved mobility-divergence operator, no-flux natural boundary conditions, nonpositive free-energy dissipation law, and spinodal dispersion relation with an identical fastest-mode selector.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Film thickness h ↔ Lithium site fraction c
    *   *Operator Role:* Conserved scalar state variable u in the divergence operator for both systems. The dimensional film thickness h is scaled by h_0, and the site fraction c is scaled by c_max, producing dimensionless fields U_A and U_B in Section 3. Both fields are real scalar states whose spatial integral is conserved under the displayed boundary conditions.
*   Lubrication mobility M_A(h) ↔ Darken mobility M_B(c)
    *   *Operator Role:* Positive scalar mobility multiplying the gradient of the chemical potential in the conserved flux. Both enter the identical operator structure where the time derivative is the divergence of a mobility-weighted chemical-potential gradient. They are nondimensionalized by reference values M_A(h_0) and M_B(c_0).
*   Effective interface potential derivative Phi_A'(h) ↔ Regular-solution chemical derivative f_B'(c)
    *   *Operator Role:* Local functional derivative of the non-gradient free-energy density. Both supply the nonlinear local term in the chemical potential. After scaling by Phi_A''(h_0) h_0 and f_B''(c_0), respectively, they enter the same dimensionless chemical-potential operator as the derivative of a dimensionless local potential.
*   Surface tension gamma_A ↔ Gradient-energy coefficient kappa_B
    *   *Operator Role:* Square-gradient coefficient in the free energy. Both generate the second-order spatial operator contribution to the chemical potential and, after one additional divergence, the fourth-order regularization in the evolution equation. The corresponding length scales ell_A and ell_B are defined in Section 3.
*   Neutral-substrate no-flux pair n dot M_A(h) grad mu_A = 0 and n dot grad h = 0 ↔ Insulated-particle no-flux pair n dot M_B(c) grad mu_B = 0 and n dot grad c = 0
    *   *Operator Role:* Homogeneous natural boundary conditions that remove boundary flux terms from the dissipation identity and preserve total mass or total site inventory. Both are boundary constraints on the chemical-potential flux and on the gradient of the conserved scalar.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models dewetting as a conserved lubrication flow. The film free energy contains a capillary square-gradient term and an effective interface potential Phi_A(h) encoding van der Waals or polar substrate interactions. The disjoining pressure is Pi(h) = -Phi_A'(h). The variational derivative is the capillary chemical potential, and mass conservation gives a mobility-weighted divergence form:

```math
F_A[h]=\int_{\Omega}\left[\frac{\gamma_A}{2}|\nabla h|^2+\Phi_A(h)\right]d\mathbf{x},
\qquad
\Pi(h)=-\Phi_A'(h),
```

```math
\mu_A=\frac{\delta F_A}{\delta h}
=
-\gamma_A\nabla^2 h+\Phi_A'(h)
=
-\gamma_A\nabla^2 h-\Pi(h),
```

```math
\partial_t h
=
\nabla\cdot\left(M_A(h)\nabla\mu_A\right),
\qquad
M_A(h)=\frac{h^3}{3\eta}.
```

On a neutral, impermeable substrate, the natural boundary conditions used in dewetting simulations are

```math
\mathbf{n}\cdot M_A(h)\nabla\mu_A=0,
\qquad
\mathbf{n}\cdot\nabla h=0,
```

and the free energy decays according to

```math
\frac{dF_A}{dt}
=
-\int_{\Omega}M_A(h)|\nabla\mu_A|^2d\mathbf{x}
\le 0.
```

Silo B models intercalation phase separation with a Cahn-Hilliard-type conserved dynamics. The free energy contains a regular-solution local chemical free energy f_B(c) and a square-gradient penalty with coefficient kappa_B. The chemical potential is the variational derivative with respect to lithium site fraction c, and conservation of lithium in a closed particle gives the same divergence form:

```math
F_B[c]=\int_{\Omega}\left[f_B(c)+\frac{\kappa_B}{2}|\nabla c|^2\right]d\mathbf{x},
```

```math
f_B(c)=k_BT\left[c\ln c+(1-c)\ln(1-c)\right]+\Omega c(1-c),
```

```math
\mu_B=\frac{\delta F_B}{\delta c}=f_B'(c)-\kappa_B\nabla^2 c,
```

```math
\partial_t c
=
\nabla\cdot\left(M_B(c)\nabla\mu_B\right),
\qquad
M_B(c)=\frac{D_B c(1-c)}{k_BT}.
```

For an insulated particle boundary, or for a representative volume element during a potentiostatic hold after surface reaction has equilibrated, the corresponding boundary conditions are

```math
\mathbf{n}\cdot M_B(c)\nabla\mu_B=0,
\qquad
\mathbf{n}\cdot\nabla c=0,
```

and the energy dissipation law is

```math
\frac{dF_B}{dt}
=
-\int_{\Omega}M_B(c)|\nabla\mu_B|^2d\mathbf{x}
\le 0.
```

The explicit bridge is obtained by introducing dimensionless conserved scalars and chemical potentials. Let h_0 and c_0 be uniform base states, and let c_max be the maximum site fraction, often c_max = 1. Define dimensionless perturbations

```math
U_A=\frac{h-h_0}{h_0},
\qquad
U_B=\frac{c-c_0}{c_{\max}},
```

and length scales set by the ratio of square-gradient coefficient to the magnitude of the local free-energy curvature,

```math
\ell_A=\sqrt{\frac{\gamma_A}{|\Phi_A''(h_0)|}},
\qquad
\ell_B=\sqrt{\frac{\kappa_B}{|f_B''(c_0)|}}.
```

Scale time by the corresponding reference mobility and free-energy curvature,

```math
T_A=\frac{t\,M_A(h_0)|\Phi_A''(h_0)|}{\ell_A^2},
\qquad
T_B=\frac{t\,M_B(c_0)|f_B''(c_0)|}{\ell_B^2},
```

and scale the chemical potentials as

```math
\nu_A=
\frac{\mu_A-\mu_A(h_0)}{|\Phi_A''(h_0)|h_0},
\qquad
\nu_B=
\frac{\mu_B-\mu_B(c_0)}{|f_B''(c_0)|}.
```

With dimensionless spatial coordinate X_i = x / ell_i and dimensionless mobilities m_i = M_i / M_i(base), both systems take the same dimensionless conserved gradient-flow form, up to an irrelevant additive constant in the chemical potential:

```math
\partial_{T_i}U_i
=
\nabla_{X_i}\cdot\left(m_i(U_i)\nabla_{X_i}\nu_i\right),
\qquad
\nu_i=-\nabla_{X_i}^2U_i+\psi_i'(U_i),
\qquad i=A,B.
```

The dimensionless local potentials are

```math
\psi_A(U)=
\frac{
\Phi_A(h_0(1+U))-\Phi_A(h_0)-\Phi_A'(h_0)h_0U
}{
|\Phi_A''(h_0)|h_0^2
},
```

```math
\psi_B(U)=
\frac{
f_B(c_0+c_{\max}U)-f_B(c_0)-f_B'(c_0)c_{\max}U
}{
|f_B''(c_0)|
}.
```

The correspondence extends through the free-energy dissipation identities and no-flux boundary conditions. It stops where Silo B adds non-conserved Faradaic source terms, coherent elastic strain energy, or anisotropic interfacial energy, and where Silo A adds contact-line slip, evaporation, or large-slope Navier-Stokes corrections not reducible to the lubrication gradient-flow form.

Linearizing both original equations about a uniform state gives the same dispersion relation. For Silo A,

```math
\omega_A(k)
=
-M_A(h_0)k^2
\left(
\gamma_A k^2+\Phi_A''(h_0)
\right).
```

For Silo B,

```math
\omega_B(k)
=
-M_B(c_0)k^2
\left(
\kappa_B k^2+f_B''(c_0)
\right).
```

Both systems are spinodally unstable when the local free-energy curvature is negative, namely Phi_A''(h_0) < 0 in dewetting and f_B''(c_0) < 0 in intercalation. The fastest-growing wave numbers are

```math
k_{A,*}^2=-\frac{\Phi_A''(h_0)}{2\gamma_A},
\qquad
k_{B,*}^2=-\frac{f_B''(c_0)}{2\kappa_B}.
```

For the regular-solution model in Silo B,

```math
f_B''(c)=\frac{k_BT}{c(1-c)}-2\Omega.
```

At c_0 = 1/2, define theta = k_BT / Omega. Then

```math
f_B''(1/2)=2\Omega(2\theta-1).
```

If the gradient coefficient is written as kappa_B = Omega a^2, where a is an independently measured correlation length or lattice spacing, the fastest spinodal wave number becomes

```math
k_{B,*}=\frac{\sqrt{1-2\theta}}{a},
\qquad
\theta<\frac{1}{2}.
```

Thus the selected wavelength is

```math
\lambda_{B,*}
=
\frac{2\pi}{k_{B,*}}
=
\frac{2\pi a}{\sqrt{1-2\theta}}.
```

This is the direct Silo B counterpart of the thin-film spinodal wavelength selector in Silo A.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** ultrathin-polymer-film-dewetting → lithium-intercalation-phase-separation
*   **Asymmetric Maturity Rationale:** Thin-film dewetting has developed a mature computational toolkit for degenerate-mobility conserved gradient flows: positivity-preserving finite-volume and finite-element schemes for h^3 mobility, entropy-stable convex-splitting time integrators, adaptive mesh refinement near rupture or sharp fronts, and regularization strategies for singular interface potentials. Lithium-intercalation phase separation is mature in thermodynamic parameterization, regular-solution free energies, operando diagnostics, and phase-field formulation, but it lacks an equally mature, routinely deployed toolkit for long-time, site-fraction-bounded simulation of strongly spinodal particles with degenerate mobility near c = 0 and c = 1. In battery simulations, out-of-bounds concentrations, clipping, and artificial gradient-energy inflation are common operational fixes when the regular-solution free energy is strongly nonconvex.
*   **Target Bottleneck Mitigation:** Importing the thin-film positivity-preserving, mobility-harmonic finite-volume discretization and its disjoining-potential regularization strategy will allow battery phase-separation simulations to preserve 0 <= c <= 1 without artificial clipping, while retaining the physically selected spinodal wavelength. The specific hypothesis is that a thin-film-style scheme applied to the regular-solution Cahn-Hilliard equation will resolve the fastest spinodal mode given by k_{B,*} without increasing kappa_B or adding numerical diffusion, thereby removing a persistent bottleneck in predictive particle-scale phase-pattern simulation.
*   **Falsifiable Prediction:** For a closed intercalation particle or potentiostatically held platelet with c_0 = 1/2, theta = 0.40, and kappa_B = Omega a^2 with independently measured a = 1.00 nm, the imported thin-film-bounded solver must predict a small-angle scattering peak at

```math
q_* = k_{B,*} = \frac{\sqrt{1-2(0.40)}}{1.00\ \mathrm{nm}}
=0.447\ \mathrm{nm}^{-1}.
```

The corresponding wavelength is

```math
\lambda_*=\frac{2\pi}{q_*}=14.0\ \mathrm{nm}.
```

The critical spinodal threshold is theta_c = 1/2. For theta >= 1/2, the model predicts no finite-q spinodal peak because k_{B,*} becomes zero or imaginary and separation becomes macroscopic. The named baseline is a core-shell Fickian diffusion model or a clipped semi-implicit spectral Cahn-Hilliard solver that does not preserve the bounded gradient-flow structure; such baselines either predict no finite-q peak or shift the peak by requiring artificial regularization. The prediction is falsified if operando small-angle scattering from a material with independently measured theta = 0.40 and a = 1.00 nm shows no finite-q peak during early spinodal amplification, if a finite-q spinodal peak is observed for theta >= 1/2 under the same closed-particle assumptions, or if the measured peak wavevector is inconsistent with q_* = 0.447 nm^{-1} within experimental resolution.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"disjoining pressure" AND "lubrication equation" AND "spinodal dewetting"`
*   `"regular solution" AND "Cahn-Hilliard" AND "lithium intercalation" AND "spinodal decomposition"`
*   `"positivity-preserving finite volume" AND "thin film equation" AND "degenerate mobility"`
*   `"thin-film dewetting" AND "battery phase separation" AND "fastest-growing wavelength"`
*   `"Cahn-Hilliard lithium intercalation" AND "small-angle scattering peak" AND "spinodal wavelength"`