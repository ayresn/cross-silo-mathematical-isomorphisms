---
sid_metadata:
  entry_id: "SID-0019"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "xAI"
  model_family: "Grok"
  model_version: "4.5 Fast"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "viscous-thin-film-lubrication"
  domain_b: "shallow-ice-approximation-glaciology"
  structural_family: "lubrication-reduced-stokes-free-surface-flow"
  triple_correspondence_vectors:
    - "shared_leading-order_lubrication_flux_divergence_operator"
    - "identical_free-surface_kinematic_condition"
    - "hydrostatic_vertical_momentum_balance_reduction"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / mismatched_constitutive_rheology_emphasis"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.4
  community_separation_score: 8.9
  representation_mismatch_score: 7.6
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.2
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0019

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Viscous thin-film lubrication theory for gravity- and capillary-driven free-surface flows of Newtonian or power-law liquids on substrates, focusing on the evolution of film height under the lubrication approximation.
* **Silo B (Field 2):** Shallow-ice approximation (SIA) for the large-scale flow of grounded ice sheets and glaciers under Glen-type power-law rheology, focusing on the evolution of ice thickness under the same geometric aspect-ratio reduction.
* **Mathematical Isomorphism:** Both systems are obtained from the Stokes equations by the identical small-aspect-ratio asymptotic reduction that yields a divergence-form nonlinear parabolic evolution for free-surface height driven by a flux whose leading-order operator is the product of a power of height and a gradient of hydrostatic (or capillary-modified) pressure; the correspondence holds under the explicit identification of the power-law index and the hydrostatic vertical balance, and stops when full Stokes or higher-order inertial corrections become leading.

## 2. DIAGNOSTIC VOCABULARY MATRIX
* Film height \(h(x,y,t)\) ↔ Ice thickness \(H(x,y,t)\)
    * *Operator Role:* Both are the scalar free-surface elevation that enters the kinematic condition and the flux prefactor as the same power-law weight; the nondimensionalization \(h = H/H_0\), \(x = X/L\) with aspect ratio \(\varepsilon = H_0/L \ll 1\) reconciles the geometric variables so that the operators act on identical dimensionless fields.
* Lubrication flux \(\mathbf{q} = -\frac{h^{n+2}}{n+2}\lvert\nabla p\rvert^{n-1}\nabla p\) ↔ SIA ice flux \(\mathbf{Q} = -\frac{2A}{n+2}H^{n+2}\lvert\nabla s\rvert^{n-1}\nabla s\)
    * *Operator Role:* Both are the identical divergence-form nonlinear flux operator obtained after vertical integration of the power-law constitutive relation under the lubrication ordering; the shared mathematical object is the quasilinear elliptic operator \(\nabla\cdot\bigl(H^{n+2}\lvert\nabla\cdot\rvert^{n-1}\nabla\cdot\bigr)\) acting on the free-surface potential.
* Capillary-hydrostatic pressure \(p = \rho g h - \sigma\nabla^2 h\) ↔ Ice-surface hydrostatic potential \(s = H + b\) (bed \(b\))
    * *Operator Role:* Both supply the driving gradient after the vertical momentum equation has been reduced to hydrostatic balance; the explicit transformation that equates them is the capillary number limit \(\mathrm{Ca}\to 0\) (or \(\sigma=0\)) on the thin-film side, recovering pure gravitational driving identical to the glaciological potential.

## 3. CORE MATHEMATICAL PARALLELISM
In viscous thin-film lubrication the Stokes equations together with the free-surface stress conditions are reduced under the aspect-ratio ordering \(\varepsilon\ll 1\). Vertical integration of the power-law constitutive relation \(\boldsymbol{\tau}=K\lvert\dot{\gamma}\rvert^{n-1}\dot{\gamma}\) yields the evolution equation for film height
```math
\frac{\partial h}{\partial t}+\nabla\cdot\mathbf{q}=0,\qquad
\mathbf{q}=-\frac{h^{n+2}}{n+2}\lvert\nabla p\rvert^{n-1}\nabla p,
\qquad
p=\rho g h-\sigma\nabla^2 h.
```
The same asymptotic procedure applied to the Stokes equations for ice (Glen’s law with rate factor \(A\) and exponent \(n\)) under the shallow-ice ordering produces the thickness evolution
```math
\frac{\partial H}{\partial t}+\nabla\cdot\mathbf{Q}=0,\qquad
\mathbf{Q}=-\frac{2A}{n+2}H^{n+2}\lvert\nabla s\rvert^{n-1}\nabla s,
\qquad
s=H+b(x,y).
```
The operators coincide once the identifications \(h\leftrightarrow H\), \(p\leftrightarrow\rho g s\) (capillary number \(\to 0\)), and the identical power \(n\) are made; the free-surface kinematic condition is literally the same statement of mass conservation, and the hydrostatic reduction of the vertical momentum equation is the identical leading-order balance that closes the pressure (or surface potential) in both derivations. The correspondence is exact inside the lubrication/SIA regime and ceases when either the aspect ratio is no longer small or inertial terms become order-one.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
* **Preferred Transfer Direction:** Viscous-thin-film-lubrication → Shallow-ice-approximation-glaciology
* **Asymmetric Maturity Rationale:** The thin-film community possesses a mature suite of adaptive finite-element and finite-volume schemes specifically engineered for the degenerate nonlinear parabolic operator, including rigorous singularity tracking for finite-time rupture and moving-contact-line regularizations; glaciology already has high-fidelity large-scale ice-sheet models but lacks equally refined local singularity-resolving discretizations for grounding-line migration and ice-shelf calving fronts, which are governed by the same operator class.
* **Target Bottleneck Mitigation:** Importing the thin-film singularity-adapted mesh-refinement and entropy-stable flux limiters into an SIA ice-sheet code will eliminate the artificial numerical diffusion that currently smears grounding-line dynamics, thereby restoring the correct local mass balance at the transition zone.
* **Falsifiable Prediction:** On the standard MISMIP+ grounding-line benchmark, an SIA model augmented with the thin-film adaptive scheme will reduce the steady-state grounding-line position error relative to the Stokes reference solution from the current community baseline of \(\approx 8\,\mathrm{km}\) to less than \(2\,\mathrm{km}\) at 1 km nominal resolution; failure to achieve this error reduction under otherwise identical rheology and forcing falsifies the claimed operator-level transfer benefit.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
* `"lubrication approximation" AND "power-law flux" AND "free-surface evolution" AND "thin film"`
* `"shallow ice approximation" AND "Glen's law" AND "thickness evolution" AND "grounding line"`
* `"thin-film singularity" AND "ice-sheet grounding-line" AND "adaptive mesh" OR "lubrication-to-SIA transfer"`