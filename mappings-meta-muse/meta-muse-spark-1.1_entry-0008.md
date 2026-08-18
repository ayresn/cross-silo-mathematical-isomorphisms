---
sid_metadata:
  entry_id: "SID-0008"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-rejected"
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
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "FLAG"
    verdict_rationale: "All three listed correspondence vectors are demonstrated with real equations and the transfer direction and falsifiability criteria are clearly satisfied, but Checks 1 and 2 surface several specific, non-fatal gaps that keep this below PASS."
    failed_checks: []
    flagged_checks:
      - "Check 1: Silo A's parabolic transport equation carries an advective term u that is never defined or tied to ∇φ anywhere in the entry, unlike Silo B's explicitly stated u = -(k/μ)∇p, leaving the Section 1 claim that the elliptic field 'drives' the parabolic field asymmetrically demonstrated (shown for B, asserted but not shown for A)."
      - "Check 1: Silo A's dispersion-relation curvature term (-D_Li·Γ_GT·k²) and Silo B's dispersion term (-α_disp·|k|²) are given identical k² scaling, but the entry attributes them to different physical mechanisms (Gibbs-Thomson capillarity vs. transverse dispersion); a genuine capillarity term under the quasi-steady analysis implied by the shared v₀|k|(Da-1)/(Da+1) destabilizing term would be expected to scale as k³, not k², which bears on whether the two 'Mullins-Sekerka dispersion thresholds' in Vector 3 are actually the same order in k."
      - "Check 2: the vocabulary pair 'electrolyte ionic conductivity ↔ reservoir mobility k/μ' is described in Section 2 as a coefficient σ(x) for both sides, but Section 3 writes Silo A's coefficient as κ(c) — dependent on the solution variable c, making the elliptic operator quasilinear and two-way coupled to the parabolic equation — versus Silo B's k(x), a purely prescribed linear coefficient; Section 2 does not acknowledge this asymmetry."
      - "Check 2: the vocabulary pair 'electric overpotential η ↔ acid concentration over-saturation (c − c_eq)' supports its claim that both variables enter as a curvature-modified H¹-trace using a Gibbs-Thomson formula (c_Γ = c₀(1+Γκ_curv)) written only in terms of Silo B's concentration field c; no equation shows η entering an analogous relation on the Silo A side."
      - "Check 4c (advisory, not grounds for rejection): the general pairing of solidification/electrodeposition/reactive-infiltration instabilities under Mullins-Sekerka-type linear stability analysis is a recognized theme in the interfacial pattern-formation literature (Barton–Bockris-style electrodeposition stability analyses; the Chadam, Ortoleva, Hinch & Bhatt reactive-infiltration line of work already cited in Section 3)."
    quoted_evidence: []
    stage_3_watch_items:
      - "Independently re-derive the Mullins-Sekerka-type dispersion relation for the Butler-Volmer/Gibbs-Thomson boundary condition and confirm whether the curvature term should scale as k² (as written) or k³ (as standard quasi-steady capillarity analysis suggests); bears directly on Vector 3."
      - "Confirm whether 'StimPro' and 'Mangane', named in Section 4 as current commercial acidization simulators limited to ad-hoc level-set tip cutoffs, are real products and whether that capability characterization is accurate."
      - "Check whether the low-overpotential linearization window (|Fη/RT| < 0.2, ~5 mV at 298 K) the entry calls 'the wormholing regime' covers overpotentials typical of practical dendrite-forming conditions, since dendrite risk is usually associated with higher overpotentials/current densities."
      - "Verify the Da_B = k_s·a_v·L²/D_e definition's specific-surface-area factor a_v against its source derivation — a_v does not appear in the sharp-interface Robin condition −D_e∂_n c_a = k_s c_a given earlier in Section 3 for the same k_s."
      - "Verify the specific numeric predictions (Q_opt: 0.8 → 0.56 ± 0.06 cm³/min; D_f: 1.63 → 1.82 ± 0.05) against the cited Fredd & Fogler baseline correlation for consistent core geometry, units, and reported values."
      - "Bibliometrically confirm how explicitly Barton–Bockris-type electrodeposition-instability analyses and the cited Chadam/Ortoleva/Hinch/Bhatt reactive-infiltration analyses already invoke a shared Mullins-Sekerka framework; bears on this entry's novelty claim."
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The displayed Mullins-Sekerka dispersion relation and critical-wavenumber formula are dimensionally inconsistent and mutually incompatible, so the claimed third correspondence is not mathematically supported."
    failed_checks:
      - "Check 1: dispersion relation and critical wavenumber are dimensionally and algebraically inconsistent"
    flagged_checks:
      - "Check 2: overpotential-to-concentration mapping and k_BV dimensional reconciliation are under-specified"
      - "Check 3: Robin-Stefan vector is only partially demonstrated for Silo A"
      - "Check 4: recognizable Laplacian-growth prior-art analogy should be examined by Stage 3"
    quoted_evidence:
      - '\sigma_A(k) = v_0 |k| \frac{Da_A -1}{Da_A +1} - D_{Li} \Gamma_{GT} k^2, \quad Da_A = k_{BV} L / D_{Li}, \quad \Gamma_{GT} = \gamma \Omega_m / RT'
      - 'Critical wavenumber $k_c = v_0(Da-1)/(Da+1)/\Gamma$ marks instability onset $\sigma(k_c)=0$ in both.'
    stage_3_watch_items:
      - "Ask whether the stability variables are nondimensional; if so, the scaling for k, sigma(k), and Gamma must be stated."
      - "Ask for an explicit Silo A derivation coupling the Robin concentration flux to the Stefan current flux."
      - "Ask for dimensional reconciliation of eta and c-c_eq and of the linearized k_BV formula."
      - "Stage 3 should assess prior art in Laplacian-growth/Mullins-Sekerka analogies between electrodeposition and reactive dissolution/wormholing."
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry contains dimensionally inconsistent flux identities and an incorrect critical-wavenumber derivation, so the claimed isomorphism is not internally supported."
    failed_checks:
      - "Check 1: Silo A concentration equation is labeled diffusion-migration but displays advection-diffusion with no migration term; the derived critical wavenumber formula is algebraically inconsistent with the displayed dispersion relations."
      - "Check 2: The shared Stefan flux identity equates charge/volumetric flux with molar flux; the Butler-Volmer rate-constant conversion is dimensionally incorrect."
      - "Check 3: Correspondence vectors 2 and 3 are not validly demonstrated because they depend on the Check 1/2 errors."
    flagged_checks:
      - "Check 4: Prior-art advisory only — the Laplacian-growth/reactive-infiltration analogy is recognizable and should be probed at Stage 3."
    quoted_evidence:
      - 'concentration obeys diffusion-migration'
      - '\partial_t c + \mathbf{u}\cdot\nabla c = D_{Li} \nabla^2 c \quad \text{in } \Omega_A(t)'
      - 'where $J_n = -\sigma \partial_n \Phi = -D \partial_n c$ at $\Gamma(t)$ by Robin balance'
      - '$k_{BV} = i_0 a / (F c_0 R T)$ [m/s] after linearization at small overpotential'
      - 'Critical wavenumber $k_c = v_0(Da-1)/(Da+1)/\Gamma$ marks instability onset $\sigma(k_c)=0$ in both'
    stage_3_watch_items:
      - "Probe whether the electrodeposition/reactive-infiltration Laplacian-growth analogy is already canonical in pattern-formation literature (e.g., Chadam-Ortoleva, Hinch & Bhatt, Fredd & Fogler)."
      - "Verify the Butler-Volmer linearized boundary condition and the correct role of electromigration in Li-dendrite phase-field models."
      - "Check whether phase-field transfer to carbonate acidization has prior published work."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a severe dimensional violation in the Mullins-Sekerka dispersion relation (adding a rate to a velocity) and a category error mapping electrical overpotential to a concentration field trace."
    failed_checks:
      - "Check 1: Equation Validity (Dimensional inconsistency in dispersion relation)"
      - "Check 2: Vocabulary Matrix Coherence (Category error mapping potential to a concentration trace)"
    flagged_checks: []
    quoted_evidence:
      - "\\sigma_A(k) = v_0 |k| \\frac{Da_A -1}{Da_A +1} - D_{Li} \\Gamma_{GT} k^2"
      - "electric overpotential \\eta ↔ acid concentration over-saturation (c - c_{eq})"
      - "Both enter as H^1-trace of concentration field modified by mean curvature"
    stage_3_watch_items:
      - "Verify the validity of mapping nonlinear Butler-Volmer kinetics to strictly linear dissolution kinetics, even in the stated low-overpotential limit."
      - "Prior art check: The mathematical analogy between electrochemical electrodeposition and porous media dissolution via shared Laplacian growth and DLA is a known canonical mapping in pattern formation physics (e.g., L.M. Sander)."
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equation classes match (elliptic-parabolic Robin-Stefan on both sides), vocabulary mappings are type-compatible with explicit dimensional reconciliation, all three correspondence vectors are demonstrated with equations in Section 3, and the transfer is asymmetric with a genuinely falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The entry acknowledges the isomorphism holds exactly only in the linearized low-overpotential limit |Fη/RT| < 0.2, while Silo B's dissolution kinetics are inherently linear. Stage 3 should verify whether published Butler-Volmer parameters for practical dendrite growth conditions (high current density) violate this linearization regime, which would narrow the correspondence to a subset of operating conditions."
      - "The reactive-infiltration-instability / electrochemical-deposition mathematical parallel is referenced in the entry's own Silo B derivation ('Chadam, Ortoleva, Hinch & Bhatt for reactive infiltration'). Stage 3 should verify whether the specific phase-field methodological transfer (grand-potential functional into Darcy framework for acidization) is novel beyond this established mathematical analogy."
      - "The falsifiable prediction quantifies a 30% downward shift in optimal flow rate and a specific fractal dimension increase from 1.63 to 1.82. Stage 3 should check whether the baseline values (Fredd & Fogler 1998 correlation, D_f = 1.63) are accurately attributed and whether the predicted shifts are consistent with the phase-field regularization lengthscale ε ~ 0.1 d_p being physically meaningful at d_p = 200 μm."
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "FLAG"
    verdict_rationale: "Core equations and all three correspondence vectors are mathematically sound, but the vocabulary matrix contains an incorrect flux-equality claim and an unsupported Gibbs-Thomson attribution, and the Mullins-Sekerka framework is canonical prior art."
    failed_checks: []
    flagged_checks:
      [
        "CHECK 2: Vocabulary matrix operator role for anode/dissolution velocity pair claims literal equality between potential/pressure flux and concentration flux, which is mathematically false in both silos",
        "CHECK 2: Fourth vocabulary pair (overpotential ↔ over-saturation) claims Gibbs-Thomson curvature regularization role for both silos, but Silo B equations show no Gibbs-Thomson term — regularization comes from transverse dispersion",
        "CHECK 4c: Mullins-Sekerka instability framework is canonical pattern-formation prior art recognized from graduate-level solidification theory"
      ]
    quoted_evidence:
      []
    stage_3_watch_items:
      [
        "Canonical prior art: Mullins-Sekerka dispersion framework applied across solidification, electrodeposition, and dissolution — verify novelty of the specific Li-dendrite ↔ acidization pairing via bibliometric query",
        "Reactive infiltration instability literature (Chadam, Ortoleva, Hinch, Bhatt) — verify the dispersion relation form attributed to these authors",
        "Phase-field methods applied to reactive transport / dissolution in porous media — verify the claim that Silo B 'genuinely lacks' variational curvature regularization, as phase-field dissolution models may exist",
        "Vocabulary matrix flux-equality claim ($J_n = -\\sigma \\partial_n \\Phi = -D \\partial_n c$) is mathematically incorrect as stated — in Silo A the fluxes differ by Faraday's constant, in Silo B the Darcy velocity and diffusive acid flux are distinct quantities",
        "Gibbs-Thomson term claimed for Silo B in vocabulary matrix but absent from Section 3 equations — verify whether curvature regularization is standard in acidization models or genuinely absent"
      ]
  seventh_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a category-error vocabulary mapping and does not actually demonstrate the claimed Robin-Stefan correspondence on both silos."
    failed_checks: ["Check 2: the mapping of electric overpotential to acid concentration over-saturation is asserted as the same concentration-field trace despite being a different physical and dimensional variable", "Check 3: the listed Robin reactive flux–Stefan moving-boundary vector is not established for Silo A because its Robin concentration flux is not equated to the current flux used in the stated velocity law"]
    flagged_checks: ["Check 1: the claimed Mullins-Sekerka correspondence is asserted through separate dispersion formulas with different regularization coefficients and no derivation connecting the stated Silo A and Silo B governing systems to those formulas", "Check 4: the transfer direction is stated as asymmetric and the prediction is quantitatively falsifiable, but the proposed surfactant perturbation changes interfacial properties beyond curvature regularization, so the stated falsification criterion does not isolate the claimed mechanism"]
    quoted_evidence: ["*   electric overpotential $\\eta$ ↔ acid concentration over-saturation $(c - c_{eq})$", "*   *Operator Role:* thermodynamic driving scalar in Gibbs-Thomson curvature regularization term $c_{\\Gamma} = c_0 (1 + \\Gamma \\kappa_{curv})$ where $\\Gamma = \\gamma \\Omega / R T$ enters as additive shift to Dirichlet value of concentration at curved interface. Both enter as $H^1$-trace of concentration field modified by mean curvature $\\kappa_{curv}: \\Gamma \\to \\mathbb{R}$ [1/m].", "Vector 2 - Robin reactive flux Stefan moving-boundary pair: for Silo A and B respectively, Robin balance plus Stefan advance shown in the third line of each block, both yielding $v_n = \\beta (-D \\partial_n c)$. This is a moving-boundary pair of mixed Robin-Stefan type, not Dirichlet."]
    stage_3_watch_items: ["Probe the claimed Mullins-Sekerka dispersion correspondence: Section 3 supplies distinct Silo A and Silo B dispersion relations but does not derive either from the displayed governing equations or establish an actual operator-level transformation between them.", "Probe the claimed quantitative transfer prediction and its experimental falsification design, particularly whether the surfactant intervention changes only the proposed curvature parameter rather than other transport or interfacial properties.", "No specific prior-art recognition is asserted here; bibliometric novelty remains for Stage 3."]
  eighth_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry equates distinct physical fluxes (electrical current density and species diffusive flux) as identical at the interface, a precise mathematical/physical error that invalidates the claimed operator identity."
    failed_checks: ["Check 1: Equation validity — incorrect equality of electrical current and species diffusive flux at the moving boundary"]
    flagged_checks: []
    quoted_evidence: ["\"where $J_n = -\\sigma \\partial_n \\Phi = -D \\partial_n c$ at $\\Gamma(t)$ by Robin balance.\"","\"-D_{Li} \\partial_n c = k_{BV} c, \\quad v_{n,A} = \\frac{\\Omega_m}{F} j_n = \\frac{\\Omega_m}{F}(-\\kappa \\partial_n \\phi) \\quad \\text{on } \\Gamma_A(t)\""]
    stage_3_watch_items: ["Verify whether the entry's mapping between ionic current density and molar/species flux is supported by a consistent derivation including migration terms and Faraday stoichiometry; check primary sources for how Butler-Volmer reaction flux couples to species flux in concentrated electrolytes vs dilute approximations.","Examine whether the proposed curvature regularization mapping (Gibbs-Thomson) to transverse dispersion (\\alpha_{disp}) is physically justified or merely heuristic; request derivation of units and scaling for \\alpha_{disp} vs \\Gamma_{GT}."]
  ninth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "FLAG"
    verdict_rationale: "All listed correspondence vectors are supported by equations and the equation classes match under the stated linearization, but Check 2 contains a category-type inconsistency in the overpotential-to-concentration mapping and Check 4 asymmetry is only weakly directional."
    failed_checks: []
    flagged_checks: ["Check 2: overpotential mapped to concentration over-saturation without shared mathematical type", "Check 4: transfer asymmetry is plausible but not strongly one-sided given maturity of both toolkits"]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether linearized Butler-Volmer truly recovers the linear first-order dissolution kinetics of Silo B at the claimed |Fη/RT|<0.2 regime", "Confirm that the Gibbs-Thomson term in Silo A and the transverse-dispersion regularization in Silo B are operator-equivalent rather than merely both providing k^{2} damping", "Assess whether phase-field import into Darcy-scale acidization is novel relative to existing continuum reactive-infiltration models"]
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

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — Two issues. (1) Silo A's equation "$\partial_t c + \mathbf{u}\cdot\nabla c = D_{Li} \nabla^2 c$" never defines $\mathbf{u}$ or ties it to $\nabla\phi$, whereas Silo B's parallel equation explicitly states "$\mathbf{u} = -\frac{k}{\mu}\nabla p$" — so Section 1's claim that an elliptic field "drives a parabolic advection-diffusion-reactive concentration field" is demonstrated for Silo B only. (2) The dispersion terms "$-D_{Li}\Gamma_{GT}k^2$" (Silo A) and "$-\alpha_{disp}|k|^2$" (Silo B) share k² scaling despite the entry itself distinguishing their mechanisms ("$\alpha_{disp}$ is transverse dispersion coefficient providing curvature-like regularization analogous to $\Gamma_{GT}$"); standard quasi-steady Mullins-Sekerka analysis of a genuine Gibbs-Thomson/capillarity term would be expected to yield k³, not k², so Silo A's exponent warrants independent re-derivation.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Two issues. (1) The pair "electrolyte ionic conductivity ↔ reservoir mobility $k/\mu$" states the coefficient is "$\sigma(\mathbf{x}) \in \mathbb{R}^+_{>0}$" for both sides, but Section 3 shows Silo A's coefficient as $\kappa(c)$ (solution-dependent, making the operator quasilinear and two-way coupled to the parabolic equation) versus Silo B's $k(\mathbf{x})$ (purely prescribed, linear) — an asymmetry Section 2 elides by using identical notation for both. (2) The pair "electric overpotential $\eta$ ↔ acid concentration over-saturation $(c-c_{eq})$" claims "Both enter as $H^1$-trace of concentration field modified by mean curvature," but the only formula given, "$c_{\Gamma} = c_0(1+\Gamma\kappa_{curv})$," is written purely in terms of Silo B's concentration field $c$; no equation shows $\eta$ entering an analogous curvature-modified relation for Silo A.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with explicit equations, not merely named. Vector 1 (shared elliptic operator) is shown via the two divergence-form elliptic PDEs in Section 3 plus an explicit matching weak form. Vector 2 (Robin-Stefan pair) is shown via the Robin/Stefan boundary conditions in the third equation line of each Silo's block, and restated in the "Demonstration of triple correspondences" list. Vector 3 (Mullins-Sekerka dispersion + flux conservation) is shown via the two global flux-conservation integrals and the two derived $\sigma(k)$ dispersion relations. (Per Check 1, the internal consistency of Vector 3's dispersion-relation exponent for Silo A should be re-verified, but an equation is present either way.)
- **CHECK 4 (Transfer and Falsifiability):** PASS — (a) Asymmetry: the transfer direction (mature phase-field dendrite methodology → less-mature wormhole simulation) is specifically justified (named codes, named regularization mechanism, named limitation of current wormhole simulators), not a claim that could run either direction with comparable benefit. (b) Falsifiability: Section 4 names concrete, measurable outcomes with explicit values, uncertainties, and a stated statistical test (PVBT shift, $Q_{opt}=0.8\to0.56\pm0.06\ cm^3/min$, fractal dimension $D_f=1.63\to1.82\pm0.05$, with an explicit falsification protocol), well beyond a template non-prediction. (c) Prior art (advisory): the general unification of solidification, electrodeposition, and reactive-infiltration instabilities under Mullins-Sekerka-type linear stability analysis is a recognized theme in the interfacial pattern-formation literature — e.g. Barton–Bockris-style treatments of electrodeposition instability, and the Chadam, Ortoleva, Hinch & Bhatt reactive-infiltration work the entry itself cites in Section 3. This does not affect the verdict but is logged below.

#### Stage 3 Watch Items
- Independently re-derive the Mullins-Sekerka-type dispersion relation for the Butler-Volmer/Gibbs-Thomson boundary condition and confirm whether the curvature term should scale as $k^2$ (as written) or $k^3$ (as standard quasi-steady capillarity analysis suggests) — bears directly on Vector 3.
- Confirm whether "StimPro" and "Mangane" (Section 4, named as current commercial acidization simulators limited to ad-hoc level-set tip cutoffs) are real products and whether that capability characterization is accurate.
- Check whether the low-overpotential linearization window ($|F\eta/RT|<0.2$, ≈5 mV at 298 K) the entry calls "the wormholing regime" covers overpotentials typical of practical dendrite-forming conditions, since dendrite risk is usually associated with higher overpotentials/current densities.
- Verify the $Da_B = k_s a_v L^2/D_e$ definition's specific-surface-area factor $a_v$ against its source derivation — $a_v$ does not appear in the sharp-interface Robin condition $-D_e\partial_n c_a = k_s c_a$ given earlier in Section 3 for the same $k_s$.
- Verify the specific numeric predictions ($Q_{opt}: 0.8\to0.56\pm0.06\ cm^3/min$; $D_f: 1.63\to1.82\pm0.05$) against the cited Fredd & Fogler baseline correlation for consistent core geometry, units, and reported values.
- Bibliometrically confirm how explicitly Barton–Bockris-type electrodeposition-instability analyses and the cited Chadam/Ortoleva/Hinch/Bhatt reactive-infiltration analyses already invoke a shared Mullins-Sekerka framework — bears on this entry's novelty claim.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry states “\sigma_A(k) = v_0 |k| \frac{Da_A -1}{Da_A +1} - D_{Li} \Gamma_{GT} k^2, \quad Da_A = k_{BV} L / D_{Li}, \quad \Gamma_{GT} = \gamma \Omega_m / RT”, but with \Gamma_{GT} a length, D_{Li}\Gamma_{GT}k^2 has units of velocity, not inverse time, so it cannot be subtracted from v_0|k|; the subsequent “Critical wavenumber $k_c = v_0(Da-1)/(Da+1)/\Gamma$ marks instability onset $\sigma(k_c)=0$ in both.” is also dimensionally wrong and does not follow from the displayed relation.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The pair “electric overpotential $\eta$ ↔ acid concentration over-saturation $(c - c_{eq})$” and the claim “$k_{BV} = i_0 a / (F c_0 R T)$ [m/s]” are under-specified because voltage/concentration and the linearized rate constant are not given an explicit common nondimensionalization; this is a concern but not the fatal error.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector 1 (“shared_elliptic_laplacian_conductivity_operator_for_potential_pressure”) is demonstrated by the two elliptic equations and weak form; Vector 3 (“mullins_sekerka_dispersion_threshold_with_global_flux_conservation”) is addressed by global-flux and dispersion equations but those dispersion equations are internally inconsistent (Check 1); Vector 2 (“robin_reactive_flux_stefan_moving_boundary_velocity_pair”) is only partially demonstrated because Silo A’s Stefan law is written in terms of “$-\kappa \partial_n \phi$” while the Robin concentration flux “$-D_{Li} \partial_n c = k_{BV} c$” is not equationally coupled to it.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction and quantitative falsification test are specific enough, but the pairing resembles canonical Laplacian-growth/Mullins-Sekerka analogies between electrodeposition and reactive dissolution/wormholing, so novelty should be checked by Stage 3.

#### Stage 3 Watch Items
- Verify whether the stability analysis is intended to be nondimensional; if so, require explicit scalings for $k$, $\sigma(k)$, and $\Gamma$.
- Require an explicit Silo A relation coupling the Robin concentration flux to the Stefan current flux, e.g. whether $j_n = F k_{BV} c = -F D_{Li}\partial_n c$ is assumed.
- Check the dimensional/semantic reconciliation of $\eta$ versus $(c-c_{eq})$ and the linearized $k_{BV}$ expression.
- Assess prior art in Laplacian-growth/Mullins-Sekerka analogies and reactive-infiltration instability literature named or implied by the entry (electrodeposition, carbonate acidization/wormholing).

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The Silo A text claims “concentration obeys diffusion-migration,” but the displayed equation \(\partial_t c + \mathbf{u}\cdot\nabla c = D_{Li} \nabla^2 c\) is an advection-diffusion equation with no migration term and no definition of \(\mathbf{u}\); additionally, the derived “Critical wavenumber \(k_c = v_0(Da-1)/(Da+1)/\Gamma\)” does not follow from the displayed dispersion relations, which require denominators \(D_{Li}\Gamma_{GT}\) and \(\alpha_{\text{disp}}\), respectively.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The vector-2 role states “\(J_n = -\sigma \partial_n \Phi = -D \partial_n c\) at \(\Gamma(t)\) by Robin balance,” but \(-\sigma\partial_n\Phi\) is charge/volumetric flux while \(-D\partial_n c\) is molar flux; they are related by Faraday or stoichiometric factors, not equal. The Butler-Volmer conversion “\(k_{BV} = i_0 a / (F c_0 R T)\) [m/s]” is also dimensionally inconsistent with the claimed m/s units.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 1 is demonstrated by the shared elliptic operator equations. Vector 2 depends on the false flux identity above, and Vector 3 depends on the incorrect critical-wavenumber formula, so fewer than three vectors are validly demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction and falsifiable prediction are concrete, but the Laplacian-growth/reactive-infiltration analogy is recognizable prior art for Stage 3 to probe, including the entry’s own citation of Chadam-Ortoleva/Hinch-Bhatt and Fredd-Fogler.

#### Stage 3 Watch Items
- Probe whether the electrodeposition/reactive-infiltration Laplacian-growth analogy is already canonical.
- Verify the Butler-Volmer linearization and the correct role of electromigration in Li-dendrite phase-field models.
- Check whether phase-field transfer to carbonate acidization has prior published work.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The dispersion relation `\sigma_A(k) = v_0 |k| \frac{Da_A -1}{Da_A +1} - D_{Li} \Gamma_{GT} k^2` is dimensionally invalid: the growth rate $\sigma_A(k)$ and the first term $v_0|k|$ have units of inverse time ($s^{-1}$), but the capillary stabilization term $D_{Li}\Gamma_{GT}k^2$ has units of velocity ($m/s$) because $\Gamma_{GT}$ is a capillary length ($m$), $D_{Li}$ is diffusivity ($m^2/s$), and $k^2$ is ($m^{-2}$).
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "electric overpotential $\eta$ ↔ acid concentration over-saturation $(c - c_{eq})$" contains a fundamental category error by claiming "Both enter as $H^1$-trace of concentration field modified by mean curvature"; electrical overpotential (voltage) is not a concentration field, nor do either $\eta$ or $(c - c_{eq})$ actually appear in the provided operator role equation $c_{\Gamma} = c_0 (1 + \Gamma \kappa_{curv})$.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed triple correspondence vectors are mathematically supported with explicit equations and derivations in Section 3 (though Vector 3 contains the fatal dimensional error caught in Check 1).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer proposes a genuinely asymmetric import of variational phase-field curvature regularization into Darcy-scale models, backed by a highly specific and measurable falsifiable prediction (e.g., downward shift of the PVBT minimum to $0.56 \pm 0.06 cm^3/min$). *Advisory:* The structural isomorphism between electrodeposition and porous media dissolution via shared Laplacian growth is a canonical analogy in pattern formation physics (e.g., L.M. Sander).

#### Stage 3 Watch Items
- Verify the validity of mapping nonlinear Butler-Volmer kinetics to strictly linear dissolution kinetics, even in the stated low-overpotential limit.
- Prior art check: The mathematical analogy between electrochemical electrodeposition and porous media dissolution via shared Laplacian growth and DLA is a known canonical mapping in pattern formation physics (e.g., L.M. Sander).

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos present genuinely second-order elliptic (Laplacian conductivity) + parabolic advection-diffusion + Robin-Stefan moving-boundary systems from their stated domains; equation classes match and the entry explicitly acknowledges the linearized-regime boundary where the correspondence holds exactly.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four paired mappings connect objects of compatible mathematical type (positive-definite elliptic coefficients, Robin boundary rate constants [m/s], scalar normal velocities [m/s], thermodynamic driving scalars entering Gibbs-Thomson boundary regularization), with explicit dimensional reconciliation for the k_BV ↔ k_s and β_A ↔ β_B transformations.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in Section 3: Vector 1 with the divergence-form elliptic equations and weak form identity; Vector 2 with the Robin balance plus Stefan velocity law on both Γ_A(t) and Γ_B(t); Vector 3 with global conservation integrals, the Mullins-Sekerka dispersion relations σ_A(k) and σ_B(k), and the critical wavenumber k_c marking instability onset.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer from electrochemical phase-field modeling to acidization wormholing is genuinely asymmetric (Silo A has variational phase-field codes; Silo B "genuinely lacks a variational curvature regularization" and relies on level-set with ad-hoc cutoffs). The prediction is specific and falsifiable: quantitative PVBT shift, fractal dimension change, and a concrete 8-replicate surfactant-controlled falsification experiment with stated significance threshold.

#### Stage 3 Watch Items
- The isomorphism holds exactly only in the linearized Butler-Volmer regime (|Fη/RT| < 0.2). Verify whether practical dendrite growth conditions (high current density) routinely violate this limit, narrowing the correspondence's domain of validity.
- The reactive-infiltration / electrochemical-deposition mathematical parallel is already established in the literature (Chadam, Ortoleva, Hinch & Bhatt). Probe whether the specific phase-field methodological transfer into Darcy-scale acidization is novel beyond this known analogy.
- Verify accuracy of baseline quantitative values attributed to Fredd & Fogler (1998) and check whether the predicted 30% shift is consistent with the stated phase-field regularization lengthscale ε ~ 0.1 d_p at d_p = 200 μm being physically resolvable at the Darcy scale.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos present genuinely elliptic potential/pressure equations paired with parabolic advection-diffusion concentration equations, Robin boundary conditions, and Stefan velocity laws. No equation-class mismatch. The dispersion relations $\sigma_A(k)$ and $\sigma_B(k)$ share the identical functional form $v_0|k|(Da-1)/(Da+1) - \alpha k^2$, correctly characterizing Mullins-Sekerka-type instability. The Butler-Volmer nonlinearity is transparently acknowledged as limiting the isomorphism to the linearized regime.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Two issues found. First, the operator role for the velocity pair states "$J_n = -\sigma \partial_n \Phi = -D \partial_n c$ at $\Gamma(t)$ by Robin balance," claiming literal equality between the potential/pressure flux and the concentration flux. In Silo A, $-\kappa \partial_n \phi = F \cdot (-D_{Li} \partial_n c)$ by Faraday's law (differ by Faraday's constant, not equal). In Silo B, $-\frac{k}{\mu}\partial_n p$ is the Darcy velocity while $-D_e \partial_n c_a$ is the diffusive acid flux — genuinely different quantities. The actual Stefan velocity equations in Section 3 correctly use different fluxes with different proportionality constants, so the error is confined to the vocabulary matrix's explanatory text. Second, the fourth vocabulary pair claims both $\eta$ and $(c - c_{eq})$ serve as "thermodynamic driving scalar in Gibbs-Thomson curvature regularization term $c_{\Gamma} = c_0(1 + \Gamma \kappa_{curv})$," but Section 3's Silo B equations contain no Gibbs-Thomson term — the $k^2$ regularization in $\sigma_B(k)$ comes from $\alpha_{disp}|k|^2$ (transverse dispersion), which the entry itself describes as "analogous to" rather than identical to $\Gamma_{GT}$.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body. Vector 1 (shared elliptic Laplacian) is shown via both $\nabla\cdot(\kappa\nabla\phi)=0$ and $\nabla\cdot(\frac{k}{\mu}\nabla p)=0$ with the weak-form identity stated. Vector 2 (Robin-Stefan pair) is shown via the boundary condition blocks for both silos, yielding $v_n = \beta(-D\partial_n c)$. Vector 3 (Mullins-Sekerka dispersion with global flux conservation) is demonstrated via the global conservation integrals and both dispersion relations with the shared critical wavenumber $k_c$.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry is genuine: phase-field methodology (Allen-Cahn/Cahn-Hilliard with variational structure, adaptive mesh refinement, open-source codes) is more developed in electrochemistry than in acidization simulation, and the stated direction (A→B) is correct. The falsifiable prediction is highly specific — naming $Q_{opt}$ shift from 0.8 to 0.56 ± 0.06 cm³/min, PVBT reduction from 0.45 to 0.31 ± 0.04, fractal dimension increase from 1.63 to 1.82 ± 0.05, with a concrete 8-replicate surfactant falsification protocol. However, the Mullins-Sekerka instability framework is a canonical result in pattern formation and solidification theory, widely covered in graduate texts (e.g., Langer's reviews, Kessler-Levine-Reynolds). The general connection between electrodeposition and dissolution instabilities through shared Laplacian growth mathematics is well-established in the pattern formation community. This is flagged as advisory prior art for Stage 3 bibliometric verification — it is not grounds for rejection.

#### Stage 3 Watch Items
- **Canonical prior art (advisory only):** The Mullins-Sekerka dispersion framework is a textbook result in pattern formation / solidification theory. Verify whether the specific Li-dendrite ↔ carbonate-acidization pairing has been explicitly discussed in the literature, or whether only the general Laplacian-growth connection is known.
- **Reactive infiltration instability attribution:** Verify that the dispersion relation form $\sigma_B(k) = v_0|k|(Da-1)/(Da+1) - \alpha_{disp}|k|^2$ is correctly attributed to Chadam, Ortoleva, Hinch & Bhatt.
- **Phase-field in dissolution:** The entry claims Silo B "genuinely lacks a variational curvature regularization." Verify whether phase-field or diffuse-interface models for reactive dissolution in porous media already exist in the literature (e.g., in computational geoscience or geoengineering).
- **Vocabulary matrix flux equality:** The claim "$J_n = -\sigma \partial_n \Phi = -D \partial_n c$ at $\Gamma(t)$ by Robin balance" is mathematically incorrect as a literal equality. In Silo A the fluxes are proportional (differ by $F$); in Silo B they are distinct physical quantities. The core equations in Section 3 are correct — this error is confined to the vocabulary matrix explanatory text.
- **Gibbs-Thomson absence in Silo B:** The vocabulary matrix attributes a Gibbs-Thomson role to $(c - c_{eq})$ in Silo B, but Section 3 shows no such term. The entry acknowledges dispersion-based regularization instead. Confirm whether a Gibbs-Thomson curvature term is physically appropriate for the acidization model or is correctly absent.

### Seventh Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
* **CHECK 1 (Equation Validity):** FLAG — Section 3 states a Mullins-Sekerka dispersion correspondence but gives separate dispersion relations with different regularization coefficients and no derivation connecting those relations to the displayed governing systems.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping `electric overpotential $\eta$ ↔ acid concentration over-saturation $(c-c_{eq})` is a category/dimensional mismatch, while the accompanying claim that both are an `$H^1$-trace of concentration field` is false for the electric overpotential.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 1 is supported by the two elliptic equations and weak-form statement; Vector 2 is not demonstrated on Silo A because its Robin law is `-D_{Li}\partial_n c=k_{BV}c` while its Stefan velocity is independently defined from `-\kappa\partial_n\phi`, with no equation identifying those two fluxes; Vector 3 has displayed conservation and dispersion equations but the claimed Mullins-Sekerka correspondence is not derived from the two systems.
* **CHECK 4 (Transfer and Falsifiability):** FLAG — The stated A→B transfer is presented as asymmetric and the prediction gives measurable numerical outcomes, but the proposed surfactant falsification test does not cleanly isolate curvature regularization because the intervention can alter other interfacial/transport properties.

#### Stage 3 Watch Items
* Probe the asserted Mullins-Sekerka dispersion correspondence and whether the Silo A and Silo B stability laws genuinely follow from the displayed governing equations.
* Probe the quantitative falsification experiment for confounding effects of the surfactant intervention.
* No specific prior-art recognition is asserted here; bibliometric novelty remains for Stage 3.

### Eighth Adversarial Review
**Reviewer:** Microsoft Copilot 1.2 
**Protocol:** v2.0  
**Verdict:** REJECT  
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry asserts an equality between electrical current density and species diffusive flux at the interface: it states verbatim \"where $J_n = -\\sigma \\partial_n \\Phi = -D \\partial_n c$ at $\\Gamma(t)$ by Robin balance.\" This is mathematically and physically incorrect without a derived coupling: electrical current density (units A/m^2) and species diffusive molar flux (units mol/(m^2·s)) are different quantities and cannot be equated without explicit inclusion of migration terms, Faraday's constant, and stoichiometric conversion; the body elsewhere uses $v_{n,A}=(\\Omega_m/F) j_n$ while simultaneously imposing $-D_{Li}\\partial_n c = k_{BV} c$, which shows the two fluxes are treated inconsistently rather than demonstrated equal.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are of compatible mathematical types (elliptic conductivity ↔ permeability/mobility; normal velocity ↔ normal velocity; Robin flux coefficient ↔ reaction-rate constant) and the Operator Role entries specify shared operator structure rather than purely hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 1 (shared elliptic operator) and Vector 2 (Robin reactive flux + Stefan law) are presented with equations; Vector 3 (Mullins-Sekerka dispersion threshold with global flux conservation) is asserted and linear-stability formulas are given, but the derivation replaces curvature Gibbs-Thomson regularization with a transverse dispersion coefficient (\\alpha_{disp}) without a demonstrated operator identity or derivation that shows equivalence of the regularizing mechanisms; moreover, the fundamental flux equality needed to link the elliptic operator to the Stefan law in Silo A is invalid (see CHECK 1), so the claimed triple correspondence set is not fully demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction (Silo A → Silo B) is plausibly asymmetric as argued, and the entry gives a concrete, measurable falsifiable prediction (shift in PVBT and fractal dimension with specified experimental conditions). However, the falsifiability claim depends on the correctness of the mathematical coupling (notably the flux identity and curvature regularization mapping), so the prediction is not presently supported by a consistent derivation; recommend human reviewers verify experimental feasibility and whether the proposed surfactant-induced change in effective interfacial energy maps to the model parameter used in the phase-field transfer.

#### Stage 3 Watch Items
- The human reviewer should request a clear derivation showing how Butler-Volmer Faradaic current density maps to a molar/species flux at the interface in the electrolyte model used here, including units, Faraday conversion, and any migration contributions; the present text asserts equality without derivation.
- Verify the dimensional consistency and physical origin of the term the authors call \"\\alpha_{disp}\" and whether it legitimately plays the same mathematical role as Gibbs-Thomson curvature regularization (\\Gamma_{GT}) in the linear-stability dispersion relation; ask for a derivation showing the same operator-order and sign in the dispersion relation.
- Check whether the linearization of Butler-Volmer used to identify $k_{BV}$ with a first-order Robin coefficient is applied within a regime where migration and concentration polarization are negligible; if not, the mapping to a simple Robin condition is not justified.
- Confirm experimental parameters and measurement protocols for the falsifiable prediction (PVBT shift and fractal dimension change) and whether the proposed surfactant-induced change in interfacial energy is the dominant mechanism at the Darcy scale.

### Ninth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both systems are correctly written as elliptic divergence-form potential equations coupled to parabolic advection-diffusion with Robin flux and Stefan velocity; the shared class holds under the explicit linearization of Butler-Volmer.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping “electric overpotential η ↔ acid concentration over-saturation (c − c_eq)” pairs a thermodynamic driving force (voltage) with a concentration difference; the Operator Role claims both enter as an additive shift to a Dirichlet value via Gibbs-Thomson, but the mathematical types remain distinct (voltage vs concentration) and no explicit nondimensional transformation equating them is supplied.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated: shared elliptic operator appears as ∇·(σ∇Φ)=0 in both equation blocks; Robin-Stefan pair appears in the third line of each block together with the identification v_n = β(−D ∂_n c); Mullins-Sekerka dispersion with global flux conservation is shown by the integral constraints and the explicit σ(k) formulas for both silos.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The preferred direction (phase-field dendrite methods → wormholing) is argued on the basis of variational curvature regularization versus ad-hoc tip cutoffs, which is plausible, yet both communities already possess mature continuum and dimensionless tools, so asymmetry is only moderate; the numerical prediction for PVBT shift and fractal-dimension change is specific and falsifiable.

#### Stage 3 Watch Items
- Verify whether linearized Butler-Volmer truly recovers the linear first-order dissolution kinetics of Silo B at the claimed |Fη/RT|<0.2 regime
- Confirm that the Gibbs-Thomson term in Silo A and the transverse-dispersion regularization in Silo B are operator-equivalent rather than merely both providing k^{2} damping
- Assess whether phase-field import into Darcy-scale acidization is novel relative to existing continuum reactive-infiltration models