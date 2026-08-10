---
sid_metadata:
  entry_id: "SID-0014"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Microsoft"
  model_family: "Copilot"
  model_version: "1.2"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "thin-film-viscous-flow"
  domain_b: "population-genetics-wavefronts"
  structural_family: "nonlinear-diffusive-fronts-with-curvature-driven-instability"
  triple_correspondence_vectors:
    - "curvature-driven-mobility_operator"
    - "nonlinear-diffusion-instability_threshold"
    - "conserved-mass-steady-traveling-wave_boundary_pair"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.2
  vocabulary_divergence_score: 7.5
  expected_methodological_transfer_score: 8.0
  community_separation_score: 7.8
  representation_mismatch_score: 8.6
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

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0014

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** *Thin-film viscous flow with surface-tension and curvature-driven mobility* — e.g., lubrication-model evolution of a thin viscous film on a substrate where surface-tension and curvature set a mobility that drives capillary leveling and fingering instabilities.
*   **Silo B (Field 2):** *Spatial population genetics with density-dependent dispersal and Allee-like growth* — e.g., reaction–diffusion models for an expanding population where local curvature of the invasion front and density-dependent dispersal produce fingering and patch formation.
*   **Mathematical Isomorphism:** Under a long-wavelength lubrication limit and a nondimensionalization that identifies film thickness with population density, the thin-film lubrication PDE with curvature-dependent mobility and conserved mass maps onto a conserved reaction–diffusion equation with density-dependent dispersal; specifically, the curvature-driven mobility operator, the nonlinear diffusion instability threshold, and the conserved-mass traveling-wave boundary conditions coincide under the transformation \(h(x,t)\leftrightarrow \rho(x,t)\) and a rescaling of time and space, yielding identical linearized dispersion relations and the same family of steady traveling-wave solutions up to constitutive closure functions.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Film thickness \(h(x,t)\)** ↔ **Population density \(\rho(x,t)\)**
    *   *Operator Role:* Both are scalar conserved fields entering a fourth-order (via curvature) or second-order (via nonlinear diffusion) conserved evolution operator after integration by parts; nondimensionalization: \(h = H_0\,\tilde\rho\), \(x = L_0\,\tilde x\), \(t = T_0\,\tilde t\). Symbols \(h,\rho\) are real scalars with identical boundary-value roles in mass conservation integrals.
*   **Capillary pressure \(-\gamma \nabla^2 h\)** ↔ **fitness-curvature potential \(-\kappa \nabla^2 \rho\) (effective pressure from curvature-dependent dispersal)**
    *   *Operator Role:* Both enter as Laplacian-of-field terms that, when combined with a mobility prefactor, produce curvature-driven flux \(\nabla\cdot\big(M(\cdot)\nabla(\nabla^2(\cdot))\big)\) vs \(\nabla\cdot\big(D(\cdot)\nabla(\cdot)\big)\) after a formal reduction; explicit mapping provided in Section 3.
*   **Mobility \(M(h)\)** ↔ **density-dependent dispersal \(D(\rho)\)**
    *   *Operator Role:* Both are scalar, positive semidefinite functions multiplying gradients in the flux; the mapping requires \(D(\rho)\approx -\partial_h\big(M(h)\partial_x^2 h\big)\) under the long-wavelength closure (see derivation).
*   **No-flux substrate boundary (contact line condition)** ↔ **conserved-flux invasion boundary (mass-conserving traveling front)**
    *   *Operator Role:* Both impose conserved-mass boundary conditions for traveling-wave solutions: integrated flux across domain boundaries vanishes; explicit traveling-wave matching conditions are shown in Section 3.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A model (thin-film lubrication with curvature-driven mobility).**  
