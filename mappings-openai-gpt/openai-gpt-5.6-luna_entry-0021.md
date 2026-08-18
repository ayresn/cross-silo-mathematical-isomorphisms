---
sid_metadata:
  entry_id: "SID-0021"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "OpenAI"
  model_family: "GPT"
  model_version: "5.6 Luna"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "reactive-infiltration-instability-in-porous-geochemistry"
  domain_b: "autothermal-reactive-transport-in-porous-catalysts"
  structural_family: "advection-diffusion-reaction-front-instabilities"
  triple_correspondence_vectors:
    - "Darcy-advection-diffusion-reaction_operator"
    - "mixed_Dirichlet-Neumann_inlet-outlet_flux_boundary_pair"
    - "Peclet-Damkohler_instability_parameter_pair"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / different_constitutive_ontologies"
prior_discovery_metrics:
  structural_isomorphism_score: 8.1
  vocabulary_divergence_score: 8.8
  expected_methodological_transfer_score: 8.4
  community_separation_score: 8.7
  representation_mismatch_score: 7.9
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.6
    uncertainty: "±1.4"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "Section 4's Falsifiable Prediction is mathematically false under the entry's own Section 3 eigenvalue relation, since holding Λ=Da/Pe fixed while doubling (Pe,Da) from (100,10) to (200,20) exactly doubles both λ±, making the claimed sub-1% profile collapse contradicted by the entry's own mathematics."
    failed_checks: ["Check 4 (Falsifiability): the (Pe,Da)=(100,10) vs (200,20) worked example claims sub-1% dimensionless-profile collapse from matching Λ alone; the entry's own eigenvalue formula shows this is false."]
    flagged_checks: ["Check 1 (Equation Validity): the nondimensional transient PDEs silently drop the storage coefficients φ (Silo A) / ε (Silo B) present in the dimensional equations, inconsistent with the entry's own stated τ=u0t/L; does not affect the spatial-operator vector actually claimed.", "Check 4c (Prior Art, advisory only): Peclet-Damkohler-parameterized front-localization analysis is a recurring technique across combustion theory and reaction-diffusion front literature; Stage 3 should check for prior work pairing reactive-infiltration and autothermal-catalysis fronts specifically."]
    quoted_evidence: ['two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (\hat c(\xi)) below (1%) after convergence.', '\lambda_{\pm} = \frac{Pe}{2}\left(1\pm\sqrt{1+\frac{4Da}{Pe}}\right)', 'A successful transfer should collapse geometrically similar simulations onto the same nondimensional front-localization curve when (Pe) and (Da) are held fixed, despite changes in (L), (u), (D), and (k).']
    stage_3_watch_items: ["Bibliometric check for prior work connecting reactive-infiltration/dissolution fronts to combustion or autothermal-catalysis fronts via Peclet-Damkohler-type front-localization analysis (Check 4c, advisory only, not grounds for rejection).", "Verify the literature-maturity claim that autothermal catalytic-reactor continuation/bifurcation methods for (Pe,Da)-parameterized fronts are more developed than equivalent methods in the geochemical reactive-infiltration literature (Section 4, Asymmetric Maturity Rationale); not verifiable from the entry text alone.", "If revised, confirm any replacement falsifiable prediction holds both Pe and Da fixed individually, not merely their ratio Λ=Da/Pe, consistent with the entry's own correct statement in Target Bottleneck Mitigation.", "Confirm whether τ is intended as a porosity/voidage-normalized time (e.g. τ=u0t/(φL)) in both silos; if so, Silo A's φ and Silo B's ε need not be equal, so the two τ axes may not represent the same physical time-normalization, even though the spatial-operator correspondence itself is unaffected."]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The Section 4 prediction asserts that equal Λ=Da/Pe alone guarantees identical dimensionless steady profiles for (Pe,Da)=(100,10) and (200,20), but the entry's own Section 3 operator depends separately on Pe and Da and coincides only when both match."
    failed_checks: ["Check 4: prediction claims collapse from equal Λ alone, contradicted by the entry's dimensionless operator and operator-coincidence condition"]
    flagged_checks: []
    quoted_evidence: ["two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (\\hat c(\\xi)) below (1%) after convergence."]
    stage_3_watch_items: ["Verify whether the Pe-Damkohler 'instability' vector is supported by a temporal stability or bifurcation analysis rather than only steady spatial eigenvalue localization.", "Assess prior art: Pe/Damkohler scaling and advection-diffusion-reaction front localization are standard in reactive-transport and catalytic reactor literature.", "Check whether constant porosity factors (φ, ε) are legitimately absorbed into the time scale, since the nondimensional equations omit them despite τ = u_0 t/L."]
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a mathematically false falsifiable prediction that contradicts its own eigenvalue formula, and its nondimensionalized equations omit the porosity/storage coefficients present in the dimensional equations without stating the required restriction."
    failed_checks:
      - "Check 1: Nondimensional ADR equations omit φ/ε under the stated τ=u0t/L scaling."
      - "Check 4: The falsifiable prediction asserts that fixed Λ=Da/Pe implies identical dimensionless steady profiles when Pe and Da are doubled, but the entry's own λ± formula implies the profiles change."
    flagged_checks: []
    quoted_evidence:
      - '\phi \frac{\partial c_A}{\partial t} + u_A\frac{\partial c_A}{\partial x} = D_A\frac{\partial^2 c_A}{\partial x^2} - k_A c_A'
      - '\varepsilon \frac{\partial c_B}{\partial t} + u_B\frac{\partial c_B}{\partial x} = D_B\frac{\partial^2 c_B}{\partial x^2} - k_B(T)c_B'
      - '\frac{\partial \hat c_A}{\partial \tau} + \frac{\partial \hat c_A}{\partial \xi} = \frac{1}{Pe_A}\frac{\partial^2\hat c_A}{\partial \xi^2} - Da_A\hat c_A'
      - '\frac{\partial \hat c_B}{\partial \tau} + \frac{\partial \hat c_B}{\partial \xi} = \frac{1}{Pe_B}\frac{\partial^2\hat c_B}{\partial \xi^2} - Da_B\hat c_B'
      - 'two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (\hat c(\xi)) below (1%) after convergence'
      - '\lambda_{\pm} = \frac{Pe}{2} \left( 1\pm\sqrt{1+\frac{4Da}{Pe}} \right)'
    stage_3_watch_items:
      - "Check whether the omitted φ/ε is an unstated porosity=1 restriction or a derivation error."
      - "Verify the claimed asymmetry: whether autothermal catalysis actually has the more developed continuation/bifurcation toolkit for ADR fronts compared with reactive-infiltration geochemistry."
      - "Probe the boundary-condition label: 'convective-dispersive outlet flux' is written as -D ∂c/∂x=0, i.e. zero diffusive flux, not zero total flux."
      - "Prior-art watch: Pe-Da ADR front localization is a canonical framework in both porous-media and reactor-engineering literatures; Stage 3 should check whether this operator-level identity is already standard."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The falsifiable prediction makes a mathematically impossible claim that directly contradicts the spatial eigenvalues derived in Section 3."
    failed_checks: ["Check 4: Mathematically invalid falsifiable prediction"]
    flagged_checks: ["Check 1: Imprecise nondimensionalization of time derivatives"]
    quoted_evidence: ["two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L)"]
    stage_3_watch_items: ["Verify if the structural analogy between reactive infiltration and autothermal catalysts is already canonical prior art (e.g., works by Luss, Aris, or Ortoleva).", "Address the omitted porosity/void fraction coefficients in the transient terms if time-dependent dynamics are to be simulated."]
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "All four equations are valid and belong to the same parabolic advection-diffusion-reaction class; all three vocabulary mappings pair objects of compatible mathematical type; all three correspondence vectors are demonstrated with explicit equations and derivations; and the transfer direction and falsifiable prediction are specific and well-scoped."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The general class of advection-diffusion-reaction front instabilities in porous media is well-studied in both geochemistry and catalytic-reactor engineering. The human reviewer should verify via bibliometric search that this specific cross-disciplinary operator-level mapping (reactive-infiltration instability ↔ autothermal catalytic transport, parameterized identically in Pe-Da space) has not been made explicitly in published review articles or monographs on reactive transport in porous media."
      - "The entry restricts the linearized operator to constant-coefficient form by freezing porosity/permeability (Silo A) and temperature-dependent kinetics (Silo B). The human reviewer should confirm that the catalytic-reactor community's continuation/bifurcation toolkit is in fact more mature than the geochemical community's for this restricted operator class, as the asymmetry claim depends on this being true."
      - "The falsifiable prediction specifies (Pe, Da) = (100, 10) and (200, 20) with Λ = 0.1 and a 1% collapse tolerance. The human reviewer should check whether this tolerance is physically achievable given numerical diffusion in standard finite-volume schemes at these parameter values, and whether the linearized (constant-coefficient) restriction is sufficient to reach steady state in a computationally accessible domain length."
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "REJECT"
    verdict_rationale: "The falsifiable prediction in Section 4 claims that two simulations sharing the same ratio Λ=Da/Pe but having different Pe and Da must yield identical concentration profiles, which is directly contradicted by the eigenvalue analysis derived in the entry's own Section 3."
    failed_checks: ["Check 4b: Prediction claims same Λ=Da/Pe implies same steady-state concentration profile, but the entry's own eigenvalues λ±=(Pe/2)(1±√(1+4Da/Pe)) depend on Pe and Da separately, not solely on their ratio"]
    flagged_checks: ["Check 4c: Advection-diffusion-reaction equation with Danckwerts boundary conditions and Pe-Da framework are canonical in transport phenomena and chemical reaction engineering"]
    quoted_evidence: ["two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (Λ=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (ĉ(ξ)) below (1%) after convergence"]
    stage_3_watch_items: ["ADR equation with Danckwerts BCs is canonical in transport phenomena (Bird, Stewart, Lightfoot; Levenspiel); Stage 3 should assess novelty of the specific geochemistry–catalysis pairing beyond the shared PDE", "Section 4 prediction contradicts Section 3 eigenvalue analysis; Stage 3 should verify whether the intended claim was about front-position scaling or eigenvalue ratio rather than full profile identity"]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "FLAG"
    verdict_rationale: "All mathematical correspondences are demonstrated, but the claimed methodological asymmetry in Section 4 is not convincingly justified and should be probed by a human reviewer."
    failed_checks: []
    flagged_checks:
      - "Check 4: Asymmetry claim — the entry asserts a one-way transfer (autothermal → reactive-infiltration) without sufficient evidence that the reverse direction would not be equally viable."
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify the practical asymmetry claim in Section 4: the entry states a preferred transfer direction 'Autothermal reactive-transport in porous catalysts → reactive-infiltration instability in porous geochemistry' but provides only qualitative maturity arguments; quantify toolset differences before accepting asymmetry."
      - "Confirm numerical-continuation readiness: the entry proposes transferring continuation/bifurcation machinery — check whether the source-field algorithms handle the specific boundary-value structure and parameter ranges typical of geological permeability feedback."
      - "Check constitutive-limits caveat: the entry explicitly notes 'the correspondence does not extend to the nonlinear constitutive laws linking permeability to mineral dissolution or reaction rate to temperature' — ensure Stage 3 examines whether this caveat undermines the proposed numerical-transfer experiments."
      - "Document verbatim evidence (for Stage 3 reference): 'This establishes the first correspondence vector, **Darcy-advection-diffusion-reaction operator**, without claiming that the full nonlinear physical systems are identical.'"
      - "Document verbatim evidence (for Stage 3 reference): 'Thus the front localization length is controlled by the same two dimensionless groups in both silos.'"
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency of the claimed linearized ADR operator, mixed BCs, and Pe-Da control with no category errors, undemonstrated vectors, or non-falsifiable transfer claims."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-13"
    verdict: "PASS"
    verdict_rationale: "All equations are same-class parabolic advection-diffusion-reaction operators with explicit restriction excluding nonlinear constitutive laws, vocabulary mappings are type-compatible, and all three claimed vectors are demonstrated with operator identities and boundary equations and a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Pe-Da scaling and collapse of ADR fronts is textbook porous-media reactive transport — probe bibliometrically whether the specific continuation/bifurcation transfer from autothermal catalysis to geochemical infiltration adds novelty beyond textbook operator equivalence", "Verify that Stage 3 distinguishes shared linearized operator (demonstrated) from full constitutive equivalence, which entry explicitly disclaims"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0021

