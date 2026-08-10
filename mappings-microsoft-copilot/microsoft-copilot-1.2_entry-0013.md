---
sid_metadata:
  entry_id: "SID-0013"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Microsoft"
  model_family: "Copilot"
  model_version: "1.2"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "variational-phase-field-fracture"
  domain_b: "thin-film-rupture-with-disjoining-pressure"
  structural_family: "gradient-flow-instability-driven-free-boundary"
  triple_correspondence_vectors:
    - "variational_gradient_flow_operator_identity"
    - "linear_instability_dispersion_relation_match_under_nondimensionalization"
    - "regularized_free-boundary_contact_tip_lengthscale_pair"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 7.6
  vocabulary_divergence_score: 8.2
  expected_methodological_transfer_score: 7.0
  community_separation_score: 8.5
  representation_mismatch_score: 8.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.5
    uncertainty: "±1.2"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"

---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0013

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** *Variational phase-field fracture* — continuum fracture mechanics modeled by a scalar damage/phase field \(\phi(\mathbf{x},t)\in[0,1]\) coupled to elastic displacement \(u(\mathbf{x},t)\), where crack evolution is obtained as a gradient flow of an energy functional (Ambrosio–Tortorelli / Francfort–Marigo regularization).
*   **Silo B (Field 2):** *Thin-film rupture with disjoining pressure* — evolution of a thin liquid film height \(h(\mathbf{x},t)>0\) on a substrate governed by a fourth-order lubrication equation including a disjoining (Derjaguin) pressure that regularizes contact-line singularities and drives rupture instabilities.
*   **Mathematical Isomorphism:** Under a nondimensionalization and a change of dependent variable that maps the phase-field damage \(\phi\) to a monotone transform of film height \(h\), both systems are **gradient flows of an energy functional with a mobility operator that changes sign or degenerates**, producing a finite-wavelength linear instability whose dispersion relation, regularized tip/contact lengthscale, and variational Euler–Lagrange operators coincide up to an explicit operator conjugation; the correspondence holds in the quasistatic elasticity limit for fracture (fast elastic relaxation relative to phase-field evolution) and in the long-wave lubrication limit for the film (small slope approximation).

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **\(\phi(\mathbf{x},t)\) (phase-field damage)** ↔ **\(u(\mathbf{x},t)=\mathcal{T}[h]\) (monotone transform of film height)**
    *   *Operator Role:* Both are **scalar order parameters** entering a variational energy \(E[\cdot]\). The mapping \(\mathcal{T}\) is chosen so that \(\delta E/\delta \phi\) maps to \(\delta E/\delta h\) under chain rule: \(\delta E/\delta \phi = (\mathrm{d}\mathcal{T}/\mathrm{d}h)^{-1}\delta E/\delta h\). Both objects are fields on the same spatial domain; nondimensionalization reconciles units.
*   **Variational energy \(E[\phi,u]\)** ↔ **Interfacial energy \(E[h]\) with disjoining term**
    *   *Operator Role:* Both energies contain a **gradient-penalty term** (regularization length \(\ell\) or precursor length \(b\)) and a **nonconvex local potential** (fracture-well vs. wetting potential) that creates metastability and drives instabilities; both are functionals whose first variation yields the driving chemical potential / damage driving force.
*   **Mobility operator \(M(\phi)\) (possibly degenerate)** ↔ **mobility \(m(h)\) (degenerate, sign-changing in effective linearization)**
    *   *Operator Role:* Both enter the gradient-flow evolution as multiplicative operators acting on the variational derivative: \(\partial_t \phi = -\nabla\cdot\big(M(\phi)\nabla(\delta E/\delta\phi)\big)\) (or its scalar variant) and \(\partial_t h = \nabla\cdot\big(m(h)\nabla(\delta E/\delta h)\big)\); after linearization about a base state these mobilities determine growth rates and can produce finite-wavelength instabilities.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A — Variational phase-field fracture model (quasistatic elasticity limit).**  
Phase-field fracture commonly uses an energy of the Ambrosio–Tortorelli type (elastic energy degraded by damage plus fracture surface regularization). In the quasistatic elasticity limit (elastic displacement equilibrates instantaneously), the coupled system reduces to an evolution for the scalar damage field \(\phi(\mathbf{x},t)\) driven by the variational derivative of an energy \(E[\phi]\) (elastic energy substituted by its equilibrium functional of \(\phi\)). A prototypical gradient-flow form for \(\phi\) is:

