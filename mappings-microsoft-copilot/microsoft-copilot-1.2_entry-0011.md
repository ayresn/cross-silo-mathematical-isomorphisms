---
sid_metadata:
  entry_id: "SID-0011"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Microsoft"
  model_family: "Copilot"
  model_version: "1.2"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "electrodeposition-dendrite-growth"
  domain_b: "evaporative-colloidal-fingering-deposition"
  structural_family: "moving-boundary-flux-driven-instabilities"
  triple_correspondence_vectors:
    - "flux_limited_advection-diffusion_operator"
    - "normal_flux_to_interface_stefan_like_boundary_condition_with_kinetics"
    - "linear_dispersion_relation_with_curvature_stabilization_term"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.2
  vocabulary_divergence_score: 7.6
  expected_methodological_transfer_score: 7.9
  community_separation_score: 8.5
  representation_mismatch_score: 8.0
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
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "FLAG"
    verdict_rationale: "Checks 1-3 pass cleanly — the two governing equations are class-consistent, all three vocabulary pairs share genuine mathematical structure with no category errors, and all three correspondence vectors are equation-supported rather than merely named — and Check 4's asymmetry and falsifiability sub-claims both hold on their own terms, but Check 4c's advisory recognition of the broader Mullins-Sekerka moving-boundary universality class triggers a non-fatal FLAG for Stage 3 to investigate."
    failed_checks: []
    flagged_checks: ["Check 4 (4c): prior-art / universality-class recognition — advisory only, non-fatal per protocol"]
    quoted_evidence: []
    stage_3_watch_items: ["Prior art: the broader Mullins-Sekerka / diffusion-limited moving-boundary pattern-formation framework (e.g., Langer, Rev. Mod. Phys. 1980; Ben-Jacob & Garik, Nature 1990) already links electrodeposition dendrite growth to other diffusive growth instabilities such as solidification and viscous fingering; confirm whether the specific pairing with evaporative colloidal fingering deposition has itself already appeared in the literature.", "The Section 3 dispersion relation is asserted via 'the standard linearization ... to leading orders' and described as derived independently for both silos, but only one unified derivation is shown; verify the sigma(k) functional form directly, in particular the origin of the -Pe^-1 k^2 term given that the model retains the full time-dependent (non-quasi-steady) diffusion equation rather than a quasi-static Laplacian reduction.", "Section 2's second vocabulary pair labels its two transport terms 'flux' and 'drift' inconsistently, since both are written with an explicit factor of c and are therefore both literally fluxes, while the accompanying Operator Role text treats both as pure velocity fields U_eff without the c factor; not a category error, but confirm the underlying derivations are consistent with this relabeling.", "The curvature terms in each kinetic boundary condition (-kappa_m H and -kappa_p H) are added directly to the interfacial flux rather than expressed as a Gibbs-Thomson correction to c_eq or c_sat; this is algebraically equivalent to a linearized Gibbs-Thomson correction and is not an error, but confirm the implied coefficient definitions against how each field's literature actually reports curvature coefficients."]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "FLAG"
    verdict_rationale: "The moving-boundary parabolic correspondence and falsifiable transfer are internally coherent, but the claimed 'flux-limited' operator is not instantiated by the displayed equations and the curvature contribution to the claimed |k|^3 dispersion term is not derived from the local interface law shown."
    failed_checks: []
    flagged_checks:
      - "Check 3: vector 'flux_limited_advection-diffusion_operator' is only partially demonstrated; Section 3 displays ordinary advection-diffusion equations without a flux-limiting operator or constraint."
      - "Check 1: the claimed '|k|^3' curvature-capillary stabilization in Section 3 is not shown to follow from the displayed local curvature term '- Gamma_c Htilde' in the interface condition."
      - "Check 4: advisory prior-art flag; the general flux-driven moving-boundary instability framework is recognizable from Mullins-Sekerka/Saffman-Taylor-type pattern-formation literature."
    quoted_evidence: []
    stage_3_watch_items:
      - "Determine whether 'flux-limited advection-diffusion' is used technically (e.g., nonlinear flux limiter) or rhetorically in the source domains."
      - "Verify whether published electrodeposition/colloidal-fingering linear-stability models produce a k^2 or |k|^3 curvature stabilization term under the stated reduced boundary condition."
      - "Search for prior mappings between electrodeposition dendrite stability and evaporative/capillary fingering within Mullins-Sekerka or Saffman-Taylor frameworks."
      - "Check whether Faradaic current density and colloidal attachment flux mappings require explicit Faraday/molar-volume conversion factors in the bibliometric record."
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "REJECT"
    verdict_rationale: "The displayed linear-stability dispersion relation attributes a |k|^3 term to curvature, but the displayed nondimensional interface condition places curvature in the velocity law and linearizes to a k^2 contribution; the body does not demonstrate the coupling needed for the claimed term."
    failed_checks:
      - "Check 1: Dispersion relation curvature term is inconsistent with the displayed interface condition"
      - "Check 3: The listed vector linear_dispersion_relation_with_curvature_stabilization_term is not demonstrated by a valid derivation"
    flagged_checks: []
    quoted_evidence:
      - "The interface condition in nondimensional variables is \\tilde V_n = \\Lambda\\big(\\tilde c|_{\\Gamma}-\\tilde c_*\\big) - \\Gamma_c\\,\\tilde{\\mathcal H}"
      - "\\sigma(k) = \\Lambda\\,\\tilde J_0\\,|k| - \\mathrm{Pe}^{-1} k^2 - \\Gamma_c |k|^3 + \\mathcal{O}(k^4)"
      - "the |k|^3 term is curvature-capillary stabilization mapped from surface-energy in electrodeposition to capillary pressure in colloidal fronts"
    stage_3_watch_items:
      - "Determine whether the displayed moving-boundary equations actually produce the claimed dispersion relation; the |k| and |k|^3 terms require an unstated nonlocal flux/gradient condition."
      - "Query prior art on electrodeposition dendrite growth and colloidal/diffusion-limited fingering analogies (Mullins-Sekerka, viscous fingering)."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "REJECT"
    verdict_rationale: "The linear dispersion relation contains a fatal mathematical error where the leading flux-driven instability term is incorrectly multiplied by the kinetic coefficient."
    failed_checks: ["Check 1: Equation Validity"]
    flagged_checks: []
    quoted_evidence: ['\sigma(k) = \Lambda\,\tilde J_0\,|k| - \mathrm{Pe}^{-1} k^2 - \Gamma_c |k|^3 + \mathcal{O}(k^4)']
    stage_3_watch_items: ["Prior art: Check standard references on the Mullins-Sekerka instability to verify that the leading diffusion-limited destabilizing term is independent of the kinetic rate coefficient.", "Prior art: Investigate whether pulsed or AC flux-shaping protocols have already been translated to evaporative colloidal deposition to suppress fingering."]
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with explicit equations and operator identities in both domains; equation classes match (parabolic advection-diffusion with Stefan-type moving boundaries); vocabulary mappings are between compatible mathematical types; the transfer is genuinely asymmetric with a specific falsifiable prediction."
    failed_checks: []
    flagged_checks:
      - "Check 4c: The Mullins-Sekerka linear stability framework applied to electrodeposition dendrite growth is a canonical topic in the electrodeposition literature, and similar stability analyses for colloidal/drying front instabilities are established within that community. The specific novelty claim — transferring flux-shaping control protocols across domains — should be bibliometrically verified."
      - "Check 1 (minor): Section 1 writes σ(k)=αk − βk² − γk³ (plain k) while Section 3 correctly uses |k| for the odd-power terms to ensure symmetry σ(k)=σ(−k). The Section 1 version is non-symmetric and only valid for k>0; this is standard shorthand but technically inconsistent between the two sections."
    quoted_evidence:
      - "Section 1: σ(k)=αk − βk² − γk³ (leading-order terms shown)"
      - "Section 3: σ(k) = Λ J̃₀ |k| − Pe⁻¹ k² − Γ_c |k|³"
    stage_3_watch_items:
      - "Verify whether the specific cross-domain transfer of flux-shaping/pulsed-supply control strategies from electrodeposition to colloidal deposition has been published. The Mullins-Sekerka framework applied to each domain individually is well-established; the novelty lies in the methodological transfer."
      - "Confirm that the colloidal deposition community genuinely lacks operator-level pulse/flux-shaping instability-control tools — if such tools exist in the colloidal literature, the asymmetry rationale weakens."
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are from the stated domains and share the same parabolic class with Stefan-type boundary conditions, vocabulary mappings are type-compatible with shared structure named, all three correspondence vectors are demonstrated with equations, and the transfer is genuinely asymmetric with a specific falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The Mullins-Sekerka dispersion relation form σ(k) ~ |k| - k² - |k|³ is canonical in solidification theory; verify whether its application to evaporative colloidal fingering has been independently published."
      - "The specific transfer of pulsed-current/flux-shaping methodology from electrodeposition to colloidal deposition should be checked against the colloidal self-assembly and drying-mediated assembly literature for prior art."
      - "The claim that the colloidal deposition community lacks operator-level pulse/flux-shaping methodology should be verified — control of evaporation rates and contact-line pinning protocols may constitute an analogous existing toolkit."
  seventh_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "REJECT"
    verdict_rationale: "The claimed common dispersion relation is mathematically inconsistent with the explicitly stated local curvature-in-flux boundary condition, which produces a curvature contribution proportional to k^2 rather than the asserted |k|^3 term."
    failed_checks: ["Check 1: the stated boundary conditions do not support the claimed identical |k|^3 curvature stabilization in the dispersion relation", "Check 2: Faradaic current density is mapped directly to an adsorption particle flux without a stated charge-to-mass or molar-flux conversion"]
    flagged_checks: []
    quoted_evidence: ["j_n = k_0\\big(c|*{\\Gamma} - c*{eq}(\\phi|*{\\Gamma})\\big) - \\kappa_m \\mathcal{H},", "j_n^{(B)} = k*{ads}\\big(c|*{\\Gamma} - c*{sat}\\big) - \\kappa_p \\mathcal{H},", "\\sigma(k) = \\Lambda\\,\\tilde J_0\\,|k| - \\mathrm{Pe}^{-1} k^2 - \\Gamma_c |k|^3 + \\mathcal{O}(k^4),", "**Faradaic reaction current density (j_F)** ↔ **adsorption/attachment flux (j_{ads})**"]
    stage_3_watch_items: ["Probe the claimed electrodeposition ↔ evaporative-colloidal correspondence bibliometrically, especially the asserted common Mullins–Sekerka dispersion structure and flux-shaping transfer.", "Verify whether the electrodeposition current-density formulation has an explicit Faraday-law conversion to ionic molar/particle flux before comparison with the colloidal attachment flux."]
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: matching parabolic advection-diffusion operators, compatible Stefan-type kinetic boundary conditions with curvature, demonstrated dispersion relations of identical structure, coherent vocabulary types, and a specific falsifiable prediction under an asymmetric transfer direction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the quasi-electroneutral reduction for electrodeposition truly yields an effective advection field U_eff that is structurally interchangeable with a prescribed capillary drift (potential coupling vs. prescribed flow) under the stated limits."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-12"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with identical nondimensional advection-diffusion operator, Stefan-like flux-to-velocity law with curvature, and matching Mullins-Sekerka dispersion relation; no equation-class mismatch, vocabulary category error, or unfalsifiable prediction found."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0011

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** **Electrodeposition dendrite growth** in concentrated electrolytes (metal plating on a planar electrode) where ionic transport (diffusion + electromigration) supplies mass to a moving metal/electrolyte interface whose normal velocity is set by Faradaic reaction kinetics (Butler–Volmer type) and surface-energy (curvature) effects.
*   **Silo B (Field 2):** **Evaporative colloidal fingering deposition** (pattern formation at a receding contact line or drying front) where colloidal particles are transported by advection and diffusion toward a moving deposition front whose normal advance is set by adsorption/attachment kinetics and capillary/curvature-driven smoothing.
*   **Mathematical Isomorphism:** Under the quasi-electroneutral, thin-double-layer, and dilute-colloid limits, both systems reduce to a **flux-limited advection–diffusion operator** for a conserved scalar \(c\) supplying mass to a **moving boundary** whose normal velocity \(V_n\) is proportional to the **normal flux** \(J_n\) at the interface with a local kinetic law that includes a curvature-dependent term; linearizing about a flat front yields an identical **dispersion relation** of the form \(\sigma(k)=\alpha k - \beta k^2 - \gamma k^3\) (leading-order terms shown) where the destabilizing term is proportional to the steady flux and the stabilizing terms arise from diffusion and curvature — the correspondence holds after the explicit variable identifications and nondimensionalizations shown below.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Ion concentration \(c_i(\mathbf{x},t)\)** ↔ **colloid volume fraction \(c(\mathbf{x},t)\)**
  *   *Operator Role:* Both enter the same **advection–diffusion operator** \(\partial_t c + \nabla\cdot(\mathbf{u} c) = -\nabla\cdot \mathbf{J}\) with \(\mathbf{J}\) a diffusive (and electromigrative for ions) flux; both are scalar fields (conserved mass per unit volume) after nondimensionalization \(c\mapsto c/c_0\).
