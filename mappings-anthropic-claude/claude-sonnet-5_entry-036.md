---
sid_metadata:
  entry_id: "SID-036"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Claude Sonnet 5"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "power-grid-cascading-failure-analysis"
  domain_b: "structural-progressive-collapse-analysis"
  structural_family: "cascading-failure-network-instabilities"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "instability_mechanism"
    - "numerical_solution_family"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 7.8
  vocabulary_divergence_score: 8.0
  expected_methodological_transfer_score: 6.5
  community_separation_score: 8.5
  representation_mismatch_score: 3.5
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 5.5
    uncertainty: "±1.8"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "target_bottleneck_partially_addressed_by_existing_guidelines"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 036

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Power systems engineering — cascading outage propagation in transmission networks following line trips, analyzed via linearized (DC) power flow and contingency screening.
*   **Silo B (Field 2):** Structural engineering — progressive (pancake) collapse propagation in framed structures following localized member loss, analyzed via alternate-load-path methods.
*   **Mathematical Isomorphism:** Both systems are governed by a sparse linear network operator (nodal admittance/Laplacian-type matrix vs. global stiffness matrix) mapping conserved flow-like quantities to potential-like state variables, and both exhibit threshold-triggered cascading instabilities whose post-removal redistribution can be computed via identical low-rank operator-update mathematics (Sherman–Morrison–Woodbury), differing chiefly in their constitutive laws (linear reactive power flow vs. elastoplastic force–deformation behavior).

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   N-1 contingency ↔ single-member removal scenario
    *   *Operator Role:* Both denote a single-component deletion test applied to the network operator to probe whether the redistribution of the conserved quantity (power flow vs. internal force) exceeds a stability threshold elsewhere in the network.
*   line overload / cascading trip ↔ member failure / progressive collapse
    *   *Operator Role:* Both are threshold-triggered removal events: once a component's load exceeds its rated/limit capacity, it is removed from the operator, forcing a further redistribution step that can recursively trigger additional removals.
*   line outage distribution factor (LODF) ↔ force (load) redistribution factor
    *   *Operator Role:* Both are sensitivity coefficients derived from a rank-1 update of the governing linear operator, quantifying how much of the removed component's flow/force is reassigned to each surviving component.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models steady-state transmission flow via the linearized DC power-flow equation

```math
P = B\,\theta
```

where $B$ is the network susceptance (Laplacian-type) matrix, $P$ the vector of nodal power injections, and $\theta$ the vector of voltage phase angles. When a line is removed, its effect on $B$ is a rank-1 perturbation, and the resulting flow redistribution across surviving lines is computed via LODFs derived from the Sherman–Morrison update of $B^{-1}$, avoiding a full matrix re-inversion.

Silo B models static structural equilibrium via

```math
F = K\,u
```

where $K$ is the global stiffness matrix, $F$ the applied nodal force vector, and $u$ the nodal displacement vector. When a member (e.g., a column) is removed, its contribution to $K$ is likewise a low-rank perturbation, and the redistributed internal forces on surviving members can, in the elastic regime, be obtained through an analogous Woodbury-based reanalysis rather than a full re-solve of the perturbed system. In latent operator space, both problems trace the same trajectory: a sparse linear operator undergoes a sequence of rank-1 deletions, and each deletion's downstream effect is read off a precomputed sensitivity factor rather than a fresh full-system solve — the two domains differ mainly in what happens after the linear-elastic stage, since power flow remains linear post-trip while structural members transition into plastic/dynamic collapse behavior not captured by the linear operator alone.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Power Systems Engineering → Structural Engineering
*   **Asymmetric Maturity Rationale:** Power systems operators have, over decades of NERC-driven reliability mandates, matured real-time N-k contingency screening pipelines that use LODF/Woodbury rank-1 updates to evaluate thousands of contingencies per second without re-inverting the network operator. Structural progressive-collapse assessment, by contrast, still typically relies on repeated full nonlinear dynamic finite-element re-simulation (e.g., Applied Element Method, Extreme Loading for Structures) for each candidate member-removal scenario, making exhaustive alternate-load-path scanning across many possible column losses computationally prohibitive for large or irregular buildings. Existing guidelines (e.g., GSA 2016, UFC 4-023-03) already define a simplified Linear Static procedure below the nonlinear tiers, but it is typically applied per-scenario to a small, judgment-selected set of columns rather than as an exhaustive, computationally cheap scan across all candidate removals — narrowing, but not eliminating, the transfer opportunity to the specific gain of low-rank-update-accelerated exhaustive screening.
*   **Target Bottleneck Mitigation:** Importing a Woodbury-update-based elastic redistribution-factor screen from power systems would let structural engineers rapidly rank all candidate member-removal scenarios by their linear-elastic force redistribution severity, reserving expensive full nonlinear collapse simulation only for the subset of scenarios flagged as high-severity — sharply reducing the total computational cost of exhaustive alternate-load-path assessment.
*   **Falsifiable Prediction:** For a defined class of steel moment-frame structures, a stiffness-based Woodbury redistribution-factor screen is predicted to identify the same top-quartile-severity column-removal scenarios (ranked by peak dynamic amplification factor) as full nonlinear Applied Element Method simulation with greater than 90% precision and recall, while executing orders of magnitude faster — a claim directly falsifiable by benchmarking against standard progressive-collapse test structures.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"line outage distribution factor" AND "Sherman-Morrison-Woodbury" AND "contingency analysis"`
*   `"alternate load path" AND "progressive collapse" AND "stiffness matrix reanalysis"`