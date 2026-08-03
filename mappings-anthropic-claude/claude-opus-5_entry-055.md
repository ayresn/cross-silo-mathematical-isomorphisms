---
sid_metadata:
  entry_id: "SID-055"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-03"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "athermal-amorphous-plasticity"
  domain_b: "power-grid-cascading-outage-analysis"
  structural_family: "long-range-signed-kernel-threshold-avalanches"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "conserved_quantities"
    - "instability_mechanism"
    - "numerical_solution_family"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / distinct_disciplinary_language / historically_isolated_communities — the only existing contact between statistical physics and power systems is at the mean-field level (self-organized-criticality framings, equal-load-sharing fiber-bundle models, Galton-Watson branching estimators), all of which discard the signed, anisotropic, sum-rule-constrained redistribution kernel that actually carries the correspondence"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.4
  vocabulary_divergence_score: 8.8
  expected_methodological_transfer_score: 8.1
  community_separation_score: 7.9
  representation_mismatch_score: 9.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.8
    uncertainty: "±1.6"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "kernel_geometry_mismatch — a transmission network is neither translation-invariant nor isometrically embedded in a Euclidean metric, so the quadrupolar angular structure and clean power-law decay of the Eshelby propagator may not survive on real topologies, invalidating the imported finite-size-scaling relations even if the operator identification holds"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 055

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Athermal quasi-static plasticity of amorphous solids — mesoscale elastoplastic modelling of metallic glasses, dense emulsions, and foams, where localized shear transformations trigger system-spanning plastic avalanches at the yielding transition.
*   **Silo B (Field 2):** Cascading outage analysis in electric power transmission — the propagation of line trips through a meshed high-voltage network after an initiating contingency, producing heavy-tailed blackout size distributions.
*   **Mathematical Isomorphism:** Both systems are extremal threshold dynamics on a scalar residual-stability field driven by an instantaneous, *signed*, sum-rule-constrained long-range Green's function of a linear equilibrium constraint — the Eshelby propagator of $\nabla\!\cdot\!\sigma=0$ in Silo A and the Line Outage Distribution Factor matrix of the susceptance-weighted graph Laplacian in Silo B — with correspondence established across the **governing differential operator** (Green's function of an elliptic equilibrium operator), the **conserved quantity** (mechanical force balance ↔ Kirchhoff current law, which is what forces redistribution to be instantaneous and nonlocal), the **instability mechanism** (quenched-disorder threshold crossing under marginal stability), and the **numerical solution family** (extremal-dynamics kinetic Monte Carlo with finite-size scaling of avalanche cutoffs).

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Eshelby quadrupolar stress propagator** ↔ **Line Outage Distribution Factor (LODF) matrix**
    *   *Operator Role:* Each is the Green's function obtained by inverting the system's equilibrium constraint operator subject to a unit local relaxation event. Both are *signed* (a released load relieves some neighbours and overloads others — the mechanical $\cos 4\phi$ lobes and the grid's Braess-type negative entries are the same phenomenon), both are long-ranged with no intrinsic cutoff, and both obey a strict sum rule inherited from the underlying conservation law, so the far-field angular/cutset average of the redistributed quantity vanishes. This sign alternation is the mathematical origin of marginal stability in *both* systems and is exactly what mean-field treatments in each field discard.
*   **Local distance to threshold $x = \sigma_{\rm th} - \sigma$ ("residual strength")** ↔ **Line flow margin $x_\ell = f_\ell^{\max} - |f_\ell|$ ("thermal headroom")**
    *   *Operator Role:* Both are the quenched-disorder gap variable of the threshold dynamics. The avalanche statistics of each system are controlled not by the mean of this field but by the shape of its density $P(x)$ as $x \to 0^{+}$, because the extremal (smallest-$x$) site sets the driving increment required to trigger the next event.
*   **Pseudogap exponent $\theta$ in $P(x)\sim x^{\theta}$** ↔ **[no established term]**
    *   *Operator Role:* A pure diagnostic asymmetry. In Silo A, $\theta>0$ is a derived consequence of the signed kernel and is measured routinely; in Silo B the corresponding density is never characterized, and the field implicitly assumes $\theta = 0$ (finite density of near-critical lines) whenever it fits branching processes. The exponent is the same functional object in both.
*   **Plastic avalanche / stress drop $S$** ↔ **Cascading outage / load shed $S$**
    *   *Operator Role:* The integrated relaxation of the driven field between two mechanically (respectively electrically) admissible quasi-static equilibria, following the same $P(S)\sim S^{-\tau}\mathcal{F}(S/S_c)$ scaling ansatz with a system-size-dependent cutoff.
*   **Quasi-static shear driving $\dot\gamma \to 0$** ↔ **Slow demand growth / dispatch re-securing between contingencies**
    *   *Operator Role:* Both are adiabatic loading protocols that advance the control parameter only until the extremal site reaches threshold, ensuring timescale separation between driving and redistribution — the defining condition for extremal dynamics.
*   **Soft spots / low-frequency mode localization** ↔ **Critical contingency pairs / vulnerable cutsets**
    *   *Operator Role:* Both name the sites where the low-lying spectrum of the equilibrium operator localizes, and in both cases these sites predict where the next relaxation event nucleates without simulating the dynamics.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** Mesoscale elastoplastic models coarse-grain an amorphous solid into a lattice of blocks carrying a local shear stress $\sigma(\mathbf r)$ and a quenched yield threshold $\sigma_{\rm th}(\mathbf r)$. When a block yields it releases a local plastic strain increment, and because the surrounding matrix must remain in mechanical equilibrium, $\nabla\!\cdot\!\sigma = 0$, that release is transmitted instantaneously to the entire system through the Eshelby inclusion Green's function:

```math
\sigma(\mathbf{r},t)=\Sigma(t)+\int G(\mathbf{r}-\mathbf{r}')\,\epsilon^{\mathrm{pl}}(\mathbf{r}',t)\,d^{d}\mathbf{r}',
\qquad
\hat{G}(\mathbf{q})=-\,\frac{4\mu\,q_x^{2}q_y^{2}}{|\mathbf{q}|^{4}},
\qquad
G(r,\phi)\ \propto\ \frac{\cos 4\phi}{r^{d}}
```

The system self-organizes so that the density of local distances to threshold develops a *pseudogap*, $P(x)\sim x^{\theta}$ with $\theta \approx 0.5$ in $d=2$ and $\theta \approx 0.4$ in $d=3$, a state of marginal stability that exists precisely because the kernel changes sign: a strictly stabilizing kernel would permit a finite density of near-critical sites, whereas the alternating lobes force the population away from $x=0$ just enough to keep the solid from being unconditionally unstable.

**Silo B.** Under the DC power flow approximation, a transmission network with incidence matrix $\mathbf{A}$ and branch susceptances $\mathbf{D}$ satisfies a discrete Poisson equation on the susceptance-weighted graph Laplacian $\mathbf{B}=\mathbf{A}\mathbf{D}\mathbf{A}^{\top}$, with the injection vector $\mathbf{P}$ as source. When a line trips, its pre-outage flow is re-expressed as a compensating injection pair and redistributed instantaneously — again because a conservation law (Kirchhoff's current law) admits no transient storage:

```math
\mathbf{B}\,\boldsymbol{\theta}=\mathbf{P},\qquad
\mathbf{f}=\mathbf{D}\mathbf{A}^{\top}\mathbf{B}^{+}\mathbf{P},\qquad
\mathrm{LODF}_{\ell k}=\frac{\mathrm{PTDF}_{\ell k}}{1-\mathrm{PTDF}_{kk}},\qquad
\Delta f_{\ell}=\mathrm{LODF}_{\ell k}\,f_{k}^{-}
```

where $\mathbf{B}^{+}$ is the Moore–Penrose pseudoinverse. The LODF matrix is thus *literally* the discrete Eshelby propagator: it is the Green's function of an elliptic equilibrium operator, evaluated for a unit local relaxation, and it inherits the identical signed, sum-rule-constrained, slowly-decaying structure.

**Latent-space correspondence.** Strip both systems of their ontology — one a continuum second-rank stress tensor field on $\mathbb{R}^{d}$, the other a scalar flow vector on the cycle space of a discrete random graph — and each reduces to the *same* two-parameter latent object: (i) the spectral decay exponent of the signed redistribution kernel, and (ii) the pseudogap exponent of the residual-margin density. Every observable of interest in both fields lies on the universality surface these two coordinates parameterize:

```math
P(x)\sim x^{\theta}\ (x\to0^{+})
\ \Longrightarrow\
\langle x_{\min}\rangle \sim N^{-\frac{1}{1+\theta}},
\qquad
P(S)\sim S^{-\tau}\,\mathcal{F}\!\left(S/N^{\,d_f/d}\right)
```

The first relation is elementary extreme-value statistics of $N$ samples drawn from a pseudogapped density; it is used constantly in Silo A and is entirely absent from Silo B. The mean-field limit $\theta \to 0$, kernel $\to$ equal-load-sharing collapses both to $\tau = 3/2$ — which is exactly the exponent the power-systems Galton–Watson branching estimators produce and the exponent that equal-load-sharing fiber-bundle models produce. That coincidence is strong evidence the two fields have independently discovered the *mean-field shadow* of a single non-mean-field problem.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Athermal Amorphous Plasticity → Power Grid Cascading Outage Analysis

*   **Asymmetric Maturity Rationale:** Silo A has spent roughly twenty-five years building a tightly coupled theory-plus-simulation program around exactly this operator: analytically solvable mean-field closures (Hébraud–Lequeux, ABBM) that yield closed-form avalanche distributions from kernel statistics; a derivation of $\theta$ from marginal-stability arguments rather than from fitting; standardized finite-size-scaling protocols that extrapolate exponents and cutoffs from small lattices to the thermodynamic limit; extreme-value machinery relating $\langle x_{\min}\rangle$ to system size; and machine-learned "softness" classifiers validated against molecular dynamics that predict rearrangement sites without integrating the dynamics. Silo B's *linear algebra* is comparably mature — LODF computation, Woodbury rank-one updates, and screening heuristics are standard utility practice — but its *statistical layer* is almost purely empirical. Contingency analysis remains enumerative: N-1 is mandated and tractable, N-1-1 is expensive, and exhaustive N-2 on an interconnection with $M \sim 10^{4}$–$10^{5}$ branches requires $10^{8}$–$10^{9}$ solves and is simply not performed. Blackout-size modelling relies on branching processes whose critical exponent is fixed at the mean-field value by construction and therefore cannot be linked predictively to network topology or to operating margins. The maturity gap is thus not in solving the Green's function but in knowing what its *statistics* imply.

*   **Target Bottleneck Mitigation:** *Hypothesis.* If the ensemble of N-1-secure dispatch states of a large transmission network is characterized by (a) the empirical margin density $P(x)$ and (b) the empirical decay and sign structure of the LODF kernel, then the identity of the cascade-critical N-2 pairs is determined by a joint extremal statistic of $(x_\ell,\ \mathrm{LODF}_{\ell k})$ rather than by exhaustive enumeration. Concretely: importing extremal-dynamics ranking plus the pseudogap-conditioned extreme-value estimate should allow a screening procedure evaluating $O(M\log M)$ candidate pairs to recover $\geq 90\%$ of the N-2 pairs that exhaustive DC-cascade simulation identifies as producing $>1\%$ system load loss — collapsing the combinatorial screening bottleneck by three to four orders of magnitude on interconnection-scale cases.

*   **Falsifiable Prediction:**
    1.  **Pseudogap existence and value.** Measured across the ensemble of N-1-secure dispatches on synthetic interconnection-scale grids and on real ISO state estimates, the margin density will exhibit $P(x)\sim x^{\theta}$ with $\theta$ significantly greater than zero (predicted range $0.3 \lesssim \theta \lesssim 0.7$), rather than the finite non-zero density at $x\to 0^{+}$ implicitly assumed by branching-process fits. **Falsifier:** a flat or diverging $P(x)$ near zero on real dispatch data kills the marginal-stability import outright.
    2.  **Non-mean-field blackout exponent, topology-dependent.** The cascade size exponent will deviate measurably below the branching-process value, $\tau < 3/2$, and — critically — will *vary systematically with the LODF kernel's decay rate*, approaching $3/2$ only in highly meshed grids where the kernel is effectively equal-load-sharing. This is a sharp, distinguishing departure from the current state of the art, which treats $\tau$ as a universal constant carrying no topological information.
    3.  **Extreme-value scaling of the loading margin.** The expected headroom of the closest-to-trip line, and hence the increment of load growth between cascade-initiating events, will scale as $M^{-1/(1+\theta)}$ with the number of branches $M$, using the $\theta$ measured in prediction (1). This is directly testable by finite-size scaling across the IEEE 118 / 300 / 1354 / 2000-bus synthetic series and predicts a specific, currently unmodelled *increase* in cascade susceptibility with grid size at fixed relative loading.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"Eshelby propagator" AND "elastoplastic model" AND ("pseudogap exponent" OR "distance to threshold")`
*   `"line outage distribution factor" AND "DC power flow" AND "cascading failure" AND "contingency screening"`
*   `"marginal stability" AND "avalanche size distribution" AND "long-range sign-changing kernel"`
*   `"branching process" AND "blackout size distribution" AND "critical exponent" AND "power grid"` *(prior-art probe: establishes the mean-field baseline this entry claims to generalize)*
*   `"fiber bundle model" AND "power grid" AND "cascading outage"` *(prior-art probe: nearest known neighbour; confirm it is restricted to equal-load-sharing and does not use a signed anisotropic propagator)*
*   `("Eshelby" OR "amorphous plasticity" OR "yielding transition") AND ("transmission network" OR "power system")` *(direct collision check for the mapping itself)*