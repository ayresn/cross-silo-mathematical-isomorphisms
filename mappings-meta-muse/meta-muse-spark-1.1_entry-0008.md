---
sid_metadata:
  entry_id: "SID-0008"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Meta"
  model_family: "Muse"
  model_version: "Spark 1.1"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "electrochemical-lithium-dendrite-electrodeposition"
  domain_b: "carbonate-acidization-reactive-wormholing"
  structural_family: "reactive-infiltration-laplacian-growth-instabilities"
  triple_correspondence_vectors:
    - "shared_elliptic_laplacian_conductivity_operator_for_potential_pressure"
    - "robin_reactive_flux_stefan_moving_boundary_velocity_pair"
    - "mullins_sekerka_dispersion_threshold_with_global_flux_conservation"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language_electrochemical_overpotential_vs_geochemical_dissolution_rate, incompatible_ontologies_ion_transport_vs_porous_darcy_flow, historically_isolated_communities_battery_engineering_vs_petroleum_reservoir_engineering"
prior_discovery_metrics:
  structural_isomorphism_score: 8.4
  vocabulary_divergence_score: 8.9
  expected_methodological_transfer_score: 8.1
  community_separation_score: 9.2
  representation_mismatch_score: 7.6
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±1.2"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_butler_volmer_nonlinearity_vs_linear_first_order_dissolution"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0008

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Lithium-metal battery engineering - galvanostatic electrodeposition instability leading to dendritic short-circuit growth at the anode-electrolyte interface.
*   **Silo B (Field 2):** Petroleum reservoir engineering - reactive wormhole formation during carbonate acidization by hydrochloric acid injection in porous limestone.
*   **Mathematical Isomorphism:** Both systems are governed by an identical coupled elliptic-parabolic operator system where an elliptic Laplacian potential field (electric potential / Darcy pressure) drives a parabolic advection-diffusion-reactive concentration field toward a single moving reactive boundary that evolves under a shared Robin flux condition coupled to a Stefan velocity law, exhibiting the same Mullins-Sekerka dispersion threshold and global flux conservation under the transformation $\Phi_A = \phi$, $\Phi_B = p$, $\sigma_A = \kappa(c)$, $\sigma_B = k(\mathbf{x})/\mu$, $v_{n,A} = (\Omega/F)j_n$, $v_{n,B} = (M_s/\rho_s)k_s c$.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   electrolyte ionic conductivity ↔ reservoir mobility $k/\mu$
    *   *Operator Role:* coefficient $\sigma(\mathbf{x}) \in \mathbb{R}^+_{>0}$ in the shared second-order elliptic operator $L_{\sigma}[\Phi] = \nabla\cdot(\sigma \nabla \Phi)$ of divergence form acting on real scalar potential field $\Phi: \Omega \subset \mathbb{R}^3 \to \mathbb{R}$. Both $\kappa$ and $k/\mu$ enter as $L^2$-elliptic, symmetric positive-definite. No type conversion required after nondimensionalization $\tilde{\sigma} = \sigma / \sigma_0$.
*   Butler-Volmer linearized exchange rate $k_{BV}$ ↔ mineral dissolution rate constant $k_s$
    *   *Operator Role:* coefficient $k_{r} \in \mathbb{R}^+ [m/s]$ in the shared Robin boundary operator $B_R[c] = -D \partial_n c - k_r c = 0$ on moving boundary $\Gamma(t)$. Both map real scalar concentration field $c: \Omega \to \mathbb{R}^+$ to normal flux. Transformation to reconcile dimensions: $k_{BV} = i_0 a / (F c_0 R T)$ [m/s] after linearization at small overpotential, identical type to $k_s$ [m/s].
*   anode normal growth velocity $v_n$ ↔ dissolution front normal velocity $v_n$
    *   *Operator Role:* scalar normal velocity field $v_n: \Gamma(t) \to \mathbb{R}$ [m/s] in the shared Stefan moving-boundary law $v_n = \beta \, J_n$ where $J_n = -\sigma \partial_n \Phi = -D \partial_n c$ at $\Gamma(t)$ by Robin balance. Reconciliation: $\beta_A = \Omega_m / F$ [m^3 / C] times $F$ yields [m^3 / mol], $\beta_B = M_s / \rho_s / (1-\phi)$ [m^3 / mol], both convert molar flux to interface advance.