*   **Electromigration flux \(-\mu z c \nabla\phi\)** ↔ **advective capillary-driven drift \(c\,\mathbf{u}_{cap}\)**
  *   *Operator Role:* Both contribute a directed transport term that can be written as an effective advective flux \(\mathbf{U}_{\rm eff} c\); define \(\mathbf{U}_{\rm eff}^{(A)} = -\mu z \nabla\phi\), \(\mathbf{U}_{\rm eff}^{(B)}=\mathbf{u}_{cap}\); both are vector fields entering \(\nabla\cdot(\mathbf{U}_{\rm eff} c)\).
*   **Faradaic reaction current density \(j_F\)** ↔ **adsorption/attachment flux \(j_{ads}\)**
  *   *Operator Role:* Both set the **normal mass flux** into the moving interface and appear in the **Stefan-like boundary condition** \(V_n = \Omega j_n\) (with appropriate molecular/particle volume \(\Omega\)); both are scalar flux densities with kinetic dependence on local concentration and overpotential / local chemical potential.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A (Electrodeposition) — governing model (reduced, quasi-electroneutral limit).**  
Transport in the electrolyte for a single dominant cation species (after electroneutrality and thin double layer reduction) can be written as an advection–diffusion–migration equation for the cation concentration \(c(\mathbf{x},t)\):
```math
\partial_t c + \nabla\cdot\big(\mathbf{U}_{\rm eff}^{(A)} c\big) = D\,\nabla^2 c,
```
where \(\mathbf{U}_{\rm eff}^{(A)} = -\mu z \nabla\phi\) is the electromigration-induced drift (mobility \(\mu\), valence \(z\)), \(D\) is the ionic diffusivity, and \(\phi\) solves a quasi-electroneutral potential equation (Poisson reduced to a constraint) consistent with current continuity. At the metal/electrolyte interface \(\Gamma(t)\) the normal mass balance (Stefan-like) and kinetic law (Butler–Volmer linearized form shown) read:
```math
V_n = \Omega\, j_n,\qquad
j_n = k_0\big(c|_{\Gamma} - c_{eq}(\phi|_{\Gamma})\big) - \kappa_m \mathcal{H},
```
where \(V_n\) is the interface normal velocity, \(\Omega\) is atomic volume, \(j_n\) is the normal ionic flux consumed by plating, \(k_0\) is an effective kinetic coefficient (linearized Faradaic response), \(c_{eq}\) is the local equilibrium concentration (function of local potential), \(\kappa_m\) is a curvature-mobility coupling, and \(\mathcal{H}\) is mean curvature (surface-energy contribution).