## 1. CROSS-SILO SYSTEM DEFINITION

* **Silo A (Field 1):** Reactive-infiltration instability in porous geochemistry, specifically chemically reactive fluid penetration through a porous rock matrix where dissolution changes permeability and destabilizes the advancing reaction front.
* **Silo B (Field 2):** Autothermal reactive transport in porous catalytic media, specifically spatially distributed exothermic conversion where reactant transport and temperature-dependent reaction rates generate localized reaction fronts and thermal localization.
* **Mathematical Isomorphism:** After nondimensionalization and restriction to a one-dimensional homogeneous Darcy medium with a single mobile reactant, both systems possess the same linearized advection-diffusion-reaction operator, the same mixed inlet concentration/flux boundary structure, and the same controlling Peclet-Damkohler parameter combination governing front localization; the correspondence does not extend to the nonlinear constitutive laws linking permeability to mineral dissolution or reaction rate to temperature. 

## 2. DIAGNOSTIC VOCABULARY MATRIX

* **Reactive-infiltration transport operator** ↔ **reactant transport operator**

  * *Operator Role:* Both act on a scalar mobile-species field (c(x,t)) through the dimensional operator (D\partial_{xx}-u\partial_x) plus a local sink/source term (R), with (c) having units of concentration in both silos; no tensor-to-scalar or dimensional-to-dimensionless identification is required before the nondimensionalization in Section 3.

