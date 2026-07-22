---
providence:
  company: "OpenAI"
  model_family: "GPT-5"
  model_version: "GPT-5.5"
  generation_timestamp: "2026-07-20"
  prompt_type: "unsupervised-cross-silo-latent-extraction"
isomorphism_metadata:
  domain_a: "electrochemical-phase-field-dendrite-growth"
  domain_b: "directional-solidification-mullins-sekerka-instability"
prior_discovery_metrics:
  structural_isomorphism_score: 9.8
  vocabulary_divergence_score: 4.2
  expected_methodological_transfer_score: 8.5
  community_separation_score: 5.1
  novelty_prior_estimate: 3.2
validation_status:
  mathematical_confidence: "very_high"
  bibliometric_validation: "historical_framework_borrowing_detected"
---


# INTERDISCIPLINARY LATENT VECTOR MAPPING: ENTRY 001

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Electrochemical phase-field modeling of lithium metal dendrite growth during electrodeposition under transport-limited conditions.
* **Silo B (Field 2):** Directional solidification theory describing Mullins–Sekerka morphological instability at advancing solid-liquid interfaces.
* **Mathematical Isomorphism:** Both systems are governed by moving-boundary instability in which interfacial curvature, diffusion-limited transport, and Gibbs–Thomson regularization produce mathematically homologous free-boundary evolution equations whose linear stability spectra possess equivalent wavelength-selection mechanisms.

## 2. VOCABULARY TRANSLATION MATRIX
* Interface overpotential = Interface undercooling
* Exchange-current-controlled deposition = Attachment kinetics
* Concentration polarization layer = Solutal diffusion boundary layer
* Electrochemical phase-field order parameter = Solidification phase-field order parameter

## 3. CORE MATHEMATICAL PARALLELISM

Electrochemical dendrite growth is commonly modeled using coupled Cahn–Hilliard/Allen–Cahn phase-field dynamics together with ionic transport and electrochemical kinetics. The interface velocity emerges from diffusion-limited ionic flux combined with curvature-dependent chemical potential, naturally regularizing unstable protrusions while preserving thermodynamic consistency.

```math
\tau \frac{\partial \phi}{\partial t}
=
W^2\nabla^2\phi
-
\frac{\partial f(\phi)}{\partial \phi}
-
\lambda(c,\eta)
\frac{\partial g(\phi)}{\partial \phi},
\qquad
\frac{\partial c}{\partial t}
=
\nabla\cdot(D\nabla c)
-
\frac{1}{F}\nabla\cdot\mathbf{J},
\qquad
V_n
\propto
\mathbf{J}\cdot\mathbf{n}
```

Directional solidification theory describes an advancing solid-liquid interface whose morphology is destabilized when diffusion cannot smooth concentration or temperature gradients sufficiently rapidly. The Mullins–Sekerka instability analysis derives a dispersion relation relating perturbation wavelength to exponential growth rate while Gibbs–Thomson curvature suppresses high-frequency modes.

```math
\frac{\partial C}{\partial t}
=
D\nabla^2C,
\qquad
V_n
=
-D\frac{\partial C}{\partial n},
\qquad
T_i
=
T_m
-
\Gamma\kappa
-
mC_i
```

In latent mathematical space, ionic concentration corresponds to solute concentration, electrochemical overpotential corresponds to thermodynamic driving force, Butler–Volmer interface kinetics correspond to attachment kinetics, and curvature-dependent stabilization enters through the same capillarity operator. Linearization around a planar interface yields dispersion relations with homologous stability structure, allowing numerical continuation, wavelength-selection analysis, and adaptive interface tracking techniques developed for one field to be translated with only constitutive substitutions.

## 4. SCIENTIFIC HYPOTHESIS & UNREALIZED BENEFIT

* **Hypothesis:** Applying the complete nonlinear stability framework developed for Mullins–Sekerka interface selection—including anisotropic capillary regularization and solvability-based tip-selection theory—to lithium electrodeposition will improve quantitative prediction of dendrite tip radius, branching frequency, and critical current density beyond existing electrochemical phase-field parameterizations.

* **Methodological Transfer:** Replace thermal undercooling with electrochemical overpotential in established directional-solidification phase-field solvers, substitute ionic transport for solute diffusion while preserving the moving-boundary numerical framework, and calibrate only electrochemical constitutive parameters. Existing adaptive mesh refinement, dispersion-relation analysis, and interface-tracking algorithms can then be benchmarked directly against galvanostatic dendrite-growth experiments.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"electrochemical phase-field dendrite growth" AND "Allen-Cahn" AND "Butler-Volmer kinetics"`
* `"Mullins-Sekerka instability" AND "Gibbs-Thomson equation" AND "directional solidification"`