---
sid_metadata:
  entry_id: "SID-041"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "qwen3.8"
  generation_timestamp: "2026-07-23"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "computational-elastoplasticity"
  domain_b: "network-traffic-equilibrium"
  structural_family: "constrained-variational-inequality-localization"
  triple_correspondence_vectors:
    - "variational_principle_normal_cone_projection"
    - "boundary_conditions_loading_path"
    - "instability_mechanism_tangent_bifurcation_localization"
    - "numerical_solution_family_return_mapping_arc_length"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 7.9
  vocabulary_divergence_score: 8.6
  expected_methodological_transfer_score: 8.7
  community_separation_score: 8.1
  representation_mismatch_score: 8.8
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.2
    uncertainty: "±0.7"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "nonconvex_traffic_cost_and_nonassociated_queue_flow"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 041

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Computational elastoplasticity — quasi-static rate-independent yielding, hardening, and strain localization in continuum solids under imposed displacement or traction paths.
*   **Silo B (Field 2):** Network traffic equilibrium — user-optimal link-flow assignment with bottleneck queues, spillback, and congestion localization in directed transportation networks under imposed origin-destination demand paths.
*   **Mathematical Isomorphism:** Both systems are rate-independent constrained dissipative evolutions whose incremental state update is a metric projection onto a convex admissible set — elastic yield domain or capacity-feasible flow polytope — so the variational normal-cone operator, imposed boundary/loading path, tangent-loss-of-monotonicity localization, and return-mapping/arc-length numerical solution families correspond directly.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Yield surface ↔ Link capacity / queue-spillback threshold
    *   *Operator Role:* Both are zero-level constraint functions defining the boundary of a convex admissible set. The solution remains interior while the trial state is admissible; once the boundary is reached, a nonnegative Lagrange multiplier activates and produces irreversible evolution.
*   Plastic multiplier ↔ Excess-demand queue rate
    *   *Operator Role:* Both are nonnegative complementarity multipliers enforcing the active constraint. Under associated flow, they scale the normal to the constraint surface; under nonassociated flow, they scale a separate flow potential while preserving the same KKT normal-cone structure.
*   Consistent tangent operator ↔ Marginal-cost network Jacobian
    *   *Operator Role:* Both are linearizations of the projected incremental map used by Newton-type active-set solvers. Loss of positive definiteness or monotonicity in this tangent signals nonuniqueness, snap-back, or localization.
*   Hardening internal variable ↔ Adaptive capacity / queue-memory state
    *   *Operator Role:* Both evolve with accumulated irreversible flow and deform the admissible set. This creates path dependence, hysteresis, and history-dependent stability thresholds.
*   Strain localization ↔ Congestion localization / spillback cutset
    *   *Operator Role:* Both are post-bifurcation concentration patterns selected when the tangent operator becomes singular. Dissipation localizes onto a lower-dimensional subset: a shear band in the continuum, or a critical link cutset / queue corridor in the network.

## 3. CORE MATHEMATICAL PARALLELISM
In computational elastoplasticity, the stress state is constrained to an elastic domain, and irreversible plastic strain accumulates only when the stress reaches the yield surface. The rate-independent KKT/normal-cone structure is commonly integrated by an implicit return-mapping algorithm:

```math
\begin{aligned}
\sigma &= C : \left(\varepsilon - \varepsilon^{p}\right), \\
f(\sigma,\kappa) &\le 0, \quad \dot{\lambda} \ge 0, \quad \dot{\lambda}\,f(\sigma,\kappa)=0, \\
\dot{\varepsilon}^{p} &= \dot{\lambda}\,\frac{\partial g}{\partial \sigma}, \quad
\dot{\kappa} = \dot{\lambda}\,h(\sigma,\kappa).
\end{aligned}
```

In network traffic equilibrium, link flows are constrained by conservation, nonnegativity, and effective capacity/queue thresholds. The Beckmann user-equilibrium formulation, augmented with queue-state-dependent costs and spillback complementarity, has the same convex-projection and KKT normal-cone architecture:

```math
\min_{f \ge 0}\; Z(f,Q)
=
\sum_{a \in A}
\int_{0}^{f_a}
c_a(x;Q_a)\,dx
\quad
\text{s.t.}
\quad
Bf = d,
```

```math
0 \le f_a \perp
c_a(f^{*},Q^{*}) + (B^{T}\pi)_a - \pi_{od(a)}
\ge 0,
```

```math
\dot{Q}_a = \dot{\lambda}_a,
\qquad
0 \le \dot{\lambda}_a \perp
c_a(f,Q) - \bar{c}_a
\ge 0.
```

In latent-space topology, the elastic domain in stress space and the feasible flow polytope in link-flow space are both convex bodies. The incremental solution is the admissible point closest to the trial state under a metric supplied by elastic compliance or by the Hessian of link-cost functions. When the trial state exits the admissible body, the normal-cone multiplier generates irreversible plastic strain or queue accumulation. Hardening and adaptive capacity management correspond to history-dependent deformation of the admissible body itself.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Computational Elastoplasticity → Network Traffic Equilibrium
*   **Asymmetric Maturity Rationale:** Computational elastoplasticity possesses a deeply mature toolkit for path-dependent constrained evolution: implicit return mapping, consistent tangent operators, active-set identification, arc-length continuation for snap-back, bifurcation and loss-of-ellipticity diagnostics, and regularization methods for localization. Dynamic traffic assignment and queue-spillback simulation have comparable variational-inequality formulations but less systematically deployed path-following, bifurcation, and localization-control machinery, especially for metastable congested states and gridlock onset.
*   **Target Bottleneck Mitigation:** Importing elastoplastic return-mapping and consistent-tangent path-following into dynamic traffic network loading will produce mesh- and time-step-independent congested equilibrium paths, detect saddle-node bifurcations associated with capacity drop, and identify the emergent critical cutset from the null eigenvector of the active-set-reduced network tangent.
*   **Falsifiable Prediction:** For a two-corridor network with coupled bottlenecks subjected to a triangular origin-destination demand cycle crossing saturation, a plasticity-return-mapping traffic solver predicts a nonzero hysteresis loop area in total network travel time that converges to a nonzero constant as the temporal step is refined, and predicts queue localization on the cutset selected by the first tangent singularity. Standard static user equilibrium predicts a single-valued response with zero hysteresis area, while standard explicit cell-transmission queueing predicts hysteresis area that changes materially with numerical discretization due to artificial diffusion.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"return mapping algorithm" AND "consistent tangent operator" AND "loss of ellipticity"`
*   `"Beckmann user equilibrium" AND "queue spillback" AND "Braess paradox"`
*   `"variational inequality" AND "dynamic traffic assignment" AND "complementarity"`