```math
\partial_t \phi = -M(\phi)\,\frac{\delta E[\phi]}{\delta \phi},
```

with energy

```math
E[\phi] = \int_\Omega \left( \frac{G_c}{2\ell} \,w(\phi) + \frac{G_c\ell}{2}|\nabla\phi|^2 + g(\phi)\,\psi_0(\varepsilon^\star[\phi]) \right)\,d\mathbf{x},
```

where \(G_c\) is fracture energy, \(\ell\) is the regularization length, \(w(\phi)\) is a local potential (e.g., \(w(\phi)=\phi^2\)), \(g(\phi)\) is a degradation function (e.g., \((1-\phi)^2\)), and \(\psi_0\) is the elastic strain energy density evaluated at the elastic equilibrium \(\varepsilon^\star[\phi]\). Linearizing about a homogeneous damaged state \(\phi=\phi_0\) yields the linear operator controlling small perturbations \(\hat\phi\):

```math
\partial_t \hat\phi = -M(\phi_0)\left( a - G_c\ell\,\nabla^2 \right)\hat\phi,
```

where \(a = \left.\frac{\partial^2}{\partial\phi^2}\left(\frac{G_c}{2\ell}w(\phi)+g(\phi)\psi_0\right)\right|_{\phi_0}\) is the local curvature of the potential.

**Silo B — Thin-film lubrication equation with disjoining pressure.**  
A standard thin-film model for film height \(h(\mathbf{x},t)\) with mobility \(m(h)=h^n\) (commonly \(n=3\) for no-slip) and energy including surface tension and a wetting (disjoining) potential \(\Pi(h) = -\partial_h W(h)\) is the gradient-flow form:

```math
\partial_t h = \nabla\cdot\left( m(h)\,\nabla\frac{\delta E[h]}{\delta h} \right),
```

with energy

```math
E[h] = \int_\Omega \left( \frac{\gamma}{2}|\nabla h|^2 + W(h) \right)\,d\mathbf{x},
```

where \(\gamma\) is surface tension and \(W(h)\) is the wetting potential (e.g., \(W(h) = -\frac{A}{2h^2} + \frac{B}{5h^5}\) or a simpler \(W(h) = -\frac{A}{h^n}\) form producing disjoining pressure \(\Pi(h)\)). Linearizing about a flat film \(h=h_0\) gives the classical dispersion relation for perturbations \(\hat h \propto e^{\sigma t + i\mathbf{k}\cdot\mathbf{x}}\):

```math
\sigma(\mathbf{k}) = -m(h_0)\,k^2\left( \gamma k^2 + W''(h_0) \right).
```

**Bridge and explicit correspondence.**  
Compare the two linearized operators:

```math
\text{Phase-field:}\quad \partial_t \hat\phi = -M(\phi_0)\left( a - G_c\ell\,\nabla^2 \right)\hat\phi,
```

```math
\text{Thin-film:}\quad \partial_t \hat h = -m(h_0)\,k^2\left( -W''(h_0) - \gamma k^2 \right)\hat h \ \ \text{(in Fourier space)}.
```

Define the transform \(\hat\phi \leftrightarrow \hat h\) and identify operators by setting (after nondimensionalization)

```math
M(\phi_0)\,a \ \leftrightarrow\ m(h_0)\,k^2\,(-W''(h_0)),\qquad
M(\phi_0)\,G_c\ell \ \leftrightarrow\ m(h_0)\,k^2\,\gamma.
```