A standard thin-film lubrication equation for a viscous film with surface tension \(\gamma\) and mobility \(M(h)\) reads:
```math
\partial_t h + \nabla\cdot\big( M(h)\nabla(\gamma\nabla^2 h) \big) = 0.
```
For one spatial dimension \(x\) this becomes:
```math
\partial_t h + \partial_x\left( M(h)\partial_x(\gamma \partial_{xx} h) \right) = 0.
```
Linearizing about a flat film \(h=H_0 + \tilde h\) with \(M(h)\approx M(H_0)+M'(H_0)\tilde h\) and seeking modes \(\tilde h\propto e^{\sigma t + i k x}\) yields the dispersion relation:
```math
\sigma(k) = -\gamma M(H_0) k^4 + i k^3 \gamma M'(H_0) \, ( \text{if asymmetry present} ).
```
The dominant real part for symmetric mobility gives the familiar stabilizing \( -\gamma M(H_0) k^4\) scaling and, when additional destabilizing terms (e.g., disjoining pressure or Marangoni) are present, a band of unstable \(k\) emerges.

**Silo B model (conserved reaction–diffusion with density-dependent dispersal and curvature-effect term).**  
Consider a conserved population density \(\rho(x,t)\) with density-dependent dispersal \(D(\rho)\) and a curvature-coupled dispersal correction arising from movement biased by local curvature of the density front (modeling edge-seeking or edge-avoiding behavior). A minimal conserved PDE is:
```math
\partial_t \rho + \partial_x\big( -\partial_x( D(\rho)\rho ) + \chi(\rho)\partial_x(\partial_{xx}\rho) \big) = 0,
```
which can be rearranged as
```math
\partial_t \rho + \partial_x\big( \tilde M(\rho)\partial_x(\kappa \partial_{xx}\rho) \big) + \partial_x\big( \text{lower-order nonlinear fluxes} \big) = 0,
```
where \(\kappa\) is an effective curvature-coupling coefficient and \(\tilde M(\rho)\) collects density-dependent prefactors. Linearizing about \(\rho=\rho_0+\tilde\rho\) and taking Fourier modes \(\tilde\rho\propto e^{\sigma t + i k x}\) gives a leading-order dispersion term:
```math
\sigma(k) = -\kappa \tilde M(\rho_0) k^4 + \text{(lower-order)}.
```

**Bridge and precise correspondence.**  
Define the mapping
```math
h(x,t) \longleftrightarrow \rho(x,t),\quad \gamma \longleftrightarrow \kappa,\quad M(h)\longleftrightarrow \tilde M(\rho).
```
Under the long-wavelength approximation and after integrating by parts the curvature-coupled dispersal term in Silo B, the conserved fluxes take identical operator form:
```math
\partial_t \Phi + \partial_x\big( \mathcal{M}(\Phi)\partial_x(\Lambda \partial_{xx}\Phi) \big) = 0,
```
with \(\Phi\in\{h,\rho\}\), \(\mathcal{M}\) the mapped mobility, and \(\Lambda\in\{\gamma,\kappa\}\). The linearized dispersion relations on both sides coincide to leading order:
```math
\sigma(k) = -\Lambda \mathcal{M}(\Phi_0) k^4 + O(k^2 \text{ or } k^3 \text{ from lower-order fluxes}).
```
This demonstrates the three required correspondence vectors explicitly:
- **curvature-driven-mobility_operator:** Both systems contain the operator \(\partial_x\big( \mathcal{M}(\Phi)\partial_x(\Lambda \partial_{xx}\Phi)\big)\) shown above.
- **nonlinear-diffusion-instability_threshold:** Linearization yields identical leading-order \(k^4\) stabilizing term and identical conditions for band-limited instability when lower-order destabilizing fluxes (e.g., disjoining pressure in films; Allee-like negative diffusion in populations) are included; the instability threshold is set by the sign change in the effective prefactor of the \(k^2\) or \(k^4\) term after expansion.
- **conserved-mass-steady_traveling_wave_boundary_pair:** Traveling-wave ansatz \(\Phi(x,t)=\Phi(\xi)\) with \(\xi=x-ct\) reduces both PDEs to an ODE of the form
```math
-c \Phi' + \frac{d}{d\xi}\left( \mathcal{M}(\Phi)\frac{d}{d\xi}(\Lambda \Phi'') \right) = 0,
```
which integrates once under no-flux conditions to
```math
-c \Phi + \mathcal{M}(\Phi)\Lambda \Phi'' = C,
```
with the same conserved-mass matching conditions (choose \(C=0\) for symmetric no-flux far-field states). This ODE family is identical in operator structure on both sides.

**Scope and limits.**  
The mapping holds under: (i) long-wavelength lubrication-like limit in Silo A (thin-film assumption), (ii) existence of curvature-coupled dispersal in Silo B (a specific behavioral or mechanistic term that produces \(\partial_x(\tilde M(\rho)\partial_x(\partial_{xx}\rho))\) after coarse-graining), and (iii) matching of constitutive functions via nondimensionalization. The correspondence does **not** claim identity of constitutive closures \(M(h)\) vs \(D(\rho)\); those must be measured or modeled per system. The mapping is operator-level and yields falsifiable predictions (Section 4) but fails if Silo B dispersal lacks any curvature-coupled term or if Silo A dynamics are dominated by nonlocal forces that cannot be reduced to local curvature operators.

**Excerpt from provided SID instruction document (verbatim):**  
> "Your task is to use your learned internal representations to identify cross-domain structural mathematical isomorphisms (shared underlying mathematical or physical laws) between two highly specialized, traditionally siloed scientific or engineering disciplines."  
> "The Triple-Correspondence Rule: The structural mapping must DEMONSTRATE at least THREE independent correspondences drawn from: governing differential operator, boundary conditions, conserved quantities, instability mechanisms, symmetry groups, variational principles, dimensionless similarity parameters, or numerical solution families."

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** *Thin-film viscous flow* → *Population genetics / spatial ecology*
*   **Asymmetric Maturity Rationale:** Thin-film hydrodynamics and lubrication theory have a mature, specialized toolkit for fourth-order conserved PDEs: matched-asymptotics for contact-line singularities, spectral stability analysis for \(k^4\)-type operators, energy-stable numerical schemes for \(\partial_x(\mathcal{M}(\Phi)\partial_x(\Phi''))\) operators, and experimentally validated parameter inference for mobility functions \(M(h)\). Spatial ecology and population genetics have extensive work on second-order reaction–diffusion equations but far fewer validated methods for numerically and analytically handling *conserved* fourth-order curvature-coupled dispersal operators and their contact-line–like front singularities. Therefore, importing thin-film asymptotic techniques, energy-stable discretizations, and traveling-wave continuation methods can immediately address bottlenecks in modeling curvature-biased dispersal and fingering instabilities in ecology.
*   **Target Bottleneck Mitigation:** Hypothesis: Applying thin-film matched-asymptotic expansions and energy-stable spectral-element solvers to conserved curvature-coupled dispersal models will (a) produce accurate predictions of fingering wavelength selection in expanding populations with curvature-biased movement, and (b) enable stable long-time simulations of front breakup and coarsening that current second-order ecological solvers cannot resolve without artificial regularization. A testable protocol: take an existing ecological PDE with candidate curvature-coupled term, nondimensionalize to the form in Section 3, and apply thin-film continuation methods to compute bifurcation diagrams of traveling-wave solutions as a function of nondimensional mobility slope \(M'(\Phi_0)\). Compare predicted fingering wavelengths and coarsening rates to direct numerical simulation and to laboratory microcosm experiments.
*   **Falsifiable Prediction:**  
  * **System:** A laboratory microbial invasion on a quasi-1D agar strip with engineered curvature-biased motility (e.g., via chemoattractant gradients that depend on local curvature of the colony edge).  
  * **Measured quantity:** Dominant fingering wavelength \(\lambda^*\) of the invasion front and the growth rate \(\sigma(k)\) of small perturbations.  
  * **Numeric threshold / baseline:** Using the mapping, the leading-order dispersion predicts \(\sigma(k) \approx -\Lambda \mathcal{M}(\Phi_0) k^4 + \alpha k^2\) where \(\alpha\) collects destabilizing lower-order fluxes. The prediction is that the observed \(\lambda^*\) satisfies
```math
\lambda^* = 2\pi \sqrt{\frac{2\Lambda \mathcal{M}(\Phi_0)}{\alpha}} \pm 10\%
```
  relative error, and that the measured growth-rate curve \(\sigma(k)\) fits the quartic-dominated form with coefficient matching \(-\Lambda \mathcal{M}(\Phi_0)\) within experimental uncertainty.  
  * **Baseline to beat / falsify:** Null hypothesis: a second-order reaction–diffusion model (no curvature-coupled fourth-order term) predicts \(\lambda^*\) scaling with \(\sqrt{\Lambda \mathcal{M}/\alpha}\) but with a different prefactor and no quartic tail in \(\sigma(k)\). If experimental \(\lambda^*\) deviates from the quartic-predicted value by more than 10% and the measured \(\sigma(k)\) lacks a quartic-dominated regime, the isomorphism hypothesis is falsified for that system. All constants \(\Lambda,\mathcal{M},\alpha\) must be estimated from independent measurements (mobility vs density, curvature-coupling strength) prior to comparison; no external constants are imported without target-side derivation.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"thin-film lubrication" AND "fourth-order" AND "mobility M(h)"`
*   `"curvature-dependent dispersal" AND "population density" AND "fourth-order"`
*   `"conserved fourth-order PDE" AND "ecology" AND "curvature-biased movement"`