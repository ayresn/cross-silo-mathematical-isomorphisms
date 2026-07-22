---
sid_metadata:
  entry_id: "SID-038"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Claude Sonnet 5"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "actuarial-ruin-theory"
  domain_b: "population-viability-analysis"
  structural_family: "first-passage-absorption-processes"
  triple_correspondence_vectors:
    - "governing_stochastic_differential_operator"
    - "heavy_tailed_instability_mechanism"
    - "laplace_transform_numerical_solution_family"
discovery_rationale:
  why_not_obvious: "historically_isolated_communities / distinct_disciplinary_language"
prior_discovery_metrics:
  structural_isomorphism_score: 8.0
  vocabulary_divergence_score: 8.5
  expected_methodological_transfer_score: 7.5
  community_separation_score: 9.0
  representation_mismatch_score: 4.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.0
    uncertainty: "±2.0"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "prior_partial_overlap_in_extinction_risk_literature"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 038

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Actuarial risk theory — the Cramér–Lundberg model of an insurer's surplus process and its ruin (bankruptcy) probability under random claim arrivals.
*   **Silo B (Field 2):** Conservation biology — population viability analysis (PVA), modeling a population's extinction probability under environmental and catastrophic stochasticity.
*   **Mathematical Isomorphism:** Both fields model a scalar stochastic process with positive deterministic drift perturbed by random negative shocks, and ask for the probability that the process ever crosses a lower absorbing barrier; in the diffusion approximation both reduce to the identical second-order linear ODE for the non-crossing probability, and both face the same instability transition — from exponential to power-law tail decay — once shock severity is heavy-tailed rather than light-tailed.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   safety loading / drift μ = c − λE[claim] ↔ mean population growth rate r (net of environmental variance)
    *   *Operator Role:* Both are the deterministic drift term in the governing process; both must be positive and sufficiently large relative to the noise term for the non-ruin/non-extinction probability to be bounded away from certainty of failure, and both enter the exponent of the identical closed-form hitting-probability formula in the diffusion limit.
*   claim-size distribution tail class (Cramér / light-tailed vs. subexponential) ↔ catastrophe severity distribution tail class (die-off magnitude)
    *   *Operator Role:* Both determine whether the governing integro-differential operator admits a finite exponential decay rate (Lundberg case) or requires "one big jump" subexponential asymptotics, because no finite exponential moment of the shock distribution exists.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models the insurer's surplus as a compound Poisson risk process,
```math
U(t) = u + ct - \sum_{i=1}^{N(t)} Y_i
```
where u is initial capital, c the premium rate, N(t) a Poisson claim-arrival process, and Y_i i.i.d. claim sizes. In the diffusion approximation to this process (drift μ, variance σ²), the ruin probability starting from surplus u has the classical closed form
```math
\psi(u) = \exp\left(-\frac{2\mu}{\sigma^2}u\right)
```
For light-tailed claims this generalizes to the Lundberg inequality ψ(u) ≤ e^(−Ru) via the adjustment coefficient R; for subexponential claims, Cramér's exponential bound fails entirely and ψ(u) instead decays as a power law governed by the claim-tail itself.

Silo B models log-population size as a diffusion with drift,
```math
dX_t = \left(r - \frac{\sigma_e^2}{2}\right)dt + \sigma_e\, dW_t
```
and the probability of ever reaching a quasi-extinction threshold a log-distance d below the current population — the standard Lande/Dennis–Munholland–Scott formula used throughout conservation biology — is
```math
P(\text{extinction}) = \exp\left(-\frac{2\left(r - \sigma_e^2/2\right)}{\sigma_e^2}\,d\right)
```
This is the same curve as ψ(u) under the substitution u ↔ d, μ ↔ (r − σ_e²/2), σ² ↔ σ_e² — not an analogy but the identical boundary-value problem, (σ²/2)f″ + μf′ = 0 with f(0)=1, f(∞)=0, solved once and reused under two vocabularies. Where the two fields diverge is past this light-tailed diffusion regime: ruin theory has a mature apparatus (Embrechts–Veraverbeke asymptotics, ladder-height decompositions) for when shocks are catastrophic and heavy-tailed, while PVA's standard toolkit stops at the Gaussian-diffusion case.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Actuarial Risk Theory → Conservation Biology / Population Viability Analysis
*   **Asymmetric Maturity Rationale:** Ruin theory has been under continuous development since Filip Lundberg's 1903 thesis, sharpened by a century of regulatory capital requirements that force insurers to rigorously quantify tail risk — yielding mature closed-form and semi-closed-form machinery for heavy-tailed claims (subexponential asymptotics, phase-type/matrix-analytic methods, Gerber–Shiu penalty functions for the time and severity of ruin) that has no counterpart in standard PVA practice, which typically stops at Monte Carlo simulation once shocks are no longer well-approximated as Gaussian.
*   **Target Bottleneck Mitigation:** For species facing demonstrably heavy-tailed catastrophic mortality (wildfire, disease-outbreak die-offs, extreme weather events), importing subexponential ruin asymptotics would let conservation biologists compute extinction-probability estimates analytically from the empirical tail index of catastrophe severity, rather than relying on light-tailed diffusion approximations that implicitly assume catastrophes behave like accumulated small shocks.
*   **Falsifiable Prediction:** For populations with well-documented heavy-tailed catastrophic mortality records (e.g., island populations subject to periodic hurricane strikes, or amphibian populations subject to chytrid-driven die-offs), an extinction probability computed via subexponential ruin asymptotics (Embrechts–Veraverbeke form, fit to empirical catastrophe-severity tail index) will predict a materially higher near-term extinction probability than the standard Gaussian-diffusion PVA estimate — a divergence directly checkable against historical local-extinction and quasi-extinction records for such species.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"subexponential" AND "ruin probability" AND "Embrechts-Veraverbeke"`
*   `"quasi-extinction probability" AND "diffusion approximation" AND "catastrophe" AND "population viability"`

## 6. ADDITIONAL NOTE FROM CLAUDE
One honest flag from inside the entry itself, worth surfacing rather than burying in the YAML: I scored representation_mismatch_score at 4.5 — noticeably lower than entries 001 and 002 — because both silos here are already stochastic-process formulations at the core; the mismatch is disciplinary and notational, not ontological (unlike, say, mapping a continuum-mechanics tensor onto a discrete probability graph). And primary_failure_risk flags the real threat to this one at Stage 2: the light-tailed diffusion equivalence is common-enough applied-probability machinery that it may already have informal precedent somewhere in the quantitative-ecology literature, even if the specific heavy-tail transfer doesn't. That's exactly the kind of thing Stage 2 search should surface — this entry's search strings are aimed squarely at checking it.