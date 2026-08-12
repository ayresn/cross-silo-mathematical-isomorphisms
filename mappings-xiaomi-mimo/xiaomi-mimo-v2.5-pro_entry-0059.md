---
sid_metadata:
  entry_id: "SID-0059"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Xiaomi"
  model_family: "MiMo"
  model_version: "V2.5 Pro"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "elastohydrodynamic-lubrication"
  domain_b: "pulmonary-airway-thin-film-mechanics"
  structural_family: "coupled-reynolds-elasticity-free-boundary-problems"
  triple_correspondence_vectors:
    - "reynolds_thin_film_equation_with_entrainment_convection"
    - "linear_elastic_pressure_to_film_thickness_operator_coupling"
    - "swift_stieber_cavitation_closure_free_boundary_condition"
    - "viscous_elastic_pressure_ratio_dimensionless_group"
discovery_rationale:
  why_not_obvious: "Tribology (ASME Journal of Tribology, Tribology International) and respiratory physiology (J. Appl. Physiol., Resp. Physiol. Neurobiol.) share no authorship overlap, no conference cross-attendance, and entirely distinct terminology (lubricant/surfactant, cavitation/closure, elastic half-space/airway wall). Each field independently derived its own Reynolds-equation-based models without cross-reference. The shared coupled Reynolds-elasticity free-boundary structure has not been explicitly identified."
prior_discovery_metrics:
  structural_isomorphism_score: 7.5
  vocabulary_divergence_score: 8.5
  expected_methodological_transfer_score: 8.0
  community_separation_score: 9.0
  representation_mismatch_score: 5.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.5
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_in_elastic_operator_form"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0059

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Elastohydrodynamic lubrication (EHL) in tribology — the analysis of thin viscous films separating elastic machine components (gears, bearings, seals), governed by the Reynolds equation coupled to half-space elastic deformation of the contacting surfaces.
*   **Silo B (Field 2):** Pulmonary airway thin-film mechanics — the analysis of the surfactant-laden liquid lining coating the interior of conducting airways, governing liquid plug propagation, airway closure, and reopening, governed by the thin-film lubrication equation coupled to airway wall compliance.
*   **Mathematical Isomorphism:** Both systems are governed by the Reynolds thin-film equation $\partial/\partial x\,[h^3/(\beta\mu)\,\partial p/\partial x] = U\,\partial h/\partial x + \partial h/\partial t$ coupled to a linear elastic operator $h = h_0 + \mathcal{A}[p]$ mapping hydrodynamic pressure to film thickness (Boussinesq integral for EHL, Laplace compliance for pulmonary airways), producing identical free-boundary problems at the liquid-film rupture front (cavitation or airway closure) characterized by the shared Swift-Stieber condition $p = p_\star,\;\partial p/\partial x = 0$, and governed by the same dimensionless viscous-to-elastic pressure ratio controlling the coupling strength.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Lubricant film thickness** $h(x,t)$ **(EHL)** ↔ **Airway liquid lining thickness** $h(x,t)$ **(Pulmonary)**
    *   *Operator Role:* Both are the dependent variable in the Reynolds thin-film equation $\partial_x[h^3/(\beta\mu)\,\partial_x p] = U\,\partial_x h + \partial_t h$, representing the local gap occupied by a viscous liquid driven by a pressure gradient $\partial_x p$ and an entrainment velocity $U$. The coefficient $\beta = 12$ (EHL: two no-slip walls) or $\beta = 3$ (pulmonary: one no-slip wall, one stress-free air–liquid interface) encodes the shear boundary conditions at the bounding surfaces.

*   **Entrainment velocity** $\bar{U} = (U_1+U_2)/2$ **(EHL)** ↔ **Liquid plug propagation speed** $U$ **(Pulmonary)**
    *   *Operator Role:* Both enter the Reynolds equation identically as the coefficient of the convective Couette-flow term $U\,\partial_x h$. In EHL, $\bar{U}$ is the mean of the two surface velocities bracketing the film; in pulmonary mechanics, $U$ is the speed at which a bolus of liquid translates through the airway, entraining a trailing film.

