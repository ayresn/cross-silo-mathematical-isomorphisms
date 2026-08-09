---
sid_metadata:
  entry_id: "SID-041"
  schema_version: "1.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
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
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "Both equation systems are individually valid and correctly domain-attributed with a genuinely shared KKT/normal-cone structure, and three of four listed correspondence vectors clear the equation-level bar, but one vector is asserted without any supporting equation and the bridging prose overclaims in two identifiable places — real, specifically-named, non-fatal issues rather than fatal flaws."
    failed_checks: []
    flagged_checks:
      - "Check 1: Section 3's bridging prose contains the undefined, domain-mismatched phrase 'In latent-space topology' and an unqualified closest-point/metric-projection claim that the shown non-associated flow rule does not fully support"
      - "Check 3: correspondence vector 'instability_mechanism_tangent_bifurcation_localization' is named and discussed in three places but never demonstrated with an equation, operator identity, or derivation"
      - "Check 4: the general variational-inequality/complementarity-theory unification of constrained mechanics problems and network-equilibrium problems is recognized prior art (advisory only, not grounds for rejection)"
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify whether the specific proposed transfer (return-mapping / consistent-tangent / arc-length methods from computational plasticity into dynamic traffic assignment) has prior precedent, as distinct from the well-known general fact that mechanics-type and network-equilibrium-type problems both fall under variational-inequality/complementarity theory (e.g., texts treating contact/plasticity problems and traffic/spatial equilibrium as parallel VI example classes)"
      - "Have a domain expert check whether Section 3's claim that the update is 'the admissible point closest to the trial state under a metric' needs qualification for non-associated flow (g≠f, explicitly permitted by the shown flow rule ε̇^p = λ̇ ∂g/∂σ), since the literal closest-point/projection reading is cleanest for associated flow"
      - "Determine whether an explicit singularity/bifurcation condition (an acoustic-tensor-type criterion on the elastoplasticity side, a Jacobian-singularity criterion on the traffic side) can actually be written down for both domains, since Section 2's tangent-operator and localization pairings are currently asserted only in qualitative prose"
      - "Confirm the source of the 'In latent-space topology' phrase in Section 3 — it does not correspond to either stated domain and may indicate partial template reuse from an unrelated entry, worth checking against the rest of the entry's prose"
      - "Cross-check the entry's own validation_status.primary_failure_risk ('nonconvex_traffic_cost_and_nonassociated_queue_flow') against Section 1's premise that both admissible sets are convex and the update is a metric projection; the entry appears to already flag internally the same convexity/associativity soft spots raised independently in Check 1"
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.4 Thinking-Mini"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "FLAG"
    verdict_rationale: "The core variational-inequality correspondence is internally consistent, but one listed correspondence vector is only named rather than demonstrated in the body."
    failed_checks: []
    flagged_checks: ["Check 3: numerical_solution_family_return_mapping_arc_length is only partially supported"]
    quoted_evidence: []
    stage_3_watch_items:
      - "Section 1 / Section 3: the listed vector 'numerical_solution_family_return_mapping_arc_length' is asserted, but the traffic side never derives an arc-length continuation or equivalent numerical family."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "Three of the four claimed correspondence vectors lack any supporting equations, operator identities, or mathematical derivations in Section 3."
    failed_checks: ["Check 3: Undemonstrated correspondence vectors"]
    flagged_checks: []
    quoted_evidence:
      - "boundary_conditions_loading_path"
      - "instability_mechanism_tangent_bifurcation_localization"
      - "numerical_solution_family_return_mapping_arc_length"
      - "imposed boundary/loading path, tangent-loss-of-monotonicity localization, and return-mapping/arc-length numerical solution families correspond directly."
    stage_3_watch_items:
      - "Assess whether the local-to-global mapping between pointwise elastoplastic constitutive equations and network-wide flow equilibrium is mathematically sound without including the continuum momentum balance equations."
      - "Verify literature to see if arc-length continuation and elastoplastic consistent tangents have already been applied to dynamic traffic assignment."
  fourth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "Both equation sets are correctly stated rate-independent KKT/variational-inequality systems with compatible mathematical structure, all vocabulary mappings pair objects of compatible type with shared structure named, all four correspondence vectors are demonstrated in the body, and the falsifiable prediction specifies measurable outcomes with comparison baselines."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the specific cross-domain mapping between elastoplastic return-mapping algorithms and dynamic traffic assignment solvers has been explored in the operations research or computational mechanics literature — the shared KKT/normal-cone structure is individually well-established in both fields (Dafermos/Nagurney for traffic VI; Simo/Hughes for computational plasticity), but the explicit methodological bridge may be novel or may already exist in niche computational transportation work.", "Probe whether the queue complementarity equation Q̇_a = λ̇_a, 0 ≤ λ̇_a ⊥ c_a(f,Q) - c̄_a ≥ 0 is a standard formulation in dynamic traffic assignment or an original construction by the entry — its rate-independent structure matches the plasticity side but may not correspond to any widely used traffic model.", "Assess whether the claimed hysteresis in traffic networks under cyclic loading has been empirically observed and whether arc-length continuation has been applied to traffic equilibrium problems under a different name."]
  fifth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All equations are correctly attributed KKT/complementarity systems, vocabulary mappings are type-compatible with shared normal-cone structure, four correspondence vectors are demonstrated in Sections 1, 3 and 4, and transfer is asymmetric with a specific falsifiable hysteresis-area prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify convexity of queue-augmented Beckmann objective Z(f,Q) with state-dependent costs for the metric-projection claim per primary_failure_risk nonconvex_traffic_cost_and_nonassociated_queue_flow", "Check nonassociated flow potential handling g != f vs asymmetric traffic cost Jacobian"]
  sixth_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "REJECT"
    verdict_rationale: "Correspondence vector 'numerical_solution_family_return_mapping_arc_length' is listed but the body provides no equation, operator identity, or derivation demonstrating the arc-length correspondence on the traffic side; only a transfer proposal is given."
    failed_checks: ["Check 3: undemonstrated correspondence vector 'numerical_solution_family_return_mapping_arc_length'"]
    flagged_checks: ["Check 4c: prior-art advisory - the isomorphism between rate-independent plasticity (sweeping process) and dynamic traffic assignment with capacity constraints is a known analogy"]
    quoted_evidence: ["YAML triple_correspondence_vectors entry: 'numerical_solution_family_return_mapping_arc_length'; Section 1 claim: 'return-mapping/arc-length numerical solution families correspond directly.' The body shows no equation, operator identity, or derivation that establishes an arc-length continuation formulation for the network traffic equilibrium problem; only a methodological transfer proposal in Section 4."]
    stage_3_watch_items: ["Known prior-art analogue: rate-independent plasticity (Moreau's sweeping process) ⇔ dynamic traffic assignment with bottleneck queues and complementarity. Bibliometric search for works applying elastoplastic return mapping or arc-length continuation to traffic equilibrium, and for earlier structural isomorphisms between the two domains."]
  seventh_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-04"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are of compatible variational-inequality/normal-cone class supporting the claimed projection structure, vocabulary mappings are type-consistent with explicit shared operator roles, every listed correspondence vector is demonstrated by equations or derivations in Sections 1–4, and the transfer is asymmetrically justified with a concrete measurable falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
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

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — Both displayed systems are individually valid and correctly attributed to their stated fields (Section 3's Silo A block is the standard KKT/return-mapping formulation of rate-independent plasticity; Silo B's block is a Beckmann-type convex program correctly extended with complementarity-based spillback), but the connecting prose opens with the undefined, out-of-domain phrase "In latent-space topology..." (neither Silo A nor Silo B involves a latent space), and separately states the update is "the admissible point closest to the trial state under a metric" — a literal closest-point/projection reading that holds cleanly for associated flow but is not established for the general case the entry's own flow rule permits ("ε̇^p = λ̇ ∂g/∂σ", with g left distinct from f).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — all five Section 2 pairs are type-coherent (constraint-boundary functions, complementarity-multiplier rates, tangent/Jacobian linearizations, path-dependent internal-state variables, and spatial concentration patterns, respectively), and every Operator Role names concrete shared mathematical structure rather than hedged language such as "analogous to."
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector "variational_principle_normal_cone_projection" is demonstrated via the explicit KKT/complementarity systems shown for both silos in Section 3. Vector "boundary_conditions_loading_path" is demonstrated, if thinly: ε and d appear in the Section 3 equations exactly in the imposed/exogenous role Section 1 assigns them, though no explicit time-indexed path equation is given for either side. Vector "numerical_solution_family_return_mapping_arc_length" is demonstrated, grounded in the same KKT/complementarity systems plus Section 4's specific elaboration on what importing them would produce. Vector "instability_mechanism_tangent_bifurcation_localization" is NOT demonstrated: it is named in Section 1 and discussed twice in Section 2 ("Consistent tangent operator ↔ Marginal-cost network Jacobian"; "Strain localization ↔ Congestion localization / spillback cutset") and again in Section 4, but no tangent-operator formula, Jacobian formula, or singularity/bifurcation condition is written down anywhere in the entry for either domain — the correspondence is asserted in qualitatively correct vocabulary only.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — (a) Asymmetry is adequately supported: Section 4 names five specific, mature elastoplasticity techniques and contrasts them against a specifically-scoped traffic-side gap ("less systematically deployed path-following, bifurcation, and localization-control machinery... for metastable congested states and gridlock onset"), and nothing in the entry indicates the direction is backwards. (b) The falsifiable prediction clears the template-non-prediction bar: it names a specific network topology, a specific measurable quantity (hysteresis loop area in total network travel time), a specific convergence behavior under mesh/time-step refinement, and two named contrasting baselines (static UE, explicit cell-transmission). (c) Prior art (advisory only): the underlying claim that constrained mechanics problems (plasticity, contact, obstacle problems) and network/spatial equilibrium problems (including traffic assignment) share variational-inequality/complementarity structure is recognized, general-purpose material in the VI/complementarity-problem literature. Flagged for Stage 3 review, not grounds for rejection.