**Silo B (Evaporative colloidal fingering) — governing model (thin-front deposition limit).**  
Colloidal particle transport toward a drying/deposition front is governed by advection–diffusion of particle concentration \(c(\mathbf{x},t)\):
```math
\partial_t c + \nabla\cdot\big(\mathbf{U}_{\rm eff}^{(B)} c\big) = D_p\,\nabla^2 c,
```
where \(\mathbf{U}_{\rm eff}^{(B)}\) is the capillary/evaporation-driven drift field (e.g., radial capillary flow toward the contact line), and \(D_p\) is the particle diffusivity. The moving deposition front \(\Gamma(t)\) satisfies a mass-balance and adsorption-limited kinetic law:
```math
V_n = \Omega_p\, j_n^{(B)},\qquad
j_n^{(B)} = k_{ads}\big(c|_{\Gamma} - c_{sat}\big) - \kappa_p \mathcal{H},
```
with \(\Omega_p\) the particle volume per deposited unit area, \(k_{ads}\) an attachment rate, \(c_{sat}\) a saturation concentration at the front, and \(\kappa_p\) a curvature-dependent smoothing coefficient (capillary pressure effect).

**Explicit operator-level correspondence and nondimensionalization.**  
Define nondimensional concentration \(\tilde c = c/c_0\), length scale \(L\), time scale \(T=L/U_0\) with \(U_0\) a characteristic drift speed, and nondimensional curvature \(\tilde{\mathcal H}=L\mathcal H\). Under the identifications
```math
\mathbf{U}_{\rm eff}^{(A)} \leftrightarrow \mathbf{U}_{\rm eff}^{(B)},\quad
D \leftrightarrow D_p,\quad
\Omega\,k_0 \leftrightarrow \Omega_p\,k_{ads},\quad
c_{eq}(\phi)\leftrightarrow c_{sat},
```
the two transport equations become identical in nondimensional form:
```math
\partial_{\tilde t}\tilde c + \nabla_{\tilde x}\cdot(\tilde{\mathbf U}\,\tilde c) = \mathrm{Pe}^{-1}\nabla_{\tilde x}^2\tilde c,
```
with \(\mathrm{Pe}=U_0 L/D\). The interface condition in nondimensional variables is
```math
\tilde V_n = \Lambda\big(\tilde c|_{\Gamma}-\tilde c_*\big) - \Gamma_c\,\tilde{\mathcal H},
```
where \(\Lambda\) is a nondimensional kinetic Damköhler-like number and \(\Gamma_c\) is the nondimensional curvature coefficient. Both systems therefore share the same **flux-to-velocity operator** mapping \(j_n\mapsto V_n\) and the same advection–diffusion operator for the supplying scalar.