*   **Elastic half-space deformation** $\delta(x) = -\frac{2}{\pi E'}\int p(x')\ln|x-x'|\,dx'$ **(EHL)** ↔ **Airway wall compliance displacement** $\delta(x) = \frac{R_0^2}{E_w\,t_w}(p(x)-p_{\rm ext})$ **(Pulmonary)**
    *   *Operator Role:* Both are the linear operator $\mathcal{A}[p]$ in the film-geometry relation $h = h_0(x) + \delta(x)$, mapping the hydrodynamic pressure field to the elastic displacement of the boundary. The EHL operator is the Boussinesq integral (nonlocal, logarithmic kernel over the half-space); the pulmonary operator is the Laplace-law compliance for a thin-walled cylinder (local, algebraic). Both are linear in $p$, both map scalar-valued functions to scalar-valued functions, and both produce a second-order coupled free-boundary problem when substituted into the Reynolds equation. For very soft EHL contacts (elastomeric seals, O-rings), the Winkler-foundation approximation $\delta \approx C \cdot p$ reduces the EHL operator to the identical algebraic form as the pulmonary compliance model.

*   **Swift-Stieber cavitation condition** **(EHL)** ↔ **Airway closure/reopening boundary condition** **(Pulmonary)**
    *   *Operator Role:* Both are the free-boundary conditions of the Reynolds equation at the point of liquid-film rupture or reformation: $p = p_\star$ and $\partial p/\partial x = 0$. In EHL, $p_\star = p_{\rm cav}$ (cavitation pressure, typically atmospheric) and the condition is the Swift-Stieber or Reynolds boundary condition marking the rupture boundary. In pulmonary mechanics, $p_\star = p_{\rm close}$ (closing pressure, set by the capillary meniscus: $p_{\rm close} \sim 2\sigma/R_0$) and the same pair of conditions marks the airway closure front.

*   **Viscosity–pressure constitutive law** $\mu(p) = \mu_0\exp(\alpha_p p)$ **(EHL)** ↔ **Surface tension–surfactant coverage relation** $\sigma(\Gamma)$ **(Pulmonary)**
    *   *Operator Role:* Both are nonlinear equations of state coupling the thermodynamic state of the thin-film fluid to the effective transport coefficient in the Reynolds equation. In thermo-EHL, the Barus (or Roelands) relation modifies the viscosity $\mu$ entering $h^3/(12\mu)$, creating a pressure-viscosity positive feedback. In pulmonary surfactant mechanics, the Langmuir-type isotherm $\sigma(\Gamma)$ modifies the capillary pressure boundary condition, where $\Gamma$ satisfies its own advection–diffusion equation coupled to the film flow. Both represent constitutive closures that render the Reynolds equation nonlinear through the state-dependent transport coefficient.

## 3. CORE MATHEMATICAL PARALLELISM

In elastohydrodynamic lubrication, the pressure field in a thin viscous film separating two elastic bodies is determined by the Reynolds lubrication equation, with the film geometry self-consistently computed from the elastic deformation of the bounding surfaces under the hydrodynamic pressure. For a one-dimensional line contact with an incompressible, isothermal Newtonian lubricant, the governing system is:

```math
\frac{\partial}{\partial x}\!\left(\frac{h^3}{12\mu}\frac{\partial p}{\partial x}\right) = \bar{U}\frac{\partial h}{\partial x} + \frac{\partial h}{\partial t}
```

```math
h(x,t) = h_0(t) + \frac{x^2}{2R} + \delta(x,t), \qquad \delta(x,t) = -\frac{2}{\pi E'}\int_{x_{\rm in}}^{x_{\rm out}} p(x',t)\,\ln|x - x'|\,dx'
```

with the Swift-Stieber free-boundary condition at the cavitation front:

```math
p = p_{\rm cav}, \quad \frac{\partial p}{\partial x} = 0 \quad \text{at } x = x_{\rm cav}
```

Here $h$ is the film thickness, $p$ the hydrodynamic pressure, $\mu$ the lubricant viscosity, $\bar{U}$ the entrainment velocity, $R$ the equivalent radius of curvature, and $E' = E/(1-\nu^2)$ the plane-strain elastic modulus. The Boussinesq integral $\delta(x)$ is the nonlocal elastic displacement of the half-space surface under the pressure loading.

In pulmonary airway mechanics, the thin liquid lining (mucus and serous fluid, with surface-active surfactant) coating the interior of conducting airways is modeled by the lubrication (thin-film) equation, with the airway wall treated as a compliant elastic shell. For a cylindrical airway segment, the governing system is:

```math
\frac{\partial}{\partial x}\!\left(\frac{h^3}{3\mu}\frac{\partial p}{\partial x}\right) = U\frac{\partial h}{\partial x} + \frac{\partial h}{\partial t}
```

```math
h(x,t) = h_{\rm eq} + \delta(x,t), \qquad \delta(x,t) = \frac{R_0^2}{E_w\,t_w}\bigl(p(x,t) - p_{\rm ext}\bigr)
```

with the airway closure free-boundary condition:

