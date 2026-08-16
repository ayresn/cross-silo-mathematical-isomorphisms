---
sid_metadata:
  entry_id: "SID-0049"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-rejected"
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
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The vocabulary matrix maps a scalar ensemble correlation coefficient to a discrete block-structured uncertainty set and asserts a universal shrinkage inequality contradicted by the entry's own statement that positive ρ is destabilizing."
    failed_checks: ["Check 2: vocabulary mapping pairs scalar correlation ρ with Δ block-diagonal structure and asserts universal (1+ρ)<1 shrinkage contradicted by ρ>0 destabilizing"]
    flagged_checks: ["Check 3: vector 2 is only partially supported and is described as an open translation step; vectors 1, 3, and 4 are otherwise supported"]
    quoted_evidence: [
      "Pairwise interaction sign-correlation ρ = corr(A_ij, A_ji) ↔ Δ block-diagonal structure (repeated-scalar / full-block partition of the admissible uncertainty set)",
      "They are explicitly NOT the same mathematical type: ρ is a scalar correlation coefficient shaping an ensemble-AVERAGE perturbation distribution (the covariance matrix Σ in Section 3), while Δ's block partition is a discrete, combinatorial pattern shaping one SPECIFIC, non-averaged worst-case perturbation set.",
      "imposing that shape can only shrink the destabilizing search space relative to the unstructured baseline (μ_Δ(M) ≤ σ̄(M) mirrors (1+ρ) < 1 shrinking the elliptic semi-axis below the circular radius — Section 3, Vector 2).",
      "ρ > 0 (symmetric pairs, e.g. competitive or mutualistic) destabilizing."
    ]
    stage_3_watch_items: [
      "Verify whether structured singular value or real structured stability radius methods have already been applied to ecological community matrices or food webs.",
      "Verify the precise Allesina–Tang elliptic-law axis formula and whether the entry's (1+ρ) shrinkage claim is intended only for negative ρ.",
      "Verify whether the Section 4 η-scaling is intended to scale only off-diagonal interaction strengths while holding diagonal self-regulation fixed; literal scaling of the full community matrix would not produce a finite Hurwitz threshold.",
      "Verify the stated D-scaling tightness condition and the repeated-scalar special case μ = spectral radius for the exact block structures invoked."
    ]
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The entry contains multiple non-fatal but concrete mathematical failures, including a false exact-equivalence claim between May's circular-law bound and μ_full, an explicitly type-incompatible vocabulary mapping, a false monotonicity claim contradicted by the entry's own ρ>0 case, and an ill-defined falsification quantity."
    failed_checks:
      - "Check 1: Section 3 Bridge incorrectly claims May's circular-law bound is exactly the μ_full = σ̄(M) full-block case"
      - "Check 2: Vocabulary pair ρ ↔ Δ block-diagonal structure is explicitly acknowledged as type-incompatible, and its monotonicity claim is false for ρ>0"
      - "Check 4: Falsifiable prediction defines η*_exact by scaling the full community matrix ηM, which does not model interaction-strength scaling and is ill-defined"
    flagged_checks:
      - "Check 3: Vector 4 is asserted from cited literature rather than derived in the body; Vector 2's supporting monotonicity claim is false"
    quoted_evidence:
      - "May's circular-law bound is exactly the μ(M) = σ̄(M) full-block case"
      - "Pairwise interaction sign-correlation ρ = corr(A_ij, A_ji) ↔ Δ block-diagonal structure ... They are explicitly NOT the same mathematical type: ρ is a scalar correlation coefficient shaping an ensemble-AVERAGE perturbation distribution ... while Δ's block partition is a discrete, combinatorial pattern shaping one SPECIFIC, non-averaged worst-case perturbation set."
      - "in both fields, imposing that shape can only shrink the destabilizing search space relative to the unstructured baseline (μ_Δ(M) ≤ σ̄(M) mirrors (1+ρ) < 1 shrinking the elliptic semi-axis below the circular radius"
      - "define η*_exact(M) as the largest uniform interaction-strength scaling η at which ηM remains Hurwitz-stable"
    stage_3_watch_items:
      - "Probe whether the μ / real stability radius formalism has already been applied to ecological community matrices or food webs"
      - "Check Caravelli & Staniczenko (2016) and related pseudospectral ecology literature for prior structured-perturbation use"
      - "Verify Allesina–Tang elliptic-law sign convention and whether √(SC)σ(1+ρ) is the correct largest-real-part semi-axis for finite C and sparse matrices"
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The vocabulary matrix contains an explicitly acknowledged category error, mapping a scalar correlation coefficient to a discrete matrix block partition."
    failed_checks: ["Check 2: Incompatible mathematical types in vocabulary mapping"]
    flagged_checks: ["Check 3: Vector 2 lacks equation or derivation support"]
    quoted_evidence: [
      "Pairwise interaction sign-correlation ρ = corr(A_ij, A_ji) ↔ Δ block-diagonal structure (repeated-scalar / full-block partition of the admissible uncertainty set)",
      "They are explicitly NOT the same mathematical type: ρ is a scalar correlation coefficient shaping an ensemble-AVERAGE perturbation distribution (the covariance matrix Σ in Section 3), while Δ's block partition is a discrete, combinatorial pattern shaping one SPECIFIC, non-averaged worst-case perturbation set."
    ]
    stage_3_watch_items: ["Verify whether equating an ensemble statistical correlation parameter (ρ) with a deterministic, worst-case combinatorial block structure (Δ) renders the proposed methodological transfer mathematically intractable despite the bounds sharing generic monotonicity."]
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are correctly attributed and class-consistent, vocabulary mappings pair compatible mathematical types (with transparent acknowledgment where types diverge), all four correspondence vectors are demonstrated with equations and operator identities, and the transfer direction is genuinely asymmetric with a specific falsifiable prediction naming measurable quantities and thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The structural pairing of community-matrix stability (random matrix / ensemble asymptotic regime) with structured singular value (deterministic / worst-case finite-dimensional regime) is well-motivated but lives at the intersection of two very mature literatures. Stage 3 should verify whether the specific connection of real-sparse stability radius to empirical food-web community matrices has been proposed in the ecological-stability or control-applied-to-biology literature (e.g., Caravelli & Staniczenko 2016 is acknowledged for pseudospectra; probe whether any subsequent work extends to structured perturbation)."
      - "The entry's honest framing that ρ (an ensemble correlation statistic) and Δ-block structure (a per-network combinatorial pattern) are 'explicitly NOT the same mathematical type' and that reconciling them is 'the open translation step' is mathematically sound, but Stage 3 should confirm that the elliptic-law formulation cited (Allesina & Tang 2012) indeed gives the specific semi-axis formula √(SC)σ(1+ρ) as stated, and not a related but distinct expression."
      - "The falsifiable prediction defines η*_exact by 'direct bisection on the numerically-computed spectral abscissa' for S up to 80. Stage 3 should verify computational feasibility: spectral abscissa bisection for S=80 with structured perturbation is nontrivial, and the entry should in principle specify whether the structured stability radius computation also scales to S=80 within practical limits."
      - "The tightness condition '2K+L ≤ 3 (Packard & Doyle 1993)' for D-scaling: Stage 3 should verify this specific combinatorial condition is correctly stated, as the literature uses several slightly different notation conventions for counting repeated scalars vs. full blocks."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The entry claims 'shared monotonicity' between ecological correlation ρ and control-theoretic block structure Δ, but the ecological side is not monotone in the same direction — ρ > 0 expands the eigenvalue support, which the entry's own equations show, directly contradicting the claim that structuring 'can only shrink the destabilizing search space.'"
    failed_checks: ["CHECK 2: False monotonicity claim in vocabulary matrix — ecological correlation ρ can expand (ρ > 0) or shrink (ρ < 0) the destabilizing search space, contradicting the claimed 'shared monotonicity' with control-theoretic structuring (μ_Δ ≤ σ̄ always).", "CHECK 3: Vector 2 (elliptic_law_correlation_vs_block_structured_delta_shape_parameter) rests on the false monotonicity claim; Vectors 1, 3, and 4 are adequately demonstrated."]
    flagged_checks: []
    quoted_evidence: ["imposing that shape can only shrink the destabilizing search space relative to the unstructured baseline (μ_Δ(M) ≤ σ̄(M) mirrors (1+ρ) < 1 shrinking the elliptic semi-axis below the circular radius", "imposing either structure can only shrink the destabilizing search space", "the correspondence is one of shared functional role and shared monotonicity, not of shared formula"]
    stage_3_watch_items: ["The spectral-abscissa identity (Vector 1) and reciprocal-distance-to-instability correspondence (Vector 3) are mathematically sound; a corrected entry dropping the monotonicity claim and framing Vector 2 as a functional analogy with opposite-direction effects would likely pass.", "Stage 3 should verify whether the Caravelli & Staniczenko (2016) pseudospectra application and any subsequent work has already bridged μ-synthesis to ecological community matrices.", "Stage 3 should check whether the real structured stability radius (Hinrichsen-Pritchard / Qiu et al.) has been applied to food-web or ecological-network matrices in the computational ecology literature."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The entry contains fatal correspondence-support failures: Vector 3 equates an ensemble stability-bound scaling factor with an exact structured stability radius without establishing that equivalence, and Vector 4 is only proposed rather than demonstrated by an operator identity, equation, or derivation."
    failed_checks: ["Check 3: Vector 3 is not demonstrated as an exact reciprocal stability-radius correspondence; Vector 4 is not demonstrated by the body"]
    flagged_checks: ["Check 2: The claimed shared role of ecological correlation ρ and control-theoretic Δ structure is semantically overstated because ρ shapes an ensemble covariance law rather than an admissible perturbation set"]
    quoted_evidence: [""Both criteria are literally reciprocals of a critical destabilizing perturbation size compared to a fixed threshold, so the ecological \"stability margin\" and the control-theoretic 1/μ are the same normalized distance-to-instability object (**Vector 3**)."", ""Because ecological interactions are real-valued and S is finite, the relevant control-theoretic tool is not complex μ but the real structured stability radius ... with a further specialization in the literature for matrices carrying a prescribed, non-generic sparsity pattern — exactly the case of a food web, whose interaction matrix is nonzero only on the fraction C of pairs corresponding to a realized trophic link (**Vector 4**).""]
    stage_3_watch_items: ["Check whether the proposed sign-constrained real 2×2 trophic-pair uncertainty structure is mathematically compatible with the actual food-web interaction topology and whether it yields a valid structured-μ/stability-radius formulation rather than merely an analogy.", "Check whether the claimed ecological stability-margin reciprocal can legitimately be identified with 1/μ or a structured stability radius for a specific finite community matrix; the body itself distinguishes the ensemble-averaged ρ from a per-network perturbation structure.", "The claimed analogy between Allesina–Tang correlation structure and structured singular-value block structure should be examined carefully because the entry itself says they are different mathematical types and provides no operator identity equating their perturbation sets."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "PASS"
    verdict_rationale: "The entry consistently demonstrates a spectral-abscissa based correspondence, provides supporting equations/definitions for each claimed vector, and proposes a concrete, falsifiable transfer experiment; no category errors or equation-class mismatches were found in the text."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify the precise factorization and sign convention in the Allesina–Tang elliptic-law expression used here (the entry states `\\sqrt{SC}\\,\\sigma\\,(1+\\rho) < d`) against the original derivation to ensure the scalar multiplier (1+\\rho) is the correct semi-axis expression for the ensemble and the stated interpretation of ρ."
      - "Check the literature and numerical examples for the claimed D-scaling tightness thresholds when applied to sign-constrained, real 2×2 trophic blocks and to empirically modular/sparse networks (practical tightness and computational tractability for the proposed sign-constrained 2×2 block model)."
      - "Confirm that the real structured stability radius formulation and the proposed numerical sweep over real frequency (real-μ) as described maps cleanly to the finite-S ecological matrices with sign/sparsity constraints used in the falsifiable prediction."
      - "Examine prior-art overlap with May (1972), Allesina & Tang (2012), Doyle (1982) and the real/sparse stability-radius literature (Hinrichsen & Pritchard; Qiu et al.) to ensure the claimed methodological transfer novelty is correctly framed (advisory only)."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are correctly attributed and class-consistent, vocabulary mappings specify shared operator roles without category errors, every listed correspondence vector is demonstrated by explicit spectral/radius definitions and functional identities in Section 3, and the transfer is asymmetric with a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Whether the open translation step of converting ensemble correlation ρ into an explicit per-network real 2×2 block structure for D-scaling remains mathematically well-defined for signed sparse trophic patterns"]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are correctly attributed and share linear Hurwitz class, vocabulary mappings are type-compatible with explicit disclosure of ensemble-vs-worst-case distinction, all four correspondence vectors are demonstrated with equations/operator identities, and transfer is asymmetric with a quantitative falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify that trophic sign-pattern does decompose into repeated-scalar/full-block taxonomy for which D-scaling is provably tight (entry's own primary_failure_risk)", "Confirm no prior bibliometric hit for structured singular value μ or real stability radius r_R applied to empirical food-web community matrices beyond pseudospectra (Caravelli & Staniczenko 2016 full-block baseline cited)"]
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

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed elliptic-law inequality, structured singular value definition, and real stability radius definition are class-consistent finite-dimensional stability criteria from the stated domains; the fatal issue is not equation class but how the ρ parameter is mapped into control-theoretic structure.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "Pairwise interaction sign-correlation ρ = corr(A_ij, A_ji) ↔ Δ block-diagonal structure (repeated-scalar / full-block partition of the admissible uncertainty set)" pairs a scalar ensemble correlation parameter with a discrete uncertainty-set structure, and the entry itself states "They are explicitly NOT the same mathematical type"; the Operator Role further asserts "imposing that shape can only shrink the destabilizing search space relative to the unstructured baseline (μ_Δ(M) ≤ σ̄(M) mirrors (1+ρ) < 1 shrinking the elliptic semi-axis below the circular radius — Section 3, Vector 2)" while the entry elsewhere states "ρ > 0 (symmetric pairs, e.g. competitive or mutualistic) destabilizing," so the claimed universal shared shrinkage is mathematically incoherent.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1, 3, and 4 have supporting equations or definitions in Section 3, but vector 2 is only partially supported and is explicitly described as an open translation step rather than a demonstrated mathematical equivalence.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The control-to-ecology transfer is asymmetric as described, and the prediction specifies measurable quantities, thresholds, and a falsification condition; prior-art recognition is advisory only and does not affect the verdict.

#### Stage 3 Watch Items
- Verify whether structured singular value or real structured stability radius methods have already been applied to ecological community matrices or food webs.
- Verify the precise Allesina–Tang elliptic-law axis formula and whether the entry's (1+ρ) shrinkage claim is intended only for negative ρ.
- Verify whether the Section 4 η-scaling is intended to scale only off-diagonal interaction strengths while holding diagonal self-regulation fixed; literal scaling of the full community matrix would not produce a finite Hurwitz threshold.
- Verify the stated D-scaling tightness condition and the repeated-scalar special case μ = spectral radius for the exact block structures invoked.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed equations are individually standard, but the Bridge states "May's circular-law bound is exactly the μ(M) = σ̄(M) full-block case"; this is false because a circular-law asymptotic spectral radius is not the induced 2-norm σ̄(M) of a fixed nominal loop.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping pairs scalar correlation coefficient ρ with a discrete block-diagonal structure and explicitly says "They are explicitly NOT the same mathematical type", while the role claim that "imposing that shape can only shrink the destabilizing search space... (1+ρ) < 1" is contradicted by Section 3's own statement that ρ>0 is destabilizing.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector 1 is demonstrated by the shared spectral-abscissa condition, and Vector 3 is asserted through solving the inequality, but Vector 4 is only cited from Hinrichsen–Pritchard and Qiu et al. rather than derived, and Vector 2's supporting monotonicity claim is false as noted.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The asymmetry rationale is plausible, but the falsifiable prediction defines "η*_exact(M) as the largest uniform interaction-strength scaling η at which ηM remains Hurwitz-stable"; if M is the full community matrix, positive scaling of M preserves Hurwitz stability, so the quantity is ill-defined and does not test interaction-strength scaling.

#### Stage 3 Watch Items
- Probe whether the μ / real stability radius formalism has already been applied to ecological community matrices or food webs.
- Check Caravelli & Staniczenko (2016) and related pseudospectral ecology literature for prior structured-perturbation use.
- Verify Allesina–Tang elliptic-law sign convention and whether √(SC)σ(1+ρ) is the correct largest-real-part semi-axis for finite C and sparse matrices.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Equations correctly represent both the Allesina & Tang elliptic law stability criterion for community matrices and the standard definition of the structured singular value for robust control.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping of a scalar parameter to a matrix partition structure is a mathematical category error, which the entry itself explicitly acknowledges: "Pairwise interaction sign-correlation ρ = corr(A_ij, A_ji) ↔ Δ block-diagonal structure... They are explicitly NOT the same mathematical type: ρ is a scalar correlation coefficient shaping an ensemble-AVERAGE perturbation distribution... while Δ's block partition is a discrete, combinatorial pattern".
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1, 3, and 4 are demonstrated mathematically, but `elliptic_law_correlation_vs_block_structured_delta_shape_parameter` (Vector 2) is only partially covered. The concept appears, but no equation, operator identity, or derivation mathematically establishes the identity between the statistical correlation parameter and the block structure.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer is genuinely asymmetric (leveraging finite-S real stability radius from control theory for specific ecological networks) and the falsifiable prediction names a specific, measurable difference with concrete thresholds compared to current ensemble baseline methods.

#### Stage 3 Watch Items
- Verify whether equating an ensemble statistical correlation parameter (ρ) with a deterministic, worst-case combinatorial block structure (Δ) renders the proposed methodological transfer mathematically intractable despite the bounds sharing generic monotonicity.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All three displayed equations (Allesina–Tang elliptic-law stability criterion, structured singular value definition, real stability radius) are correctly attributed to their stated domains, belong to compatible equation classes (stability conditions on finite-dimensional real linear operators), and the ecological equation genuinely models community-matrix stability while the control-theoretic equations genuinely model robust stability under structured uncertainty. The entry explicitly bounds the correspondence to shared spectral-abscissa functional rather than claiming equation identity.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four mapping pairs pair objects of compatible mathematical type: generator↔generator (state matrices), magnitude↔magnitude (non-negative real scalars), shape-parameter↔shape-parameter (with transparent admission of the ensemble-statistic vs. combinatorial-pattern type mismatch), and dimensionless-threshold↔dimensionless-threshold. The Operator Role explanations specify concrete shared mathematical structure (the spectral abscissa functional, monotonicity of stability margin under perturbation-class restriction, reciprocal-of-critical-destabilizing-perturbation-size) rather than relying on hedged similarity assertions.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in Section 3: Vector 1 (spectral abscissa identity) is established by the shared Hurwitz-stability condition on ẋ = Jx and ẋ = A_cl x; Vector 2 (elliptic-law correlation vs. block-structured Δ) is demonstrated by the parallel between √(SC)σ(1+ρ) and μ_Δ(M) ≤ σ̄(M) as structure-aware refinements of circular-law/unstructured bounds; Vector 3 (reciprocal critical threshold) is demonstrated by identifying √(SC)σ(1+ρ)/d and μ_Δ(M) as both being reciprocals of the stability margin; Vector 4 (real sparse stability radius) is demonstrated by the r_R(A₀; S) equation and its connection to food-web sparsity patterns.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (robust control → ecology) is genuinely asymmetric: control theory possesses a mature, decades-refined computational pipeline (D-scaling, LMI/SDP, real-μ) for structured perturbation stability, while ecology's tools are asymptotic ensemble laws or unstructured pseudospectra. The falsifiable prediction is specific: it names measurable quantities (η*_exact, η*_ens, η*_struct), specific thresholds (1/√S for finite-size deviation, 60% improvement fraction), specific network subsets (Q > 0.3, S < 50), and a clear falsification condition (η*_struct no closer to η*_exact than η*_ens across the specified subset). No prior-art recognition beyond what the entry itself acknowledges.

#### Stage 3 Watch Items
- The pairing of community-matrix stability (random matrix / ensemble asymptotic regime) with structured singular value (deterministic / worst-case finite-dimensional regime) sits at the intersection of two mature literatures. Probe whether the specific real-sparse stability radius applied to empirical food-web community matrices has appeared in the ecological-stability or control-applied-to-biology literature beyond the pseudospectra work (Caravelli & Staniczenko 2016) the entry already acknowledges.
- Verify that the Allesina & Tang (2012) elliptic-law formulation yields the specific semi-axis expression √(SC)σ(1+ρ) as stated, and that the Packard & Doyle (1993) D-scaling tightness condition 2K+L ≤ 3 is correctly stated under the entry's notation convention.
- The falsifiable prediction defines η*_exact by bisection on the spectral abscissa and η*_struct by real-μ/D-scaling computation for networks up to S = 80. Verify computational feasibility of both quantities at that scale within practical resource limits.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The elliptic-law stability criterion √(SC)σ(1+ρ) < d, the structured singular value definition μ_Δ(M) = [min{σ̄(Δ) : det(I−MΔ)=0}]⁻¹, and the real stability radius r_R(A₀;𝒮) are all correctly stated and properly attributed to their respective domains. Both sides concern spectral stability of finite-dimensional linear operators, so no equation-class mismatch arises.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The entry claims "shared monotonicity" between ecological correlation ρ and control-theoretic block structure Δ, but this is mathematically false. The specific failing text in Section 2 reads: *"imposing that shape can only shrink the destabilizing search space relative to the unstructured baseline (μ_Δ(M) ≤ σ̄(M) mirrors (1+ρ) < 1 shrinking the elliptic semi-axis below the circular radius"* and in Section 3: *"imposing either structure can only shrink the destabilizing search space."* In control theory, μ_Δ(M) ≤ σ̄(M) always holds because the structured uncertainty set is literally a subset of the unstructured set. In ecology, the elliptic-law real semi-axis is √(SC)σ(1+ρ); when ρ > 0 this *exceeds* the circular-law radius √(SC)σ, expanding the destabilizing region. The entry itself states *"ρ > 0 (symmetric pairs, e.g. competitive or mutualistic) destabilizing,"* directly contradicting its own "can only shrink" claim. The directions are opposite: control-theoretic structuring is monotonically stabilizing, while ecological correlation is bidirectionally monotone in ρ (stabilizing for ρ < 0, destabilizing for ρ > 0). The claimed "shared monotonicity" in Section 1 (*"the correspondence is one of shared functional role and shared monotonicity"*) does not exist.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector 1 (spectral_abscissa_stability_operator_identity) is fully demonstrated: both ẋ = Jx and ẋ = A_cl x use the identical functional sup{Re λ} < 0. Vector 3 (reciprocal_critical_destabilizing_perturbation_threshold) is demonstrated: both √(SC)σ(1+ρ)/d and 1/μ_Δ are reciprocals of a critical destabilizing perturbation size compared to a threshold. Vector 4 (real_sparse_stability_radius_vs_asymptotic_ensemble_law_computation) is demonstrated: the real stability radius r_R is defined and connected to food-web sparsity patterns. Vector 2 (elliptic_law_correlation_vs_block_structured_delta_shape_parameter) is partially covered — the concept appears and equations are present on both sides, but the key mathematical claim establishing the correspondence (shared monotonicity) is false as detailed in CHECK 2. Three vectors are demonstrated, so the floor is met, but Vector 2's demonstration contains a mathematical error.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (robust control → ecology) is genuinely asymmetric: control theory possesses a mature, decades-refined computational pipeline (D-scaling, LMI/SDP bounds, real-μ) for structure-aware stability margins, while ecology has asymptotic ensemble laws but lacks finite-S, structure-aware stability radius tools. The falsifiable prediction is specific and measurable: it defines η*_exact, η*_ens, and η*_struct, names a subset (S < 50, Q > 0.3), specifies a 60% threshold, and provides a clear falsification condition (η*_struct no closer to η*_exact than η*_ens). No prior-art recognition triggering advisory FLAG.

#### Stage 3 Watch Items
- The spectral-abscissa identity (Vector 1) and the reciprocal-distance-to-instability correspondence (Vector 3) are mathematically sound. A revised entry that drops the false "shared monotonicity" claim and instead frames Vector 2 as a functional analogy where the two structure parameters can have *opposite* directional effects would likely pass Stage 2.
- Stage 3 should verify whether Caravelli & Staniczenko (2016) or subsequent work has already applied structured singular value or real stability radius methods to ecological community matrices.
- Stage 3 should check whether the Hinrichsen–Pritchard / Qiu et al. real structured stability radius has been applied to food-web matrices in the computational ecology or network science literature.
- Stage 3 should probe whether the D-scaling tightness condition (2K+L ≤ 3) practically limits the proposed transfer for S ∈ [15,80] food webs, where the number of trophic-pair 2×2 blocks would far exceed this bound.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The displayed ecological and control equations are individually recognizable as equations for their stated mathematical domains, and the entry explicitly qualifies the ecological/control formula correspondence rather than asserting that the elliptic-law expression is literally the structured-singular-value formula away from the unstructured/uncorrelated limit.
* **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping `Pairwise interaction sign-correlation ρ ↔ Δ block-diagonal structure` is semantically overstated: ρ is explicitly defined as an ensemble covariance/correlation parameter, whereas Δ's block partition defines a concrete admissible perturbation set, so the stated shared role is not established as a common mathematical structure.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 3 is asserted through the statement that the ensemble stability ratio is “literally” the reciprocal of a critical perturbation size, but no perturbation operator or stability-radius derivation establishes equality with 1/μ for a specific community matrix; Vector 4 is likewise only introduced as the proposed real/sparse stability-radius formulation and is not demonstrated by an equation or operator identity connecting trophic topology to the proposed 2×2 uncertainty blocks.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer direction is genuinely asymmetric within the entry's stated maturity rationale, and the prediction specifies measurable quantities, thresholds, a benchmark subset, and a falsification condition; no fatal transfer-direction or template-non-prediction issue is present.

#### Stage 3 Watch Items
* Probe whether the proposed sign-constrained real 2×2 uncertainty block for each trophic pair is mathematically justified by the actual community-matrix topology and uncertainty semantics.
* Probe the asserted identification of the ecological stability-margin reciprocal with `1/μ` or a structured stability radius for an individual finite network, rather than an asymptotic ensemble bound.
* Probe the distinction between the ensemble correlation parameter `ρ` and a control-theoretic admissible perturbation structure `Δ`; the entry itself acknowledges that they are different mathematical types but does not supply a formal translation.
* Prior-art recognition: none relied upon for the verdict.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2 
**Protocol:** v2.0  
**Verdict:** PASS  
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The entry's equations (May circular-law radius, Allesina–Tang elliptic-law inequality, μ definition, and the real stability radius \(r_{\mathbb R}\)) are all presented in the correct mathematical context and model the stated spectral-abscissa stability problem on both sides; no equation-class mismatches (elliptic vs parabolic, first-order vs higher-order, linear vs nonlinear) are present.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token in Section 2 maps objects of compatible mathematical type (finite-dimensional linear generator ↔ finite-dimensional linear generator; scalar perturbation magnitude ↔ induced-norm bound scalar; shape-of-perturbation ensemble-statistic ↔ combinatorial block-structure constraint), and the Operator Role entries specify shared mathematical structure (restriction of admissible perturbation directions and monotonic shrinking of destabilizing search space) rather than mere hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four YAML-listed vectors are demonstrated in the body:
  - **spectral_abscissa_stability_operator_identity** — shown by the common Hurwitz/spectral-abscissa criterion for \(J\) and \(A_{cl}\) (Section 1 and Section 3, Vector 1).
  - **elliptic_law_correlation_vs_block_structured_delta_shape_parameter** — discussed with the elliptic-law expression and the Δ block-structure role, including explicit commentary on type differences and monotonicity (Section 2 and Section 3, Vector 2).
  - **reciprocal_critical_destabilizing_perturbation_threshold** — supported by the μ definition and the reciprocal distance-to-instability interpretation and the real stability radius \(r_{\mathbb R}\) (Section 3, Vector 3).
  - **real_sparse_stability_radius_vs_asymptotic_ensemble_law_computation** — addressed by introducing \(r_{\mathbb R}\), citing the real/sparse literature and explaining its relevance to finite-S, sign/sparsity-constrained food webs (Section 3, Vector 4).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (robust control → ecology) is plausibly asymmetric and justified; the entry proposes a concrete, measurable falsifiable experiment (definitions of \(\eta^*_{exact}\), \(\eta^*_{ens}\), \(\eta^*_{struct}\), explicit thresholds and a testable 60% success claim for a specified subset), satisfying falsifiability requirements. Prior-art connections (May; Allesina–Tang; Doyle; real/sparse stability-radius literature) are noted in the entry and should be checked by Stage 3 as advisory watch items.

#### Stage 3 Watch Items
- Verify the exact form and prefactor of the elliptic-law semi-axis used in the Allesina–Tang inequality as written (`\sqrt{SC}\,\sigma\,(1+\rho) < d`) against the original derivation and sign conventions.
- Validate numerical tightness and computational feasibility of D-scaling / real-μ methods when applied to sign-constrained 2×2 trophic blocks and to empirically modular/sparse networks.
- Confirm that the proposed real stability-radius computation protocol (sweeping real frequency, sign/sparsity-respecting Δ) is implementable for the S ranges and modularity thresholds used in the falsifiable prediction.
- Advisory: cross-check overlap with canonical works (May 1972; Allesina & Tang 2012; Doyle 1982; Hinrichsen & Pritchard; Qiu et al.) during bibliometric Stage 3.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed equations (Allesina–Tang elliptic criterion, structured singular value definition, and real stability radius) correctly model the claimed spectral-abscissa stability problems in each domain and share the same operator class.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired mapping joins objects of compatible type (linear generators, perturbation magnitudes, shape restrictors, dimensionless distance-to-instability functionals) and the Operator Role statements name explicit shared mathematical structure rather than mere analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — spectral_abscissa_stability_operator_identity, elliptic_law_correlation_vs_block_structured_delta_shape_parameter, reciprocal_critical_destabilizing_perturbation_threshold, and real_sparse_stability_radius_vs_asymptotic_ensemble_law_computation are each demonstrated by explicit definitions, spectral identities, or derivations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by the maturity of structure-aware real-μ / sparse radius computation versus ensemble laws; the prediction supplies concrete measurable quantities (η*_exact, η*_ens, η*_struct, modularity thresholds, percentage improvement) and an explicit falsification condition.

#### Stage 3 Watch Items
- Whether the open translation step of converting ensemble correlation ρ into an explicit per-network real 2×2 block structure for D-scaling remains mathematically well-defined for signed sparse trophic patterns

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The three displayed equations correctly model the claimed domains: √(SC)σ(1+ρ)<d as the elliptic-law ecological stability bound, μ_Δ(M) as Doyle's structured singular value definition, and r_R(A0;S) as the real sparse stability radius; all are linear Hurwitz stability criteria with no elliptic/parabolic or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four pairings map compatible types (J↔A_cl both real finite-dimensional linear generators; √(SC)σ↔σ̄(M) both non-negative scalar magnitudes; ρ↔Δ-structure both shape-restrictors with explicit acknowledgment that ρ is ensemble-average covariance while Δ is per-network combinatorial pattern and shared structure named as monotonic shrinkage μ_Δ≤σ̄ mirroring (1+ρ)<1; stability ratio↔μ both dimensionless reciprocal distance-to-instability functionals).
- **CHECK 3 (Correspondence Vector Support):** PASS — Four vectors listed and all demonstrated: Vector 1 spectral_abscissa_stability_operator_identity via identical sup{Re λ}<0 functional in Sec 2 and Bridge para 1; Vector 2 elliptic_law_correlation_vs_block_structured_delta_shape_parameter via circular vs elliptic bound and μ_full=σ̄ vs μ_Δ≤σ̄ monotonicity; Vector 3 reciprocal_critical_destabilizing_perturbation_threshold via solving √(SC)σ(1+ρ)=d for critical scaling vs 1/μ definition; Vector 4 real_sparse_stability_radius_vs_asymptotic_ensemble_law_computation via r_R equation and food-web sparsity specialization citing Hinrichsen & Pritchard and Qiu et al.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry justified: robust control has mature D-scaling/LMI/real-μ pipeline for known structured bounded sets while ecology has mature ensemble laws but only uses full unstructured pseudospectral ε-ball; falsifiability satisfied by specific measurable prediction with S∈, Q>0.3, η*_exact via bisection, η*_ens from Allesina-Tang, 1/√S heuristic, and threshold |η*_struct−η*_exact|<|η*_ens−η*_exact| for ≥60% of S<50,Q>0.3 subset with explicit falsification clause. No canonical textbook prior-art recognized; advisory watch item only.[15][80]

#### Stage 3 Watch Items
- Probe whether trophic sign/sparsity pattern can be cast as repeated-scalar/full-block Δ structure for which D-scaling upper bound is provably tight (2K+L≤3 condition); this is the entry's own stated primary failure risk.
- Bibliometric search should specifically check "structured singular value AND (food web OR community matrix OR ecological network)" and "real stability radius AND food web" to confirm novelty beyond the cited pseudospectra baseline (Caravelli & Staniczenko 2016) which is correctly identified as the full/unstructured case.
- None identified as canonical textbook analogy; Schrödinger↔paraxial optics, Black-Scholes↔heat, etc. do not apply here.