**Linear stability (dispersion relation) — demonstrated on both sides.**  
Linearize a flat front at \(y=0\) with small perturbation \(h(x,t)=\hat h e^{ikx+\sigma t}\). For both systems (identical nondimensional operator and boundary condition above) the standard linearization (mass conservation + diffusion-limited supply + curvature term) yields, to leading orders,
```math
\sigma(k) = \Lambda\,\tilde J_0\,|k| - \mathrm{Pe}^{-1} k^2 - \Gamma_c |k|^3 + \mathcal{O}(k^4),
```
where \(\tilde J_0\) is the steady normal flux into the flat front (nondimensional), the \(|k|\) destabilizing term arises from the nonlocal coupling of front perturbations to the far-field flux (Mullins–Sekerka type kernel in both derivations), the \(k^2\) term is diffusion-limited smoothing, and the \(|k|^3\) term is curvature-capillary stabilization mapped from surface-energy in electrodeposition to capillary pressure in colloidal fronts. The same functional form and origin of each term are derived independently in the electrodeposition linearization (electromigration-diffusion + Butler–Volmer linear kinetics + curvature) and in the colloidal deposition linearization (capillary-driven advection + adsorption kinetics + capillary curvature), satisfying the Triple-Correspondence Rule: **(1)** governing operator, **(2)** boundary kinetic flux-to-velocity law with curvature, **(3)** linear dispersion relation with identical term structure.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** **Electrodeposition (Silo A)** → **Colloidal fingering deposition (Silo B)**
*   **Asymmetric Maturity Rationale:** The electrodeposition community has developed mature, quantitative linear-stability control strategies and time-dependent current-shaping protocols (pulsed currents, waveform engineering) grounded in operator-level models (Nernst–Planck + Butler–Volmer reductions) and fast spectral solvers for the Mullins–Sekerka kernel; they also possess experimentally validated in-situ diagnostics (electrochemical impedance spectroscopy, high-speed optical/electrochemical imaging) and control-theoretic pulse-design tools. The colloidal deposition community has precise experimental control of evaporation and flow but lacks a widely adopted operator-level pulse/flux-shaping methodology that maps a time-dependent supply flux to suppression of fingering instabilities via the same dispersion-kernel manipulation.
*   **Target Bottleneck Mitigation:** **Hypothesis:** Applying electrodeposition-style **flux-shaping protocols** (time-periodic modulation of the supply drift \(\mathbf{U}_{\rm eff}\) or the effective normal attachment rate \(k_{ads}(t)\)) designed by spectral optimization of the linear operator will reduce the maximum linear growth rate \(\max_k \sigma(k)\) for colloidal fingering below zero for a class of experimentally relevant Peclet numbers \(\mathrm{Pe}\in[10^1,10^3]\), thereby preventing fingering and producing uniform deposition fronts at higher mean flux than steady protocols allow. The transfer requires adapting pulse-design algorithms (spectral optimization, adjoint-based control) from electrodeposition to the colloidal advection–diffusion operator with the same kernel structure.
*   **Falsifiable Prediction:** For a planar drying front experiment with measured nondimensional parameters \(\mathrm{Pe}\) and \(\Gamma_c\), let the steady-state nondimensional flux be \(\tilde J_0\) and the steady maximal linear growth rate be \(\sigma_{\max}^{\rm steady}=\max_k \sigma_{\rm steady}(k)>0\). There exists a time-periodic modulation \(k_{ads}(t)=\bar k_{ads}\big(1+\epsilon\sin(2\pi f t)\big)\) with amplitude \(\epsilon\in(0,1)\) and frequency \(f\) such that the time-averaged maximal Floquet exponent \(\sigma_{\max}^{\rm pulsed}\) satisfies
```math
\sigma_{\max}^{\rm pulsed}(\epsilon,f;\mathrm{Pe},\Gamma_c,\tilde J_0) \le 0,
```
and the **quantitative** falsification test is: using the same experimental geometry and mean flux \(\bar k_{ads}\), the pulsed protocol must reduce the measured spectral power of front perturbations at the previously dominant wavenumber \(k^*\) by at least **90%** relative to steady deposition within three characteristic diffusion times \(T_D=L^2/D_p\). If repeated experiments at the same \(\mathrm{Pe}\), \(\Gamma_c\), and \(\tilde J_0\) fail to achieve \(\sigma_{\max}^{\rm pulsed}\le 0\) or do not reduce spectral power by ≥90%, the hypothesis is falsified. The inequality for \(\sigma_{\max}^{\rm pulsed}\) is computable from the linearized operator and the Floquet analysis derived from the equations above; no external numeric constants are assumed.
  
## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"electrodeposition dendrite linear stability" AND "Butler–Volmer" AND "Mullins–Sekerka"`
*   `"colloidal deposition fingering" AND "adsorption-limited deposition" AND "linear stability"`
*   `"pulsed current control" AND "morphological stability" AND "flux-shaping" `

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Section 3 governing equations for both silos are parabolic advection–diffusion PDEs (∂_t c + ∇·(U_eff c) = D∇²c and its B-side analogue) paired with linear-in-concentration Stefan-type kinetic boundary conditions plus a curvature term, matching the physical descriptions in Section 1, with no elliptic/parabolic, hyperbolic/dispersive, or linear/nonlinear class mismatch between the two sides.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three Section 2 pairs map objects of the same mathematical type onto the same operator role (scalar state variable, drift velocity field, and interfacial flux density, respectively), and each Operator Role explanation names a specific shared equation or boundary condition rather than hedged similarity language; none of the listed category-error patterns (space↔time, physical↔administrative, local field↔global scalar, rate↔position, dimensional↔dimensionless) is present.
- **CHECK 3 (Correspondence Vector Support):** PASS — Every listed vector is equation-supported: the flux-limited advection–diffusion operator is given explicitly for both silos in Section 3's first equation block and shown identical under the stated nondimensionalization; the Stefan-like boundary condition with kinetics is given explicitly in Section 3's second equation block for each silo and likewise shown identical; and the linear dispersion relation is presented in Section 3's linear-stability paragraph as the direct linearization of that now-identical system. None rests on name-only or vocabulary-only support.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (4a) is specific rather than reversible (mature pulse-plating/spectral control tools in electrodeposition vs. their documented absence in colloidal deposition control), and the falsifiable prediction (4b) names a concrete, quantitative outcome (≥90% reduction in spectral power at the dominant wavenumber within three diffusion times), not the vague template form. However, 4c is an advisory FLAG: the general Mullins–Sekerka/diffusion-limited moving-boundary framework linking electrodeposition to other pattern-forming instabilities is well established in the literature (e.g., Langer 1980; Ben-Jacob & Garik 1990), though the specific pairing with evaporative colloidal fingering deposition is not something recognizable as already-published from the entry text alone.

#### Stage 3 Watch Items
- Prior art: the broader Mullins–Sekerka / diffusion-limited moving-boundary pattern-formation framework (e.g., Langer, *Rev. Mod. Phys.* 1980; Ben-Jacob & Garik, *Nature* 1990) already links electrodeposition dendrite growth to other diffusive growth instabilities such as solidification and viscous fingering; confirm whether the specific pairing with evaporative colloidal fingering deposition has itself already appeared in the literature.
- The Section 3 dispersion relation is asserted via "the standard linearization ... to leading orders" and described as derived independently for both silos, but only one unified derivation is shown; verify the σ(k) functional form directly, in particular the origin of the −Pe⁻¹k² term given that the model retains the full time-dependent (non-quasi-steady) diffusion equation rather than a quasi-static Laplacian reduction.
- Section 2's second vocabulary pair labels its two transport terms "flux" and "drift" inconsistently, since both are written with an explicit factor of c and are therefore both literally fluxes, while the accompanying Operator Role text treats both as pure velocity fields U_eff without the c factor; not a category error, but confirm the underlying derivations are consistent with this relabeling.
- The curvature terms in each kinetic boundary condition (−κ_m H and −κ_p H) are added directly to the interfacial flux rather than expressed as a Gibbs–Thomson correction to c_eq or c_sat; this is algebraically equivalent to a linearized Gibbs–Thomson correction and is not an error, but confirm the implied coefficient definitions against how each field's literature actually reports curvature coefficients.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The two transport equations are compatible parabolic advection-diffusion moving-boundary models, but the entry claims “the \(|k|^3\) term is curvature-capillary stabilization” while the displayed interface condition contains “\(- \Gamma_c\,\tilde{\mathcal H}\)”, which linearizes locally as a \(k^2\) contribution unless an additional nonlocal field elimination is specified.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The vocabulary pairs concentration scalar fields, effective advective fluxes, and interfacial flux densities of compatible mathematical type, and the Operator Role statements name shared structures rather than mere analogy.
- **CHECK 3 (Correspondence Vector Support):** FLAG — The vectors “normal_flux_to_interface_stefan_like_boundary_condition_with_kinetics” and “linear_dispersion_relation_with_curvature_stabilization_term” are supported by the Section 3 interface conditions and dispersion formula, but “flux_limited_advection-diffusion_operator” is only partially supported because the equations in Section 3 are standard advection-diffusion equations without a flux-limiting operator.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry and falsifiability are adequately stated, but advisory prior-art recognition: the general flux-driven moving-boundary instability structure is familiar from Mullins-Sekerka/Saffman-Taylor pattern-formation frameworks; Stage 3 should verify whether this specific electrodeposition-colloid pairing has prior bibliometric coverage.