* **Mineral-dissolution reaction rate** ↔ **catalytic conversion rate**

  * *Operator Role:* Both enter as local nonlinear reaction terms (R(c,\chi)) in the same scalar balance law, while the auxiliary state (\chi) differs physically: porosity/permeability evolution in Silo A and temperature-dependent catalytic activity in Silo B. The structural identification is therefore at the reaction-operator level rather than a constitutive identity.

* **Infiltration front** ↔ **reaction/thermal front**

  * *Operator Role:* Both are represented by a steep spatial gradient of the transported scalar and are localized by competition between advection, diffusion, and reaction. The common dimensionless localization parameters are the Peclet number (Pe=uL/D) and Damkohler number (Da=kL/u).

## 3. CORE MATHEMATICAL PARALLELISM

In Silo A, a minimal reactive-infiltration model for a mobile aqueous reactant (c_A) in a homogeneous porous column is the conservation equation coupled to Darcy transport. With constant porosity and permeability during the short-time front calculation, the mobile concentration satisfies

```math
\phi \frac{\partial c_A}{\partial t}
+
u_A\frac{\partial c_A}{\partial x}
=
D_A\frac{\partial^2 c_A}{\partial x^2}
-
k_A c_A ,
\qquad
u_A=-\frac{K_A}{\mu_A}\frac{\partial p_A}{\partial x}.
```

The corresponding inlet/outlet conditions can be written as a prescribed inlet concentration and convective-dispersive outlet flux:

```math
c_A(0,t)=c_{A,0},
\qquad
-D_A\frac{\partial c_A}{\partial x}(L,t)=0 .
```

Thus the demonstrated Silo-A operator is the advection-diffusion-reaction operator

