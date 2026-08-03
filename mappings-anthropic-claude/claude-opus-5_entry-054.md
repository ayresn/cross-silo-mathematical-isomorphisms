---
sid_metadata:
  entry_id: "SID-054"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-03"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "structural-shakedown-and-limit-analysis"
  domain_b: "interbank-clearing-network-systemic-risk"
  structural_family: "cyclic-variational-inequalities-with-residual-field-certificates"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "variational_principles"
    - "instability_mechanism"
    - "conserved_quantities"
    - "dimensionless_similarity_parameters"
    - "numerical_solution_family"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / historically_isolated_communities / distinct_disciplinary_language"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.4
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.7
  community_separation_score: 9.4
  representation_mismatch_score: 9.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.2
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_non_associated_default_flow"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 054

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Structural shakedown and limit analysis in pressure-vessel and nuclear component engineering — the determination, without cycle-by-cycle integration, of whether an elastic–perfectly-plastic body under variable repeated loading eventually ceases to dissipate (shakedown), oscillates plastically with bounded strain (alternating plasticity), or accumulates strain monotonically until incremental collapse (ratcheting).
*   **Silo B (Field 2):** Systemic-risk stress testing of interbank clearing networks — the determination of whether a network of cross-holding financial institutions subjected to a repeated sequence of exogenous asset shocks absorbs those shocks after a bounded one-time cascade, cycles through recurrent but self-limiting default-and-recapitalization episodes, or erodes loss-absorbing capital monotonically until systemic insolvency.
*   **Mathematical Isomorphism:** Both systems are cyclic variational inequalities in which an "elastic" (constraint-inactive) response is corrected by a **time-independent residual field constrained to the kernel of a coboundary/equilibrium operator**, so that boundedness of the **conserved irreversible dissipation functional** is decided by a single convex feasibility problem whose lower-bound (Melan-type) and upper-bound (Koiter-type) forms are strong conic duals — yielding identical **instability stratification** (elastic / shakedown / alternating / ratcheting) over a two-parameter **dimensionless load plane** and identical **numerical solution family** (load-domain vertex reduction plus interior-point conic programming).

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Self-equilibrated residual stress field** $\bar\sigma$ ↔ **Bilateral netting circulation / residual claim redistribution** $\bar c$
    *   *Operator Role:* Both are elements of the kernel of the same first-order equilibrium operator — $\nabla\!\cdot\bar\sigma = 0$ with $\bar\sigma n = 0$ on the traction boundary, and $B\bar c = 0$ for the directed liability-graph incidence matrix $B$. In the continuum the kernel admits a Beltrami potential representation $\bar\sigma = \nabla\times\nabla\times\Phi$; on the graph it is the cycle space spanned by fundamental cycles of a spanning tree. Functionally, each is a redistribution that changes *no* external load/net position but shifts the interior state away from the constraint surface — the sole degree of freedom Melan's theorem is permitted to exploit.

*   **Yield surface + closest-point return mapping** ↔ **Limited-liability clearing map (Eisenberg–Noe fixed point)**
    *   *Operator Role:* Both are projections onto a closed convex admissible set. Plastic return mapping solves $\min \|\sigma^{\text{trial}} - \sigma\|_C$ s.t. $f(\sigma)\le 0$; the clearing map $\Phi_i(p) = \min\{\bar p_i,\ e_i + \sum_j \Pi_{ji} p_j\}$ is the monotone fixed point of the same linear complementarity structure. In each case the "min" is where irreversibility enters and where the operator ceases to be linear.

*   **Traction/displacement boundary split** ($\Gamma_t$ / $\Gamma_u$) ↔ **Exogenous asset shocks vs. fixed external-creditor obligations**
    *   *Operator Role:* Both partition the boundary of the domain into a Neumann-type portion where the forcing is prescribed and the residual field must vanish, and a Dirichlet-type portion where the kinematic/obligation variable is prescribed and the residual field carries flux. This split is what makes the residual field's admissible set a *proper* subspace rather than all of $\ker B$.

