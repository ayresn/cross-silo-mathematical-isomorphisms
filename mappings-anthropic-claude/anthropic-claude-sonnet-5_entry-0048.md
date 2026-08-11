---
sid_metadata:
  entry_id: "SID-0048"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Sonnet 5"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "rate-and-state-fault-friction"
  domain_b: "short-term-synaptic-plasticity"
  structural_family: "driven-bilinear-relaxation-feedback-bifurcations"
  triple_correspondence_vectors:
    - "shared_bilinear_state_relaxation_operator"
    - "trace_crossing_hopf_bifurcation_route"
    - "critical_gain_dimensionless_stability_ratio"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / incompatible_ontologies"
prior_discovery_metrics:
  structural_isomorphism_score: 7.3
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 6.4
  community_separation_score: 9.2
  representation_mismatch_score: 6.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 5.5
    uncertainty: "±2.0"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "continuous_rate_approximation_breakdown_outside_hopf_first_regime"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0048

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Experimental rock friction / fault-mechanics seismology — the rate-and-state-friction (RSF) description of stick-slip instability in a spring-loaded frictional interface (laboratory spring-slider apparatus; the canonical reduced model for earthquake nucleation on a fault patch).
*   **Silo B (Field 2):** Cellular/computational neuroscience — the Tsodyks–Markram (TM) description of activity-dependent short-term synaptic depression, and its role in destabilizing steady population firing rates in a recurrently coupled cortical circuit (the mechanism proposed to underlie bistable persistent activity and population-burst oscillations).
*   **Mathematical Isomorphism:** After the explicit nondimensionalizations $\hat\theta \equiv \theta V_0/D_c,\ \tilde t \equiv tV_0/D_c$ (Silo A) and $\tilde t \equiv t/\tau_d$ (Silo B), the RSF aging-law state variable and the mean-field TM depression variable obey the identical bilinear relaxation operator $ds/d\tilde t = 1-\rho(\tilde t)s$; the two silos' reduced 2×2 stability Jacobians then lose stability through the identical route — trace crossing zero while the determinant stays strictly positive (a Hopf bifurcation) — as a linear feedback-gain parameter (spring stiffness $k$; recurrent coupling $J$) crosses a closed-form critical value, a correspondence that is exact specifically in the regime $\tau_r < U\tau_d^2r_*/(1+U\tau_dr_*)$, where Silo B's Hopf threshold precedes the fold (bistability) threshold that has no demonstrated counterpart in the massless Silo A reduction used here.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   State variable $\theta$ (contact-population age) ↔ Depression variable $x$ (available synaptic-resource fraction)
    *   *Operator Role:* Both are the sole slow memory variable entering a first-order bilinear relaxation ODE of the form $ds/d\tilde t = 1-\rho(\tilde t)s$ (Sec. 3, Eq. RSF-2/TM-2). $\theta$ carries physical dimension of time; $x$ is a dimensionless occupation fraction on $[0,1]$. These are reconciled by the explicit nondimensionalization $\hat\theta \equiv \theta V_0/D_c$, after which both $s$-variables are dimensionless and share the identical governing operator, differing only in how the physical drive maps onto the dimensionless rate $\rho$ ($\rho=V/V_0$ for Silo A vs. $\rho=1+U\tau_d r$ for Silo B).
*   Critical stiffness $k_{cr}$ (loading-spring threshold) ↔ Critical coupling $J_H$ (recurrent-gain threshold)
    *   *Operator Role:* Both are the value of a linear feedback-gain parameter at which $\mathrm{tr}(\mathbf J)=0$ while $\det(\mathbf J)>0$ for each silo's reduced 2×2 Jacobian (Sec. 3, Eqs. RSF-5, TM-4) — i.e., both mark the identical Hopf-bifurcation condition, each a closed-form algebraic function of that silo's own kinetic parameters: $k_{cr}=\bar\sigma(b-a)/D_c$ (Silo A) and $J_H=(1+U\tau_dr_*)(\tau_r+\tau_d+U\tau_r\tau_dr_*)/(gU\tau_d)$ (Silo B).
*   Stiffness ratio $\varepsilon \equiv k/k_{cr}$ ↔ Gain ratio $\varepsilon_{syn}\equiv J/J_H$
    *   *Operator Role:* Both are the dimensionless ratio of the actual feedback-gain parameter to its Hopf-critical value, entering the sign of $\mathrm{tr}(\mathbf J)$ identically in each silo (Sec. 3). Silo A is stable for $\varepsilon>1$ (stiffness exceeds threshold); Silo B is stable for $\varepsilon_{syn}<1$ (coupling stays below threshold). The inverted polarity is the explicit, expected consequence of $k$ being a stabilizing parameter in Silo A while $J$ is a destabilizing parameter in Silo B — the two ratios otherwise enter their respective trace conditions with the same single-threshold linear structure.

