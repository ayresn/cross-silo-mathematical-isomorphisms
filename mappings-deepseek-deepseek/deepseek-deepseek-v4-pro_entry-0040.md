---
sid_metadata:
  entry_id: "SID-0040"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "DeepSeek"
  model_family: "DeepSeek"
  model_version: "V4 Pro"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "ostwald-ripening-in-alloys"
  domain_b: "stdp-synaptic-weight-distribution"
  structural_family: "nonlinear-drift-conservation-law-with-reciprocal-cubic-singularity"
  triple_correspondence_vectors:
    - "continuity_operator_with_reciprocal_cubic_drift_v(x)=A x^{-2}(1/x_c-1/x)"
    - "global_mass_conservation_integral_constraint"
    - "self_similar_scaling_solution_with_universal_truncated_power_law_tail"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 9.2
  vocabulary_divergence_score: 9.8
  expected_methodological_transfer_score: 8.7
  community_separation_score: 9.5
  representation_mismatch_score: 8.9
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±0.9"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "constitutive_law_mismatch_if_synaptic_drift_not_purely_deterministic"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0040

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Ostwald ripening of precipitates in a dilute solid solution; the asymptotic coarsening of a polydisperse ensemble of particles driven by the Gibbs–Thomson boundary condition and volume‑diffusion‑limited mass transport, described by the Lifshitz–Slyozov–Wagner (LSW) mean‑field theory.
*   **Silo B (Field 2):** Mean‑field dynamics of the distribution of synaptic weights under spike‑timing‑dependent plasticity (STDP) with hard bounds and a learning rule that generates a critical weight separating potentiation and depression, leading to a continuity equation for the weight probability density.
*   **Mathematical Isomorphism:** Under the transformation \(u = 1/(w_{\max} - w)\) the STDP‑governed probability density evolves according to exactly the same non‑dimensional continuity operator \(\partial_t + \partial_x\big[\,(A/x^2)(1/x_c - 1/x)\,\cdot\,\big]\) as the LSW particle‑radius distribution, exhibiting identical global mass conservation, the same self‑similar scaling solution with a universal truncated power‑law tail, and the same singular behaviour at the critical size when the drift vanishes.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Precipitate radius \(R\)** ↔ **Inverse synaptic margin \(u = 1/(w_{\max} - w)\)**
    *   *Operator Role:* Both enter the drift field \(v(x) = (A/x^2)(1/x_c - 1/x)\) of the advection operator \(\partial_t + \partial_x(v\,\cdot)\). \(x\) stands for \(R\) in LSW and for \(u\) in STDP after the transformation.
*   **Critical radius \(R_c\) (or dimensionless \(\rho = R/R_c\))** ↔ **Critical inverse margin \(u_c\)**
    *   *Operator Role:* The sign‑change point of the drift velocity; growth for \(x < x_c\) and shrinkage for \(x > x_c\). In both systems this separatrix governs the flux towards or away from the stable fixed point of the deterministic dynamics.
*   **Gibbs–Thomson interfacial concentration shift \(\Delta c \propto 2\gamma\Omega/(k_B T R)\)** ↔ **Potentiation‑depression threshold drift \(\mu(w) \propto (w - w_0)(w_{\max} - w)\)**
    *   *Operator Role:* Both determine the functional form of the drift after the appropriate change of variable. The interfacial energy \(\gamma\) maps to the plasticity asymmetry parameter \(\alpha\), and the diffusion coefficient maps to the learning rate.
*   **Total number of particles \(N = \int n\,dR\)** ↔ **Total number of synapses \(M = \int \rho\,dw\)**
    *   *Operator Role:* A conserved global scalar invariant under the evolution of the respective continuity equations, formally \(\frac{d}{dt}\int_0^\infty \phi\,dx = 0\) for both systems because the flux vanishes at the boundaries (compact support for \(w\) and zero flux at \(R\to\infty\) for LSW).

## 3. CORE MATHEMATICAL PARALLELISM
In Ostwald ripening, the density‑weighted particle size distribution \(n(R,t)\) evolves by the continuity equation
```math
\frac{\partial n}{\partial t} + \frac{\partial}{\partial R}\!\left[ \frac{D\sigma}{R^2}\!\left(\frac{1}{R_c} - \frac{1}{R}\right) n \right] = 0,
\qquad R_c(t) = \frac{1}{N}\int_0^\infty R\,n(R,t)\,dR.
```
where \(D\) is the solute diffusivity, \(\sigma\) the surface tension, and the Gibbs–Thomson relation sets the critical radius \(R_c\) equal to the number‑average radius. After the standard non‑dimensionalisation \(x = R/R_c\), \(\tau = t/t_0\) with \(t_0 = R_c^4/(D\sigma)\), the equation becomes parameter‑free:
```math
\frac{\partial f}{\partial\tau} + \frac{\partial}{\partial x}\!\left[ \frac{1}{x^2}\!\left(1 - \frac{1}{x}\right) f \right] = 0,
\qquad \int_0^{3/2} x\,f(x,\tau)\,dx = 1 .
```
The drift vanishes at \(x=1\) (the critical size) and at \(x\to\infty\); the support of the asymptotic distribution is strictly bounded by \(x=3/2\).

