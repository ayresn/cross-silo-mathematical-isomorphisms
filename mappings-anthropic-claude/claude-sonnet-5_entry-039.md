---
sid_metadata:
  entry_id: "SID-039"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Claude Sonnet 5"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "chemical-physics-barrier-crossing-kinetics"
  domain_b: "naval-architecture-capsize-risk-assessment"
  structural_family: "noise-induced-escape-from-potential-wells"
  triple_correspondence_vectors:
    - "governing_stochastic_differential_operator"
    - "potential_barrier_escape_instability"
    - "asymptotic_rate_theory_numerical_solution_family"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.0
  vocabulary_divergence_score: 8.5
  expected_methodological_transfer_score: 7.0
  community_separation_score: 8.5
  representation_mismatch_score: 6.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.0
    uncertainty: "±1.8"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "colored_nonstationary_wave_forcing_violates_white_noise_assumption"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 039

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Chemical and statistical physics — Kramers' theory of thermally-activated escape, describing the rate at which a noise-driven particle crosses a potential-energy barrier (reaction kinetics, protein folding, Josephson-junction switching).
*   **Silo B (Field 2):** Naval architecture — stochastic ship stability analysis, specifically the probability that a vessel's roll motion, driven by random wave excitation, escapes the stable equilibrium and crosses the angle of vanishing stability into capsize.
*   **Mathematical Isomorphism:** Both systems reduce to a randomly-forced, damped particle moving in a one-dimensional potential well — the vessel's righting-arm (GZ) curve is exactly the negative gradient of a potential-energy function whose barrier top is the angle of vanishing stability, giving the identical Langevin/Fokker-Planck operator, the identical escape-over-a-barrier instability mechanism, and access to Kramers' closed-form asymptotic rate formula as a candidate replacement for costly rare-event Monte Carlo simulation.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   angle of vanishing stability ↔ barrier top / saddle point (activation locus)
    *   *Operator Role:* Both mark the unstable equilibrium at the top of the governing potential — the point beyond which the restoring force reverses sign and the system is committed to escape (capsize / reaction completion) rather than returning to the stable well.
*   GZ curve (righting arm) ↔ potential gradient −dU/dx (restoring force)
    *   *Operator Role:* Both are the deterministic restoring term in the equation of motion; integrating either with respect to displacement (roll angle vs. reaction coordinate) recovers the potential-energy function whose shape entirely determines the escape rate.
*   probability of capsize (given sea state, exposure time) ↔ Kramers escape rate / mean first-passage time
    *   *Operator Role:* Both are the same object — the rate (or its reciprocal, mean first-passage time) at which a stochastically-forced trajectory first crosses the barrier — computed in naval architecture almost exclusively by simulation, and in chemical physics primarily by closed-form asymptotics.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A's canonical Langevin equation for a particle of mass $m$ in potential $U(x)$, damped by friction $\gamma$ and driven by thermal white noise, is

```math
m\ddot{x} + \gamma\dot{x} + \frac{dU}{dx} = \xi(t), \qquad \langle\xi(t)\xi(t')\rangle = 2\gamma k_B T\,\delta(t-t')
```

In the moderate-to-high-friction (Smoluchowski) limit, Kramers' theory gives a closed-form escape rate over a barrier of height $\Delta U$,

```math
k_{\text{Kramers}} = \frac{\omega_0\,\omega_b}{2\pi\gamma}\exp\left(-\frac{\Delta U}{k_B T}\right)
```

where $\omega_0$ and $\omega_b$ are the curvatures (angular frequencies) of the potential at the well bottom and barrier top respectively.

Silo B's nonlinear roll equation for a vessel of effective inertia $I$ (including added mass), nonlinear damping $b(\dot\phi)$, and righting moment $\Delta\cdot GZ(\phi)$ under wave excitation $M(t)$ is

```math
I\ddot{\phi} + b(\dot{\phi}) + \Delta\cdot GZ(\phi) = M(t)
```

Since $\Delta\cdot GZ(\phi) \equiv dU/d\phi$ for the "stability potential" $U(\phi) = -\Delta\int_0^{\phi} GZ(\phi')\,d\phi'$ — a well with a stable minimum at $\phi=0$ and a barrier top exactly at the angle of vanishing stability — this is the identical equation under $\phi\leftrightarrow x$, $I\leftrightarrow m$, $\Delta\cdot GZ(\phi)\leftrightarrow dU/dx$. Capsize probability over an exposure window is then formally a mean-first-passage-time problem on the same Fokker-Planck equation Kramers solved in closed form — the two curves are the identical trajectory through the same potential-well operator, differing only in what plays the role of the noise term, which is where the analogy's rigor is most exposed to strain (see below).

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Chemical/Statistical Physics (Kramers Escape-Rate Theory) → Naval Architecture (Stochastic Capsize Risk Assessment)
*   **Asymmetric Maturity Rationale:** Kramers' 1940 result and its extensions (Hänggi, Talkner & Borkovec's 1990 synthesis is the standard reference) have been continuously developed and cross-validated across chemistry, biophysics, and condensed-matter physics for over eighty years, including well-worked treatments of non-Markovian and colored-noise forcing. Regulatory-grade stochastic capsize assessment is comparatively young — IMO's Second Generation Intact Stability Criteria (adopted 2020, MSC.1/Circ.1627) still leans heavily on direct time-domain Monte Carlo simulation for its higher-tier vulnerability checks. A related nonlinear-dynamics research niche (Thompson, Rainey, Belenky and others on "erosion of the safe basin" and Melnikov-function escape criteria) already exists and should be treated as partial prior art; the specific closed-form Kramers asymptotic rate formula, as opposed to qualitative safe-basin geometry, does not appear to have been absorbed into standard practice.
*   **Target Bottleneck Mitigation:** Rare-event capsize probabilities (the operationally relevant regime — vessels are designed so capsize is a low-probability tail event) are exactly where Monte Carlo simulation is most expensive, since sample counts must scale with the inverse of the event probability. A Kramers-type closed-form or semi-analytical rate estimate, once the effective potential, damping, and noise intensity are identified from a vessel's GZ curve and sea-state spectrum, would let engineers screen capsize risk across many hull/loading/sea-state combinations at a fraction of the simulation cost, reserving full Monte Carlo for final certification of flagged designs.
*   **Falsifiable Prediction:** For a defined class of vessels and sea states, a Kramers-derived mean-first-passage-time estimate is predicted to converge to within a specified tolerance of long-run Monte Carlo capsize-probability estimates in the weak-noise (low-probability) regime, while requiring orders of magnitude fewer simulated wave realizations to reach the same confidence interval — a claim directly falsifiable by benchmarking against existing IMO SGISS Level 3 direct-simulation datasets.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Kramers rate" AND "ship capsize" AND "mean first passage time"`
*   `"angle of vanishing stability" AND "safe basin erosion" AND "stochastic roll motion"`

## 6. ADDITIONAL NOTE FROM CLAUDE
Two things worth flagging for Stage 2 specifically: the `constitutive_equivalence_confidence: low` isn't boilerplate hedging — the classical Kramers formula assumes stationary white thermal noise, and real ocean wave excitation is neither white nor stationary across a voyage or storm, which is a real gap, not just a formality, and is exactly why `expected_transfer_effort` sits at medium rather than low. And the adjacent "safe basin erosion" literature I cited as partial prior art is a genuine risk to the novelty claim — Stage 2 should check specifically whether anyone in that niche has already invoked the closed-form Kramers rate itself, not just the qualitative escape-geometry picture, before this entry's novelty score is trusted.