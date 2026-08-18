---
sid_metadata:
  entry_id: "SID-0056"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-rejected"
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
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "Section 3's Silo B curvature-flow equation drops the sign required by its own adjacent gradient-flow equation, and Section 2's domain-wall-mobility formula is algebraically inconsistent with the mobility formula Section 3 actually defines and uses throughout, giving two independently-verifiable wrong equations."
    failed_checks: ["Check 1: Silo B's zero-field curvature-flow equation has a sign inconsistent with the shared operator claimed in Section 1 and with Silo B's own next equation", "Check 2: Section 2's stated domain-wall mobility formula for M_dw is not algebraically equal to the M_dw formula Section 3 defines and uses in every subsequent Silo B equation"]
    flagged_checks: ["Check 4: falsifiable prediction #3 (and implicitly prediction #1) requires a multi-domain-type network with true triple junctions, a configuration Section 2 restricts to special conditions absent from the proposed [Co/Pt]x10 test system", "Check 4c: prior-art recognition (advisory) — the von Neumann-Mullins relation's own history of cross-system extension from soap froths to grain growth"]
    quoted_evidence: ["v_n = σ_w/β · κ = M_dw σ_w κ  [Section 3, Silo B, 'zero-field overdamped limit']", "v_n = -M_dw · δF_dom/δX  [Section 3, Silo B, immediately following equation]", "M_dw = γ_LL·Δ·α / [2M_s(1+α²)]  [Section 2, 'Grain boundary mobility ↔ Domain wall mobility' entry]", "M_dw = 1/β = γ_LL·Δ / (2M_s·α)  [Section 3, Silo B]"]
    stage_3_watch_items: ["Verify Silo B's zero-field curvature-flow equation and the conflicting Section 2 vs. Section 3 M_dw formulas against the cited source (Hubert & Schäfer, 1998) to determine whether these are transcription slips or a genuine derivation error", "Confirm whether the proposed test system ([Co(0.4nm)/Pt(0.7nm)]x10, quenched from above T_C, zero field) is expected to coarsen into a true multi-domain-type network with triple junctions, or a two-state up/down pattern — predictions #1 and #3 depend on the former; prediction #2's R^2 ∝ t scaling is more likely to survive regardless, since it is a general property of non-conserved curvature-driven coarsening independent of morphology", "Given the entry's own Section 3 caveat that dipolar interactions can drive stripe-to-bubble transitions in exactly this class of PMA multilayer, check whether the proposed film's thickness/anisotropy regime actually favors the grain-like cellular morphology the Hillert-distribution comparison assumes", "Search for existing literature explicitly connecting Hillert/von-Neumann-Mullins grain-growth statistics to magnetic domain coarsening or other cellular-network coarsening (foams, biological tissue) to assess novelty of this specific pairing against the broader, already-recognized 'curvature-driven 2D network coarsening' framework", "Resolve the 'Mean grain radius R̄ ↔ Mean domain width d̄' labeling in Section 2 — d̄ is never used again, R̄ (radius) is used throughout instead, and radius vs. width is not a free notational choice once the quantitative predictions in Section 4 are at stake"]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "FLAG"
    verdict_rationale: "The claimed curvature-flow, von Neumann-Mullins, junction-balance, and Hillert correspondences are demonstrated in the body, but the entry contains sign-convention and mobility-notation inconsistencies that need clarification."
    failed_checks: []
    flagged_checks:
      - "Check 1: Section 1 and Silo A use a negative curvature-flow sign, while Silo B writes the same law with a positive sign without stating a curvature/normal convention."
      - "Check 2: The vocabulary matrix defines domain-wall mobility as M_dw = sigma_w / beta, which is the interface diffusivity, and also gives an M_dw formula inconsistent with Section 3's M_dw = 1 / beta."
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify whether the sign convention for curvature kappa and interface normal is intended to differ between Silo A and Silo B; Section 1 claims v_n = -M sigma kappa, while Section 3 Silo B writes v_n = (sigma_w / beta) kappa."
      - "Verify the intended definition of domain-wall mobility: Section 2 says M_dw = sigma_w / beta and M_dw = gamma_LL Delta alpha / [2 M_s (1 + alpha^2)], while Section 3 says M_dw = 1 / beta = gamma_LL Delta / (2 M_s alpha)."
      - "Search for prior work applying von Neumann-Mullins or Hillert grain-growth statistics to magnetic-domain coarsening, or treating magnetic-domain coarsening as standard Allen-Cahn/nonconserved phase-ordering kinetics."
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "The vocabulary matrix assigns the same domain-wall mobility symbol incompatible dimensional roles and expressions, and maps a 2D line energy density to a 3D wall energy per unit area without a stated film thickness."
    failed_checks: ["Check 2: M_gb ↔ M_dw=σ_w/β is a mobility-to-diffusivity category error, and M_dw is assigned mutually inconsistent formulas."]
    flagged_checks: ["Check 1: the magnetic domain-wall equation is the linearized small-slope form while the bridge claims exact curvature-flow isomorphism without stating the linearization."]
    quoted_evidence:
      - '**Grain boundary mobility $M_{\mathrm{gb}}$** ↔ **Domain wall mobility $M_{\mathrm{dw}} = \sigma_w/\beta$**'
      - 'The grain growth mobility has units $[\mathrm{m}^3/(\mathrm{J\cdot s})]$; the domain wall mobility $M_{\mathrm{dw}} = \gamma_{\mathrm{LL}}\Delta\alpha/[2M_s(1+\alpha^2)]$ from the LLG equation maps to the same dimensional structure under the identification $M_{\mathrm{gb}}\gamma \leftrightarrow \sigma_w/\beta$.'
      - '$M_{\mathrm{dw}} = 1/\beta = \gamma_{\mathrm{LL}}\Delta/(2M_s\alpha)$ is the domain wall mobility.'
      - '**Grain boundary energy $\gamma_{\mathrm{gb}}$** ↔ **Domain wall energy density $\sigma_w$**'
      - 'Both serve as the surface energy density in the total interface energy functional $\mathcal{F} = \oint\sigma\,ds$.'
    stage_3_watch_items:
      - "Probe whether the grain-growth/magnetic-domain-coarsening analogy is already documented in materials physics or micromagnetics."
      - "Probe whether Co/Pt perpendicular-anisotropy films actually exhibit the triple-junction wall vertices required for the von Neumann-Mullins/Herring claims."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "The entry applies the 3-connected von Neumann-Mullins topological growth law to a two-state Ising-like system (perpendicular magnetic anisotropy), which topologically cannot support the three-way domain wall vertices required by the model."
    failed_checks: ["Check 1: Equation Validity"]
    flagged_checks: ["Check 4: Transfer and Falsifiability"]
    quoted_evidence: ["In a Co/Pt multilayer thin film with perpendicular magnetic anisotropy (e.g., $[\\mathrm{Co}(0.4\\;\\mathrm{nm})/\\mathrm{Pt}(0.7\\;\\mathrm{nm})]\\times 10$) [...] In a pattern with three or more domain types meeting at wall vertices, individual domain area trajectories will satisfy $dA_n/dt = -(M_{\\mathrm{dw}}\\sigma_w\\pi/3)(6-n)$"]
    stage_3_watch_items: ["Evaluate novelty: Curvature-driven coarsening mapping between grain boundaries and magnetic domains (Allen-Cahn / Model A dynamics) is a canonical textbook isomorphism in materials science kinetics (e.g., Balluffi, Allen, Carter)."]
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a fatal sign error in its Silo B curvature flow equation and an internally contradictory, dimensionally inconsistent mapping of the domain wall mobility."
    failed_checks:
      - "Check 1: Sign error in the magnetic domain wall velocity equation contradicts the stated gradient flow and von Neumann-Mullins law."
      - "Check 2: Category error mapping grain boundary mobility to a diffusivity, compounded by contradictory definitions of $M_{dw}$."
    flagged_checks: []
    quoted_evidence:
      - "v_n = \\frac{\\sigma_w}{\\beta}\\,\\kappa = M_{\\mathrm{dw}}\\,\\sigma_w\\,\\kappa"
      - "Domain wall mobility M_{\\mathrm{dw}} = \\sigma_w/\\beta"
    stage_3_watch_items:
      - "Prior Art: Curvature-driven coarsening (Allen-Cahn universality class) is a standard concept; verify if the explicit mapping of grain growth statistical laws to magnetic domains is novel."
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "Check 2 contains a genuine mathematical type/definition error: the vocabulary matrix identifies domain-wall mobility as sigma_w/beta, while the entry's own equations define the mobility as 1/beta and sigma_w/beta as the mobility-weighted interfacial energy coefficient."
    failed_checks: ["Check 2: domain wall mobility is misdefined in the vocabulary mapping"]
    flagged_checks: ["Check 1: the magnetic-domain triple-junction/von Neumann construction is restricted in the text to exotic multi-state patterns rather than the stated two-state perpendicular-anisotropy Co/Pt setting"]
    quoted_evidence: ["**Grain boundary mobility $M_{\\mathrm{gb}}$** ↔ **Domain wall mobility $M_{\\mathrm{dw}} = \\sigma_w/\\beta$**"]
    stage_3_watch_items: ["Probe whether the claimed Hillert size-distribution correspondence is actually established for two-phase magnetic-domain coarsening rather than merely asserted by writing down the same mean-field equation.", "Probe the applicability of the triple-junction and von Neumann-Mullins correspondence to the stated perpendicular-anisotropy Co/Pt systems, since the entry itself invokes three-or-more-state magnetic patterns only as special constructions.", "Probe the claimed asymmetric maturity and the assertion that the magnetic-domain community lacks a comparable analytical coarsening-statistics framework."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "REJECT"
    verdict_rationale: "The submission contains two fatal mathematical inconsistencies: a sign error in the curvature-flow velocity for the magnetic-domain equation and a dimensional/category mismatch between grain-boundary energy (per length) and domain-wall energy (stated per area) that breaks the claimed parameter identification."
    failed_checks:
      - "Check 1: Equation sign inconsistency between Silo A and Silo B curvature-flow expressions"
      - "Check 2: Vocabulary/dimensionality category error mapping domain wall energy per unit area to grain boundary energy per unit length without nondimensionalization or thickness factor"
    flagged_checks: []
    quoted_evidence:
      - "\"v_n = -M_{\\mathrm{gb}}\\,\\gamma\\,\\kappa\""
      - "\"\\beta\\,\\frac{\\partial u}{\\partial t} = \\sigma_w\\,\\frac{\\partial^{2} u}{\\partial x^{2}} + 2M_s H_{\\mathrm{ext}}\""
      - "\"v_n = \\frac{\\sigma_w}{\\beta}\\,\\kappa = M_{\\mathrm{dw}}\\,\\sigma_w\\,\\kappa\""
      - "\"\\gamma is the boundary energy per unit length $[\\mathrm{J/m}]$\""
      - "\"\\sigma_w = 4\\sqrt{AK_u} is the domain wall energy per unit area\""
    stage_3_watch_items:
      - "Verify the sign convention and derivation of the curvature term from the overdamped LLG thin-wall reduction; check whether the correct gradient-flow sign is negative (energy-reducing) and whether the manuscript's positive sign is a typographical error or a deeper derivation mistake."
      - "Check the dimensional definition of \\sigma_w in the thin-film context: confirm whether the authors mean domain-wall energy per unit length (J/m) after multiplying by film thickness, or per unit area (J/m^2); require explicit inclusion of film thickness or nondimensionalization to justify the identification $M_{\\mathrm{gb}}\\gamma_{\\mathrm{gb}} \\leftrightarrow \\sigma_w/\\beta$."
      - "Examine the thin-wall mobility definitions and units: confirm consistency of $\\beta$, $M_{\\mathrm{dw}}=1/\\beta$, and the product $M_{\\mathrm{dw}}\\sigma_w$ having units $[\\mathrm{m}^2/\\mathrm{s}]$ as claimed; flag any missing geometric factors (film thickness) or mis-specified units."
      - "Check the derivation that reduces $\\beta\\,\\partial_t u = \\sigma_w\\,\\partial_x^2 u + 2M_s H_{\\mathrm{ext}}$ to a normal-velocity curvature law; ensure curvature sign and factor conventions are consistent with the variational gradient-flow statement elsewhere in the text."
      - "Probe whether the authors implicitly assume a conversion factor (film thickness or wall area-to-length mapping) when equating 'domain wall energy per unit area' to the 1D interface energy used in the Mullins/Hillert framework; request explicit statement if present in source materials."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "PASS"
    verdict_rationale: "All four checks are satisfied: equations are of matching class and support the claimed operators, vocabulary pairs are type-compatible with shared structure named, all listed vectors are demonstrated by explicit equations/derivations in Sections 1 and 3, and the transfer is asymmetric with specific measurable falsification criteria."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Applicability of triple-junction (Herring/Neumann) vector to standard two-state PMA films, which typically lack vertices of three or more walls; the entry itself restricts this case.", "Internal sign convention for curvature κ (negative in Silo A and gradient-flow statements, positive in the zero-field domain-wall reduction); verify consistency under chosen normal orientation."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "PASS"
    verdict_rationale: "All five correspondence vectors are demonstrated with matching parabolic curvature-flow operators, junction conditions, and Hillert kinetics; no equation-class mismatch or vocabulary category error."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Bibliometric check: Allen-Cahn Model A / curvature-driven coarsening covering grain growth and magnetic domains is textbook in phase-ordering literature (Bray 1994) – verify novelty of Hillert/von Neumann-Mullins transfer specifically", "Scope check: dipolar interactions and wall inertia breakdown noted in entry – confirm quantitative limits for Co/Pt thin-wall overdamped mapping"]
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

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Silo B's stated zero-field equation "v_n = σ_w/β · κ = M_dw σ_w κ" omits the negative sign present in the shared operator Section 1 claims for both systems ("v_n = -Mσκ") and present in Silo A's parallel equation ("v_n = -M_gbγκ"); it also directly contradicts Silo B's own next equation, "v_n = -M_dw δF_dom/δX," since the standard first-variation identity δ(∮σds)/δX = +σκ — the same identity Silo A's own equations rely on — would give v_n = -M_dwσ_wκ, not the positive form shown two lines above.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — the "Grain boundary mobility ↔ Domain wall mobility" entry states "M_dw = γ_LLΔα/[2M_s(1+α²)]," which is not algebraically equal to "M_dw = 1/β = γ_LLΔ/(2M_sα)" defined in Section 3 and used in every subsequent Silo B equation (the two expressions even diverge oppositely as α→0: one vanishes, the other blows up), so the vocabulary matrix asserts a shared operator role using a mobility expression inconsistent with the one actually doing the work in Section 3.
- **CHECK 3 (Correspondence Vector Support):** PASS — all five listed vectors are demonstrated with matching equations in both Silos in Section 3: the curvature-flow operator (Silo A and B, notwithstanding the Check 1 sign defect in one displayed instance), the von Neumann-Mullins growth law (explicit Gauss-Bonnet derivation for Silo A, directly parallel and correctly-signed result stated for Silo B), the Herring/Neumann junction condition (both Silos), the parabolic ⟨R²⟩∝t coarsening law (Section 2 and the Section 3 Bridge, via the shared diffusivity), and the Hillert self-similar distribution (matching PDEs and solutions for both Silos).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — the transfer direction (grain-growth topology/statistics → magnetic domain coarsening statistics) is not stated backwards, and predictions 1–3 name specific measurable quantities and numeric falsification thresholds (KL divergence > 0.3, growth exponent outside [0.85, 1.15], K off by >2×) rather than a generic template non-prediction; however, prediction #3 explicitly requires domain patterns "with three or more domain types meeting at wall vertices," a configuration Section 2 restricts to cubic anisotropy, grain-dependent easy axes, or engineered multi-domain structures — none of which is stated for the proposed [Co(0.4nm)/Pt(0.7nm)]×10 test system — and prediction #1's Hillert-distribution-shape claim rests on the same discrete, multi-grain-like topology. Advisory (4c): the von Neumann-Mullins relation's own history — derived for soap froths, then extended by Mullins to grain growth — is a recognized precedent for exactly this kind of cross-system extension of curvature-driven coarsening theory.

#### Stage 3 Watch Items
- Verify Silo B's zero-field curvature-flow equation and the conflicting Section 2 vs. Section 3 mobility formulas against the cited source (Hubert & Schäfer, 1998) to determine whether these are transcription slips or a genuine derivation error.
- Confirm whether the proposed test system, quenched from above the Curie temperature in zero field, is expected to coarsen into a true multi-domain-type network with triple junctions or a two-state up/down pattern — predictions #1 and #3 depend on the former; prediction #2's growth-exponent scaling is more likely to survive regardless, since it is a general property of non-conserved curvature-driven coarsening independent of morphology.
- Given the entry's own Section 3 caveat that dipolar interactions can drive stripe-to-bubble transitions in exactly this class of PMA multilayer, check whether the proposed film's thickness/anisotropy regime actually favors the grain-like cellular morphology the Hillert-distribution comparison assumes.
- Search for existing literature explicitly connecting Hillert/von-Neumann-Mullins grain-growth statistics to magnetic domain coarsening or other cellular-network coarsening (foams, biological tissue) to assess the novelty of this specific pairing against the broader, already-recognized "curvature-driven 2D network coarsening" framework.
- Resolve the "Mean grain radius R̄ ↔ Mean domain width d̄" labeling in Section 2 — d̄ is never used again, R̄ (radius) is used throughout instead, and radius vs. width is not a free notational choice once the quantitative predictions in Section 4 are at stake.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The equations are curvature-flow/gradient-flow equations in both silos and support the claimed structural class, but Section 1 and Silo A state the law as “$v_n = -M\sigma\kappa$,” whereas Silo B states “$v_n = \frac{\sigma_w}{\beta}\,\kappa = M_{\mathrm{dw}}\,\sigma_w\,\kappa$” without explicitly reconciling the opposite sign through a stated convention for curvature or interface normal.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Most mappings are type-compatible, but the pair “**Grain boundary mobility $M_{\mathrm{gb}}$** ↔ **Domain wall mobility $M_{\mathrm{dw}} = \sigma_w/\beta$**” conflates a mobility with the product $M_{\mathrm{dw}}\sigma_w$, i.e. the interface diffusivity; additionally, Section 2 gives “$M_{\mathrm{dw}} = \gamma_{\mathrm{LL}}\Delta\alpha/[2M_s(1+\alpha^2)]$,” which conflicts with Section 3’s “$M_{\mathrm{dw}} = 1/\beta = \gamma_{\mathrm{LL}}\Delta/(2M_s\alpha)$.”
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors are demonstrated: the overdamped curvature-flow operator is given in both silos in Section 3; the von Neumann-Mullins/Gauss-Bonnet law is derived/stated for both silos in Section 3; the Herring/Neumann angle-balance condition is given in both silos in Section 3; the parabolic Allen-Cahn coarsening law appears in Section 2 and the Bridge; and the Hillert mean-field self-similar distribution is given by conservation equations in both silos in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction from grain-growth statistical theory to magnetic-domain coarsening is stated asymmetrically and tied to a specific toolkit gap. The prediction names measurable distribution shape, growth exponent, coarsening-rate coefficient, topological area law, experimental/simulation benchmarks, and explicit falsification thresholds. Advisory: Stage 3 should check for prior art in standard Allen-Cahn/curvature-driven coarsening analogies.

#### Stage 3 Watch Items
- Verify whether the sign convention for $\kappa$ and the interface normal is intended to differ between the two silos, since Section 1 uses $v_n = -M\sigma\kappa$ while Section 3 Silo B writes $v_n = (\sigma_w/\beta)\kappa$.
- Verify the intended definition of domain-wall mobility: Section 2 uses $M_{\mathrm{dw}} = \sigma_w/\beta$ and $M_{\mathrm{dw}} = \gamma_{\mathrm{LL}}\Delta\alpha/[2M_s(1+\alpha^2)]$, whereas Section 3 uses $M_{\mathrm{dw}} = 1/\beta = \gamma_{\mathrm{LL}}\Delta/(2M_s\alpha)$.
- Search for prior literature applying von Neumann-Mullins, Hillert, or Allen-Cahn grain-growth statistics to magnetic-domain coarsening, especially in perpendicular-anisotropy thin films.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The Silo B wall equation is the linearized small-slope form $\beta\,u_t = \sigma_w u_{xx}$; the subsequent identification of $u_{xx}$ with the full curvature $\kappa$ without stating the small-slope approximation weakens the claimed exact isomorphism.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "Grain boundary mobility $M_{\mathrm{gb}}$ ↔ Domain wall mobility $M_{\mathrm{dw}} = \sigma_w/\beta$" is a category error because $M_{\mathrm{gb}}$ has units $[\mathrm{m}^3/(\mathrm{J\cdot s})]$ while $\sigma_w/\beta$ has units $[\mathrm{m}^2/\mathrm{s}]$, and Section 3 instead defines $M_{\mathrm{dw}}=1/\beta$; the energy-density mapping $\gamma_{\mathrm{gb}}\,[\mathrm{J/m}] \leftrightarrow \sigma_w\,[\mathrm{J/m}^2]$ also lacks a stated film thickness or unit-thickness convention.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors are at least nominally demonstrated in the body by displayed equations or derivations: curvature-flow operator, von Neumann-Mullins Gauss-Bonnet law, Herring/Neumann junction condition, parabolic Allen-Cahn coarsening, and Hillert mean-field distribution.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric under the entry's stated rationale, and the prediction names quantitative thresholds (KL divergence, growth exponent bounds, coefficient factor of 2).

#### Stage 3 Watch Items
- Check whether the grain-growth/magnetic-domain-coarsening analogy is already documented in materials physics or micromagnetics.
- Probe whether Co/Pt perpendicular-anisotropy films actually exhibit the triple-junction wall vertices required for the von Neumann-Mullins/Herring claims.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The text claims "In a Co/Pt multilayer thin film with perpendicular magnetic anisotropy (e.g., $[\mathrm{Co}(0.4\;\mathrm{nm})/\mathrm{Pt}(0.7\;\mathrm{nm})]\times 10$) [...] In a pattern with three or more domain types meeting at wall vertices, individual domain area trajectories will satisfy $dA_n/dt = -(M_{\mathrm{dw}}\sigma_w\pi/3)(6-n)$", but a perpendicular magnetic anisotropy film is a two-state system (magnetization points up or down) which topologically cannot form three-way domain wall vertices (a two-color map cannot have vertices of degree 3), meaning the 3-connected von Neumann-Mullins cellular network equation cannot physically model the specified system.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped terms belong to compatible mathematical categories (1D interface to 1D interface, scalar energy density to scalar energy density, gradient flow coefficient to gradient flow coefficient) and identify matching operational roles.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five correspondence vectors listed in the YAML (overdamped flow operator, von Neumann-Mullins law, triple junction balance, parabolic Allen-Cahn kinetics, and Hillert distribution) are actively demonstrated with mathematical equations and derivations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The methodological transfer proposes a specific falsifiable prediction and is properly asymmetric. However, the foundational isomorphism mapping grain boundary motion to magnetic domain wall motion via Allen-Cahn curvature-driven dynamics is a canonical, widely taught textbook analogy in materials science.

#### Stage 3 Watch Items
- Evaluate novelty: Curvature-driven coarsening mapping between grain boundaries and magnetic domains (Allen-Cahn / Model A dynamics) is a canonical textbook isomorphism in materials science kinetics (e.g., Balluffi, Allen, Carter). Verify if the specific application of Hillert mean-field theory to magnetic domains provides sufficient novel utility beyond the well-known underlying analogy.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry states `v_n = \frac{\sigma_w}{\beta}\,\kappa = M_{\mathrm{dw}}\,\sigma_w\,\kappa`, but this positive sign contradicts the standard mean curvature flow (which shrinks convex domains) and the entry's own gradient flow equation `v_n = -M_{\mathrm{dw}}\,\frac{\delta\mathcal{F}_{\mathrm{dom}}}{\delta X}` (where $\delta\mathcal{F}/\delta X = \sigma_w\kappa$) and von Neumann-Mullins derivation `dA_n/dt = -\frac{M_{\mathrm{dw}}\,\sigma_w\,\pi}{3}(6-n)` which requires $v_n = -M_{\mathrm{dw}}\sigma_w\kappa$.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping `Grain boundary mobility $M_{\mathrm{gb}}$ ↔ Domain wall mobility $M_{\mathrm{dw}} = \sigma_w/\beta$` pairs a kinetic coefficient (mobility) with a diffusivity, as $\sigma_w/\beta$ has dimensions of $[m^2/s]$. Additionally, the entry contradicts itself by later stating in Section 3 that `where $M_{\mathrm{dw}} = 1/\beta = \dots$ is the domain wall mobility`.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed correspondence vectors (curvature flow, von Neumann-Mullins law, triple junction balance, parabolic kinetics, Hillert distribution) are explicitly demonstrated with equations in Sections 2 and 3, though the math contains the sign and definition errors noted above.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric, providing analytical statistical tools to a field lacking them, and the falsifiable prediction includes specific, measurable thresholds (KL divergence > 0.3, growth exponent bounds).

#### Stage 3 Watch Items
- Prior Art: The mapping of curvature-driven grain growth to magnetic domain coarsening relies on the shared Allen-Cahn universality class; verify whether this specific cross-domain application of von Neumann-Mullins and Hillert theories is previously published.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
* **CHECK 1 (Equation Validity):** FLAG — The stated magnetic curvature-flow and parabolic equations are internally usable in the explicitly imposed overdamped limit, but the triple-junction/von Neumann construction is only presented for special multi-state magnetic patterns rather than the main Co/Pt perpendicular-anisotropy setting.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping pair "**Grain boundary mobility $M_{\mathrm{gb}}$** ↔ **Domain wall mobility $M_{\mathrm{dw}} = \sigma_w/\beta$**" is mathematically inconsistent with the entry's own later definition $M_{\mathrm{dw}}=1/\beta$; $\sigma_w/\beta$ is instead the mobility-times-wall-energy coefficient appearing in the curvature-flow velocity.
* **CHECK 3 (Correspondence Vector Support):** PASS — The body explicitly supplies curvature-flow, von Neumann-Mullins/Gauss-Bonnet growth, Herring/Neumann angle balance, parabolic $\langle R^2\rangle\propto t$ kinetics, and Hillert-type self-similar distribution equations on both sides.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer direction is explicitly justified as grain-growth theory to magnetic-domain analysis, and the prediction gives measurable distributional, exponent, and rate-constant thresholds with explicit falsification criteria; no prior-art assessment is used as a rejection.

#### Stage 3 Watch Items
* Probe whether the claimed Hillert size-distribution correspondence is actually established for two-phase magnetic-domain coarsening rather than merely asserted by writing down the same mean-field equation.
* Probe the applicability of the triple-junction and von Neumann-Mullins correspondence to the stated perpendicular-anisotropy Co/Pt systems, since the entry itself invokes three-or-more-state magnetic patterns only as special constructions.
* Probe the claimed asymmetric maturity and the assertion that the magnetic-domain community lacks a comparable analytical coarsening-statistics framework.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The submission asserts the grain-growth curvature law `v_n = -M_{\mathrm{gb}}\,\gamma\,\kappa` but for the magnetic-domain reduction it writes `\beta\,\frac{\partial u}{\partial t} = \sigma_w\,\frac{\partial^{2} u}{\partial x^{2}} + 2M_s H_{\mathrm{ext}}` and then claims `v_n = \frac{\sigma_w}{\beta}\,\kappa = M_{\mathrm{dw}}\,\sigma_w\,\kappa`; this produces a **sign mismatch** (the grain-growth flow is energy-decreasing with a negative sign, whereas the magnetic expression is presented with a positive curvature term), which is a mathematical inconsistency in the claimed identical curvature-flow operator.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The entry states `\gamma is the boundary energy per unit length [J/m]` while also stating `\sigma_w = 4\sqrt{AK_u} is the domain wall energy per unit area`; mapping these directly without an explicit thickness or conversion is a **category/dimensionality error** (per-length vs per-area), invalidating the claimed direct identification of interface energies and the product identification $M_{\mathrm{gb}}\gamma_{\mathrm{gb}} \leftrightarrow \sigma_w/\beta$.
- **CHECK 3 (Correspondence Vector Support):** PASS — Each listed correspondence vector (overdamped curvature flow operator; von Neumann–Mullins Gauss–Bonnet growth law; Herring/Neumann triple-junction angle balance; parabolic Allen–Cahn coarsening; Hillert mean-field size distribution) is explicitly presented in the body with equations or derivations (see Section 3: Mullins relation, von Neumann–Mullins area law, Hillert PDE, and the analogous magnetic-domain equations).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (grain growth → magnetic domains) is plausibly asymmetric as argued; the submission provides concrete, falsifiable experimental benchmarks (self-similar distribution convergence time, KL divergence threshold, growth-exponent bounds, and factor-of-two agreement with micromagnetic benchmarks). Prior-art analogies (Allen–Cahn/mean-curvature flow correspondences) are noted in the text and should be checked at Stage 3 as advisory.

#### Stage 3 Watch Items
- Verify the sign and derivation of the curvature term in the thin-wall overdamped LLG reduction; confirm whether the manuscript's positive curvature coefficient is a typographical slip or a derivation error.
- Require explicit dimensional bookkeeping for domain-wall energy: clarify whether `\sigma_w` is intended per unit length (J/m) after multiplying by film thickness, or per unit area (J/m^2); if the latter, supply the missing geometric factor used to convert to the 1D interface energy.
- Confirm units and definitions of `\beta` and `M_{\mathrm{dw}}` and ensure the product `M_{\mathrm{dw}}\sigma_w` indeed has units `[m^2/s]` as claimed.
- Check the thin-wall limit assumptions (wall width, damping, neglect of dipolar fields) used to justify the exactness of the isomorphism; ensure the limits are physically and mathematically consistent for the proposed experiments.
- Examine whether the submission implicitly relies on prior canonical analogies (Allen–Cahn ↔ curvature flow) and whether those are adequately cited and distinguished from the novel claims.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos present overdamped mean-curvature flow of the same class (\(v_n \propto \kappa\)), with matching gradient-flow structure, Gauss-Bonnet/von Neumann-Mullins derivation, and Hillert conservation equation; no class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type (interfaces, energy densities, kinetic coefficients, angle-balance conditions, body-force terms, mean radii, coarsening laws) and the Operator Role statements name the shared operator or variational identity rather than mere analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors (overdamped curvature-flow operator, von Neumann-Mullins growth law, Herring/Neumann angle balance, parabolic Allen-Cahn kinetics, Hillert self-similar distribution) are derived with explicit equations in Sections 1 and 3 for both silos.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric (grain-growth statistical toolkit is mature for network coarsening while magnetic-domain community lacks the corresponding mean-field/topological framework); predictions supply concrete observables (Hillert shape parameters, growth exponent bounds, rate-constant factor-of-two window, KL divergence threshold) that can fail.

#### Stage 3 Watch Items
- Applicability of triple-junction (Herring/Neumann) vector to standard two-state PMA films, which typically lack vertices of three or more walls; the entry itself restricts this case.
- Internal sign convention for curvature \(\kappa\) (negative in Silo A and gradient-flow statements, positive in the zero-field domain-wall reduction); verify consistency under chosen normal orientation.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos present overdamped mean-curvature flow v_n = -Mσ κ as gradient flow v_n = -M δF/δX and Gauss-Bonnet derivation dA_n/dt = -Mσ π/3 (6-n); equations are correctly attributed to Mullins/Herring and Hubert & Schäfer LLG thin-wall limit and share parabolic class.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All pairings map compatible types: interface ↔ interface, energy density ↔ energy density (F = ∮σ ds, δF/δX = σκ), mobility ↔ mobility (M_gb ↔ M_dw=1/β), junction condition ↔ junction condition (Σσ_i n̂_i=0 →120°), body-force ↔ body-force (M_gb ΔE_stored ↔ M_dw 2M_s H_ext), length scale ↔ length scale (R̄ ↔ d̄ in dR/dt = Mσ(1/R̄-1/R)), kinetic law ↔ kinetic law (<R^2> ∝ Mσ t) with explicit shared structure.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors demonstrated in body: overdamped_curvature_flow_operator_v_n_eq_Msigma_kappa (Sec 3 v_n equations both silos), von_neumann_mullins_gauss_bonnet_growth_law_dA_dt_n (Sec 3 dA_n/dt derivation), herring_neumann_triple_junction_angle_balance_120deg (Sec 3 Σσ_i n̂_i=0), parabolic_allen_cahn_coarsening_kinetics_R2_linear_in_t (Sec 1, 2, 3 bridge <R^2>(t)=<R^2>(0)+cMσt), hillert_mean_field_self_similar_size_distribution (Sec 3 dR/dt mean-field and ∂P/∂t + ∂/∂R[P Mσ(1/R̄-1/R)]=0 with P=R̄^{-1}f(R/R̄)).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer asymmetric: 70-year grain-growth statistical toolkit (von Neumann-Mullins, Hillert, Lewis-Aboav-Weaire, MacPherson-Srolovitz) → magnetic domain pattern statistics where community focuses on single-wall dynamics and equilibrium Kittel/Kooy-Enz, lacking coarsening statistics. Falsifiability satisfied: self-similar Hillert form within 10 τ0 with peak ρ≈0.9 cutoff ρ=2 via Lorentz TEM/MFM, parabolic law with K 0.5-2.0 and factor-2 vs MuMax3, dA_n/dt = -(M_dwσ_wπ/3)(6-n) with n<6 shrink / n>6 grow; falsified if D_KL>0.3, exponent α outside 0.85-1.15, or K mismatch >2x. Prior-art advisory noted below, not a FAIL.

#### Stage 3 Watch Items
- Bibliometric: Verify if Hillert distribution and von Neumann-Mullins law applied to magnetic domain coarsening already appears; general Allen-Cahn Model A universality linking grain growth, soap froths, and magnetic domains is canonical in Bray Theory of Phase Ordering Kinetics – advisory check for novelty of specific topological tools transfer.
- Scope: Entry correctly lists breakdown from dipolar magnetostatics and wall inertia m_w = 2M_s/(γ_LL^2 Δ); Stage 3 should probe quantitative regime where thin-wall overdamped mapping holds in Co/Pt multilayers.
- None other identified.