```math
p = p_{\rm close}, \quad \frac{\partial p}{\partial x} = 0 \quad \text{at } x = x_{\rm close}
```

Here $h$ is the local liquid-lining thickness, $p$ the liquid pressure, $\mu$ the lining viscosity, $U$ the plug propagation speed, $R_0$ the undeformed airway radius, $E_w$ the wall Young's modulus, and $t_w$ the wall thickness. The factor 3 (versus 12 in EHL) arises from the stress-free condition at the air–liquid interface, replacing one of the two no-slip walls. The Laplace-law compliance $\delta(x)$ is the local radial displacement of the thin-walled airway under the transmural pressure difference.

**Unified structure and correspondence.** Both systems reduce to the same abstract coupled free-boundary problem:

```math
\frac{\partial}{\partial x}\!\left(\frac{h^3}{\beta\mu}\frac{\partial p}{\partial x}\right) = U\frac{\partial h}{\partial x} + \frac{\partial h}{\partial t}, \qquad h(x) = h_0(x) + \mathcal{A}[p](x)
```

with $\beta = 12$ (EHL) or $3$ (pulmonary), and $\mathcal{A}$ a linear operator (nonlocal integral or local algebraic) mapping pressure to displacement. The free boundary satisfies $p = p_\star$, $\partial_x p = 0$ in both cases.

**Correspondence 1 — Reynolds equation:** Identical second-order parabolic governing PDE with entrainment-driven convection and pressure-driven Poiseuille flux, differing only in the no-slip coefficient $\beta$.