#### Stage 3 Watch Items
- Verify whether the specific proposed transfer (return-mapping / consistent-tangent / arc-length methods from computational plasticity into dynamic traffic assignment) has prior precedent, as distinct from the well-known general fact that mechanics-type and network-equilibrium-type problems both fall under variational-inequality/complementarity theory.
- Have a domain expert check whether "the admissible point closest to the trial state under a metric" (Section 3) needs qualification for non-associated flow (g≠f, explicitly permitted by the shown flow rule), since the literal closest-point/projection reading is cleanest for associated flow.
- Determine whether an explicit singularity/bifurcation condition (e.g., an acoustic-tensor-type criterion on the elastoplasticity side and a Jacobian-singularity criterion on the traffic side) can actually be written down for both domains, since Section 2's tangent-operator and localization pairings are currently asserted qualitatively only.
- Confirm the source of the "In latent-space topology" phrase in Section 3 — it does not correspond to either stated domain and may indicate partial template reuse from an unrelated entry.
- Cross-check the entry's own `validation_status.primary_failure_risk` ("nonconvex_traffic_cost_and_nonassociated_queue_flow") against Section 1's premise that both admissible sets are convex and the update is a metric projection; the entry appears to already flag internally the same convexity/associativity soft spots raised independently in Check 1.

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.4 Thinking-Mini
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-04

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The elastoplastic and traffic formulations are internally consistent with the stated rate-independent constrained-evolution framing, and no equation-class mismatch is evident from the text alone.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired terms are mathematically compatible types, and each operator-role explanation names a shared structure rather than a pure analogy.
* **CHECK 3 (Correspondence Vector Support):** FLAG — `variational_principle_normal_cone_projection`, `boundary_conditions_loading_path`, and `instability_mechanism_tangent_bifurcation_localization` are supported in Sections 1–4, but `numerical_solution_family_return_mapping_arc_length` is only named and is not demonstrated on both sides with an equation, operator identity, or derivation.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is stated asymmetrically toward the less mature traffic side, and the prediction names specific measurable outcomes (hysteresis-loop area and queue localization) that could fail.

