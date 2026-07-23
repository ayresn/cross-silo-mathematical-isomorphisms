---
sid_metadata:
  entry_id: "SID-044"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Alibaba Group"
  model_family: "Qwen"
  model_version: "qwen3-8"
  generation_timestamp: "2026-07-23"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "nuclear-criticality-transport"
  domain_b: "spatial-invasion-ecology"
  structural_family: "linear-multiplicative-transport-eigenproblems"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "boundary_conditions"
    - "numerical_solution_family"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.9
  community_separation_score: 9.0
  representation_mismatch_score: 8.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.8
    uncertainty: "±0.7"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 044

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Nuclear criticality transport, specifically steady one-speed neutron multiplication in heterogeneous fissile assemblies, where the core observable is the angular neutron flux and the threshold eigenvalue is the effective multiplication factor.
*   **Silo B (Field 2):** Spatial invasion ecology, specifically stage-structured population persistence and spread with directional dispersal across heterogeneous habitat, where the core observable is the directional density of moving individuals and the threshold eigenvalue is the asymptotic population growth factor.
*   **Mathematical Isomorphism:** Both systems are positive linear transport eigenproblems in which a first-order streaming/removal operator is balanced by an angular redistribution integral and a local multiplicative birth/fission integral, so the dominant eigenvalue, inflow boundary trace, and discrete-ordinates/adjoint solution family obey an equivalent Perron-Frobenius threshold structure.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Effective multiplication factor ↔ Asymptotic population growth factor
    *   *Operator Role:* Both are the dominant positive eigenvalue of a linear phase-space transport operator; crossing unity separates subcritical decay or extinction from supercritical growth or invasion.
*   Macroscopic fission source ↔ Local fecundity or reproduction kernel
    *   *Operator Role:* Both supply positive multiplication into the phase-space density, converting an attenuating streaming problem into a spectral growth problem.
*   Total removal cross section ↔ Mortality plus directional emigration loss rate
    *   *Operator Role:* Both appear as diagonal attenuation terms in the transport operator, setting the residence time of particles or organisms in a phase-space cell.
*   Angular neutron flux ↔ Directional dispersal density
    *   *Operator Role:* Both are nonnegative densities over position and direction, advected by the same first-order streaming operator before scattering, removal, or reproduction.
*   Vacuum inflow boundary ↔ Absorbing or no-immigration habitat boundary
    *   *Operator Role:* Both impose a zero incoming trace on the inflow portion of the phase-space boundary, making the spectral problem self-contained within the spatial domain.
*   Adjoint neutron importance ↔ Conservation or intervention sensitivity
    *   *Operator Role:* Both are left eigenvectors of the same transport operator and give the first-order change in the dominant eigenvalue under localized removal, sterilization, or control.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models steady neutron criticality with the one-speed Boltzmann transport eigenvalue equation, in which streaming and total loss are balanced by scattering redistribution and fission multiplication. The incoming angular flux is set to zero on a vacuum boundary, making the problem a positive spectral problem for the dominant eigenvalue.

```math
\Omega \cdot \nabla \psi(x,\Omega) + \Sigma_t(x)\psi(x,\Omega)
=
\int_{S^2} \Sigma_s(x,\Omega' \to \Omega)\psi(x,\Omega')\,d\Omega'
+
\frac{1}{k_{\mathrm{eff}}}
\int_{S^2} \nu\Sigma_f(x,\Omega' \to \Omega)\psi(x,\Omega')\,d\Omega'
```

Silo B models directional population spread with a linearized stage-structured transport-growth equation, in which organisms move along directed trajectories, suffer mortality or emigration, change direction through a movement-turning kernel, and produce new individuals through a local fecundity kernel. With zero immigration at the habitat boundary, the dominant eigenvalue determines whether the metapopulation persists, grows, or goes extinct.

```math
\Omega \cdot \nabla n(x,\Omega) + \mu(x,\Omega)n(x,\Omega)
=
\int_{S^2} K(x,\Omega' \to \Omega)n(x,\Omega')\,d\Omega'
+
\frac{1}{\lambda}
\int_{S^2} F(x,\Omega' \to \Omega)n(x,\Omega')\,d\Omega'
```

Under the mapping from neutron angular flux to directional organism density, total removal cross section to mortality/emigration, scattering kernel to turning kernel, and fission kernel to fecundity kernel, the two equations occupy the same latent operator topology: a positive cone of phase-space densities, a dominant positive eigenfunction ray, a source-iteration trajectory converging to that ray, and a threshold bifurcation at eigenvalue unity.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Nuclear Criticality Transport → Spatial Invasion Ecology
*   **Asymmetric Maturity Rationale:** Nuclear transport possesses a far more mature toolkit for high-dimensional linear transport eigenproblems: discrete ordinates and method-of-characteristics solvers, source iteration and Krylov acceleration, adjoint perturbation theory, variance-reduced Monte Carlo, and routine criticality safety workflows. Spatial invasion ecology more often relies on individual-based simulations, coarse reaction-diffusion approximations, or network eigenvector centrality, which can lose directional streaming effects and rarely provide calibrated adjoint intervention maps at landscape scale.
*   **Target Bottleneck Mitigation:** Importing deterministic discrete-ordinates transport solvers and adjoint eigenvalue sensitivity from nuclear criticality will let invasion ecologists compute the landscape growth factor and rank habitat cells or corridors by true first-order impact on persistence, thereby resolving the bottleneck of expensive, non-adjoint, diffusion-limited management prioritization for strongly directional dispersal.
*   **Falsifiable Prediction:** For a calibrated wind-borne or current-borne invasion scenario on a heterogeneous landscape, removing or sterilizing the top five percent of habitat cells ranked by transport adjoint importance will reduce the dominant population growth eigenvalue by at least fifteen percent more than removing the same number of cells ranked by current state-of-the-art next-generation-matrix eigenvector centrality or reaction-diffusion sensitivity; the transport model also predicts at least one low-fecundity upstream shadow corridor whose localized suppression reduces the eigenvalue by more than five percent despite low occupancy, and failure to observe either effect in replicated field or high-fidelity simulation removals would falsify the operational transfer.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"effective multiplication factor" AND "Boltzmann transport equation" AND "adjoint importance"`
*   `"stage-structured dispersal" AND "velocity-jump movement" AND "asymptotic growth rate"`
*   `"discrete ordinates" AND "k-eigenvalue" AND "heterogeneous multiplying media"`
*   `"landscape persistence" AND "directional dispersal kernel" AND "population growth eigenvalue"`