**Correspondence 2 — Elastic coupling:** Both have $h = h_0 + \mathcal{A}[p]$ with $\mathcal{A}$ a linear operator. The EHL operator is the Boussinesq integral (nonlocal, $\mathcal{A}[p] \propto \int p(x')\ln|x-x'|dx'$); the pulmonary operator is the Laplace compliance (local, $\mathcal{A}[p] \propto p$). In the Winkler-foundation limit of soft EHL contacts, $\mathcal{A}$ reduces to the same local algebraic form.

**Correspondence 3 — Free boundary (Swift-Stieber):** Both systems share the identical two-condition free-boundary problem $p = p_\star$, $\partial_x p = 0$ at the film-rupture front. This is the Swift-Stieber condition in tribology and the closure condition in pulmonary mechanics.

**Correspondence 4 — Viscous-elastic dimensionless group:** Nondimensionalizing the Reynolds equation with length scale $R$ (or $R_0$), velocity scale $U$, and pressure scale $\mu U R / h_0^2$:

```math
\frac{\partial}{\partial \hat{x}}\!\left(\frac{\hat{h}^3}{\beta}\frac{\partial \hat{p}}{\partial \hat{x}}\right) = \frac{\partial \hat{h}}{\partial \hat{x}} + \frac{\partial \hat{h}}{\partial \hat{t}}, \qquad \hat{h} = \hat{h}_0 + \varepsilon\,\hat{\mathcal{A}}[\hat{p}]
```

EHL:
```math
\varepsilon_{\rm EHL} = \frac{12\,\mu\,\bar{U}\,R}{E'\,h_0^2}
```

Pulmonary:
```math
\varepsilon_{\rm pulm} = \frac{3\,\mu\,U\,R_0^2}{E_w\,t_w\,h_0^2}
```

Both are the ratio of viscous pressure ($\sim \mu U R / h_0^2$) to elastic restoring pressure ($\sim E'$ or $E_w t_w / R_0$). When $\varepsilon \ll 1$ the boundary is effectively rigid; when $\varepsilon \sim O(1)$ the pressure–deformation coupling qualitatively alters the film distribution and free-boundary location.

The correspondence extends over the class of quasi-steady, isothermal, Newtonian thin-film problems with linear elastic boundary coupling. It breaks where thermal effects (thermo-EHL), non-Newtonian rheology (mucus viscoelasticity), or surfactant transport ($\Gamma$-equation) become dominant, since these introduce additional coupled fields beyond the Reynolds–elasticity system.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Elastohydrodynamic Lubrication (Tribology) → Pulmonary Airway Mechanics (Respiratory Physiology)

*   **Asymmetric Maturity Rationale:** The EHL community has developed over five decades of specialized algorithms for the coupled Reynolds-elasticity free-boundary problem: multi-level multi-integration (MLMI) solvers (Lubrecht & Venner) achieving $O(N\log N)$ complexity for the integral operator; the Elrod–Adams cavitation algorithm, which reformulates the free-boundary problem as a smooth complementarity condition ($\theta \ge 0$, $p - p_{\rm cav} \ge 0$, $(p-p_{\rm cav})\theta = 0$) that eliminates explicit front tracking; full-system Newton–Raphson methods with analytical Jacobians that solve the Reynolds and elasticity equations simultaneously rather than by staggered iteration; and matched asymptotic expansions (Hooke, Evans, Snidle) yielding closed-form scaling laws for minimum film thickness and pressure spike location. The pulmonary community, while strong in biological imaging and patient-specific modeling, handles the Reynolds–compliance coupling by sequential (Picard) iteration or single-pass forward substitution, and tracks the closure/reopening front with ad-hoc phase-field or volume-of-fluid methods. The EHL toolkit offers substantial convergence and robustness improvements for the coupled problem.

*   **Target Bottleneck Mitigation:** Current small-airway closure models — where wall compliance is strongest — suffer from convergence failure of the iterative Reynolds-compliance coupling near the closure threshold, where $h \to 0$ and the pressure–deformation feedback becomes singular. Importing the Elrod–Adams algorithm, reformulated with $p_{\rm close}$ replacing $p_{\rm cav}$ and the fractional-film variable $\theta$ reinterpreted as an airway-patency indicator, would replace explicit free-boundary tracking with a smooth, iteration-free complementarity formulation. Importing the full-system Newton–Raphson approach (with analytical Jacobians of the Reynolds residuals with respect to both $p$ and $\delta$) would reduce the per-step computational cost from the current $O(N^2)$ or worse with explicit iteration to $O(N)$ per Newton step.

*   **Falsifiable Prediction:** For a steady liquid plug of length $L \gg R_0$ propagating in a compliant cylindrical tube of undeformed radius $R_0$, wall stiffness $K_w = E_w t_w / R_0^2$, liquid viscosity $\mu$, and surface tension $\sigma$, under a fixed driving pressure $\Delta P$, the EHL-derived matched-asymptotic analysis of the coupled Reynolds-compliance system predicts that the residual film thickness $h_f$ deposited behind the plug satisfies:

```math
\frac{h_f}{R_0} = 1.34\,\mathrm{Ca}^{2/3}\!\left(1 - \frac{\alpha}{\Lambda} + O(\Lambda^{-2})\right)
```

where $\mathrm{Ca} = \mu U/\sigma$ is the capillary number, $\Lambda = K_w h_0^2/(3\mu U)$ is the compliance parameter (wall-stiffness-to-viscous-pressure ratio), and $\alpha$ is a positive constant of order unity derivable from the matched asymptotic expansion in the meniscus transition region. The rigid-wall baseline (Bretherton, 1961) corresponds to $\Lambda \to \infty$, giving $h_f/R_0 = 1.34\,\mathrm{Ca}^{2/3}$.

The correction is **negative**: the capillary meniscus pressure ($\sim -2\sigma/R_0$) partially collapses the compliant wall, reducing the effective cross-section and hence the deposited film thickness.

**Baseline:** Bretherton rigid-tube prediction $h_f/R_0 = 1.34\,\mathrm{Ca}^{2/3}$.

**Measurable system:** Fluorescently labeled liquid plugs in PDMS microfluidic channels with independently calibrated compliance $K_w$ (pressure–diameter characterization), imaged by confocal fluorescence microscopy to resolve $h_f$.

**Falsification criterion:** If confocal measurements of $h_f$ in PDMS channels with $\Lambda = 5$ and $\mathrm{Ca} \in [0.005,\,0.05]$ reproduce the rigid-wall Bretherton prediction $1.34\,\mathrm{Ca}^{2/3}$ within $\pm 3\%$ experimental uncertainty — that is, no compliance correction is detected at the $\sim\!10\%$ level predicted by the $\alpha/\Lambda$ term — the structural isomorphism's predictive power is falsified.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"Reynolds equation" AND "elastic deformation" AND "cavitation" AND "elastohydrodynamic lubrication"`
*   `"thin film equation" AND "airway" AND "wall compliance" AND "plug propagation" AND "closure"`
*   `"Swift-Stieber" AND "airway closure" OR "pulmonary" AND "free boundary"`
*   `"elastohydrodynamic" AND "pulmonary" AND "thin film" AND "Reynolds"` *(falsification search — seeking the specific pairing already published)*
*   `"Bretherton" AND "compliant tube" AND "film thickness" AND "elastic"` *(falsification search — seeking compliance-corrected Bretherton scaling already derived from EHL methods)*
*   `"Elrod algorithm" AND ("airway" OR "pulmonary" OR "bronchial") AND "cavitation" OR "closure"` *(falsification search — seeking the specific algorithmic transfer)*