#### Stage 3 Watch Items
- Determine whether “flux-limited advection-diffusion” is used technically, e.g. as a nonlinear flux-limiter, or rhetorically as supply-flux-limited growth.
- Verify whether published linear-stability models for electrodeposition and colloidal fingering produce a \(k^2\) or \(|k|^3\) curvature stabilization term under the stated reduced boundary condition.
- Search for prior mappings between electrodeposition dendrite stability and evaporative/capillary fingering within Mullins-Sekerka, Saffman-Taylor, or diffusion-limited growth frameworks.
- Check whether the Faradaic current density to colloidal attachment flux mapping requires explicit Faraday/molar-volume conversion factors in the published record.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed nondimensional interface condition is \(\tilde V_n = \Lambda(\tilde c|_\Gamma-\tilde c_*)-\Gamma_c\tilde{\mathcal H}\). Since mean curvature for a small plane-wave perturbation scales as \(\tilde{\mathcal H}\sim k^2 h\), linearizing this velocity law gives a curvature contribution of order \(k^2\), not the claimed \(-\Gamma_c |k|^3\) term in \(\sigma(k)=\Lambda\tilde J_0|k|-\mathrm{Pe}^{-1}k^2-\Gamma_c|k|^3+\mathcal{O}(k^4)\). A \(|k|^3\) curvature term requires an additional unstated flux/gradient coupling multiplying the curvature contribution by \(|k|\).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are generally of compatible mathematical type: scalar concentration fields, vector transport fluxes, and interfacial flux densities. No quotable fatal category error is present.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The listed vector `linear_dispersion_relation_with_curvature_stabilization_term` is not demonstrated by a valid derivation in the body; it rests on the inconsistent dispersion relation identified in Check 1. The other two listed vectors have displayed governing/boundary equations.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric, and the falsifiable prediction names a measurable threshold: 90% spectral-power reduction at \(k^*\) within \(3T_D\). Prior-art watch: electrodeposition dendrite growth and colloidal/diffusion-limited fingering are canonical pattern-formation analogies; Stage 3 should query this pairing.

#### Stage 3 Watch Items
- Determine whether the displayed moving-boundary equations actually produce the claimed dispersion relation; the \(|k|\) and \(|k|^3\) terms require an unstated nonlocal Dirichlet-to-Neumann or flux-continuity condition.
- Query prior art on electrodeposition/colloidal fingering analogies, including Mullins-Sekerka, viscous fingering, and diffusion-limited aggregation.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The claimed dispersion relation `\sigma(k) = \Lambda\,\tilde J_0\,|k| - \mathrm{Pe}^{-1} k^2 - \Gamma_c |k|^3 + \mathcal{O}(k^4)` is mathematically inconsistent with the stated boundary condition. Equating the kinetic velocity with the diffusion-limited flux yields the exact relation `\sigma(k) = (|k| / (\Lambda + |k|)) (\Lambda \tilde J_0 - \Gamma_c k^2)`, meaning the leading destabilizing term for small `|k|` should be `\tilde J_0 |k|`, not `\Lambda \tilde J_0 |k|`. The entry incorrectly takes the numerator of the exact expression as the entire relation, erroneously implying the instability growth rate approaches infinity as kinetics become reversible ($\Lambda \to \infty$).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings pair compatible mathematical objects (scalar fields, vector fluxes, scalar flux densities) and clearly identify their shared structural roles without relying on hedged language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three correspondence vectors listed in the YAML are explicitly supported in the text with governing equations, boundary conditions, and a full (though mathematically flawed, as noted in Check 1) dispersion relation derivation.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric, leveraging mature spectral control methods from electrodeposition. The hypothesis provides a highly specific, quantitative, and falsifiable prediction (reducing spectral power at $k^*$ by at least 90% within $3 T_D$).

#### Stage 3 Watch Items
- Prior art: Check standard references on the Mullins-Sekerka instability to verify that the leading diffusion-limited destabilizing term is independent of the kinetic rate coefficient.
- Prior art: Investigate whether pulsed or AC flux-shaping protocols have already been translated to evaporative colloidal deposition to suppress fingering.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both systems are correctly modeled as parabolic advection-diffusion PDEs with Stefan-type moving boundary conditions including curvature corrections; the dispersion relation σ(k) = Λ J̃₀|k| − Pe⁻¹k² − Γ_c|k|³ has the correct Mullins-Sekerka term structure for a one-sided diffusion problem with kinetic undercooling. Minor inconsistency: Section 1 writes αk (plain k, asymmetric) while Section 3 correctly uses |k| (symmetric), but this is standard shorthand for k > 0.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three vocabulary pairs map objects of compatible mathematical type: scalar concentration ↔ scalar concentration, vector advective flux ↔ vector advective flux, scalar normal flux density ↔ scalar normal flux density. Each Operator Role specifies a shared mathematical structure (advection-diffusion operator, effective drift form, Stefan boundary condition), not merely a hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated: (1) the flux-limited advection-diffusion operator is shown as identical in nondimensional form (Section 3, Pe⁻¹∇²c̃ equation); (2) the Stefan-like boundary condition with kinetics is explicitly derived and nondimensionalized for both sides (Section 3, Λ and Γ_c boundary equation); (3) the linear dispersion relation with curvature stabilization is derived from the shared linearized operator and boundary condition with each term's physical origin traced on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (electrodeposition → colloidal deposition) is genuinely asymmetric: electrodeposition possesses mature pulsed-current control tools, spectral solvers for the Mullins-Sekerka kernel, and validated in-situ diagnostics, while colloidal deposition lacks an established operator-level flux-shaping instability-suppression methodology. The prediction is specifically falsifiable: a time-periodic modulation k_ads(t) must reduce spectral power at the dominant wavenumber by ≥90% within three diffusion times, or the hypothesis fails. A computable Floquet exponent condition σ_max^pulsed ≤ 0 is specified with named parameters.

