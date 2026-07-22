---
sid_metadata:
  entry_id: "SID-019"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
providence:
  company: "AcmeAI"
  model_family: "gptx"
  model_version: "gptx-1.0"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "phase-field-fracture-in-continuum-mechanics"
  domain_b: "information-cascade-fronts-on-complex-networks"
  structural_family: "free-boundary-instabilities / gradient-flow-variational-systems"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "variational_principle_and_energy_landscape"
    - "instability_mechanism_and_front_propagation"
discovery_rationale:
  why_not_obvious: "Different ontologies (continuum tensor fields vs discrete node-state dynamics), distinct experimental observables (mechanical crack vs information spread), and disciplinary language hide an operator-level equivalence: both evolve as gradient flows of nonconvex energies that produce propagating free-boundary fronts."
prior_discovery_metrics:
  structural_isomorphism_score: 7.6
  vocabulary_divergence_score: 8.2
  expected_methodological_transfer_score: 7.9
  community_separation_score: 8.5
  representation_mismatch_score: 9.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.2"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 019

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** *Phase‑field fracture in continuum solid mechanics* — brittle/ductile crack nucleation and propagation modeled by coupled linear momentum balance and a scalar phase‑field \( \phi(\mathbf{x},t)\) that regularizes a free surface (crack) via an energy functional (Griffith-type) and gradient-flow dynamics.
*   **Silo B (Field 2):** *Information‑cascade front propagation on complex networks* — abrupt, spatially localized spreading of adoption/rumor/contagion across nodes where local overload or thresholding produces a moving front that severs modular connectivity and arrests at community boundaries.
*   **Mathematical Isomorphism:** Both systems are **gradient flows of nonconvex energy functionals** that couple a smooth field (elastic displacement / node influence potential) to a binary/continuous order parameter (phase‑field / adoption state) whose dynamics regularize a moving free boundary; the triple correspondence explicitly links (1) the governing differential operator (elasticity PDE + Allen–Cahn/gradient flow ↔ graph Laplacian + node-wise gradient flow), (2) the variational energy (Griffith fracture energy ↔ graph-cut / modularity-penalized energy), and (3) the instability mechanism (stress concentration driven crack advance ↔ local overload/threshold-driven cascade front propagation).

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **phase field \(\phi(\mathbf{x},t)\)** ↔ **node adoption field \(u_i(t)\)**
    *   *Operator Role:* Both are scalar order parameters whose evolution is governed by a gradient-flow operator that regularizes a sharp interface; \(\phi\) interpolates intact/damaged material while \(u_i\) interpolates susceptible/adopted node states. Mathematically both enter the energy functional multiplicatively with a stiffness-like prefactor that modulates the primary operator (elastic stiffness vs network transmissibility).
*   **elastic displacement \(\mathbf{u}(\mathbf{x},t)\)** ↔ **influence potential \(\psi_i(t)\)**
    *   *Operator Role:* \(\mathbf{u}\) solves an elliptic PDE (divergence of stress) coupled to \(\phi\); \(\psi_i\) solves a discrete elliptic problem (graph Laplacian) whose coefficients depend on \(u_i\). Both provide the long-range field that concentrates "driving" (stress or influence) at the front.
*   **Griffith fracture energy \( \mathcal{E}_{\text{fracture}}[u,\phi]\)** ↔ **graph-cut / modularity-penalized energy \( \mathcal{E}_{\text{cascade}}[\psi,u]\)**
    *   *Operator Role:* Both energies combine a bulk term (elastic strain energy or influence diffusion) and an interfacial term (surface energy or cut/modularity penalty). Minimization/gradient flow of these energies yields front nucleation and propagation governed by the same variational structure.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A (Phase‑field fracture) is commonly modeled by coupling linear elasticity to a phase‑field \(\phi\in[0,1]\) with an energy of Griffith type and gradient-flow dynamics for \(\phi\). A canonical form:
```math
\begin{aligned}
&\text{Elastic equilibrium:}\quad \nabla\cdot\big( (1-\kappa(\phi))\mathbf{C}:\nabla^s \mathbf{u}\big)=\mathbf{0},\\
&\text{Phase-field evolution (gradient flow):}\quad \tau\frac{\partial \phi}{\partial t} = -\frac{\delta \mathcal{E}_{\text{fracture}}}{\delta \phi}
\end{aligned}
```
with
```math
\mathcal{E}_{\text{fracture}}[\mathbf{u},\phi]=\int_\Omega \big( (1-\phi)^2 \, \psi_e(\nabla^s\mathbf{u}) + G_c\gamma_\ell(\phi,\nabla\phi)\big)\,dV,
```
where \(\psi_e\) is elastic energy density, \(G_c\) fracture toughness, and \(\gamma_\ell\) a regularized surface term (length scale \(\ell\)).

