---
sid_metadata:
  entry_id: "SID-0056"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Xiaomi"
  model_family: "MiMo"
  model_version: "V2.5 Pro"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "polycrystalline-grain-growth"
  domain_b: "thin-film-magnetic-domain-coarsening"
  structural_family: "curvature-driven-interface-evolution"
  triple_correspondence_vectors:
    - "overdamped_curvature_flow_operator_v_n_eq_Msigma_kappa"
    - "von_neumann_mullins_gauss_bonnet_growth_law_dA_dt_n"
    - "herring_neumann_triple_junction_angle_balance_120deg"
    - "parabolic_allen_cahn_coarsening_kinetics_R2_linear_in_t"
    - "hillert_mean_field_self_similar_size_distribution"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / grain_growth_topology_statistical_tools_never_applied_to_magnetic_domain_patterns"
prior_discovery_metrics:
  structural_isomorphism_score: 8.5
  vocabulary_divergence_score: 7.5
  expected_methodological_transfer_score: 8.5
  community_separation_score: 8.0
  representation_mismatch_score: 4.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "dipolar_interactions_and_wall_inertia_break_overdamped_curvature_only_dynamics"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0056

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Polycrystalline grain growth in metallic and ceramic thin films — curvature-driven migration of grain boundaries to minimize total interfacial energy, governed by the Mullins (1956) mean curvature flow model with Herring (1952) triple-junction angle conditions.
*   **Silo B (Field 2):** Magnetic domain pattern coarsening in ferromagnetic thin films with perpendicular magnetic anisotropy (e.g., Co/Pt, Pt/Co/Pt multilayers) — curvature-driven domain wall motion to minimize wall energy in the overdamped thin-wall limit of the Landau-Lifshitz-Gilbert equation.
*   **Mathematical Isomorphism:** Both systems are governed by overdamped mean curvature flow of one-dimensional interfaces in 2D, $v_n = -M\sigma\kappa$, where $M\sigma$ is the interface diffusivity; both satisfy the Herring/Neumann triple-junction angle condition $\sum\sigma_i\hat{\mathbf{n}}_i = \mathbf{0}$ at vertices where three interfaces meet (for domain patterns with three or more distinct domain types); both belong to the Allen-Cahn non-conserved universality class with parabolic coarsening $\langle R^2\rangle \propto M\sigma\, t$; and both admit Hillert-type self-similar domain/grain size distributions governed by the same mean-field conservation equation — identified under the parameter correspondence $M_{\mathrm{gb}}\gamma_{\mathrm{gb}} \leftrightarrow \sigma_w/\beta \equiv M_{\mathrm{dw}}\sigma_w$.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Grain boundary** ↔ **Domain wall**
    *   *Operator Role:* Both are 1D interfaces in 2D whose normal velocity is governed by the mean curvature flow operator $v_n = -M\sigma\kappa$, where $\kappa$ is the local curvature (second spatial derivative of the interface position with respect to arc length) and $M\sigma$ is the interface diffusivity $[\mathrm{m}^2/\mathrm{s}]$. This operator arises identically in both the Mullins grain boundary equation and the overdamped thin-wall LLG domain wall equation.
*   **Grain boundary energy $\gamma_{\mathrm{gb}}$** ↔ **Domain wall energy density $\sigma_w$**
    *   *Operator Role:* Both serve as the surface energy density in the total interface energy functional $\mathcal{F} = \oint\sigma\,ds$, whose first variation with respect to normal interface displacement $X$ yields $\delta\mathcal{F}/\delta X = \sigma\kappa$, the driving force for curvature flow.
*   **Grain boundary mobility $M_{\mathrm{gb}}$** ↔ **Domain wall mobility $M_{\mathrm{dw}} = \sigma_w/\beta$**
    *   *Operator Role:* Both are the kinetic coefficients in the gradient flow relation $v_n = -M\,\delta\mathcal{F}/\delta X$, determining the rate of interface migration per unit thermodynamic driving force. The grain growth mobility has units $[\mathrm{m}^3/(\mathrm{J\cdot s})]$; the domain wall mobility $M_{\mathrm{dw}} = \gamma_{\mathrm{LL}}\Delta\alpha/[2M_s(1+\alpha^2)]$ from the LLG equation maps to the same dimensional structure under the identification $M_{\mathrm{gb}}\gamma \leftrightarrow \sigma_w/\beta$.
*   **Triple junction (Herring condition)** ↔ **Domain wall vertex (Neumann condition)**
    *   *Operator Role:* Both satisfy the variational angle balance $\sum_{i=1}^{3}\sigma_i\hat{\mathbf{n}}_i = \mathbf{0}$ at vertices where three interfaces meet, derived from stationarity of $\mathcal{F}$ with respect to junction position $\delta\mathcal{F}/\delta\mathbf{r}_{\mathrm{vertex}} = 0$. For isotropic interface energy this yields 120° equilibrium angles in both systems.
