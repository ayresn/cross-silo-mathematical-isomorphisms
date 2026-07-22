---
sid_metadata:
  entry_id: "SID-026"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "claude-3.5-sonnet-20241022"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "elastohydrodynamics-of-active-filaments"
  domain_b: "dislocation-dynamics-in-crystalline-solids"
  structural_family: "nonlocal-curvature-flow"
  triple_correspondence_vectors:
    - "governing_differential_operator (integro-differential curve evolution with a Riesz‑type kernel and anisotropic mobility)"
    - "instability_mechanism (Euler‑type buckling transition of an elastic line under compressive load / climb force)"
    - "numerical_solution_family (spectral Ewald methods for long‑range hydrodynamic / elastic self‑interactions)"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language (cell motility vs. metal plasticity), incompatible_ontologies (continuous viscous fluid vs. discrete crystalline lattice), historically_isolated_communities (soft matter biophysics vs. physical metallurgy)"
prior_discovery_metrics:
  structural_isomorphism_score: 8.5
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 8.0
  community_separation_score: 9.5
  representation_mismatch_score: 7.0
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.0
    uncertainty: "±1.2"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch (Stokeslet kernel vs. elastic dislocation stress kernel)"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 026

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Elastohydrodynamics of slender active filaments (e.g., eukaryotic flagella, bacterial flagella) moving in a low‑Reynolds‑number fluid.
*   **Silo B (Field 2):** Dislocation dynamics in crystalline solids, where line defects move under applied and self‑stress to govern plastic flow.
*   **Mathematical Isomorphism:** Both systems evolve a 1D curve under an integro‑differential geometric flow where an anisotropic mobility operator acts on a line‑energy functional (bending plus tension) and a nonlocal self‑interaction term, giving rise to a shared Euler‑type buckling instability and a common numerical solution strategy via spectral Ewald decomposition.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `resistive‑force theory (RFT) drag anisotropy` ↔ `dislocation mobility tensor (inverse drag coefficient B)`
    *   *Operator Role:* Both are local, anisotropic mobility operators that relate the velocity of a material point on the curve to the applied force per unit length; in filaments the drag coefficients ξ_⊥, ξ_∥ encode viscous resistance, while in dislocations the mobility tensor M = B^−1 encodes lattice friction and phonon drag.
*   `sperm number (Sp)` ↔ `climb‑force threshold (σ_c b / G)`
    *   *Operator Role:* Both are dimensionless control parameters that characterize the balance between elastic bending rigidity and a destabilizing line‑wise force; crossing the critical value triggers a buckling bifurcation from a straight to a deformed (sinuous or helical) state.

## 3. CORE MATHEMATICAL PARALLELISM

Silo A models the filament centerline r(s,t) (s arc length) using a local resistive‑force theory combined with bending elasticity. The velocity is determined by the balance of elastic, tensile, and external forces per unit length f:
```math
\frac{\partial \mathbf{r}}{\partial t} = \boldsymbol{\mu} \cdot \mathbf{f}, \qquad 
\mathbf{f} = \frac{\partial}{\partial s}\!\left(T\frac{\partial \mathbf{r}}{\partial s}\right) - B\frac{\partial^4 \mathbf{r}}{\partial s^4} + \mathbf{f}_{\text{ext}},
```
where μ is the anisotropic mobility tensor (diagonal with components 1/ξ_⊥ normal and 1/ξ_∥ tangential to the filament). The full non‑local Stokes‑flow version replaces μ by an integral operator with a Stokeslet kernel, yielding a nonlocal curvature flow.

Silo B describes the glide and climb motion of a dislocation line with Burgers vector b, where the Peach–Koehler force per unit length is (σ·b)×ξ (ξ unit tangent). The overdamped equation of motion is:
```math
\frac{\partial \mathbf{r}}{\partial t} = \mathbf{M} \cdot \bigl[(\boldsymbol{\sigma}_{\text{self}}[\mathbf{r}] + \boldsymbol{\sigma}_{\text{appl}})\cdot \mathbf{b} \times \boldsymbol{\xi}\bigr],
```
with the self‑stress tensor σ_self given by an integral over the dislocation line of the nonsingular elastic Green’s function. After extracting the local line‑tension contribution, this reduces to a nonlocal curvature‑shortening flow with an anisotropic mobility M.

Both equations are instances of the operator structure ∂_t r = A·(κ n + nonlocal integral), where A is an anisotropic mobility, κ is the local curvature, and the integral encodes long‑range interactions.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Elastohydrodynamics of active filaments → Dislocation dynamics in crystalline solids
*   **Asymmetric Maturity Rationale:** The soft‑matter community has developed highly optimised, GPU‑accelerated spectral Ewald methods for large‑scale suspensions of thousands of filaments with full hydrodynamic interactions. Dislocation dynamics codes, by contrast, largely still rely on cut‑off‑based direct summation or multipole expansions that become prohibitively slow when simulating tangled, bulk dislocation networks at realistic densities.
*   **Target Bottleneck Mitigation:** Importing the spectrally accurate, O(N log N) Ewald decomposition (originally developed for Stokes flows of slender bodies) into a 3D dislocation dynamics simulation will allow the first computational study of strain‑hardening in a bulk crystal containing over 10^5 interacting dislocation segments with exact elastic self‑interactions, a scale currently unreachable.
*   **Falsifiable Prediction:** A simulation of a face‑centred cubic copper micropillar using the transferred spectral Ewald solver will reproduce the experimentally observed low‑temperature yield‑stress anomaly (increase of yield strength around 200 K) with a quantitative error of less than 5%, whereas current state‑of‑the‑art discrete dislocation dynamics systematically under‑predict this anomaly by >20% due to truncation of long‑range stresses.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"resistive-force theory" AND "elastohydrodynamics" AND "buckling instability" AND "slender body"`
*   `"dislocation climb" AND "helical instability" AND "Bardeen‑Herring source" AND "Peach‑Koehler force"`