#### Stage 3 Watch Items
* Section 1 / Section 3: verify whether the traffic-side “return-mapping/arc-length numerical solution families” claim is actually substantiated, since the arc-length piece is not derived there.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides present differential-algebraic complementarity systems (DVI) representing constrained projection; the local elastoplastic constitutive equations logically align with the network link KKT conditions in the context of the proposed correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The vocabulary matrix maps mathematically compatible objects (e.g., threshold functions, rate multipliers, tangent operators) and clearly identifies their shared structural roles in active-set convex projection.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector "variational_principle_normal_cone_projection" is demonstrated, but the body provides no equations, operator identities, or derivations to support "boundary_conditions_loading_path", "instability_mechanism_tangent_bifurcation_localization", or "numerical_solution_family_return_mapping_arc_length", despite Section 1 explicitly claiming that the "imposed boundary/loading path, tangent-loss-of-monotonicity localization, and return-mapping/arc-length numerical solution families correspond directly."
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction appropriately leverages deeply mature continuum mechanics continuation tools for less mature dynamic traffic localization problems, and the prediction of a measurable hysteresis loop area under step refinement is highly specific and falsifiable.

#### Stage 3 Watch Items
- Assess whether the local-to-global mapping between pointwise elastoplastic constitutive equations and network-wide flow equilibrium is mathematically sound without including the continuum momentum balance equations.
- Verify literature to see if arc-length continuation and elastoplastic consistent tangents have already been applied to dynamic traffic assignment.

