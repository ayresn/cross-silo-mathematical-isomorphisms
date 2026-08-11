---
sid_metadata:
  entry_id: "SID-0049"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Sonnet 5"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "theoretical-ecology-community-matrix-stability"
  domain_b: "robust-control-structured-singular-value-theory"
  structural_family: "structured-perturbation-spectral-stability"
  triple_correspondence_vectors:
    - "spectral_abscissa_stability_operator_identity"
    - "elliptic_law_correlation_vs_block_structured_delta_shape_parameter"
    - "reciprocal_critical_destabilizing_perturbation_threshold"
    - "real_sparse_stability_radius_vs_asymptotic_ensemble_law_computation"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities (May-Wigner random-matrix lineage in statistical ecology vs. Doyle-Safonov-Zhou aerospace-robust-control lineage) / ensemble_statistical_vs_worst_case_adversarial_framing_mismatch"
prior_discovery_metrics:
  # All scores below are model-generated self-assessments produced at generation time,
  # deliberately calibrated down where verification searches found adjacent (but distinct)
  # prior art. They are triage signals for Stage 3, not evidence of validity.
  structural_isomorphism_score: 7.5
  vocabulary_divergence_score: 8.5
  expected_methodological_transfer_score: 7.0
  community_separation_score: 8.0
  representation_mismatch_score: 7.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.0
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "trophic_sign_pattern_may_not_decompose_into_the_repeated_scalar_or_full_block_taxonomy_for_which_D_scaling_is_provably_tight"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0049

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Theoretical community ecology — local asymptotic (Lyapunov) stability of large, randomly-assembled multi-species interaction networks, analyzed through the community (Jacobian) matrix.
* **Silo B (Field 2):** Robust control theory — robust stability of linear time-invariant feedback loops subject to block-structured, norm-bounded uncertainty, analyzed through the structured singular value μ.
* **Mathematical Isomorphism:** Both the local stability of a random ecological community matrix J = −dI + A and the robust stability of a linear control loop under block-structured uncertainty reduce to the identical spectral-abscissa functional sup{Re λ : λ ∈ spec(·)} < 0 applied to a nominal-plus-bounded-perturbation linear operator; the ecological move from May's uncorrelated circular-law bound √(SC)σ < d to Allesina–Tang's pairwise-correlated elliptic-law bound √(SC)σ(1+ρ) < d is the finite-ensemble analogue of the control-theoretic move from the unstructured bound μ_full(M) = σ̄(M) to the block-structured singular value μ_Δ(M) ≤ σ̄(M) — but this is an exact numerical correspondence only in the unstructured/uncorrelated limit (ρ = 0, Δ = full block) on both sides; away from that limit the correspondence is one of shared functional role and shared monotonicity, not of shared formula, since ρ parameterizes an ensemble average while Δ's block structure parameterizes one specific, non-averaged network.

## 2. DIAGNOSTIC VOCABULARY MATRIX
* Community matrix J = −dI + A ↔ Closed-loop generator A_cl = A₀ + BΔC (nominal-plus-perturbation state matrix)
    * *Operator Role:* Both are the finite-dimensional real linear generator of ẋ = (·)x whose spectrum determines Hurwitz stability; each decomposes as [nominal stable part] + [bounded perturbation], and the stability verdict in both fields is the identical scalar functional sup{Re λ : λ ∈ spec(·)} < 0 (Section 3, Vector 1).
* Connectance-scaled interaction magnitude √(SC)σ ↔ Unstructured uncertainty bound σ̄(M) (induced 2-norm of the nominal loop against a full, unconstrained Δ)
    * *Operator Role:* Both are the MAGNITUDE, not the shape, of the admissible perturbation: √(SC)σ is the radius of the circular-law eigenvalue support of A; σ̄(M) is the induced-norm bound defining the unstructured admissible Δ-ball. Each is a single non-negative real scalar entering its stability inequality by direct comparison to a threshold (Section 3, Vector 2).
* Pairwise interaction sign-correlation ρ = corr(A_ij, A_ji) ↔ Δ block-diagonal structure (repeated-scalar / full-block partition of the admissible uncertainty set)
    * *Operator Role:* Both restrict the SHAPE of the admissible perturbation and, in both fields, imposing that shape can only shrink the destabilizing search space relative to the unstructured baseline (μ_Δ(M) ≤ σ̄(M) mirrors (1+ρ) < 1 shrinking the elliptic semi-axis below the circular radius — Section 3, Vector 2). They are explicitly NOT the same mathematical type: ρ is a scalar correlation coefficient shaping an ensemble-AVERAGE perturbation distribution (the covariance matrix Σ in Section 3), while Δ's block partition is a discrete, combinatorial pattern shaping one SPECIFIC, non-averaged worst-case perturbation set. Reconciling that type difference — replacing an aggregate statistic with an explicit per-network block structure — is the open translation step named in Section 4, not an assumed identity.