Silo B (Cascade fronts on networks) can be cast as a discrete gradient flow on a graph \(G=(V,E)\) with node variables \(u_i\in[0,1]\) (adoption) and a long-range potential \(\psi_i\) solving a graph-elliptic equation. A structurally analogous formulation:
```math
\begin{aligned}
&\text{Graph elliptic field:}\quad \sum_{j} L_{ij} \psi_j = f_i(u),\\
&\text{Node-phase evolution (gradient flow):}\quad \tau_n \frac{du_i}{dt} = -\frac{\partial \mathcal{E}_{\text{cascade}}}{\partial u_i}
\end{aligned}
```
with
```math
\mathcal{E}_{\text{cascade}}[\psi,u]=\sum_{i} \big( (1-u_i)^2 \, \Phi_i(\psi) \big) + \alpha \sum_{(i,j)\in E} w_{ij} \, \Gamma_\ell(u_i,u_j),
```
where \(L\) is the graph Laplacian, \(\Phi_i(\psi)\) is a node-level "influence energy" analogous to \(\psi_e\), and \(\Gamma_\ell\) is a regularizer penalizing sharp node-state interfaces (graph-cut term with length scale \(\ell\)). The mapping sends continuum differential operators \(\nabla\cdot(\mathbf{C}\nabla)\) → discrete Laplacian \(L\), elastic energy density \(\psi_e\) → node influence potential \(\Phi_i\), and the phase-field interfacial energy \(\gamma_\ell(\phi,\nabla\phi)\) → graph-cut regularizer \(\Gamma_\ell(u_i,u_j)\). Topologically, crack-tip stress concentration ↔ high-degree/bridge-node influence concentration; both produce localized front propagation governed by the same energy descent and front-regularization length scale \(\ell\).

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Phase‑field fracture (Materials/Continuum Mechanics) → Network cascade modeling (Network Science / Computational Social Science)
*   **Asymmetric Maturity Rationale:** Phase‑field fracture modeling has a decades‑mature variational foundation, robust numerical toolchains (adaptive finite elements, energy-stable time integrators, multigrid solvers, phase‑field regularization theory), and well‑validated experimental protocols for front speed and arrest criteria. Network cascade modeling, while rich in stochastic and threshold models, lacks a widely adopted variational, energy‑stable, front‑regularized computational framework that can (a) handle sharp but regularized cascade fronts, (b) provide mesh/adaptive refinement analogues on graphs, and (c) yield deterministic, falsifiable scaling laws for front speed and arrest.
*   **Target Bottleneck Mitigation:** **Hypothesis:** Implementing a phase‑field–inspired variational formulation on graphs (graph phase‑field) and importing adaptive multigrid solvers from continuum fracture will enable (i) stable simulation of cascade front nucleation and arrest on large modular networks with controlled interface width \(\ell\), (ii) computation of a deterministic cascade toughness \(G_c^{\text{graph}}\) that predicts arrest vs. runaway, and (iii) efficient, scalable solvers that reduce computational cost from \(O(N^2)\) to near‑linear scaling via algebraic multigrid on the graph Laplacian.
*   **Falsifiable Prediction:** For synthetic networks with tunable modularity \(Q\) and average transmissibility \(T\), the imported variational model predicts a **square‑root scaling** of steady front speed \(v\) near the critical transmissibility \(T_c(Q)\):
```math
v \sim C(Q)\,\sqrt{T - T_c(Q)}\quad\text{for }T\downarrow T_c,
```
where \(C(Q)\) is a modularity-dependent prefactor analogous to the fracture energy release rate. Empirical tests: (1) On synthetic stochastic block models, measure front speed vs \(T\); verify the \(\sqrt{\cdot}\) scaling and extract \(T_c(Q)\). (2) On time‑stamped social contagion datasets (e.g., meme cascades with spatial or community metadata), fit front propagation to the predicted scaling and test whether modularity explains deviations better than classical threshold models. A failure to observe the predicted scaling across controlled synthetic networks would falsify the mapping.
*   **Additional Operational Transfer:** Adaptive refinement analogues: map continuum adaptive mesh refinement to graph coarsening/refinement (multilevel graph partitioning) to concentrate computational effort near the cascade front; import energy-stable implicit time integrators to avoid spurious oscillations in adoption fraction near the front.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"phase-field fracture" AND "Griffith energy" AND "adaptive finite element"`
*   `"graph Laplacian" AND "variational graph cut" AND "front propagation"`
*   `"phase field" AND "graph" AND "interface regularization"`
*   `"cascade front" AND "modularity" AND "front speed scaling"`