In the STDP mean‑field model, the evolution of the synaptic weight density \(P(w,t)\) follows the Fokker–Planck equation
```math
\frac{\partial P}{\partial t} = -\frac{\partial}{\partial w}\!\big[ \mu(w) P \big] + \frac{\partial^2}{\partial w^2}\!\big[ D(w) P \big],
\qquad w \in [w_{\min}, w_{\max}].
```
For a purely additive STDP rule with hard bounds and a symmetric temporal window, the deterministic drift can be written \(\mu(w) = \alpha (w - w_0)(w_{\max} - w)\). In the noiseless limit (\(D(w)\to 0\)) and under the transformation \(u = 1/(w_{\max} - w)\), the density \(\tilde{P}(u,t) = P(w(u),t)\,|dw/du|\) satisfies the closed continuity equation
```math
\frac{\partial \tilde{P}}{\partial t} + \frac{\partial}{\partial u}\!\left[ \frac{\alpha\,(w_{\max}-w_0)}{u^2}\!\left(\frac{1}{u_c} - \frac{1}{u}\right) \tilde{P} \right] = 0,
\qquad u_c = \frac{1}{w_{\max}-w_0}.
```
Scaling time by \(t_0 = u_c^4/[\alpha(w_{\max}-w_0)]\) and length by \(u_c\) yields the identical dimensionless operator
```math
\frac{\partial F}{\partial \tau} + \frac{\partial}{\partial \xi}\!\left[ \frac{1}{\xi^2}\!\left(1 - \frac{1}{\xi}\right) F \right] = 0,
\qquad F(\xi,\tau) = u_c\,\tilde{P}(u_c\xi,\tau).
```
Thus the two systems are governed by the same non‑canonical, first‑order hyperbolic conservation law whose drift has a reciprocal cubic singularity at the origin and a linear zero at the critical point. The correspondence is exact on the operator level; the diffusion term in the original STDP equation is a higher‑order perturbation that maps to a small Laplacian‑like regularisation in the LSW picture, but the conservative backbone is structurally identical.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Ostwald Ripening (Materials Science) → Mean‑Field STDP Theory (Computational Neuroscience)
*   **Asymmetric Maturity Rationale:** The LSW community has developed a highly refined set of analytical and numerical tools for solving singular drift‑continuity equations: rigorous self‑similar asymptotic analysis, the method of matched asymptotic expansions for the depletion zone at the critical point, proven convergence to the universal distribution via a maximum principle, and efficient flux‑limited finite‑volume schemes that preserve the cutoff without spurious oscillations. While computational neuroscience possesses advanced spike‑train statistics and biophysical plasticity models, the specific problem of solving a non‑linear, first‑order hyperbolic equation with a singular drift and a moving critical point is routinely handled only by ad hoc Gaussian approximations or Monte Carlo simulations; the target field currently lacks dedicated, fast, and provably mass‑conserving algorithms for this operator class.
*   **Target Bottleneck Mitigation:** We hypothesise that directly importing the LSW flux‑corrected transport algorithm (a semi‑implicit scheme with the LSW exact equilibrium solution as the limiter basis) into the numerical integration of the large‑scale STDP‑Fokker‑Planck equation will reduce the computational cost of evaluating long‑time synaptic weight distributions by at least two orders of magnitude compared to current forward Euler Monte Carlo benchmarks, while simultaneously guaranteeing non‑negativity and exact conservation of the total synapse count.
*   **Falsifiable Prediction:** When applied to a network of \(N=10^5\) excitatory synapses undergoing a standard symmetric STDP protocol (\(w_{\max}=1\), \(w_0=0.5\), \(\alpha=0.01\) s⁻¹) that is numerically integrated for the equivalent LSW long time \(\tau = 10^3\) (corresponding to \(t \approx 10^5\) seconds of biological time under the given scaling), the imported LSW solver will produce a steady‑state weight distribution whose tail for \(w>0.9\) deviates from the best‑fit Gaussian distribution by a Kolmogorov–Smirnov statistic \(D > 0.15\) and instead follows the predicted LSW universal tail form \(F(\xi) \propto \xi^{-3} \exp[-1/(1-\xi)]\) for \(1<\xi<3/2\) with a reduced chi‑square \(\chi^2_\nu < 1.5\) when binned in 100 bins. The comparison baseline is the state‑of‑the‑art Monte Carlo simulation (10⁸ independent realisations) of the identical STDP rule, which currently reports an exponential weight distribution with an effective thermal noise. If the LSW solver fails to produce a sharper cutoff than the exponential tail at the 95% confidence level, or if the simulated distribution under the same STDP rule (with realistic shot‑noise variance \(\sigma^2 = 10^{-3}\)) yields a KS distance \(D < 0.10\) from a Gaussian, the isomorphism is falsified.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Lifshitz-Slyozov-Wagner" AND "continuity equation" AND "self-similar distribution" AND "coarsening"`
*   `"STDP" AND "Fokker-Planck" AND "synaptic weight distribution" AND "mean-field"`
*   `"LSW equation" AND "neural" OR "synaptic plasticity" AND "universal distribution"`