```math
\mathcal L_A
=
D_A\partial_{xx}
-
u_A\partial_x
-
k_A .
```

In Silo B, the independently recognizable porous-catalyst model is the one-dimensional reactant balance for an exothermic catalytic medium,

```math
\varepsilon \frac{\partial c_B}{\partial t}
+
u_B\frac{\partial c_B}{\partial x}
=
D_B\frac{\partial^2 c_B}{\partial x^2}
-
k_B(T)c_B ,
```

with the temperature field coupled through the heat balance

```math
\rho C_p\frac{\partial T}{\partial t}
+
\rho C_p u_T\frac{\partial T}{\partial x}
=
\lambda\frac{\partial^2T}{\partial x^2}
+
(-\Delta H)k_B(T)c_B .
```

For the reactant field, an independently recognizable inlet/outlet specification is

```math
c_B(0,t)=c_{B,0},
\qquad
-D_B\frac{\partial c_B}{\partial x}(L,t)=0 .
```

Consequently, the reactant-sector operator is

```math
\mathcal L_B
=
D_B\partial_{xx}
-
u_B\partial_x
-
k_B(T).
```

The structural bridge is obtained by defining

```math
\xi=\frac{x}{L},
\qquad
\tau=\frac{u_0t}{L},
\qquad
\hat c=\frac{c}{c_0},
```

and, for each silo,

```math
Pe=\frac{u_0L}{D},
\qquad
Da=\frac{k_0L}{u_0}.
```

The nondimensional linearized reactant equations then become

```math
\frac{\partial \hat c_A}{\partial \tau}
+
\frac{\partial \hat c_A}{\partial \xi}
=
\frac{1}{Pe_A}\frac{\partial^2\hat c_A}{\partial \xi^2}
-
Da_A\hat c_A ,
```

and

```math
\frac{\partial \hat c_B}{\partial \tau}
+
\frac{\partial \hat c_B}{\partial \xi}
=
\frac{1}{Pe_B}\frac{\partial^2\hat c_B}{\partial \xi^2}
-
Da_B\hat c_B .
```

Under the explicit restriction

```math
Pe_A=Pe_B=Pe,
\qquad
Da_A=Da_B=Da,
```

the operators coincide:

```math
\mathcal L_A^\ast
=
\mathcal L_B^\ast
=
\frac{1}{Pe}\partial_{\xi\xi}
-
\partial_\xi
-
Da .
```

This establishes the first correspondence vector, **Darcy-advection-diffusion-reaction operator**, without claiming that the full nonlinear physical systems are identical.

The second correspondence vector, **mixed Dirichlet-Neumann inlet-outlet flux boundary pair**, follows directly from

```math
\hat c_A(0,\tau)=1,
\qquad
\partial_\xi\hat c_A(1,\tau)=0,
```

and

```math
\hat c_B(0,\tau)=1,
\qquad
\partial_\xi\hat c_B(1,\tau)=0.
```

The third correspondence vector, **Peclet-Damkohler instability parameter pair**, follows because the spatial eigenvalues of either common operator satisfy

```math
\frac{1}{Pe}\lambda^2-\lambda-Da=0,
```

or

```math
\lambda_{\pm}
=
\frac{Pe}{2}
\left(
1\pm\sqrt{1+\frac{4Da}{Pe}}
\right).
```

Thus the front localization length is controlled by the same two dimensionless groups in both silos. In particular, the ratio

```math
\Lambda=\frac{Da}{Pe}
=
\frac{kD}{u^2}
```

is identical under the mapping and determines the relative importance of reaction localization to advective transport.

The correspondence stops at this operator level. Silo A modifies permeability through a geological constitutive law, whereas Silo B couples reaction to temperature through an Arrhenius-type law,

```math
k_B(T)=k_{B,0}
\exp\!\left[
-\frac{E_a}{R}
\left(
\frac{1}{T}-\frac{1}{T_0}
\right)
\right].
```

Therefore the candidate claims a shared transport/front operator and parameter structure, not a complete constitutive equivalence.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

* **Preferred Transfer Direction:** Autothermal reactive-transport in porous catalysts → reactive-infiltration instability in porous geochemistry

* **Asymmetric Maturity Rationale:** The source field has comparatively mature continuation, parameter-sweep, stiffness-aware time integration, and front-localization analysis for coupled advection-diffusion-reaction systems, particularly when sharp reaction zones coexist with slowly varying transported fields. The target field is mature in reactive-transport formulation and geological constitutive modeling but has a narrower operational toolkit for systematically continuing front solutions across (Pe)-(Da) parameter space while retaining the geological permeability feedback. The proposed transfer is therefore specifically the numerical continuation and bifurcation-analysis machinery, not generic finite-element transport software.

* **Target Bottleneck Mitigation:** The testable hypothesis is that continuation of the geological front solutions using the source-field parameterization in ((Pe,Da)), rather than independent dimensional parameter sweeps, will identify a reproducible localization transition associated with the dimensionless ratio (\Lambda=Da/Pe). A successful transfer should collapse geometrically similar simulations onto the same nondimensional front-localization curve when (Pe) and (Da) are held fixed, despite changes in (L), (u), (D), and (k).

