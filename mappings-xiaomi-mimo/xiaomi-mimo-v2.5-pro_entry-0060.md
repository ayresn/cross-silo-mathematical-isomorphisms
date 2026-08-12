---
sid_metadata:
  entry_id: "SID-0060"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Xiaomi"
  model_family: "MiMo"
  model_version: "V2.5 Pro"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "memristive-valence-change-resistive-switching"
  domain_b: "lithium-ion-battery-sei-growth-and-degradation"
  structural_family: "electrochemical-reaction-diffusion-with-moving-boundaries"
  triple_correspondence_vectors:
    - "nernst_planck_electrodiffusion_operator"
    - "poisson_electrostatic_space_charge_coupling"
    - "butler_volmer_interface_charge_transfer_kinetics"
    - "stefan_flux_balance_moving_interface_condition"
    - "reaction_transport_damkohler_similarity_group"
discovery_rationale:
  why_not_obvious: "qualitative_electrochemical_nature_of_memristors_recognised_in_recent_reviews_but_operator_equivalence_with_sei_transport_not_established / multi_species_aging_framework_never_transferred_between_communities / distinct_jargon_for_identical_operators"
prior_discovery_metrics:
  structural_isomorphism_score: 9.2
  vocabulary_divergence_score: 6.5
  expected_methodological_transfer_score: 7.5
  community_separation_score: 6.5
  representation_mismatch_score: 3.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.5
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "constitutive_nonlinearity_divergence_in_high_field_regime_and_pore_scale_geometry_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0060

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Memristive resistive switching in transition-metal-oxide devices — specifically the valence-change-memory (VCM) mechanism in systems such as TiN/TaOₓ/TiN, where oxygen-vacancy transport, electrochemical reactions at electrode interfaces, and conductive-filament (CF) tip advancement govern the forming, SET, and RESET operations and the gradual resistance-state drift during endurance cycling.
*   **Silo B (Field 2):** Solid electrolyte interphase (SEI) nucleation, growth, and cycle-dependent evolution on lithium-ion battery anodes (graphite, silicon), where lithium-ion transport through the SEI, electrochemical reduction reactions at the SEI/electrolyte interface, and SEI-front advancement govern irreversible capacity fade and impedance rise over hundreds to thousands of cycles.
*   **Mathematical Isomorphism:** Both systems are governed by the Nernst–Planck–Poisson electrodiffusion operator coupled to Butler–Volmer electrochemical kinetics at solid–solid interfaces whose spatial advance satisfies a Stefan-type flux-balance condition, producing identical nonlinear parabolic–elliptic free-boundary problems that share the same electric Péclet number, electrochemical Stefan number, and reaction–transport Damköhler similarity group, and that exhibit a two-timescale degradation dynamics governed by the diffusion-limited redistribution of a fast and a slow ionic species.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Oxygen vacancy concentration** c_v ↔ **Dissolved Li⁺ concentration** c_Li
    *   *Operator Role:* Conserved scalar dependent variable in the Nernst–Planck drift–diffusion PDE, ∂c/∂t = ∇·[D∇c + (zeD/k_BT)c∇φ]. Both are local number densities (m⁻³) of the mobile ionic species that mediates charge transport through the solid film and enter the identical parabolic electrodiffusion operator.

*   **Conductive-filament tip position** x_CF ↔ **SEI growth-front position** δ_SEI
    *   *Operator Role:* Moving solid–solid phase boundary whose normal velocity is set by the Stefan flux-balance condition v_n = (D/Δc) ∂c/∂n |_interface. In both systems the concentration jump Δc converts a diffusive flux into an interface velocity.

*   **Electroforming voltage** V_form ↔ **SEI formation potential** E_SEI
    *   *Operator Role:* Critical applied potential at which the Butler–Volmer current first exceeds the nucleation threshold for irreversible new-phase formation. Both enter as the overpotential η = V_applied − E_eq in j = j₀[exp(α_a zeη/k_BT) − exp(−α_c zeη/k_BT)], which is the sole boundary reaction-rate operator on both sides.