*   **Stored elastic energy $\Delta E_{\mathrm{stored}}$** ↔ **Zeeman energy $2M_s H_{\mathrm{ext}}$**
    *   *Operator Role:* Both enter the curvature flow equation as additive body-force driving terms: $v_n = -M\sigma\kappa + v_{\mathrm{body}}$, where $v_{\mathrm{body}} = M_{\mathrm{gb}}\Delta E_{\mathrm{stored}}$ for grain growth (from dislocation density differences between grains) and $v_{\mathrm{body}} = M_{\mathrm{dw}} \cdot 2M_s H_{\mathrm{ext}}$ for domain walls (from the Zeeman energy of the applied field favoring one magnetization orientation).
*   **Mean grain radius $\bar{R}$** ↔ **Mean domain width $\bar{d}$**
    *   *Operator Role:* Both enter the Hillert mean-field growth law $dR/dt = M\sigma(1/\bar{R} - 1/R)$ as the critical radius separating growing domains ($R > \bar{R}$) from shrinking domains ($R < \bar{R}$), and both set the self-similar scaling variable $\rho = R/\bar{R}$ in the Hillert size distribution.
*   **Parabolic grain growth law** ↔ **Parabolic domain coarsening law**
    *   *Operator Role:* Both obey $\langle R^2\rangle(t) = \langle R^2\rangle(0) + c\,M\sigma\,t$ (Allen-Cahn coarsening), where $c$ is a dimensionless geometric constant of order unity determined by the network topology. The growth exponent $\alpha = 1$ (in $\langle R^2\rangle \propto t^\alpha$) is a shared universality-class invariant of non-conserved curvature-driven coarsening.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A — Grain growth.** The classical theory of curvature-driven grain growth (Mullins, 1956) models the 2D grain boundary network as a collection of one-dimensional interfaces whose normal velocity is proportional to local curvature, driven by the reduction of total boundary energy. Each boundary segment evolves as:

```math
v_n = -M_{\mathrm{gb}}\,\gamma\,\kappa
```

where $M_{\mathrm{gb}}$ is the grain boundary mobility $[\mathrm{m}^3/(\mathrm{J\cdot s})]$, $\gamma$ is the boundary energy per unit length $[\mathrm{J/m}]$, and $\kappa$ is the local curvature $[\mathrm{m}^{-1}]$. This equation is a gradient flow of the total boundary energy $\mathcal{F}_{\mathrm{gb}} = \oint_{\text{all GBs}}\gamma\,ds$:

```math
v_n = -M_{\mathrm{gb}}\,\frac{\delta\mathcal{F}_{\mathrm{gb}}}{\delta X}
```

At triple junctions where three grain boundaries meet, the Herring (1952) condition minimizes total boundary energy with respect to junction position:

```math
\sum_{i=1}^{3}\gamma_i\,\hat{\mathbf{n}}_i = \mathbf{0}
```

For isotropic $\gamma$, this yields 120° equilibrium angles. Applying the Gauss-Bonnet theorem to a grain $\Omega_n$ with $n$ sides and 120° interior angles at each vertex, with exterior angles $\alpha_i = \pi - 2\pi/3 = \pi/3$:

```math
\frac{dA_n}{dt} = -M_{\mathrm{gb}}\,\gamma\oint_{\partial\Omega_n}\kappa\,ds = -M_{\mathrm{gb}}\,\gamma\!\left[2\pi - \sum_{i=1}^{n}\!\left(\pi - \frac{2\pi}{3}\right)\right] = -\frac{M_{\mathrm{gb}}\,\gamma\,\pi}{3}(6-n)
```

This is the von Neumann-Mullins relation: grains with $n>6$ grow, $n<6$ shrink, $n=6$ is neutral. Hillert (1965) derived the mean-field size evolution law for a grain of radius $R$ in a network with mean radius $\bar{R}$:

```math
\frac{dR}{dt} = M_{\mathrm{gb}}\,\gamma\!\left(\frac{1}{\bar{R}} - \frac{1}{R}\right)
```

yielding a self-similar size distribution from the conservation equation:

```math
\frac{\partial P(R,t)}{\partial t} + \frac{\partial}{\partial R}\!\left[P(R,t)\cdot M_{\mathrm{gb}}\,\gamma\!\left(\frac{1}{\bar{R}} - \frac{1}{R}\right)\right] = 0
```

whose self-similar solution $P(R,t) = \bar{R}^{-1}f(R/\bar{R})$ is the Hillert distribution.