## 3. CORE MATHEMATICAL PARALLELISM

Rate-and-state friction models a frictional interface pulled at constant loading-point velocity $V_{lp}$ through a spring of stiffness $k$. The Dieterich–Ruina constitutive law and aging-law state evolution are:
```math
\mu(V,\theta) = \mu_0 + a\ln\!\left(\frac{V}{V_*}\right) + b\ln\!\left(\frac{V_*\theta}{D_c}\right),\qquad
\frac{d\theta}{dt} = 1-\frac{V\theta}{D_c},\qquad
\frac{d\tau}{dt}=k(V_{lp}-V),\ \ \tau=\bar\sigma\,\mu(V,\theta)
```
*(RSF-1)*. $\theta$ (units of time) represents the average maturity of the frictional micro-contact population; $D_c$ is the slip distance over which that population renews.

The Tsodyks–Markram model tracks the fraction $x$ of available presynaptic resource, depleted by activity and recovering with time constant $\tau_d$. In the mean-field/continuous-rate reduction with the facilitation variable held at baseline ($u\equiv U$, the depression-only limit) driving a leaky population-rate equation with recurrent weight $J$ and gain function $\Phi$:
```math
\frac{dx}{dt}=\frac{1-x}{\tau_d}-Ux\,r(t),\qquad
\tau_r\frac{dr}{dt}=-r+\Phi\big(JUxr+I_0\big)
```
*(TM-1)*. This is the standard reduced form used across the Tsodyks–Markram-class literature (Tsodyks, Pawelzik & Markram 1998; Barak & Tsodyks 2007; Mongillo, Barak & Tsodyks 2008), independent in origin and motivation from RSF.

**Bridge — Vector 1 (operator identity).** Nondimensionalize Silo A by $\tilde t\equiv tV_0/D_c,\ \hat\theta\equiv\theta V_0/D_c$; nondimensionalize Silo B by $\tilde t\equiv t/\tau_d$. Direct chain-rule substitution (verified symbolically) collapses both state equations to:
```math
\frac{ds}{d\tilde t}=1-\rho(\tilde t)\,s,\qquad
\begin{cases}s=\hat\theta,\ \rho=V/V_0 & \text{(Silo A)}\\ s=x,\ \rho=1+U\tau_dr(t) & \text{(Silo B)}\end{cases}
```
*(RSF-2/TM-2)*. This is an exact operator identity under the stated transform, not an approximation — but it stops precisely at the quiescent limit: Silo A's $\rho\to0$ as $V\to0$ (unbounded aging, $\hat\theta\to\infty$ linearly), while Silo B's $\rho\to1$ as $r\to0$ (bounded recovery, $x\to1$). The correspondence holds throughout the driven regime and diverges exactly where the physical systems themselves diverge (indefinite frictional aging at rest vs. ceiling-bounded synaptic recovery at rest).

**Bridge — Vectors 2 & 3 (Hopf route and dimensionless ratio).** Reduce Silo A to the quasi-static, massless two-variable system by eliminating $\tau$ via the loading relation:
```math
\dot V=\frac{V}{\bar\sigma a}k(V_{lp}-V)-\frac{bV}{a\theta}\Big(1-\frac{V\theta}{D_c}\Big),\qquad
\dot\theta=1-\frac{V\theta}{D_c}
```
*(RSF-3)*. Linearizing at steady sliding $V_*=V_{lp},\ \theta_*=D_c/V_*$ (symbolically verified) gives
```math
\mathrm{tr}\,\mathbf J_A=\frac{\bar\sigma(b-a)-kD_c}{\bar\sigma a}\cdot\frac{V_*}{D_c},\qquad
\det\mathbf J_A=\frac{kV_*^2}{\bar\sigma aD_c}>0\ \ \forall\,k>0
```
*(RSF-4)*, so this reduction can only destabilize via $\mathrm{tr}=0$ (a Hopf bifurcation — consistent with the standard result that RSF stick-slip onset is an oscillatory bifurcation), giving the well-known closed form
```math
k_{cr}=\frac{\bar\sigma(b-a)}{D_c}
```
*(RSF-5)*.