### Fourth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The elastoplasticity equations are a standard rate-independent KKT system with return-mapping integration (σ = C:(ε−εᵖ), f ≤ 0, λ̇ ≥ 0, λ̇f = 0, flow and hardening rules), and the traffic equations are a Beckmann UE formulation with augmented queue-spillback complementarity (min Z s.t. Bf = d, flow complementarity, and Q̇_a = λ̇_a with cost-threshold complementarity). Both are rate-independent variational inequality / KKT systems — no equation-class mismatch. The shared normal-cone projection structure claimed in Section 1 is supported: both systems compute an admissible point closest to a trial state under a problem-specific metric (elastic compliance Hessian vs. link-cost Hessian), with complementarity multipliers activating on constraint boundaries.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five mappings pair compatible mathematical types: yield surface and capacity threshold are both zero-level scalar constraint functions; plastic multiplier and excess-demand queue rate are both nonnegative complementarity multipliers; consistent tangent and network Jacobian are both linearizations of projected incremental maps; hardening variable and queue-memory state are both evolving state variables deforming the admissible set; strain localization and congestion localization are both post-bifurcation concentration patterns. Each operator role explanation names specific shared mathematical structure (KKT normal-cone, convex admissible set boundary, Newton active-set linearization) rather than relying on hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 (normal-cone projection) is demonstrated by the parallel KKT complementarity structures in both equation sets and the explicit projection discussion in Section 3. Vector 2 (boundary conditions/loading path) is demonstrated by the total strain ε in the elastoplasticity equations and the demand constraint Bf = d in the traffic equations, both representing externally imposed driving paths. Vector 3 (tangent bifurcation/localization) is demonstrated through the consistent tangent ↔ network Jacobian mapping in Section 2 and the localization discussion connecting tangent singularity to shear band / critical cutset selection. Vector 4 (return-mapping/arc-length) is demonstrated through the shared KKT structure enabling the same numerical solution family and the specific application to snap-back/bifurcation in Section 4.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (elastoplasticity → traffic) is genuinely asymmetric: computational plasticity has a decades-developed toolkit of return mapping, consistent tangent operators, arc-length continuation, and loss-of-ellipticity diagnostics, while traffic equilibrium has variational inequality formulations but less systematically deployed path-following and localization-control machinery. The falsifiable prediction is specific: a two-corridor network under triangular demand cycling should exhibit nonzero hysteresis loop area converging to a constant under temporal refinement (vs. zero for static UE, vs. discretization-dependent for cell-transmission), with queue localization on the cutset selected by the first tangent singularity. This names measurable quantities, comparison baselines, and outcomes that could falsify the prediction. No canonical prior-art analogy recognized — the individual VI/KKT frameworks in each field are well-established but the explicit cross-domain methodological bridge appears unexplored.

#### Stage 3 Watch Items
- Verify whether the specific mapping between elastoplastic return-mapping algorithms and dynamic traffic assignment solvers has been explored in the computational transportation or operations research literature. The shared KKT/normal-cone structure is individually well-established in both fields (Dafermos/Nagurney for traffic VI; Simo/Hughes for computational plasticity), but the explicit methodological bridge may be novel.
- Probe whether the queue complementarity equation (Q̇_a = λ̇_a, 0 ≤ λ̇_a ⊥ c_a(f,Q) − c̄_a ≥ 0) is a standard formulation in dynamic traffic assignment or an original construction. Its rate-independent structure matches the plasticity side but may not correspond to any widely deployed traffic model.
- Assess whether hysteresis in traffic networks under cyclic demand loading has been empirically observed, and whether arc-length continuation has been applied to traffic equilibrium problems under a different name (e.g., path-following in parametric VI solvers).
- Investigate whether the entry's primary failure risk (nonconvex traffic costs breaking the projection interpretation) is a practical or merely theoretical concern — nonconvex link cost functions do appear in real traffic networks with capacity drop phenomena.

