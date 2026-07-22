---
sid_metadata:
  entry_id: "SID-037"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Claude Sonnet 5"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "seismic-tomography"
  domain_b: "paleoclimate-field-reconstruction"
  structural_family: "ill-posed-linear-inverse-problems"
  triple_correspondence_vectors:
    - "governing_linear_forward_operator"
    - "ill_posedness_conditioning_instability"
    - "resolution_matrix_numerical_solution_family"
discovery_rationale:
  why_not_obvious: "historically_isolated_communities / distinct_disciplinary_language"
prior_discovery_metrics:
  structural_isomorphism_score: 7.5
  vocabulary_divergence_score: 8.0
  expected_methodological_transfer_score: 8.0
  community_separation_score: 7.0
  representation_mismatch_score: 5.5
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 6.5
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "nonlinear_nonstationary_proxy_transfer_functions"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 037

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Geophysical seismic tomography — inferring the Earth's subsurface velocity structure from travel-time or waveform data recorded by an irregular, spatially clustered network of seismic stations and sources.
*   **Silo B (Field 2):** Paleoclimatology — climate field reconstruction (CFR), inferring past spatiotemporal climate fields (e.g., surface temperature over past centuries) from a sparse, irregularly distributed network of natural proxy archives (tree rings, ice cores, corals, speleothems).
*   **Mathematical Isomorphism:** Both are regularized linear (or linearized) discrete inverse problems of the form d = Gm + ε, in which an irregular, spatially clustered observation network constrains a continuous spatial field through a rank-deficient forward operator, so the recovered field m̂ = R m_true is a spatially blurred/leaked version of the truth governed by the model resolution matrix R = (GᵀG + λLᵀL)⁻¹GᵀG — an object seismic tomography routinely computes and visualizes via checkerboard resolution tests, but which paleoclimate reconstruction, despite comparably (often worse) irregular network geometry, does not typically compute explicitly.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   checkerboard resolution test ↔ pseudoproxy experiment
    *   *Operator Role:* Both forward-model a known synthetic "true" field through the real observation-network geometry, invert it with the actual reconstruction method, and compare the recovery to the known truth — functionally the same synthetic-recovery test, but seismology's version is explicitly used to extract the full resolution matrix R, while paleoclimate's version typically reports only aggregate skill scores.
*   resolution matrix R ↔ reconstruction skill score (RE / CE)
    *   *Operator Role:* R's off-diagonal entries quantify exactly how much of a recovered value at one location is smeared in from neighboring, better-sampled regions; RE/CE scores summarize overall reconstruction quality per location without decomposing it into this local-versus-leaked breakdown, so a good skill score is fully consistent with severe, undetected spatial smearing.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A formulates travel-time or waveform residuals as
```math
d = Gm + \varepsilon
```
where m is the discretized slowness/velocity perturbation field and G is the ray-path or sensitivity-kernel matrix built from actual source-receiver geometry. Because stations and events cluster unevenly, GᵀG is generally ill-conditioned, so tomographers use a damped generalized inverse m̂ = (GᵀG + λLᵀL)⁻¹Gᵀd, and explicitly compute the resolution matrix R = (GᵀG + λLᵀL)⁻¹GᵀG, since in the noise-free limit m̂ = R m_true; R = I only under dense, uniform sampling. Checkerboard tests — forward-modeling an alternating-sign synthetic pattern through the real acquisition geometry and inverting it — visualize R's smearing pattern directly, and are treated as close to mandatory for a published tomographic model.

Silo B formulates a network of P proxy series as an observation equation of the same shape,
```math
y = Hx + \eta
```
with x the unknown spatiotemporal climate field on a grid and H a sparse (or proxy-specific, sometimes linearized) operator mapping the field to each proxy's recorded response. Standard CFR methods (RegEM, CCA-based reconstruction, hierarchical Bayesian methods) invert this with an analogous regularized generalized inverse, and validate it via pseudoproxy experiments — sampling a known synthetic climate field at the real proxy locations, reconstructing it with the actual method, and comparing to the truth. In resolution-operator terms, this is the checkerboard test under a different name, but the paleoclimate literature's dominant reporting convention — scalar RE/CE/correlation skill, typically per grid cell — never extracts the explicit R that seismology treats as its primary diagnostic, so a reconstructed trend in a historically under-sampled region can be reported as "skillful" while still being substantially a leaked estimate borrowed from a distant, denser proxy cluster — a distinction only the off-diagonal structure of R is built to expose.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Geophysical Inverse Theory (Seismic Tomography) → Paleoclimatology (Climate Field Reconstruction)
*   **Asymmetric Maturity Rationale:** Resolution-matrix analysis traces to Backus-Gilbert theory in the 1960s and has been standard, near-mandatory practice in seismic tomography for decades, with mature software, reporting conventions, and closely related diagnostics (depth-of-investigation indices, full sensitivity-kernel visualization) built around it. Paleoclimate CFR is a younger quantitative inverse-problem discipline whose validation culture — pseudoproxy experiments reported as scalar skill scores — evolved largely independently and has not converged on the same operator-level resolution decomposition.
*   **Target Bottleneck Mitigation:** Computing an explicit resolution matrix (or its Monte Carlo checkerboard approximation) for existing CFR networks would let paleoclimatologists directly separate genuinely locally-resolved grid cells from ones whose reconstructed values are substantially smeared in from distant, denser proxy clusters — a distinction current scalar skill metrics cannot make, since they average over exactly the spatial structure R is designed to expose.
*   **Falsifiable Prediction:** Applying resolution-matrix (or checkerboard) analysis to a standard multiproxy network (e.g., a PAGES 2k-style compilation) is predicted to identify spatially contiguous, historically low-proxy-density regions — plausibly parts of the tropical oceans, Southern Hemisphere continents, and high-latitude interiors — where off-diagonal leakage contributes more to reconstructed signal variance than the diagonal (locally-resolved) term, even where the network's standard aggregate RE/CE skill scores read as acceptable — a skill/resolution dissociation current CFR validation practice has no mechanism to detect.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"resolution matrix" AND "checkerboard test" AND "seismic tomography"`
*   `"pseudoproxy experiment" AND "climate field reconstruction" AND "spatial resolution"`