*   electric overpotential $\eta$ ↔ acid concentration over-saturation $(c - c_{eq})$
    *   *Operator Role:* thermodynamic driving scalar in Gibbs-Thomson curvature regularization term $c_{\Gamma} = c_0 (1 + \Gamma \kappa_{curv})$ where $\Gamma = \gamma \Omega / R T$ enters as additive shift to Dirichlet value of concentration at curved interface. Both enter as $H^1$-trace of concentration field modified by mean curvature $\kappa_{curv}: \Gamma \to \mathbb{R}$ [1/m].

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models Li dendrite growth as a coupled elliptic potential problem for ion transport with parabolic Li+ diffusion toward a moving deposition front. In the electrolyte domain $\Omega_A(t)$ bounded by dendrite surface $\Gamma_A(t)$, potential is quasi-static because double-layer charging is fast, and concentration obeys diffusion-migration.

```math
\nabla \cdot (\kappa(c) \nabla \phi) = 0 \quad \text{in } \Omega_A(t)
```
```math
\partial_t c + \mathbf{u}\cdot\nabla c = D_{Li} \nabla^2 c \quad \text{in } \Omega_A(t)
```
```math
-D_{Li} \partial_n c = k_{BV} c, \quad v_{n,A} = \frac{\Omega_m}{F} j_n = \frac{\Omega_m}{F}(-\kappa \partial_n \phi) \quad \text{on } \Gamma_A(t)
```
where $k_{BV} = k_0 \exp(\alpha F \eta /RT)$ linearized to $k_{BV} \approx k_0(1+\alpha F\eta/RT)$ for small overpotential, and $\Omega_m$ is molar volume of Li.

Silo B models wormhole formation as Darcy flow of acid in porous carbonate $\Omega_B(t)$ bounded by dissolution front $\Gamma_B(t)$. Pressure obeys incompressibility with heterogeneous permeability, and acid concentration obeys advection-diffusion with consumption at the wall, a formulation independently recognized as the Darcy-scale reactive-transport model of Fredd and Fogler, Economides.

```math
\nabla \cdot \left( \frac{k(\mathbf{x})}{\mu} \nabla p \right) = 0 \quad \text{in } \Omega_B(t)
```
```math
\phi \partial_t c_a + \mathbf{u}\cdot\nabla c_a = \nabla\cdot(D_e \nabla c_a) \quad \text{in } \Omega_B(t), \quad \mathbf{u} = -\frac{k}{\mu}\nabla p
```
```math
-D_e \partial_n c_a = k_s c_a, \quad v_{n,B} = \frac{M_s}{\rho_s(1-\phi)} k_s c_a = \frac{M_s}{\rho_s(1-\phi)}(-D_e \partial_n c_a) \quad \text{on } \Gamma_B(t)
```
Under the identification $\Phi_A \leftrightarrow \Phi_B$, $\sigma_A = \kappa \leftrightarrow \sigma_B = k/\mu$, $D_A = D_{Li} \leftrightarrow D_B = D_e/\phi$, $k_{r,A}=k_{BV} \leftrightarrow k_{r,B}=k_s$, the elliptic operator $L_{\sigma}$ coincides, and the coupled system is second-order elliptic + parabolic advection-diffusion on both sides, satisfying same equation class. The correspondence extends up to the nonlinear Butler-Volmer exponential where Silo A retains $k_{BV}(\eta)=k_0[\exp(\alpha_a F\eta/RT)-\exp(-\alpha_c F\eta/RT)]$ while Silo B is strictly linear $k_s = const$; the isomorphism holds exactly in the linearized low-overpotential limit $|F\eta/RT| < 0.2$ which is the wormholing regime.

Demonstration of triple correspondences:

Vector 1 - shared elliptic Laplacian conductivity operator: displayed above as $\nabla\cdot(\sigma\nabla\Phi)=0$ for both silos, with weak form $\int_{\Omega} \sigma \nabla\Phi\cdot\nabla w = \int_{\Gamma} J_n w$ identical.

Vector 2 - Robin reactive flux Stefan moving-boundary pair: for Silo A and B respectively, Robin balance plus Stefan advance shown in the third line of each block, both yielding $v_n = \beta (-D \partial_n c)$. This is a moving-boundary pair of mixed Robin-Stefan type, not Dirichlet.

Vector 3 - Mullins-Sekerka dispersion threshold with global flux conservation: both obey global conservation $\int_{\Gamma} J_n dS = I_{total}$ (total current) vs $Q_{total}$ (injection rate).

```math
\int_{\Gamma_A(t)} -\kappa \partial_n \phi \, dS = I_0 = const, \quad \int_{\Gamma_B(t)} -\frac{k}{\mu}\partial_n p \, dS = Q_0 = const
```
Linear stability of planar front $z = vt + \epsilon \exp(\sigma t + i k x)$ yields for Silo A:

