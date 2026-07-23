---
sid_metadata:
  entry_id: "SID-045"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "qwen3.8"
  generation_timestamp: "2026-07-23"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "non-hermitian-topolectrical-lattices"
  domain_b: "directed-metapopulation-epidemiology"
  structural_family: "non-hermitian-skin-instabilities"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "boundary_condition_correspondence"
    - "instability_mechanism"
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
  vocabulary_divergence_score: 8.9
  expected_methodological_transfer_score: 8.5
  community_separation_score: 8.8
  representation_mismatch_score: 8.6
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±0.7"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "nonlinear_saturation_and_stochastic_demographic_noise"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 045

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Non-Hermitian topolectrical lattices, specifically voltage-mode skin localization and admittance spectral collapse in non-reciprocal circuit arrays built from asymmetric conductances, gyrators, or negative-impedance converters.
*   **Silo B (Field 2):** Directed metapopulation epidemiology, specifically outbreak onset and downstream patch localization in asymmetric travel-coupled susceptible-infected-susceptible patch systems with open migration boundaries.
*   **Mathematical Isomorphism:** Both systems are first-order non-normal graph dynamical systems whose open-boundary spectra are governed by the same non-reciprocal hopping operator, so that circuit admittance hopping maps to the epidemic mobility Jacobian, open-boundary skin localization maps to sink-patch outbreak concentration, and non-Bloch transfer-matrix threshold analysis maps to directed epidemic criticality.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `nodal voltage phasor` ↔ `patch infection-probability deviation`
    *   *Operator Role:* Both are scalar node amplitudes acted on by the same directed hopping generator; they occupy identical coordinate positions in a linear state vector even though one is a deterministic electrical phasor and the other is a stochastic epidemiological occupancy deviation.
*   `non-reciprocal admittance matrix` ↔ `directed next-generation/mobility Jacobian`
    *   *Operator Role:* Both are non-self-adjoint graph operators whose right eigenvectors define modal outbreak or voltage shapes, whose left eigenvectors define observability or excitation sensitivity, and whose spectral abscissa determines linear stability.
*   `open-circuit skin mode` ↔ `downstream sink-patch outbreak mode`
    *   *Operator Role:* Under open boundaries, asymmetric hopping produces a gauge transformation that pushes the dominant right eigenmode toward one boundary; the same logarithmic hopping ratio sets the electrical skin length and the epidemiological sink-localization length.
*   `admittance point-gap winding` ↔ `directed mobility circulation`
    *   *Operator Role:* Both quantify the non-Bloch topology of the periodic spectrum around a reference growth or loss value; the winding predicts boundary-induced spectral collapse and the failure of conventional Bloch or row-sum threshold criteria.
*   `non-reciprocal conductance ratio` ↔ `asymmetric travel ratio`
    *   *Operator Role:* Both are dimensionless similarity parameters controlling the same non-Hermitian gauge field, transient amplification, and boundary localization strength.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models a one-dimensional non-reciprocal topolectrical lattice by assigning a node voltage to each circuit cell and writing a Hatano-Nelson-style nodal admittance equation. The primary dynamical equation is:

```math
C\frac{dV_n}{dt}= -G_0 V_n + G_R V_{n+1}+G_L V_{n-1}+I_n^{\mathrm{ext}}
```

where `C` is node capacitance, `G_0` is shunt loss or effective gain-loss offset, and `G_R` and `G_L` are right- and left-directed hopping conductances. For a periodic array, the Bloch eigenvalue curve is:

```math
\lambda_A(k)= -\frac{G_0}{C} + \frac{G_R e^{ik}+G_L e^{-ik}}{C}
```

When `G_R` differs from `G_L`, the open-boundary problem is not solved by ordinary real Bloch waves. The mature non-Hermitian circuit toolkit replaces the Bloch factor by a complex generalized Brillouin-zone factor:

```math
z_{\mathrm{GBZ}} = \sqrt{\frac{G_L}{G_R}}\,e^{ik}
```

This produces boundary skin modes and a non-Bloch spectral threshold.

Silo B models a directed metapopulation near the disease-free state by linearizing a susceptible-infected-susceptible patch system with asymmetric travel coupling. The corresponding linear force-of-infection equation is:

```math
\frac{dp_n}{dt}= -\gamma p_n + \beta_R p_{n+1}+\beta_L p_{n-1}
```

where `p_n` is the infection-probability deviation in patch `n`, `gamma` is recovery or removal rate, and `beta_R` and `beta_L` are directed mobility-mediated infection coefficients. The operator-level mapping is:

```math
\frac{G_R}{C}\leftrightarrow \beta_R,\qquad
\frac{G_L}{C}\leftrightarrow \beta_L,\qquad
\frac{G_0}{C}\leftrightarrow \gamma
```

The shared non-reciprocity parameter and localization length are:

```math
g = \ln\left(\frac{G_R}{G_L}\right)
  = \ln\left(\frac{\beta_R}{\beta_L}\right),
\qquad
\xi = |g|^{-1}
```

In latent spectral topology, the Bloch eigenvalue loops of the circuit admittance operator and the epidemic mobility Jacobian are affine copies of one another and carry the same point-gap winding. Under open boundaries, both systems collapse onto the same generalized Brillouin-zone contour, so the voltage skin mode and the downstream outbreak mode are the same non-Hermitian right-eigenvector localization phenomenon expressed in different physical ontologies.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Non-Hermitian Topolectrical Lattices → Directed Metapopulation Epidemiology
*   **Asymmetric Maturity Rationale:** Non-Hermitian topolectrical metamaterials possess a highly mature toolkit for non-reciprocal spectral analysis: generalized Brillouin-zone construction, non-Bloch winding numbers, biorthogonal pseudospectra, transfer-matrix skin-length extraction, and direct impedance-tomography measurement of non-normal mode amplification. Directed metapopulation epidemiology commonly still relies on the spectral radius of the next-generation matrix, row-sum reproductive numbers, or periodic-boundary approximations, which can fail catastrophically when mobility is strongly asymmetric and boundaries are open.
*   **Target Bottleneck Mitigation:** Importing non-Bloch spectral solvers from topolectrical circuits will resolve the persistent bottleneck of false outbreak-threshold prediction in finite directed mobility networks. The testable hypothesis is that replacing conventional spectral-radius early-warning indicators with non-Bloch spectral abscissa, point-gap winding, and biorthogonal transient-amplification metrics will more accurately predict both the critical recovery rate and the spatial location of initial outbreak amplification in directed patch systems.
*   **Falsifiable Prediction:** For a controlled directed chain or ring with asymmetric coupling ratio `beta_R / beta_L = 4`, the finite open-boundary outbreak threshold should follow the non-Bloch skin threshold rather than the periodic or row-sum threshold:

```math
\gamma_c^{\mathrm{open}}(N)
\approx
2\sqrt{\beta_R\beta_L}
\cos\left(\frac{\pi}{N+1}\right),
\qquad
\gamma_c^{\mathrm{periodic}}
=
\beta_R+\beta_L
```

If the observed critical recovery rate instead scales with `beta_R + beta_L`, or if pre-outbreak covariance fails to localize at the downstream sink patch with localization length approximately `1 / ln(4)`, the proposed structural transfer is falsified.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Hatano-Nelson model" AND "non-Bloch band theory" AND "topolectrical circuit skin effect"`
*   `"directed metapopulation SIS" AND "next-generation matrix" AND "non-normal epidemic threshold"`
*   `"generalized Brillouin zone" AND "non-Hermitian skin effect" AND "asymmetric mobility network"`
*   `"biorthogonal pseudospectrum" AND "transient amplification" AND "outbreak early warning"`