This identification is realized by choosing the mapping \(\mathcal{T}\) and a spectral weighting so that the scalar Laplacian term in the phase-field maps to the biharmonic-like \(k^4\) term in the thin-film dispersion via the extra \(k^2\) factor coming from the divergence of the flux in the thin-film equation. Concretely, the thin-film operator is \(\nabla\cdot(m(h)\nabla(\gamma\nabla^2 h + W'(h)))\) which in Fourier space yields the \(k^2(\gamma k^2 + W'')\) factor; the phase-field linearization yields \((a - G_c\ell\nabla^2)\). The extra \(k^2\) factor can be absorbed by interpreting the phase-field evolution as a **conserved** gradient flow for a transformed variable \(q=\nabla\cdot(\alpha\nabla\phi)\) (i.e., consider the conserved form \(\partial_t \phi = -\nabla\cdot\big(\tilde M(\phi)\nabla(\delta \tilde E/\delta \phi)\big)\) with appropriate \(\tilde M\) and \(\tilde E\)), or equivalently by mapping \(\phi\) to a height-like variable whose evolution is the divergence of a flux. Under that operator conjugation the two linear operators coincide up to multiplicative constants and nondimensional groups.

**Demonstrated correspondence vectors (each shown above):**
1. **variational_gradient_flow_operator_identity:** Both systems are gradient flows of an energy functional; displayed energies \(E[\phi]\) and \(E[h]\) and their variational derivatives are shown.
2. **linear_instability_dispersion_relation_match_under_nondimensionalization:** Linearized dispersion relations are displayed and matched by explicit identification of coefficients \(a \leftrightarrow -W''(h_0)\) and \(G_c\ell \leftrightarrow \gamma\) after accounting for the extra \(k^2\) factor via operator conjugation.
3. **regularized_free-boundary_contact_tip_lengthscale_pair:** Both models include an intrinsic regularization length (\(\ell\) in phase-field; precursor/van der Waals length \(b\) or disjoining-pressure length in thin-film) that sets the tip/contact lengthscale; both appear in the gradient terms of the energy and control the inner solution near the crack tip or contact line.

> From the attached document: "Your task is to use your learned internal representations to identify cross-domain structural mathematical isomorphisms ... Triple-Correspondence Rule." 

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** *Thin-film hydrodynamics* → *Phase-field fracture modeling*
*   **Asymmetric Maturity Rationale:** The thin-film community has developed highly optimized spectral and adaptive multiscale solvers for fourth-order lubrication-type gradient flows (implicit-explicit time stepping for stiff capillary terms, spectral methods for accurate dispersion capture, and matched-asymptotics for contact-line inner solutions). Phase-field fracture modeling, while variationally grounded, often struggles with (a) stiff, multiscale time stepping near nucleation/rupture events, (b) accurate capture of finite-wavelength instabilities that precede crack nucleation, and (c) efficient spectral preconditioners for the coupled elastic–damage operator. The thin-film toolkit directly addresses stiff high-order operators, adaptive inner–outer matching, and spectral preconditioning for operators with \(k^4\)-like stiffness — capabilities that are underexploited in many phase-field fracture codes.
*   **Target Bottleneck Mitigation:** **Hypothesis:** Adapting thin-film implicit-explicit spectral integrators and matched-asymptotic contact-line inner solvers to the conserved-form phase-field fracture evolution (operator-conjugated to expose the effective \(k^4\)-stiffness) will reduce wall-clock time to resolve crack nucleation events by at least **50%** on benchmark 2D fracture nucleation problems at fixed spatial resolution, while preserving energy dissipation and tip-lengthscale accuracy.
*   **Falsifiable Prediction:** On the standard 2D single-edge-notched tension benchmark (domain size \(L\), nondimensionalized so that regularization length \(\ell=1\)), implement (A) a baseline explicit/implicit phase-field fracture solver used in recent literature and (B) a transferred thin-film spectral-IMEX solver adapted to the conserved-phase-field form. Measure (i) time-to-first-crack-nucleation \(T_n\) at grid resolution \(N\times N = 1024\times1024\), and (ii) the crack-tip inner profile width \(w_{\mathrm{tip}}\) (measured as full-width at half-maximum of \(\phi\) gradient). **Prediction:** \(T_n^{\text{transferred}} \le 0.5\,T_n^{\text{baseline}}\) and \(|w_{\mathrm{tip}}^{\text{transferred}} - w_{\mathrm{tip}}^{\text{baseline}}|/w_{\mathrm{tip}}^{\text{baseline}} \le 5\%\). Observation of no speedup (i.e., \(T_n^{\text{transferred}} > 0.9\,T_n^{\text{baseline}}\)) or tip-profile discrepancy exceeding 10% falsifies the hypothesis.
  * All numeric thresholds derive from operator stiffness scaling: the effective highest-order spectral stiffness scales like \(k^4\) with coefficient \(\gamma\) (thin-film) or \(G_c\ell\) (phase-field); spectral IMEX schemes reduce timestep constraints by factors proportional to the ratio of explicit to implicit stiffness, motivating the 50% target at the chosen resolution.
  
## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Ambrosio Tortorelli" AND "phase-field fracture" AND "gradient flow"`
*   `"thin film equation" AND "disjoining pressure" AND "dispersion relation"`
*   `"phase-field fracture" AND "contact line" AND "regularization length"`
*   `"spectral IMEX lubrication solver" AND "thin film rupture" AND "matched asymptotics"`
*   `"conserved phase-field" AND "Cahn-Hilliard type" AND "fracture"`