#### Stage 3 Watch Items
- The Mullins-Sekerka linear stability framework applied to electrodeposition dendrite growth is canonical (extending back to Mullins-Sekerka 1963 for solidification, adapted to electrodeposition in the 1980s–90s). Similarly, linear stability analyses of colloidal/drying front instabilities are established within that community. The novelty claim specifically concerns the cross-domain transfer of flux-shaping control protocols. Bibliometric verification is needed to confirm this transfer has not been previously published.
- Verify whether the colloidal deposition community already possesses operator-level pulse or flux-shaping instability-control tools. If such methods exist, the asymmetry rationale in Section 4 weakens substantially.
- The entry's claim that the colloidal system is "dilute-colloid" limited should be checked against typical experimental parameters in the evaporative fingering literature — if typical experiments involve concentrated colloidal suspensions, the reduction to a simple advection-diffusion equation may not hold in practice.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B present parabolic advection–diffusion equations (∂_t c + ∇·(U_eff c) = D∇²c) with Stefan-type moving-boundary conditions (V_n = Ω j_n) incorporating linearized kinetics and curvature regularization. The equation classes match, both are genuinely from their stated domains (Nernst–Planck reduction for electrodeposition; capillary-driven colloidal transport for Silo B), and the shared nondimensional form Pe⁻¹∇²c̃ - ∇·(Ũ c̃) supports the claimed operator correspondence. The dispersion relation σ(k) = ΛJ̃₀|k| - Pe⁻¹k² - Γ_c|k|³ is the standard Mullins–Sekerka form and is consistent with the linearization of the stated equations and boundary conditions.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mappings pair compatible mathematical types: scalar concentration fields ↔ scalar concentration fields; vector advective fluxes ↔ vector advective fluxes (with explicit decomposition U_eff^(A) = -μz∇φ, U_eff^(B) = u_cap); scalar normal flux densities ↔ scalar normal flux densities. Each operator-role explanation names a specific shared structure (advection–diffusion operator, Stefan-like boundary condition V_n = Ωj_n, kinetic+curvature law) rather than relying on hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body. (1) "flux_limited_advection-diffusion_operator" is shown via the two transport equations reduced to identical nondimensional form (Section 3, "Explicit operator-level correspondence"). (2) "normal_flux_to_interface_stefan_like_boundary_condition_with_kinetics" is shown via both Stefan conditions V_n = Ωj_n with kinetic+curvature terms, nondimensionalized to Ṽ_n = Λ(c̃-c̃*) - Γ_c H̃ (Section 3). (3) "linear_dispersion_relation_with_curvature_stabilization_term" is shown via the shared dispersion relation σ(k) = ΛJ̃₀|k| - Pe⁻¹k² - Γ_c|k|³ derived from the identical nondimensional operator and boundary condition (Section 3, "Linear stability").
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetry is genuine: electrodeposition possesses mature pulsed-current and spectral pulse-design toolkits (Nernst–Planck + Butler–Volmer linearization, adjoint-based waveform optimization, in-situ impedance diagnostics), while the stated target (colloidal fingering) is claimed to lack an equivalent operator-level flux-shaping methodology despite having experimental flow control. The falsifiable prediction is specific: a time-periodic modulation k_ads(t) = k̄_ads(1 + ε sin(2πft)) must achieve σ_max^pulsed ≤ 0 (Floquet) and reduce spectral power at the dominant wavenumber k* by ≥90% within three diffusion times T_D = L²/D_p, at specified Pe ∈ [10¹, 10³] and Γ_c. Failure to meet either criterion under matched parameters falsifies the hypothesis. Prior-art advisory: the Mullins–Sekerka instability framework is canonical in solidification and electrodeposition theory; Stage 3 should verify whether its application to evaporative colloidal fingering has been previously published.

#### Stage 3 Watch Items
- The Mullins–Sekerka dispersion relation σ(k) ~ |k| - k² - |k|³ is canonical in solidification/electrodeposition theory; verify whether its specific application to evaporative colloidal fingering deposition has been independently published.
- The transfer of pulsed-current/flux-shaping methodology from electrodeposition to colloidal deposition should be checked against the drying-mediated assembly and evaporative lithography literature for prior art.
- The claim that the colloidal deposition community lacks operator-level pulse/flux-shaping methodology should be verified — existing evaporation-rate control and contact-line manipulation protocols may constitute a comparable toolkit under different terminology.
- The dispersion relation derivation relies on the quasi-static (Mullins–Sekerka) limit for the |k| kernel; Stage 3 should verify that this limit is physically appropriate for the stated Pe ∈ [10¹, 10³] range, where advection is non-negligible and the kernel may deviate from pure |k|.