* **Falsifiable Prediction:** For a geometrically similar reactive-infiltration benchmark satisfying the restricted scalar model in Section 3, two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (\hat c(\xi)) below (1%) after convergence. The baseline is an independently resolved dimensional finite-volume solution of the same scalar benchmark. The hypothesis is falsified if either case differs by (1%) or more after grid refinement, or if simulations having identical (Pe) and (Da) do not collapse. This prediction is deliberately restricted to the demonstrated common operator and does not assert collapse once permeability evolution or temperature coupling becomes dynamically important.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"reactive infiltration instability" AND "Damkohler" AND "Peclet" AND "continuation"`
* `"autothermal reactor" AND "advection diffusion reaction" AND "Peclet" AND "Damkohler" AND "bifurcation"`
* `"reactive infiltration" AND "autothermal" AND "Peclet Damkohler" AND "porous"`
* `"mineral dissolution" AND "catalytic reactor" AND "front localization" AND "advection diffusion reaction"`
* `"reactive infiltration" AND "autothermal reactive transport" AND "operator equivalence"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The governing PDEs are correctly-classed linear parabolic advection-diffusion-reaction models and the claimed spatial operator identity 𝓛_A*=𝓛_B* is validly derived, but the nondimensional transient equations ("∂ĉ_A/∂τ+∂ĉ_A/∂ξ=(1/Pe_A)∂²ĉ_A/∂ξ²−Da_Aĉ_A") silently drop the storage coefficients carried by the dimensional equations ("φ ∂c_A/∂t" in Silo A, "ε ∂c_B/∂t" in Silo B), which is inconsistent with the entry's own stated "τ=u_0t/L" (no φ or ε); this gap does not affect the spatial-operator vector actually claimed, but it is unexplained in the derivation as displayed.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairings (transport operator↔transport operator, reaction rate↔reaction rate, front↔front) are type-compatible, and each Operator Role entry specifies a concrete shared mathematical structure (an explicit operator form, or the shared Pe/Da parameters) rather than resting on hedged similarity language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with derivations in Section 3: the operator coincidence 𝓛_A*=𝓛_B*=(1/Pe)∂_ξξ−∂_ξ−Da once Pe and Da are matched; the mixed Dirichlet-Neumann inlet-outlet flux boundary pair, shown identical in nondimensional form for both silos; and the Peclet-Damkohler instability parameter pair, shown via the shared eigenvalue equation (1/Pe)λ²−λ−Da=0.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — Asymmetry is adequately argued (a specific mechanism — continuation/bifurcation machinery for (Pe,Da)-parameterized fronts — is named, not generic software). Falsifiability fails: the entry claims (Pe,Da)=(100,10) and (200,20) "must have the same (\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile ... with the maximum pointwise difference in (\hat c(\xi)) below (1%)," but its own Section 3 relation "\lambda_{\pm}=\frac{Pe}{2}(1\pm\sqrt{1+4Da/Pe})" shows λ± scale linearly with Pe at fixed Λ, so doubling (Pe,Da) exactly doubles both eigenvalues (λ₋≈−9.16 → ≈−18.32). Solving the stated boundary-value problem gives ĉ(ξ)≈e^(λ₋ξ), e.g. ĉ(0.1)≈0.40 vs ≈0.16 — tens of percent apart, not sub-1%. This also directly contradicts the entry's own correct statement one paragraph earlier in Target Bottleneck Mitigation that collapse requires "(Pe) and (Da)" to be "held fixed," not merely their ratio Λ. No further prior art recognized beyond the general watch item below.

#### Stage 3 Watch Items
- Bibliometric check for prior work connecting reactive-infiltration/dissolution fronts to combustion or autothermal-catalysis fronts via Peclet-Damkohler-type front-localization analysis (Check 4c, advisory only, not grounds for rejection).
- Verify the literature-maturity claim that autothermal catalytic-reactor continuation/bifurcation methods for (Pe,Da)-parameterized fronts are more developed than equivalent methods in the geochemical reactive-infiltration literature (Section 4, Asymmetric Maturity Rationale); not verifiable from the entry text alone.
- If revised, confirm any replacement falsifiable prediction holds both Pe and Da fixed individually, not merely their ratio Λ=Da/Pe, consistent with the entry's own correct statement in Target Bottleneck Mitigation.
- Confirm whether τ is intended as a porosity/voidage-normalized time (e.g. τ=u₀t/(φL)) in both silos; if so, Silo A's φ and Silo B's ε need not be equal, so the two τ axes may not represent the same physical time-normalization, even though the spatial-operator correspondence itself is unaffected.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A and Silo B reactant equations are both parabolic advection-diffusion-reaction balances, and the displayed linearized operators support the stated shared linear transport-sector correspondence under the entry's explicit restriction to frozen/linearized coefficients.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are compatible mathematical objects (transport operators, reaction-rate terms, front features), and the Operator Role descriptions identify shared scalar balance-law structure rather than mere analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — The body demonstrates the operator vector via the nondimensional equations and operator identity, the boundary-pair vector via the dimensional and dimensionless Dirichlet/Neumann conditions, and the Pe-Da parameter-pair vector via the spatial eigenvalue equation; the word "instability" is not independently demonstrated as temporal instability, but the listed parameter-pair vector is equationally supported.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The proposed direction is plausibly asymmetric, but the prediction "two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (\hat c(\xi)) below (1%) after convergence." is contradicted by Section 3's operator \(\frac{1}{Pe}\partial_{\xi\xi}-\partial_\xi-Da\), whose coefficients depend separately on Pe and Da and whose coincidence is explicitly restricted to equal Pe and equal Da; prior-art advisory: Pe/Damkohler ADR front scaling is a standard reactive-transport/catalytic-reactor analogy.