*   **Oxide transport-domain thickness** d_ox ↔ **SEI transport-domain thickness** d_SEI
    *   *Operator Role:* Spatial extent of the domain for the NPP operator. Both determine the characteristic diffusion time τ = d²/D and enter the Damköhler number Da = k_rxn d/D, which measures reaction-limited vs. transport-limited behaviour.

*   **Macroscopic device resistance** R_dev ↔ **Cell charge-transfer resistance** R_ct
    *   *Operator Role:* Experimentally measurable functional of the concentration-profile solution of the NPP system: R = ∫₀ᵈ dx / σ(c(x)), where σ is the local conductivity (electronic for memristors: σ ∝ c_v; ionic for SEI: σ ∝ c_Li^γ). Both observables evolve under slow redistribution of the minority mobile species during cycling.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A — Valence-Change Memristor Model.**

In VCM devices (e.g., TaOₓ, HfOₓ), resistive switching is initiated by electroforming: a sub-stoichiometric, oxygen-vacancy-rich conductive filament nucleates and propagates through the oxide. The spatial distribution of oxygen vacancies c_v(x, t) and the electric potential φ(x, t) within the oxide layer satisfy the Nernst–Planck–Poisson system. The vacancy transport equation is:

```math
\frac{\partial c_v}{\partial t} \;=\; \nabla \cdot \!\left[\, D_v\,\nabla c_v \;+\; \frac{z_v\,e\,D_v}{k_B T}\,c_v\,\nabla\phi \,\right]
```

where D_v is the vacancy diffusivity, z_v = +2 for oxygen vacancies in TaOₓ, and the term in brackets is the Nernst–Planck flux with drift and diffusion components. The electric potential satisfies the Poisson equation:

```math
\nabla \cdot \bigl(\epsilon_{\text{ox}}\,\nabla\phi\bigr) \;=\; -\,e\bigl(z_v\,c_v + z_{\text{ox}}\,c_{\text{ox}}\bigr)
```

where ε_ox is the oxide permittivity and c_ox is the immobile oxide-ion background charge density. At the active-electrode/oxide interface, vacancy injection or annihilation is governed by the Butler–Volmer current:

```math
j_v \;=\; j_{0,v}\!\left[\,\exp\!\left(\frac{\alpha_{a,v}\,z_v\,e\,\eta}{k_B T}\right) - \exp\!\left(-\frac{\alpha_{c,v}\,z_v\,e\,\eta}{k_B T}\right)\right]
```

where η = V_applied − E_eq^v is the overpotential relative to the vacancy redox equilibrium potential. The CF tip advances under a Stefan flux-balance condition:

```math
v_{\text{CF}} \;=\; \frac{\Omega_v\,D_v}{\Delta c_v}\;\left.\frac{\partial c_v}{\partial n}\right|_{\text{tip}}
```

where Ω_v is the volume per formula unit of the newly formed sub-oxide and Δc_v is the concentration jump across the moving tip.

**Silo B — SEI Growth Model.**

In lithium-ion batteries the SEI forms at the anode/electrolyte interface via electrochemical reduction of solvent molecules. The Li⁺ concentration c_Li(x, t) and the electric potential φ(x, t) within the SEI satisfy the identical Nernst–Planck–Poisson system. The lithium-ion transport equation is:

```math
\frac{\partial c_{\text{Li}}}{\partial t} \;=\; \nabla \cdot \!\left[\, D_{\text{Li}}\,\nabla c_{\text{Li}} \;+\; \frac{z_{\text{Li}}\,e\,D_{\text{Li}}}{k_B T}\,c_{\text{Li}}\,\nabla\phi \,\right]
```

where D_Li is the Li⁺ diffusivity through the SEI and z_Li = +1. The Poisson equation is:

```math
\nabla \cdot \bigl(\epsilon_{\text{SEI}}\,\nabla\phi\bigr) \;=\; -\,e\!\left(z_{\text{Li}}\,c_{\text{Li}} + z_{\text{an}}\,c_{\text{an}} + \frac{\rho_{\text{fix}}}{e}\right)
```

where ε_SEI is the SEI permittivity, c_an is the mobile-anion concentration, and ρ_fix is the fixed charge in the SEI matrix. At the SEI/electrolyte interface, the SEI-forming reduction is governed by:

```math
j_{\text{SEI}} \;=\; j_{0,\text{SEI}}\!\left[\,\exp\!\left(\frac{\alpha_a\,z_{\text{Li}}\,e\,\eta}{k_B T}\right) - \exp\!\left(-\frac{\alpha_c\,z_{\text{Li}}\,e\,\eta}{k_B T}\right)\right]
```

where η is the overpotential at the SEI/electrolyte interface. The SEI growth front advances via the Stefan condition:

```math
v_{\text{SEI}} \;=\; \frac{M_{\text{SEI}}}{\rho_{\text{SEI}}}\;D_{\text{Li}}\;\left.\frac{\partial c_{\text{Li}}}{\partial n}\right|_{\text{front}}
```

where M_SEI/ρ_SEI is the molar volume of the SEI product phase.

**Bridging correspondence.**

Under the identification c_v ↔ c_Li, z_v ↔ z_Li, D_v ↔ D_Li, ε_ox ↔ ε_SEI, and Ω_v ↔ M_SEI/ρ_SEI (both being the molar volume of the product phase at the moving interface), every operator in the two systems is symbol-for-symbol identical:

| Operator | Memristor | SEI | Shared form |
|---|---|---|---|
| Nernst–Planck | ∇·[D_v∇c_v + (z_veD_v/k_BT)c_v∇φ] | ∇·[D_Li∇c_Li + (z_LieD_Li/k_BT)c_Li∇φ] | ∇·[D∇c + (zeD/k_BT)c∇φ] |
| Poisson | ∇·(ε_ox∇φ) = −e(z_vc_v + z_oxc_ox) | ∇·(ε_SEI∇φ) = −e(z_Lic_Li + z_anc_an + ρ_fix/e) | ∇·(ε∇φ) = −ρ_free |
| Butler–Volmer | j₀[exp(α_a zveη/k_BT) − exp(−α_c zveη/k_BT)] | j₀[exp(α_a z_Lieη/k_BT) − exp(−α_c z_Lieη/k_BT)] | j₀[exp(α_a zeη/k_BT) − exp(−α_c zeη/k_BT)] |
| Stefan condition | v_n = (ΩD/Δc)∂c/∂n\|_interface | v_n = (MD/ρΔc)∂c/∂n\|_interface | v_n = (V_mD/Δc)∂c/∂n\|_interface |

**Shared dimensionless groups.**

Electric Péclet number (drift-to-diffusion ratio):

```math
\mathrm{Pe}_e = \frac{z\,e\,\Delta\phi}{k_B T}
```

Memristor: Pe_e ~ 40–80 (forming voltage ~1–2 V at 300 K). SEI: Pe_e ~ 20–40 (formation overpotential ~0.5–1 V at 300 K). Both: Pe_e ≫ 1, confirming drift-dominated transport in both systems.

Electrochemical Stefan number (product-phase density to mobile-species density):

```math
\mathrm{Ste} = \frac{c_{\text{product}}}{c_{\text{mobile}}}
```

Memristor: Ste = c_v,incorporated / c_v,bulk ~ 10–100. SEI: Ste = ρ_SEI/(M_SEI c_Li) ~ 10–100. Both: Ste ≫ 1 justifying a sharp-interface Stefan formulation.

Reaction–transport Damköhler number:

```math
\mathrm{Da} = \frac{k_{\text{rxn}}\,d}{D}
```

where k_rxn is the Butler–Volmer exchange rate and d is the film thickness. The critical thickness d* = D/k_rxn marks the transition from reaction-limited (d ≪ d*) to transport-limited (d ≫ d*) growth. For memristors, d* ~ 1–5 nm; for SEI, d* ~ 1–5 nm. Both systems transition from reaction-limited nucleation to transport-limited thickening as the film exceeds d*.

**Two-timescale cycling dynamics.**

Both systems contain a fast species (oxygen vacancies / Li⁺) and a slow minority species (metal cations from the active electrode in memristors; solvent-decomposition oligomers in SEI). After the fast species reaches quasi-steady state, further drift is controlled by the slow species. The crossover cycle number is:

```math
N^* \;\approx\; \frac{D_{\text{fast}}}{D_{\text{slow}}}
```

For TaOₓ memristors: D_v ~ 10⁻¹⁵ m²/s, D_cation ~ 10⁻¹⁷ m²/s → N* ~ 100. For graphite SEI: D_Li ~ 10⁻¹⁶ m²/s, D_oligomer ~ 10⁻¹⁸ m²/s → N* ~ 100. The activation energy of the observable drift rate should switch at N* from E_a,D_fast to E_a,D_slow.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Battery SEI modelling → Memristor modelling.
*   **Asymmetric Maturity Rationale:** The battery community has developed multi-species reactive transport models for SEI growth (Pinson & Bazant, J. Electrochem. Soc. 2013; Reniers et al., J. Power Sources 2019), coupled mechanical–electrochemical degradation frameworks (Deshpande et al., J. Electrochem. Soc. 2012; Bucci et al., J. Mech. Phys. Solids 2017), and physics-based aging models that predict capacity fade over thousands of cycles from first-principles transport parameters. The memristor community has primarily built single-species (vacancy-only for VCM, cation-only for ECM) drift-diffusion models and relies on empirical power-law or logarithmic fits for endurance drift characterisation (Ielmini & Waser, 2019). The memristor community is mature in nanoscale in-situ characterisation (TEM, C-AFM) but lacks multi-species continuum aging frameworks.
*   **Target Bottleneck Mitigation:** The gradual drift of the OFF-state resistance R_OFF with cycling is a critical reliability bottleneck for VCM memristors (affecting multi-level storage and neuromorphic computing). Single-species vacancy models cannot explain the observed temperature dependence of the drift rate beyond a few hundred cycles. Importing the battery community's multi-species transport + aging framework provides a physics-based model for R_OFF(N) that captures both the fast-vacancy-redistribution phase (N < N*) and the slow-cation-redistribution phase (N > N*), with a predicted crossover in the Arrhenius activation energy of the drift rate.
*   **Falsifiable Prediction:** In TiN/TaOₓ/TiN VCM memristors, the activation energy E_a of the resistance drift rate β(T), defined by R_OFF(N) = R_OFF,0 [1 + β N^α], should show two distinct regimes when extracted from temperature-dependent cycling data at multiple N values:

    For N < N* (before vacancy saturation):
    ```math
    E_{a,\beta} \;\approx\; E_{a,D_v} \;\approx\; 0.3\text{–}0.5\;\text{eV}
    ```

    For N > N* (after vacancy saturation, cation-limited drift):
    ```math
    E_{a,\beta} \;\approx\; E_{a,D_c} \;\approx\; 1.0\text{–}1.5\;\text{eV}
    ```

    where N* ≈ D_v/D_c ~ 100, E_{a,D_v} is independently measurable from impedance spectroscopy on as-deposited TaOₓ, and E_{a,D_c} is independently measurable from tracer diffusion or from temperature-dependent forming kinetics.

    **Baseline:** Single-species vacancy-only models (Strukov et al. 2008; Larentis et al. 2012) predict E_{a,β} ≈ E_{a,D_v} ≈ 0.3–0.5 eV for all cycle numbers, with no crossover.

    **Falsification:** If E_{a,β} measured at N = 50 and N = 10,000 agree within ±0.1 eV across temperatures from 25 °C to 150 °C on ≥10 devices, and both values match E_{a,D_v}, the multi-species model adds no predictive value and the cation transport channel is inactive.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"Nernst-Planck-Poisson" AND "Butler-Volmer" AND ("memristor" OR "resistive switching") AND ("SEI" OR "solid electrolyte interphase")`
*   `"valence change memory" AND "endurance drift" AND "activation energy" AND "multi-species transport"`
*   `"oxygen vacancy drift diffusion" AND "Stefan condition" AND "conductive filament" AND "moving boundary"`
*   `"SEI growth model" AND "moving boundary" AND "Nernst-Planck" AND "memristive"`
*   `"resistive switching" AND "electrochemical" AND ("battery" OR "lithium") AND "isomorphism" AND "free boundary"`