* May–Allesina-Tang stability ratio √(SC)σ(1+ρ)/d ↔ Structured singular value μ_Δ(M), equivalently 1/r_R for the real/sparse case
    * *Operator Role:* Both are the single dimensionless functional whose comparison to unity constitutes the stability verdict, and both are, by construction, the reciprocal of the smallest admissible perturbation size that first produces a marginally unstable (imaginary-axis) eigenvalue: solving √(SC)σ(1+ρ) = d for the critical scaling factor recovers exactly the "distance to instability" that 1/μ_Δ(M) — the control-theoretic robust stability margin — measures directly (Section 3, Vector 3).

## 3. CORE MATHEMATICAL PARALLELISM
Theoretical community ecology models a multi-species equilibrium as locally stable when the community (Jacobian) matrix J, obtained by linearizing ẋ = F(x) about the equilibrium, has every eigenvalue in the open left half-plane. May (1972) modeled J as J = −dI + A, a random matrix whose off-diagonal entries are nonzero with probability C (connectance) and drawn i.i.d. with mean 0 and variance σ². By the circular law, the eigenvalues of A fill a disk of radius √(SC)σ as S → ∞, giving May's stability criterion. Allesina & Tang (2012) relaxed the independence assumption, sampling paired entries (A_ij, A_ji) from a bivariate distribution with covariance Σ = σ²[[1,ρ],[ρ,1]]; by the elliptic law this reshapes the eigenvalue support into an ellipse with real semi-axis √(SC)σ(1+ρ), giving:

```math
\sqrt{SC}\,\sigma\,(1+\rho) < d, \qquad \rho \equiv \mathrm{corr}(A_{ij}, A_{ji})
```

with ρ < 0 (antagonistic pairs, e.g. predator–prey) stabilizing and ρ > 0 (symmetric pairs, e.g. competitive or mutualistic) destabilizing.

Robust control theory represents a nominal linear loop M in feedback with a norm-bounded uncertainty block Δ restricted to a known block-diagonal structure Δ = diag(δ₁I,...,δ_KI, Δ₁,...,Δ_L) (repeated scalars and full blocks), reflecting where physical uncertainty actually enters the system. Doyle (1982) and Safonov independently introduced the structured singular value:

```math
\mu_{\boldsymbol\Delta}(M) := \Big[\min_{\Delta \in \boldsymbol\Delta}\big\{\bar\sigma(\Delta) : \det(I - M\Delta) = 0\big\}\Big]^{-1}
```

The loop is robustly stable against every admissible Δ (‖Δ‖ ≤ 1) if and only if μ_Δ(M(jω)) < 1 at every frequency ω. Since μ is NP-hard to compute exactly, the standard tool is the D-scaling upper bound μ_Δ(M) ≤ inf_{D∈𝒟} σ̄(DMD⁻¹) over scalings D commuting with the structure — a quasi-convex (LMI/SDP) problem, provably tight whenever the structure satisfies 2K+L ≤ 3 (Packard & Doyle 1993). Two special cases anchor the correspondence: μ(M) = σ̄(M) for a full, unstructured block, and μ(M) = ρ_spec(M) (spectral radius) for a repeated-scalar block.

**Bridge.** Both ẋ = Jx and ẋ = A_cl x are Hurwitz-stable iff their spectral abscissa is negative — the identical scalar functional applied to a nominal-plus-bounded-perturbation operator (**Vector 1**). May's circular-law bound is exactly the μ(M) = σ̄(M) full-block case; Allesina–Tang's ρ plays, for the pairwise-coupled ensemble, the role that Δ's block structure plays for μ — both encode which perturbation *directions* are admissible, and imposing either structure can only shrink the destabilizing search space (**Vector 2**). Both criteria are literally reciprocals of a critical destabilizing perturbation size compared to a fixed threshold, so the ecological "stability margin" and the control-theoretic 1/μ are the same normalized distance-to-instability object (**Vector 3**). Because ecological interactions are real-valued and S is finite, the relevant control-theoretic tool is not complex μ but the real structured stability radius

```math
r_{\mathbb R}(A_0;\mathcal S) := \inf\big\{\,\|\Delta\|_2 : \Delta \in \mathbb R^{S\times S},\ \Delta \text{ respects the sign/sparsity pattern } \mathcal S,\ A_0+\Delta \text{ has an eigenvalue on } i\mathbb R \,\big\}
```