#### Stage 3 Watch Items
- Verify whether the "instability" in the Pe-Damkohler vector has bibliometric support as a temporal/bifurcation instability, since the body only demonstrates steady spatial eigenvalues/front localization.
- Prior-art advisory: Pe/Damkohler scaling for advection-diffusion-reaction fronts is a standard reactive-transport/catalytic-reactor analogy; Stage 3 should check novelty against that literature.
- Check whether porosity factors φ and ε are legitimately absorbed into the time scale, since the nondimensional equations omit them although τ = u0 t/L.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The dimensional reactant equations contain the storage coefficients `φ` and `ε`, but the nondimensional equations under `τ = u0t/L` drop them without stating `φ=ε=1`; for example, `φ ∂c_A/∂t + u_A ∂c_A/∂x = ...` becomes `∂_τ ĉ_A + ∂_ξ ĉ_A = ...`, which does not follow from the stated scaling.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired terms are rate/operator objects of compatible type, and the operator-role explanations name the shared scalar balance-law structure rather than only hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are supported in Section 3: the common spatial ADR operator, the identical dimensionless boundary pair, and the Pe-Da eigenvalue/Lambda parameterization.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The prediction that `(Pe,Da)=(100,10)` and `(Pe,Da)=(200,20)` must have the same `Λ=0.1` and therefore the same dimensionless steady concentration profile is contradicted by the entry’s own `λ±` formula: doubling `Pe` and `Da` at fixed `Λ` doubles the spatial eigenvalues, so the boundary-layer profiles cannot coincide to 1%.

#### Stage 3 Watch Items
- Confirm whether the dropped `φ`/`ε` in the nondimensional equations is an intended but unstated unit-porosity restriction.
- Check whether the claimed transfer direction is actually asymmetric, given that both fields have mature ADR front-analysis traditions.
- Examine whether the outlet condition should be total flux `u c - D ∂c/∂x = 0` rather than the displayed zero-diffusive-flux condition `-D ∂c/∂x = 0`.
- Prior-art probe: the Pe-Da ADR front-localization operator identity may already be a textbook-level analogy across porous-media and catalytic-reactor modeling.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The nondimensionalized equations in Section 3 omit the porosity ($\phi$) and void fraction ($\varepsilon$) coefficients on the time derivative terms ($\partial \hat c / \partial \tau$) that would necessarily carry over from the dimensional equations given the explicitly defined timescale $\tau = u_0 t / L$.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped vocabulary correctly pairs objects of compatible mathematical type (scalar fields, rate terms, spatial gradients) and explicitly identifies their shared structural roles without relying on hedged language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed correspondence vectors (Darcy-advection-diffusion-reaction operator, mixed Dirichlet-Neumann inlet-outlet flux boundary pair, and Peclet-Damkohler instability parameter pair) are explicitly demonstrated with equations and mathematical derivations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The falsifiable prediction makes a mathematically impossible claim: "two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (\Lambda=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L)". As proven by the spatial eigenvalues $\lambda_{\pm} = \frac{Pe}{2} \left(1\pm\sqrt{1+\frac{4Da}{Pe}}\right)$ derived in Section 3, the steady-state profile $\hat c(\xi)$ depends independently on $Pe$ through the $Pe/2$ prefactor. Rescaling $x$ by $L$ (which produces $\xi$) does not collapse the spatial profiles for different $Pe$ values even if $\Lambda$ is identical. 

#### Stage 3 Watch Items
- Verify if the structural analogy between reactive infiltration and autothermal catalysts is already canonical prior art in the advection-diffusion-reaction literature (e.g., classical works by Luss, Aris, or Ortoleva).
- Address the omitted porosity/void fraction coefficients in the nondimensional transient equations if unsteady dynamics are to be analyzed.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B equations are standard parabolic advection-diffusion-reaction equations consistent with their stated physical domains; the nondimensionalization is algebraically correct; the eigenvalue derivation $\lambda_\pm = \frac{Pe}{2}(1 \pm \sqrt{1 + 4Da/Pe})$ follows correctly from the quadratic $\frac{1}{Pe}\lambda^2 - \lambda - Da = 0$; and the ratio $\Lambda = Da/Pe = kD/u^2$ is correctly derived and dimensionless.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three paired mappings (transport operators, reaction rates, front positions) connect objects of compatible mathematical type, and each Operator Role explanation specifies the shared structure explicitly (second-order linear differential operators on scalar fields, local nonlinear sink/source terms in identical balance-law positions, and steep spatial gradients localized by the same dimensionless parameter competition).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with equations in Section 3: the Darcy-advection-diffusion-reaction operator identity via nondimensionalization (§3, $\mathcal{L}_A^* = \mathcal{L}_B^*$), the mixed Dirichlet-Neumann boundary pair via explicit boundary conditions on both sides, and the Peclet-Damkohler instability parameter pair via the shared spatial eigenvalue equation and the $\Lambda = Da/Pe$ ratio.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (catalytic → geological) is genuinely asymmetric, targeting a specific methodological capability (numerical continuation and bifurcation analysis in Pe-Da parameter space) that the stated rationale argues is more developed in catalytic-reactor engineering. The falsifiable prediction is specific: two simulations at (Pe, Da) = (100, 10) and (200, 20) must yield identical dimensionless steady-state profiles within 1% pointwise tolerance after grid refinement, with explicit falsification criteria. No canonical prior-art pairing recognized for this specific cross-disciplinary mapping.