*   **Ratcheting (incremental collapse)** ↔ **Persistent recapitalization deficit / non-stationary capital depletion path**
    *   *Operator Role:* Both name the failure of the residual-field feasibility problem: no time-independent element of the kernel exists that keeps the amplified elastic response inside the admissible set for every point of the load domain, so the irreversible-dissipation functional diverges linearly in cycle count.

*   **Load-domain vertices** ($\mathcal{L}$, a convex polytope of load histories) ↔ **Adverse-scenario polytope of exogenous shocks** $\mathcal{S}$
    *   *Operator Role:* Because the admissible set is convex and the elastic response is linear in the load, constraint satisfaction over the entire (infinite) history set reduces to satisfaction at the finite vertex set. This is the theorem that converts scenario enumeration into a finite conic program in both fields.

## 3. CORE MATHEMATICAL PARALLELISM

Silo A models cyclic inelasticity by decomposing the true stress into a fictitious purely elastic response $\sigma^E(x,t)$ — computed once, from a *linear* boundary-value problem — plus a residual field generated by whatever plastic strain the body has already sustained. Melan's static theorem then states that the body shakes down if and only if there exists a single time-independent, self-equilibrated $\bar\sigma$ that pulls the amplified elastic response inside the yield locus at every material point and every instant. The shakedown multiplier is therefore the value of a convex feasibility program (a second-order cone program for von Mises yielding), and Koiter's kinematic theorem supplies its exact dual as a minimization over admissible plastic strain-rate cycles with compatible net increment:

```math
\alpha_{\mathrm{SD}}
=\max_{\alpha,\ \bar{\sigma}}\ \alpha
\quad\text{s.t.}\quad
\nabla\!\cdot\bar{\sigma}=0\ \text{in}\ \Omega,\qquad
\bar{\sigma}\,n=0\ \text{on}\ \Gamma_t,\qquad
f\!\big(\alpha\,\sigma^{E}(x,t)+\bar{\sigma}(x)\big)\le 0
\quad \forall x\in\Omega,\ \forall t\in[0,T]
```

Silo B models contagion by an Eisenberg–Noe clearing vector: given relative liabilities $\Pi$, gross obligations $\bar p$, and exogenous assets $e$, payments are the greatest fixed point of a monotone concave map, and the current practice is to re-solve this fixed point separately for each hand-selected adverse scenario, then read off realized losses. Written in shakedown form, the "elastic" object is the no-default balance-sheet response $q^{E}(s,t)$ to a shock $s$, the admissible set is the solvency cone $g(\cdot)\le 0$, and the residual field is a liability circulation $\bar c$ in the cycle space of the liability graph:

```math
p^{\star}=\Phi(p^{\star}),\quad \Phi_i(p)=\min\Big\{\bar p_i,\ e_i+\textstyle\sum_j \Pi_{ji}p_j\Big\}
\qquad\Longrightarrow\qquad
\alpha_{\mathrm{SD}}
=\max_{\alpha,\ \bar{c}}\ \alpha
\quad\text{s.t.}\quad
B\,\bar{c}=0,\qquad
g\!\big(\alpha\,q^{E}(s,t)+\bar{c}\big)\le 0
\quad \forall s\in\mathcal{S},\ \forall t
```

The two programs are the same object in latent-space topology. Each is the intersection of (i) the kernel of a coboundary operator — a linear subspace whose dimension is set by the first Betti number of the domain (holes in $\Omega$; independent cycles in the liability graph) — with (ii) a convex admissible cone, scaled by a single homogeneity parameter $\alpha$. The feasibility boundary in each field is therefore the boundary of the *same* convex body, and its support function is the field's respective limit surface. Because both admissible sets are polyhedral-or-conic and both elastic responses are positively homogeneous in the load, the resulting regime maps are stratified identically: an interior region where the constraint is never active, a shell where feasibility holds only with a nonzero residual field, and an exterior split into an amplitude-driven stratum (constraint activated symmetrically each cycle, net increment zero) and a mean-driven stratum (constraint activated with nonzero net increment). What the mechanics literature draws as a Bree diagram is, structurally, the same stratification a financial network must exhibit in the plane of chronic versus cyclic shock magnitude.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Structural Shakedown and Limit Analysis → Interbank Clearing Network Systemic Risk