```math
\sigma_A(k) = v_0 |k| \frac{Da_A -1}{Da_A +1} - D_{Li} \Gamma_{GT} k^2, \quad Da_A = k_{BV} L / D_{Li}, \quad \Gamma_{GT} = \gamma \Omega_m / RT
```
and for Silo B (as derived by Chadam, Ortoleva, Hinch & Bhatt for reactive infiltration):

```math
\sigma_B(k) = v_0 |k| \frac{Da_B -1}{Da_B +1} - \alpha_{disp} |k|^2, \quad Da_B = k_s a_v L^2 / D_e, \quad v_0 = Q_0 / A \phi
```
where $\alpha_{disp}$ is transverse dispersion coefficient providing curvature-like regularization analogous to $\Gamma_{GT}$. Critical wavenumber $k_c = v_0(Da-1)/(Da+1)/\Gamma$ marks instability onset $\sigma(k_c)=0$ in both.

Dimensionless collapse: $Pe = v_0 L / D$, $Da = k_r L / D$, Wagner number $Wa_A = \kappa RT / (F L k_0) = 1/Da_A$ maps to acidization $Da_B$.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** electrochemical dendrite phase-field modeling (Silo A) → carbonate acidization wormholing (Silo B)
*   **Asymmetric Maturity Rationale:** Source field Silo A has developed thermodynamically consistent variational phase-field models (Allen-Cahn + Cahn-Hilliard coupled to Butler-Volmer) with explicit Gibbs-Thomson curvature regularization $\gamma \kappa_{curv}$, adaptive mesh refinement via $W(\nabla \psi)$ double-well potentials, and open-source codes (e.g., PRISMS-PF, MOOSE) that handle tip-splitting and merging without explicit front tracking. Target field Silo B is highly mature at Darcy-scale streamline simulation and dimensionless $Pe$-$Da$ type-curve collapse for breakthrough prediction, but genuinely lacks a variational curvature regularization for the dissolution front; current commercial acidization simulators (StimPro, Mangane) use explicit level-set with ad-hoc tip radius cutoff that fails to predict branching fractal dimension and requires manual re-meshing at coalescence, creating a bottleneck for predicting wormhole competition at high $Da$.
*   **Target Bottleneck Mitigation:** Importing Silo A's phase-field grand-potential functional $\mathcal{F} = \int [W(\psi) + \epsilon^2 |\nabla\psi|^2/2 + h(\psi) f_{chem}(c)] dV$ with $\psi$ as solid-liquid order parameter and Gibbs-Thomson term $\lambda = \gamma \Omega /RT$ into Silo B's Darcy framework, replacing explicit $\Gamma_B(t)$ with diffusive interface $\epsilon \sim 0.1 d_p$, will allow automatic handling of wormhole tip-splitting, coalescence, and Ostwald-like competition without re-meshing, and provide physical regularization of the ill-posed Mullins-Sekerka singularity at $k \to \infty$.
*   **Falsifiable Prediction:** In Indiana limestone core-flood benchmarks at $T=25^{\circ}C$, $15 wt\% HCl$, core $L=0.15 m$, $d_p=200 \mu m$, the phase-field-augmented Darcy model predicts a 30% downward shift of the pore-volumes-to-breakthrough (PVBT) minimum from $Q_{opt}=0.8 cm^3/min$ (baseline Fredd & Fogler 1998 correlation and StimPro simulator) to $Q_{opt}^{new}=0.56 \pm 0.06 cm^3/min$, with reduction of optimal PVBT from $0.45$ to $0.31 \pm 0.04$, and increase of micro-CT measured wormhole fractal dimension from $D_f=1.63$ (baseline) to $D_f=1.82 \pm 0.05$ at $Pe=0.5$, $Da_B=5$. Falsification occurs if $8$ replicate core floods with controlled addition of $0.5 wt\%$ non-ionic surfactant (increasing effective $\gamma$ from $0.02$ to $0.08 J/m^2$) show $<10\%$ shift in $Q_{opt}$ and $D_f$ remains $1.65 \pm 0.10$ ($p>0.05$ t-test vs baseline), indicating curvature regularization is negligible at Darcy scale.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"lithium dendrite" AND "Butler-Volmer" AND "Mullins-Sekerka" AND "phase-field"`
*   `"wormhole" AND "carbonate acidization" AND "Fredd Fogler" AND "reactive infiltration instability"`
*   `"electrodeposition dendrite" AND "carbonate wormhole" AND "isomorphism" AND "Damköhler"`
*   `"Li dendrite phase-field model" AND "acidization" AND "Stefan condition" transfer`
*   `"reactive infiltration" AND "electrochemical deposition" AND "shared Laplacian growth"`