#### Stage 3 Watch Items
- The general advection-diffusion-reaction front-instability framework is well-studied in both communities; bibliometric search should confirm that this specific cross-disciplinary operator-level mapping in Pe-Da parameter space has not been made explicitly in published reviews or monographs on reactive transport in porous media.
- The asymmetry claim rests on the catalytic-reactor community's continuation/bifurcation toolkit being more mature than the geochemical community's for this specific operator class; the human reviewer should verify this comparative-maturity claim against the actual methodological literature in both fields.
- The 1% collapse tolerance in the falsifiable prediction should be checked for achievability given numerical diffusion at the specified (Pe, Da) values, and whether the linearized constant-coefficient restriction is sufficient to reach the steady states being compared.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B present parabolic advection-diffusion-reaction equations of the same class; the Darcy velocity, coupled heat balance, Arrhenius law, Danckwerts-type boundary conditions, and nondimensionalization are all correctly stated and drawn from the appropriate physical domains.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three vocabulary mappings pair objects of compatible mathematical type (transport operators acting on scalar concentration fields, local reaction rates entering the same scalar balance law, front descriptors characterized by steep spatial gradients); the operator-role explanations name specific shared structures such as "(D∂_{xx}−u∂_x) plus a local sink/source term (R)" rather than relying on hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body: (1) the operator coincidence 𝓛*_A = 𝓛*_B = (1/Pe)∂_ξξ − ∂_ξ − Da is derived explicitly with nondimensionalization; (2) the mixed Dirichlet–Neumann boundary pair is shown to coincide after rescaling for both silos; (3) the Pe–Da eigenvalue equation (1/Pe)λ² − λ − Da = 0 is derived and shown to control front localization in both silos, with the ratio Λ=Da/Pe=kD/u² identified as shared.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The falsifiable prediction states: "two simulations with ((Pe,Da)=(100,10)) and ((Pe,Da)=(200,20)) must have the same (Λ=0.1) and therefore the same dimensionless steady-state concentration profile after rescaling (x) by (L), with the maximum pointwise difference in (ĉ(ξ)) below (1%) after convergence." This claimed implication (same Λ ⟹ same profile) is false. The spatial eigenvalues derived in the entry's own Section 3 are λ± = (Pe/2)(1 ± √(1+4Da/Pe)), which depend on Pe and Da separately, not solely on Λ=Da/Pe. For (Pe,Da)=(100,10), λ₋ ≈ −9.16; for (Pe,Da)=(200,20), λ₋ ≈ −18.32. Since the steady-state profile is governed by these eigenvalues, different eigenvalues yield different profiles, so the entry's Section 3 analysis directly contradicts its Section 4 prediction. The asymmetry criterion (4a) is satisfied — the transfer of continuation/bifurcation machinery from catalysis to geochemistry is plausibly directional. Prior art advisory: the advection-diffusion-reaction equation with Danckwerts boundary conditions and the Peclet–Damköhler framework are canonical in transport phenomena and chemical reaction engineering (Bird, Stewart, Lightfoot; Levenspiel), noted for Stage 3 bibliometric investigation.

#### Stage 3 Watch Items
- The advection-diffusion-reaction equation with Danckwerts (Dirichlet-inlet, Neumann-outlet) boundary conditions and the Pe–Da parameter framework are canonical in transport phenomena and chemical reaction engineering. Stage 3 should assess whether the specific cross-domain pairing (reactive-infiltration geochemistry ↔ autothermal catalysis) is novel beyond the shared PDE.
- The Section 4 prediction contradicts the Section 3 eigenvalue analysis. Stage 3 should verify whether the intended claim was about a different kind of collapse (e.g., front-position scaling, eigenvalue ratio, or a regime where Pe is fixed and only Da varies) rather than full profile identity across different Pe values.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0  
**Verdict:** FLAG  
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A and Silo B PDEs are both presented as advection–diffusion–reaction scalar balance laws; the nondimensionalization and resulting linear operators are algebraically consistent and of the same parabolic class (both backward/forward parabolic advection–diffusion operators with local linear sink terms).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Mapped tokens are type-compatible: transport operator ↔ transport operator (both act on scalar concentration fields), reaction-rate ↔ catalytic conversion rate (both local scalar reaction operators), and front ↔ front (both steep gradients/localized structures controlled by Pe and Da).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed correspondence vectors are demonstrated in the body with equations or boundary specifications:  
  - **Darcy-advection-diffusion-reaction_operator** — shown by \(\mathcal L_A = D_A\partial_{xx}-u_A\partial_x-k_A\) and \(\mathcal L_B = D_B\partial_{xx}-u_B\partial_x-k_B(T)\) and the nondimensional coincidence under \(Pe_A=Pe_B,\ Da_A=Da_B\).  
  - **mixed_Dirichlet-Neumann_inlet-outlet_flux_boundary_pair** — shown by the inlet Dirichlet \(c(0,t)=c_0\) and outlet Neumann \(\partial_\xi \hat c(1,\tau)=0\) conditions for both silos.  
  - **Peclet-Damkohler_instability_parameter_pair** — shown by the shared characteristic equation \(\tfrac{1}{Pe}\lambda^2-\lambda-Da=0\) and its roots, and the identification \(\Lambda=Da/Pe\).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The falsifiability requirement is satisfied: the entry gives a concrete, testable numerical prediction (two parameter pairs with identical \(\Lambda\) must collapse to within 1% after nondimensional rescaling). However, the **asymmetry** claim is not convincingly established: the entry asserts that autothermal-catalyst methods are the appropriate source for transfer without providing quantitative evidence that the reverse transfer would be less effective or that the source tools uniquely address the target's bottleneck. This asymmetry statement therefore requires human scrutiny.