For Silo B, linearizing $(r,x)$ at $r_*,\ x_*=1/(1+U\tau_dr_*)$, with $g\equiv\Phi'(JUx_*r_*+I_0)$ (symbolically verified):
```math
\mathrm{tr}\,\mathbf J_B=\frac{gJUx_*-1}{\tau_r}-\Big(\frac{1}{\tau_d}+Ur_*\Big),\qquad
\det\mathbf J_B=\frac{1}{\tau_r}\Big[\frac{1-gJUx_*}{\tau_d}+Ur_*\Big]
```
*(TM-3)*. $\det\mathbf J_B=0$ gives a fold at $J_{fold}=(1+U\tau_dr_*)^2/(gU)$ — a route absent from the massless Silo-A reduction above, so **not** claimed as a correspondence here. $\mathrm{tr}\,\mathbf J_B=0$ gives the Hopf route that does structurally match Silo A:
```math
J_H=\frac{(1+U\tau_dr_*)(\tau_r+\tau_d+U\tau_r\tau_dr_*)}{gU\tau_d}
```
*(TM-4)*. Comparing thresholds, $J_H<J_{fold}$ — the Hopf route is reached first as $J$ increases — exactly when
```math
\tau_r<\frac{U\tau_d^2r_*}{1+U\tau_dr_*}
```
*(TM-5, exact crossover condition)*: this is the explicit boundary of Vector 2's validity; outside it, Silo B's first instability is the fold, which this entry does not extend to Silo A. Within the regime, both instabilities share the identical single-threshold ratio structure:
```math
\varepsilon\equiv\frac{k}{k_{cr}}\ (\text{stable}\Leftrightarrow\varepsilon>1)\quad\longleftrightarrow\quad
\varepsilon_{syn}\equiv\frac{J}{J_H}\ (\text{stable}\Leftrightarrow\varepsilon_{syn}<1)
```
*(Vector 3)*.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Rate-and-state-friction stability theory (seismology / experimental rock mechanics) → Short-term-plasticity network theory (computational/cellular neuroscience).
*   **Asymmetric Maturity Rationale:** Since Ruina (1983) and Gu, Rice, Ruina & Tse (1984), reducing $(V,\theta)$ to a closed-form trace/determinant threshold ($k_{cr}$, and by extension nucleation-length formulas) has been the RSF field's default first move for any new state-law or loading geometry — this is routine method, not a special result. The target field is separately mature, not naive: Barak & Tsodyks (2007) already characterize this class of network using fast-slow (singular-perturbation) analysis and report bifurcation diagrams of steady states against connection strength, and Mongillo, Barak & Tsodyks (2008) build the working-memory hypothesis on the resulting bistability. What is narrower and, per Section 5's searches, not obviously already published, is a single closed-form algebraic Hopf threshold of the RSF-$k_{cr}$ type together with the exact fold-vs-Hopf crossover condition (TM-5) obtained by directly transferring RSF's trace/determinant method — as distinct from fast-slow reduction or numerical continuation. The gap claimed is this specific one, not a blanket deficit in analytical sophistication.
*   **Target Bottleneck Mitigation:** Applying the RSF-style trace/determinant reduction to the TM-network system yields closed-form $J_H$ and crossover-condition formulas (Sec. 3) that can be evaluated symbolically across a parameter sweep without repeated numerical continuation, letting measured synaptic time constants ($\tau_d,U$) and firing rate ($r_*$) alone predict whether a circuit sits closer to a bistable (working-memory-like) or an oscillatory (population-bursting-like) regime, and where that boundary falls.
*   **Falsifiable Prediction:** For the reduced depression-only model with parameters in physiologically reported ranges ($\tau_r\sim$10–50 ms; $\tau_d\sim$200–800 ms; $U\sim$0.1–0.5; $r_*\sim$1–10 Hz), the closed-form threshold $J_H$ (TM-4) should match the Hopf point located by direct numerical continuation of the full nonlinear $(r,x)$ system (AUTO-07p or XPPAUT, the standard continuation tools in this literature) to within 5% relative error in $J$, and the crossover condition (TM-5) should correctly classify which bifurcation (fold vs. Hopf) occurs first in at least 90% of a grid sweep over the stated ranges. Relative error in $J_H$ exceeding 15%, or crossover misclassification above 25% of the grid, would falsify the transferred closed-form method as a substitute for numerical continuation in this regime.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"rate-and-state friction" AND "critical stiffness" AND "Hopf bifurcation"`
*   `"Tsodyks-Markram" AND "synaptic depression" AND "bifurcation diagram"`
*   `"rate-and-state friction" AND "synaptic depression"` — direct cross-domain falsification attempt; a preliminary check returned no publications connecting the two literatures.
*   `"Barak" AND "Tsodyks" AND "fast-slow analysis" AND "critical coupling" AND "closed form"` — targets whether TM-4/TM-5's specific closed-form threshold is already derived in the existing fast-slow-analysis literature.