which Hinrichsen & Pritchard (1986) and Qiu, Bernhardsson, Rantzer, Davison, Young & Doyle (1995) show is computable via a real-μ quantity swept over real frequency ω, with a further specialization in the literature for matrices carrying a prescribed, non-generic sparsity pattern — exactly the case of a food web, whose interaction matrix is nonzero only on the fraction C of pairs corresponding to a realized trophic link (**Vector 4**). The correspondence is exact at the level of the governing spectral-abscissa operator (Vector 1) and at the level of shared functional form and shared monotonicity of the structure-aware bounds (Vectors 2–4). It is **not** a claim that Allesina–Tang's asymptotic, ensemble-averaged ρ equals any specific numerical μ for a given empirical network — translating an aggregate correlation statistic into an explicit, per-network Δ-block structure is exactly the open methodological step Section 4 proposes, and precisely where the correspondence stops.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
* **Preferred Transfer Direction:** Robust control theory (structured singular value / real stability radius) → Theoretical ecology (community-matrix stability analysis)
* **Asymmetric Maturity Rationale:** Since Doyle's 1982 introduction of μ, control theory has built a closed, decades-refined computational pipeline for exactly the problem "does a nominal stable matrix remain stable under every member of a *known, structured, bounded* perturbation set" — D-scaling as a tractable convex/LMI upper bound, provable tightness for low-complexity structures, and a dedicated real/sparse branch (Hinrichsen & Pritchard 1986; Qiu et al. 1995; the sparse-structured real stability radius literature) built for matrices whose nonzero *pattern*, not just magnitude, is known in advance. Ecology is genuinely mature on a different, adjacent front: deriving asymptotic *ensemble* laws for broad classes of random interaction structure (circular law, elliptic law, and further extensions for modular/nested/bipartite ensembles), and it has already reached, independently, for one adjacent perturbation-robustness tool — Caravelli & Staniczenko (2016) apply Trefethen–Embree pseudospectra to bound transient amplification under community-matrix uncertainty. But the pseudospectral ε-ball is, in μ's own vocabulary, exactly the trivial full/unstructured block case: it perturbs every entry, including non-trophic pairs and the wrong sign of a real trophic link, in whatever direction is worst-case, discarding the sign/sparsity information ecologists already have. The narrow, specific capability ecology lacks is a structure-aware, finite-S, provably-bounded stability radius for a *given* empirical network — the same step control theory itself took in moving from the small-gain theorem to μ-synthesis.
* **Target Bottleneck Mitigation:** Representing each realized trophic pair (i,j) as a real, sign-constrained 2×2 uncertainty block (a predator's effect on prey and the reciprocal effect cannot vary independently or change sign) and applying D-scaled real-μ / sparse real-stability-radius computation to a *specific* empirical community matrix would give ecologists a provably-bounded, finite-S stability margin for that exact network, resolving the documented gap between asymptotic ensemble laws (accurate only as S, SC → ∞) and the small, structured, frequently modular or nested networks that make up most empirically reconstructed food webs.
* **Falsifiable Prediction:** For a benchmark set of empirically reconstructed food-web community matrices (S ∈ [15,80], drawn from compiled ecological-network databases or classic hand-digitized webs), define η*_exact(M) as the largest uniform interaction-strength scaling η at which ηM remains Hurwitz-stable, found by direct bisection on the numerically-computed spectral abscissa (no ensemble assumption required), and η*_ens(M) as the value implied by solving the Allesina–Tang criterion √(ŜĈ)σ̂(1+ρ̂)η = d̂ for η using that same matrix's own empirical statistics. For networks with modularity Q > 0.3 (Newman's modularity statistic, a proxy for departure from a "typical" well-mixed draw), the relative deviation |η*_exact − η*_ens| / η*_ens is predicted to exceed the generic finite-size heuristic 1/√S (≈18% at S=30, ≈11% at S=80) for a majority of networks in the set; a real-μ/D-scaled structured stability radius η*_struct(M) — computed by treating each trophic pair as a sign-constrained real 2×2 block — is predicted to fall closer to η*_exact than η*_ens does (|η*_struct − η*_exact| < |η*_ens − η*_exact|) for at least 60% of the S<50, Q>0.3 subset. The state-of-the-art baseline is η*_ens itself, since the Allesina–Tang criterion is the tool currently used to assess these margins. **Falsification:** if η*_struct is no closer to η*_exact than η*_ens across this subset — i.e., respecting sign/sparsity structure yields no improvement over the aggregate-correlation ensemble law once a specific network's exact topology is known — the prediction is false.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
* `"community matrix" AND "elliptic law" AND "Allesina" AND "Tang"`
* `"structured singular value" AND "D-scaling" AND "real stability radius"`
* `"structured singular value" AND ("food web" OR "community matrix" OR "ecological network")`
* `"pseudospectra" AND "community matrix" AND "structured perturbation" AND "trophic"`