#### Stage 3 Watch Items
- **Asymmetry justification:** The human reviewer should probe the claim that continuation/bifurcation tools from autothermal reactive-transport are uniquely applicable to reactive-infiltration problems; request concrete examples or benchmarks showing the source-field methods outperforming native geological toolchains on equivalent operator-level problems.  
- **Numerical experiment specification:** Validate the proposed falsifiable test (Pe/Da collapse to 1% tolerance) by checking discretization, convergence, and whether the geological permeability feedback (explicitly excluded) could subtly affect the scalar benchmark even in short-time or restricted regimes.  
- **Constitutive-law boundary:** Confirm that Stage 3 explicitly examines whether the exclusion of permeability evolution and Arrhenius coupling (noted in the entry) invalidates the practical transfer for realistic geological scenarios.  
- **Prior-art check (advisory):** Although not a rejection criterion, Stage 3 should search for canonical prior mappings between advection–diffusion–reaction systems in porous media and catalytic reactors to ensure novelty claims are accurate.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed Silo-A and Silo-B reactant balances are both linear ADR equations of identical class; after the stated nondimensionalization and Pe/Da matching they share the same operator and support the claimed structural correspondence under the explicit constant-coefficient restriction.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired mapping joins objects of compatible mathematical type (scalar transport operators, local reaction terms, and front-localization parameters) and the Operator Role statements name the shared structure without category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — Darcy-advection-diffusion-reaction_operator is established by the explicit operator equality after nondim (Section 3); mixed_Dirichlet-Neumann_inlet-outlet_flux_boundary_pair is established by the matching nondim BCs (Section 3); Peclet-Damkohler_instability_parameter_pair is established by the shared eigenvalue formula and Λ ratio (Section 3).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric on the stated maturity grounds (continuation/bifurcation toolkit versus geological constitutive emphasis); the prediction supplies concrete (Pe,Da) pairs, a quantitative 1 % threshold on the rescaled profile, and an explicit falsification criterion restricted to the demonstrated operator.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-13

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos display parabolic advection-diffusion-reaction equations (phi c_t + u c_x = D c_xx - k c) with Darcy law and correctly derived common nondimensional operator L* = (1/Pe)∂_ξξ - ∂_ξ - Da; no class mismatch, no misattribution, and explicit restriction to linearized short-time front excludes nonlinear permeability/Arrhenius laws.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairings are type-compatible: operator↔operator, reaction rate R(c,χ)↔reaction rate, front gradient↔front gradient with Pe and Da as shared dimensionless parameters, with explicit operator roles and no spatial↔temporal or dimensional↔dimensionless category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 Darcy-advection-diffusion-reaction_operator demonstrated via L_A* = L_B* identity; Vector 2 mixed_Dirichlet-Neumann_inlet-outlet_flux_boundary_pair demonstrated via \hat c(0)=1, ∂_ξ\hat c(1)=0 in both silos; Vector 3 Peclet-Damkohler_instability_parameter_pair demonstrated via eigenvalue equation (1/Pe)λ^2-λ-Da=0 and Λ=Da/Pe derivation in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is credible (catalysis source: continuation/bifurcation/front-localization machinery; geochemistry target: constitutive modeling but narrower continuation toolkit); falsifiability is quantitative: same Λ=0.1 cases (100,10) vs (200,20) must collapse to <1% max pointwise difference in \hat c(ξ) or falsified. Advisory prior-art: general Pe-Da ADR collapse is textbook porous-media transport, not the exact silo pairing, flagged for Stage 3 novelty check.

#### Stage 3 Watch Items
- Probe bibliometrically whether Pe-Da front-localization and mixed Dirichlet-Neumann inlet/outlet for ADR in porous media is textbook (Bear, etc.) and whether the specific methodological transfer of continuation/bifurcation from autothermal catalytic reactors to reactive infiltration geochemistry is novel.
- Confirm entry's explicit disclaimer that correspondence stops at operator level and does not claim constitutive equivalence between permeability evolution and Arrhenius kinetics is respected in novelty search.