*   **Asymmetric Maturity Rationale:** Shakedown analysis possesses two-sided bounding theorems with proven strong duality (Melan 1938 / Koiter 1960), a sixty-year record of conic-programming implementations at $10^6$–$10^8$ variables (Linear Matching Method, interior-point SOCP/SDP formulations), rigorous a-posteriori discretization error bounds, extensions to kinematic hardening, temperature-dependent yield and poroplasticity, dedicated experimental validation rigs, and codification in load-bearing design standards. Interbank stress testing has none of these: it is dominated by forward Monte Carlo over a small, expert-chosen scenario list, offers no certificate that the worst case within a stated shock domain has been found, provides no duality-based identification of the binding failure mechanism, and ranks intervention targets by heuristic centrality measures (DebtRank, eigenvector, Katz) that carry no optimality guarantee. Robust optimization is mature in portfolio selection but has not been applied as a *residual-field feasibility certificate* on the clearing operator. The asymmetry is therefore genuine and one-directional at the level of certified worst-case machinery, even though the target field is quantitatively sophisticated elsewhere.

*   **Target Bottleneck Mitigation:** Hypothesis — reformulating network stress testing as a Melan-type feasibility program over the cycle space of the liability graph replaces scenario enumeration with a single convex certificate covering the *entire* convex shock domain, and its Koiter dual returns the critical default cycle, i.e. the minimal set of institutions and cross-holdings whose joint failure constitutes the binding mechanism. This eliminates the two acknowledged failure modes of current practice simultaneously: scenario-selection bias (the certificate is scenario-free by construction) and the absence of a principled capital-allocation rule (the dual multipliers are exactly the marginal sensitivities of the critical multiplier to each institution's loss-absorbing capacity).

*   **Falsifiable Prediction:**
    1.  **Bounding and cost.** For a calibrated network of $N \sim 10^2$–$10^3$ institutions with a polytopal shock domain $\mathcal{S}$, the conic-program multiplier will satisfy $\alpha_{\mathrm{SD}} \le \alpha_{\mathrm{MC}}$ (the worst multiplier found by exhaustive Monte Carlo over $\mathcal{S}$) and will close to within a few percent as the vertex set of $\mathcal{S}$ is completed, at $10^3$–$10^5$ fewer clearing-map solves. **Falsified** if any admissible shock sequence scaled below $\alpha_{\mathrm{SD}}$ produces cumulative deadweight default losses that grow without bound in cycle count.
    2.  **Regime geometry.** In the plane $X = $ chronic mean shock / aggregate loss-absorbing capital, $Y = $ cyclic shock amplitude / aggregate loss-absorbing capital, the boundary between bounded and unbounded cumulative loss will be *piecewise* smooth with a distinct kink where the binding constraint switches from amplitude-driven to mean-driven — structurally the junction of the linear branch and the hyperbolic branch in a Bree diagram. Current systemic-risk literature reports only smooth monotone risk curves; observing a reproducible kink at the predicted switching point in a Monte Carlo sweep would be a novel qualitative confirmation, and its demonstrable absence would falsify the mapping.
    3.  **Intervention benchmark.** Capital injections allocated along the Koiter-dual critical cycle will raise the Monte-Carlo-measured critical shock multiplier by at least 20% more than injections of identical total size allocated by DebtRank or eigenvector centrality, on the same calibrated network.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"shakedown analysis" AND "Melan static theorem" AND "second-order cone programming"`
*   `"residual stress field" AND "Koiter kinematic theorem" AND "ratcheting boundary" AND "Bree diagram"`
*   `"Eisenberg-Noe clearing vector" AND "default cascade" AND "capital buffer allocation"`
*   `"interbank network" AND "linear complementarity" AND "worst-case scenario certificate"`
*   `("shakedown theorem" OR "limit analysis") AND ("financial network" OR "systemic risk")`  *(cross-domain novelty probe — a non-empty result set here is the primary Stage 2 disqualifier)*