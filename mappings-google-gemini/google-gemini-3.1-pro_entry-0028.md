---
sid_metadata:
  entry_id: "SID-0028"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Google"
  model_family: "Gemini"
  model_version: "3.1 Pro"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "marine-glaciology"
  domain_b: "polymer-thin-film-dynamics"
  structural_family: "singular-moving-boundary-lubrication"
  triple_correspondence_vectors:
    - "elliptic_extensional_slip_momentum_operator"
    - "hyperbolic_kinematic_mass_transport"
    - "moving_detachment_boundary_singularity"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies_and_disparate_spatial_scales"
prior_discovery_metrics:
  structural_isomorphism_score: 9.6
  vocabulary_divergence_score: 9.8
  expected_methodological_transfer_score: 9.4
  community_separation_score: 9.9
  representation_mismatch_score: 8.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 9.2
    uncertainty: "±0.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "differing_pressure_gradient_derivations"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0028

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Marine Glaciology):** The macroscopic flow of marine ice streams and the migration of grounding lines where grounded ice detaches from bedrock and becomes a floating ice shelf.
*   **Silo B (Polymer Thin-Film Dynamics):** The dewetting and retraction of ultra-thin, highly viscous polymer films on slippery solid substrates.
*   **Mathematical Isomorphism:** Both macroscopic marine ice streams and microscopic polymer dewetting films are strictly governed by an identical coupled parabolic-elliptic system—combining a kinematic mass transport equation with an elliptic momentum operator balancing extensional membrane stresses against basal drag—which must resolve a non-integrable moving-boundary stress singularity at the exact point of substrate detachment.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Grounding Line $x_g$ ↔ Dewetting Contact Line
    *   *Operator Role:* The spatial coordinate of the singular moving boundary where the basal friction term in the elliptic momentum equation transitions to zero, triggering a non-physical stress singularity if treated as a discrete step-function.
*   Shallow Shelf Approximation (SSA) ↔ Strong-Slip Lubrication Approximation
    *   *Operator Role:* The specific elliptic differential operator $\partial_x(4 \eta h \partial_x u) - \text{drag} = \text{forcing}$ governing longitudinal stress balance in a medium where viscous extensional flow dominates over vertical shear flow.
*   Basal Drag Discontinuity ↔ Huh-Scriven Singularity
    *   *Operator Role:* The mathematical singularity arising at the detachment point; both objects require regularization to permit stable numerical integration of the elliptic boundary-value problem.
*   Flotation Criterion $h(x_g) = -(\rho_w / \rho_i) z_b$ ↔ Disjoining Pressure $\Pi(h)$
    *   *Operator Role:* The mechanism governing detachment. Silo A defines it algebraically, forcing a discontinuous jump in the domain, whereas Silo B explicitly regularizes the singularity by embedding it directly into the continuous spatial gradient of the driving pressure.

## 3. CORE MATHEMATICAL PARALLELISM
In Marine Glaciology, rapidly flowing ice streams are modeled using the Shallow Shelf Approximation (SSA), which assumes horizontal extensional stresses dominate vertical shear. The system is defined by an elliptic momentum balance for the depth-averaged velocity $u$, coupled to a mass transport equation for ice thickness $h$. At the grounding line ($x_g$), the ice detaches from the bedrock, causing basal friction $\tau_b$ to drop discontinuously to zero. This discontinuity creates a profound mathematical singularity, governed by:
```math
\begin{align}
\frac{\partial}{\partial x} \left( 4 \bar{\nu} h \frac{\partial u}{\partial x} \right) - \tau_b(u, x) &= \rho_i g h \frac{\partial s}{\partial x} \\
\frac{\partial h}{\partial t} + \frac{\partial (uh)}{\partial x} &= \dot{a}
\end{align}
```
where $\bar{\nu}$ is the effective viscosity, $s$ is the surface elevation, and $\dot{a}$ is the surface mass balance. The basal drag $\tau_b$ is non-zero only for $x \le x_g$, triggering severe grid-dependence in numerical models requiring intense sub-grid parameterization.