### Seventh Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-12

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The explicitly stated local curvature terms in “(j_n = k_0(c|*{\Gamma} - c*{eq}(\phi|*{\Gamma})) - \kappa_m \mathcal{H})” and “(j_n^{(B)} = k*{ads}(c|*{\Gamma} - c*{sat}) - \kappa_p \mathcal{H})” enter the velocity directly through (V_n=\Omega j_n), so linearizing (\mathcal H) about a flat front supplies a (k^2) curvature contribution rather than the claimed (|k|^3) term; the displayed “(\sigma(k)=\Lambda\tilde J_0|k|-\mathrm{Pe}^{-1}k^2-\Gamma_c|k|^3+\mathcal O(k^4))” therefore does not follow from the stated boundary model.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping “**Faradaic reaction current density (j_F)** ↔ **adsorption/attachment flux (j_{ads})**” identifies an electrical current density with a particle/mass flux and supplies no Faraday-law or charge-to-particle conversion, despite using the latter as the quantity in (V_n=\Omega j_n).
* **CHECK 3 (Correspondence Vector Support):** PASS — The governing advection–diffusion correspondence is explicitly represented by equations in Sections 2–3, the flux-to-velocity/kinetic boundary correspondence is given by paired interface equations and nondimensional identifications in Section 3, and the dispersion-relation correspondence is stated by the displayed paired dispersion equation; however, the latter is mathematically invalid under Check 1.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction is explicitly justified as electrodeposition → colloidal deposition, and the prediction specifies measurable quantities ((\sigma_{\max}^{\rm pulsed}), a 90% spectral-power reduction, (k^*), and three diffusion times) that could falsify it; no prior-art recognition is used as a rejection basis.

#### Stage 3 Watch Items
* Probe the claimed electrodeposition ↔ evaporative-colloidal correspondence bibliometrically, especially the asserted common Mullins–Sekerka dispersion structure and flux-shaping transfer.
* Verify whether the electrodeposition current-density formulation has an explicit Faraday-law conversion to ionic molar/particle flux before comparison with the colloidal attachment flux.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both transport equations are of the same advection–diffusion class with identical Stefan-like kinetic-plus-curvature boundary conditions, and the shared nondimensional operator plus dispersion relation \(\sigma(k)=\Lambda\tilde J_0|k|-\mathrm{Pe}^{-1}k^2-\Gamma_c|k|^3+\mathcal{O}(k^4)\) are derived consistently from the stated reductions.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mapped pairs are objects of matching mathematical type (scalar concentrations, effective advective velocities, normal interface flux densities) and the Operator Role statements identify the shared advection–diffusion operator and flux-to-velocity map without category errors or pure hedging.
- **CHECK 3 (Correspondence Vector Support):** PASS — The three listed vectors (flux-limited advection–diffusion operator, normal-flux Stefan-like kinetic boundary condition with curvature, linear dispersion relation with curvature stabilization) are each exhibited by explicit equations and the common linearization in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric on the stated maturity grounds (electrodeposition pulse-control toolkit to colloidal systems); the prediction supplies a concrete, measurable threshold (\(\sigma_{\max}^{\rm pulsed}\le0\) and \(\ge90\%\) reduction in spectral power of the dominant mode within three diffusion times) that can fail experimentally.

#### Stage 3 Watch Items
- Verify whether the quasi-electroneutral reduction for electrodeposition truly yields an effective advection field \(U_{\rm eff}\) that is structurally interchangeable with a prescribed capillary drift (potential coupling vs. prescribed flow) under the stated limits.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-12

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos use the same parabolic advection-diffusion operator ∂_t c + ∇·(U_eff c) = D ∇^2 c with quasi-electroneutral / thin-front reductions, and matching Stefan-like boundary kinetics V_n = Ω j_n, j_n = k(c|_Γ - c_*) - κ H; no elliptic/parabolic, hyperbolic/dispersive, or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairs are type-compatible: scalar concentration field ↔ scalar volume fraction, vector electromigration flux ↔ vector capillary drift expressed as U_eff c entering ∇·(U_eff c), and scalar Faradaic current density ↔ scalar adsorption flux entering V_n = Ω j_n; operator roles name explicit shared structure with stated nondimensionalization c→c/c0.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors demonstrated in Section 3: flux_limited_advection-diffusion_operator via Silo A and Silo B transport equations and unified nondimensional form ∂_{tilde t}tilde c + ∇·(tilde U tilde c) = Pe^{-1}∇^2 tilde c; normal_flux_to_interface_stefan_like_boundary_condition_with_kinetics via V_n=Ω j_n and kinetic laws and nondimensional interface condition tilde V_n = Λ(tilde c|_Γ - tilde c_*) - Γ_c tilde H; linear_dispersion_relation_with_curvature_stabilization_term via σ(k)=Λ tilde J0|k| - Pe^{-1}k^2 - Γ_c|k|^3 + O(k^4) derived on both sides with Mullins-Sekerka kernel origin.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: Silo A → Silo B direction justified by mature pulsed-current waveform engineering, spectral solvers for Mullins-Sekerka kernel, and control-theoretic tools lacking in colloidal community; not reversible with comparable benefit and not backwards. Falsifiability satisfied by specific quantitative prediction: existence of periodic k_ads(t)=bar k_ads(1+ε sin(2π f t)) achieving time-averaged σ_max^pulsed ≤0 and ≥90% reduction of spectral power at dominant k* within 3 T_D = L^2/D_p at specified Pe∈[10^1,10^3], Γ_c, tilde J0; this names measurable threshold and experiment that can fail. No canonical textbook prior-art pairing (e.g., Schrödinger↔paraxial optics, Black-Scholes↔heat) recognized for this specific electrodeposition↔colloidal fingering pairing.

#### Stage 3 Watch Items
None identified.