### Fifth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A equations are the standard quasi-static elastoplastic KKT system and Silo B equations are the Beckmann UE with capacity complementarity; both are variational-inequality/KKT systems consistent with the claimed constrained-variational-inequality-localization family, no elliptic/parabolic or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five pairs map compatible types (constraint function ↔ constraint function, multiplier rate ↔ multiplier rate, tangent operator ↔ Jacobian, internal variable ↔ state, localization pattern ↔ localization pattern) and each Operator Role specifies a shared structure (zero-level set, normal-cone KKT, linearization of projected map, history-dependent admissible set deformation, singular-tangent nullspace).
- **CHECK 3 (Correspondence Vector Support):** PASS — variational_principle_normal_cone_projection demonstrated in Section 3 KKT equations and projection-metric paragraph; boundary_conditions_loading_path demonstrated via Bf=d demand constraint and imposed strain path in Sections 1 and 3; instability_mechanism_tangent_bifurcation_localization demonstrated via consistent tangent ↔ marginal-cost Jacobian mapping and null-eigenvector cutset in Sections 2 and 4; numerical_solution_family_return_mapping_arc_length demonstrated via implicit return-mapping in Section 3 and arc-length continuation plus return-mapping import in Section 4.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine (elastoplasticity mature toolkit for return-mapping, consistent tangent, arc-length, loss-of-ellipticity vs less systematized path-following in traffic); falsifiability is specific (nonzero hysteresis loop area in total travel time converging to constant under refinement and queue localization on first-singularity cutset vs zero area for static UE and mesh-dependent area for cell-transmission). No canonical textbook pairing recognized; prior-art advisory none.

#### Stage 3 Watch Items
- Verify convexity/monotonicity of augmented objective with Q-dependent costs c_a(x;Q_a) and implications for closest-point projection interpretation noted in primary_failure_risk.
- Probe handling of nonassociated flow (g ≠ f) vs asymmetric traffic Jacobian and whether metric projection becomes non-self-adjoint.
- None identified as canonical prior art; general VI unification is known but specific elastoplasticity-traffic localization isomorphism is not a standard textbook analogy.

### Sixth Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The elastoplasticity and traffic complementarity equations correctly model their respective rate-independent constrained-evolution domains, and both exhibit the claimed normal-cone/projection structure with no equation-class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All paired tokens map objects of compatible mathematical type (constraint surfaces, multipliers, operators, internal state variables, localization patterns) with shared structural roles described without category errors.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector `numerical_solution_family_return_mapping_arc_length` is listed in the YAML but is not demonstrated in the body. The text merely names “return-mapping/arc-length numerical solution families correspond directly” (Section 1) and proposes a transfer of arc-length continuation (Section 4); no equation, operator identity, or derivation establishes the arc-length method as a natural consequence of the traffic equilibrium structure. The return-mapping portion is partially illustrated by the projection interpretation, but the arc-length component lacks any supporting mathematical treatment. A vector without supporting body text constitutes a FAIL.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is genuinely asymmetric, and the falsifiable prediction (nonzero hysteresis loop area converging under refinement, cutset localization from tangent singularity) is specific and measurable. Advisory prior-art note: the analogy between rate-independent plasticity and traffic assignment with capacity constraints is a known interdisciplinary connection (e.g., sweeping-process formulations of dynamic traffic flow). This does not affect the verdict but should be probed at Stage 3.

#### Stage 3 Watch Items
- The isomorphism between rate-independent plasticity (Moreau sweeping process) and dynamic traffic assignment with complementarity constraints is a recognized analogy. Stage 3 bibliometric review should check for prior publications that explicitly map elastoplastic return mapping, consistent tangent operators, or arc-length continuation onto network traffic equilibrium, and assess whether the entry’s claimed correspondence vectors have already been formalised.

### Seventh Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-04

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The elastoplasticity KKT/return-mapping system and the Beckmann-plus-queue complementarity system are both rate-independent constrained evolutions driven by projection onto a convex admissible set under a normal-cone multiplier; the displayed equations belong to the same structural class and jointly support the Section 1 claim.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired mapping equates objects of matching mathematical type (constraint surfaces, complementarity multipliers, tangent operators, internal variables, localization patterns) and the Operator Role statements name the shared normal-cone/KKT structure without pure hedge language.
- **CHECK 3 (Correspondence Vector Support):** PASS — variational_principle_normal_cone_projection is shown by the projection/KKT equations and latent-space topology paragraph of Section 3; boundary_conditions_loading_path is identified in Section 1 and realized as the imposed strain path versus the imposed OD demand vector in Section 3; instability_mechanism_tangent_bifurcation_localization is developed via the consistent-tangent/Jacobian singularity and localization descriptions in Sections 2–3; numerical_solution_family_return_mapping_arc_length is stated in Section 1 and elaborated as the imported path-following machinery in Section 4.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The stated direction (elastoplasticity toolkit into traffic) is asymmetrically justified by the comparative maturity of return-mapping, consistent-tangent, arc-length and loss-of-ellipticity tools; the prediction supplies a concrete measurable signature (nonzero, mesh-convergent hysteresis area of total travel time plus cutset localization selected by the first tangent singularity) that distinguishes the proposed solver from both static UE and explicit CTM under a specified two-corridor triangular demand cycle.

#### Stage 3 Watch Items
None identified.