In Polymer Thin-Film Dynamics, highly viscous films on solid substrates with a large Navier slip length are modeled using the strong-slip lubrication equation. Because slip dominates over internal shear, flow is fundamentally extensional (plug flow). The singular nature of a moving contact line (the Huh-Scriven paradox) is analytically resolved by introducing a precursor film maintained by a disjoining pressure $\Pi(h) = A/h^3$, which provides continuous regularization:
```math
\begin{align}
\frac{\partial}{\partial x} \left( 4 \mu h \frac{\partial u}{\partial x} \right) - \frac{\mu}{b} u &= -h \frac{\partial}{\partial x} \left( -\gamma \frac{\partial^2 h}{\partial x^2} - \Pi(h) \right) \\
\frac{\partial h}{\partial t} + \frac{\partial (uh)}{\partial x} &= 0
\end{align}
```
where $\mu$ is the viscosity, $b$ is the slip length, and $\gamma$ is the surface tension. 

**Operator Bridge:** The two governing systems exhibit an exact, three-fold structural equivalence that proves the isomorphism. **First** (`elliptic_extensional_slip_momentum_operator`), mapping ice velocity $u \leftrightarrow$ film velocity $u$ and ice thickness $h \leftrightarrow$ film thickness $h$, the left-hand sides are structurally identical: the extensional stress divergence $4 \bar{\nu} \leftrightarrow 4 \mu$ perfectly balances the basal drag $\tau_b \leftrightarrow \frac{\mu}{b}u$. **Second** (`hyperbolic_kinematic_mass_transport`), both systems transport the domain thickness via the exact identical hyperbolic-parabolic kinematic continuity operator $\partial_t h + \partial_x(uh) = \text{Source}$. **Third** (`moving_detachment_boundary_singularity`), both models suffer from a fundamental stress singularity at the domain detachment coordinate ($x_g$ vs. the dewetting front). The driving forces on the right-hand sides ($\rho_i g \partial_x s \leftrightarrow -\partial_x p$) diverge fundamentally only in their boundary regularization: Silo A uses a blunt spatial discontinuity $x_g$, whereas Silo B avoids the singularity entirely via the continuous derivative of the disjoining pressure $\Pi(h)$.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Polymer Thin-Film Dynamics → Marine Glaciology
*   **Asymmetric Maturity Rationale:** The soft-matter fluid dynamics community possesses highly mature analytical techniques (e.g., continuous diffuse-interface and disjoining-pressure precursor models) for regularizing moving contact line singularities without needing to highly resolve the slip length on a computational mesh. Conversely, marine glaciology lacks an equivalent continuous physical regularizer and relies on heuristic discrete step-functions, which force researchers to use computationally ruinous sub-meter Adaptive Mesh Refinement (AMR) at the grounding line to prevent numerical artifacts.
*   **Target Bottleneck Mitigation:** Transporting the disjoining pressure $\Pi(h)$ formulation into glaciology—recast as a diffuse flotation regularizer modifying $\tau_b$ asymptotically rather than discontinuously—will eliminate the Huh-Scriven-like stress singularity at the grounding line, allowing coarse continent-scale grids to capture accurate detachment migration natively.
*   **Falsifiable Prediction:** Implementing a continuous basal friction regularizer translated from thin-film disjoining pressure (modeled structurally as $\tau_b(u, x) = \beta^2 u \left[1 - (h_{float}/h)^3\right]$) into the Marine Ice Sheet Model (MISMIP benchmark) will replicate the exact Schoof (2007) analytical grounding line mass flux within a 2.0% error margin on a uniform 2-km computational mesh, directly falsifying the current state-of-the-art requirement for 100-meter mesh refinement at the grounding boundary.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Shallow Shelf Approximation" AND "grounding line migration" AND "basal friction discontinuity"`
*   `"strong-slip lubrication" AND "dewetting" AND "disjoining pressure"`
*   `"disjoining pressure" AND "grounding line migration" AND "extensional flow"`
*   `"Huh-Scriven singularity" AND "Shallow Shelf Approximation"`