**Silo B — Magnetic domain coarsening.** In a ferromagnetic thin film with perpendicular magnetic anisotropy, the domain wall positions govern the magnetic domain pattern. In the overdamped thin-wall limit of the Landau-Lifshitz-Gilbert equation (valid when the wall width $\Delta = \sqrt{A/K_u}$ is much smaller than the domain size and the Gilbert damping $\alpha$ is not too small), the domain wall displacement $u(x,t)$ satisfies the standard domain wall equation of motion (Hubert & Schäfer, 1998):

```math
\beta\,\frac{\partial u}{\partial t} = \sigma_w\,\frac{\partial^{2} u}{\partial x^{2}} + 2M_s H_{\mathrm{ext}}
```

where $\beta = 2M_s\alpha/(\gamma_{\mathrm{LL}}\Delta)$ is the viscous damping per unit wall area, $\sigma_w = 4\sqrt{AK_u}$ is the domain wall energy per unit area, $M_s$ is the saturation magnetization, $A$ is the exchange stiffness, $K_u$ is the perpendicular anisotropy constant, and $H_{\mathrm{ext}}$ is the applied field component perpendicular to the wall plane. In the zero-field overdamped limit, the normal velocity of the wall is:

```math
v_n = \frac{\sigma_w}{\beta}\,\kappa = M_{\mathrm{dw}}\,\sigma_w\,\kappa
```

where $M_{\mathrm{dw}} = 1/\beta = \gamma_{\mathrm{LL}}\Delta/(2M_s\alpha)$ is the domain wall mobility. This is a gradient flow of the total domain energy $\mathcal{F}_{\mathrm{dom}} = \oint_{\text{all DWs}}\sigma_w\,ds - 2M_s H_{\mathrm{ext}}\!\int_{\Omega^\uparrow}\!dA$:

```math
v_n = -M_{\mathrm{dw}}\,\frac{\delta\mathcal{F}_{\mathrm{dom}}}{\delta X}
```

At domain wall vertices where three walls meet (in multi-state domain patterns arising from cubic magnetic anisotropy, polycrystalline films with grain-dependent anisotropy axes, or engineered multi-domain structures), the Neumann junction condition follows from variational minimization:

```math
\sum_{i=1}^{3}\sigma_i\,\hat{\mathbf{n}}_i = \mathbf{0}
```

yielding 120° angles for isotropic $\sigma_w$, identical to the Herring condition. The Gauss-Bonnet theorem applied to a domain $\Omega_n$ with $n$ sides gives the identical von Neumann-Mullins growth law for magnetic domains:

```math
\frac{dA_n}{dt} = -\frac{M_{\mathrm{dw}}\,\sigma_w\,\pi}{3}(6-n)
```

The Hillert mean-field conservation equation for the domain size distribution is:

```math
\frac{\partial P(R,t)}{\partial t} + \frac{\partial}{\partial R}\!\left[P(R,t)\cdot M_{\mathrm{dw}}\,\sigma_w\!\left(\frac{1}{\bar{R}} - \frac{1}{R}\right)\right] = 0
```

with the same self-similar Hillert solution $P(R,t) = \bar{R}^{-1}f(R/\bar{R})$.

**Bridge.** The structural isomorphism is exact in the overdamped, zero-field, thin-wall limit. The curvature flow operator, the variational gradient-flow structure, the Herring/Neumann junction conditions, the Gauss-Bonnet topological growth law, and the Hillert mean-field coarsening theory are identical mathematical objects in both systems, identified under the single parameter correspondence:

```math
M_{\mathrm{gb}}\,\gamma_{\mathrm{gb}} \quad\longleftrightarrow\quad \frac{\sigma_w}{\beta} \equiv M_{\mathrm{dw}}\,\sigma_w
```

Both products have dimensions $[\mathrm{m}^2/\mathrm{s}]$ and serve as the interface diffusivity governing coarsening kinetics. The Allen-Cahn parabolic growth law $\langle R^2\rangle(t) = \langle R^2\rangle(0) + c\,M\sigma\,t$ follows from dimensional analysis applied to the curvature flow equation in both systems, with the same dimensionless constant $c$.

**Where the correspondence breaks down.** (i) Domain wall inertia: the magnetic wall has an effective mass $m_w = 2M_s/(\gamma_{\mathrm{LL}}^2\Delta)$, giving underdamped oscillatory dynamics at high frequencies or short time scales; grain boundaries are always overdamped. (ii) Long-range dipolar (magnetostatic) interactions modify the effective domain wall energy and can drive stripe-to-bubble transitions; grain boundary curvature forces are shorter-ranged. (iii) Spin-transfer torque can drive domain walls independently of curvature, with no direct grain growth analogue (though electromigration-driven boundary migration in metallic interconnects provides a partial parallel).

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Polycrystalline grain growth theory → Thin-film magnetic domain pattern analysis.
*   **Asymmetric Maturity Rationale:** The grain growth community has developed, over 70 years, a mature analytical and statistical toolkit for predicting coarsening kinetics and topological evolution in curvature-driven interface networks: the von Neumann-Mullins topological growth law (Mullins, 1956), the Hillert mean-field coarsening theory (Hillert, 1965), the Lewis-Aboav-Weaire topological relations for face/neighbor statistics, the abnormal grain growth theory for misoriented grains with enhanced mobility, and 3D extensions (MacPherson-Srolovitz, 2007). The magnetic domain community is very mature in individual domain wall dynamics (collective-coordinate models, OOMMF/MuMax3 micromagnetics) and equilibrium domain configuration theory (Kittel stripe period, Kooy-Enz bubble domains), but lacks an analytical framework for predicting the non-equilibrium statistics of domain pattern coarsening: the time-dependent domain width distribution, the coarsening rate constant, and the topological evolution of the wall network. The specific problem class — statistical coarsening of a curvature-driven interface network in 2D — is one where grain growth theory is highly mature and the domain community has no comparable toolkit.
*   **Target Bottleneck Mitigation:** Importing the Hillert mean-field coarsening theory into magnetic domain dynamics provides an analytical, closed-form prediction for the steady-state domain width distribution and the parabolic coarsening rate constant, bypassing expensive micromagnetic simulations (which scale as $O(N^2)$ with dipolar interactions and are practically limited to $\sim 1\;\mu\mathrm{m}^2$ areas). The von Neumann-Mullins relation provides a topological growth rule for predicting which domains grow and which shrink based solely on their neighbor count, enabling analytical models of domain selection processes relevant to bit-patterned media and magnetic memory technologies.
*   **Falsifiable Prediction:** In a Co/Pt multilayer thin film with perpendicular magnetic anisotropy (e.g., $[\mathrm{Co}(0.4\;\mathrm{nm})/\mathrm{Pt}(0.7\;\mathrm{nm})]\times 10$), rapidly quenched from above the Curie temperature to room temperature in zero applied field:
    1.  The domain width distribution $P(R,t)$ will converge to a self-similar form $P(R,t) = \bar{R}^{-1}(t)\,f(R/\bar{R}(t))$ within $10\tau_0$ (where $\tau_0 = \bar{R}_0^2/(M_{\mathrm{dw}}\sigma_w)$ is the initial coarsening time scale), with the Hillert distribution shape $f(\rho)$ having a peak at $\rho \approx 0.9$ and a hard cutoff at $\rho = 2$, as measured by Lorentz TEM or magnetic force microscopy at successive time points.
    2.  The mean square domain width will follow $\langle R^2\rangle(t) = \langle R^2\rangle(0) + K \cdot (\sigma_w/\beta)\cdot t$, where $K$ is a dimensionless constant of order unity (between 0.5 and 2.0) predicted by the Hillert mean-field theory. This parabolic growth law with the SPECIFIC coefficient $K$ must agree with MuMax3 micromagnetic simulations of the same system to within a factor of 2.
    3.  In a pattern with three or more domain types meeting at wall vertices, individual domain area trajectories will satisfy $dA_n/dt = -(M_{\mathrm{dw}}\sigma_w\pi/3)(6-n)$, measurable by tracking domain areas in time-resolved Lorentz TEM. Domains with $n<6$ neighbors must shrink and those with $n>6$ must grow at the predicted rate.
    **Baseline:** Current predictions use either (a) full micromagnetic simulations (computationally expensive, limited in area) or (b) equilibrium theory (Kittel/Kooy-Enz: predicts only the equilibrium domain period, not coarsening kinetics or size distributions). The Hillert-based analytical theory provides the first closed-form prediction of domain size statistics. **Falsification:** If the measured domain width distribution deviates from the Hillert form with Kullback-Leibler divergence $D_{\mathrm{KL}} > 0.3$, or if the growth exponent in $\langle R^2\rangle \propto t^\alpha$ satisfies $\alpha < 0.85$ or $\alpha > 1.15$, or if the predicted coarsening rate constant $K$ disagrees with MuMax3 benchmarks by more than a factor of 2, the prediction is falsified.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"von Neumann-Mullins" AND "magnetic domain wall" AND "coarsening"`
*   `"Hillert distribution" AND "domain coarsening" AND "thin film magnetism"`
*   `"grain growth" AND "domain wall motion" AND "curvature-driven" AND "coarsening kinetics"`
*   `"magnetic domain" AND "topological growth law" AND "triple junction" AND "scaling"`
*   `"Allen-Cahn coarsening" AND "magnetic domain" AND "parabolic growth" AND "self-similar"`