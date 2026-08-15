---
sid_metadata:
  entry_id: "SID-0034"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "geocryology-frost-heave"
  domain_b: "lithium-metal-dendrite-electrodeposition"
  structural_family: "chemical-potential-driven-stefan-free-boundary"
  triple_correspondence_vectors:
    - "chemical_potential_divergence_mobility_transport_operator"
    - "capillary_kinetic_robin_interface_condition"
    - "stefan_faraday_normal_flux_accretion_law"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.7
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 8.1
  community_separation_score: 8.4
  representation_mismatch_score: 7.8
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±0.7"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "FLAG"
    verdict_rationale: "No equation-class mismatch, category-error vocabulary pairing, or undemonstrated correspondence vector was found, but the Γ_A/Γ_B basis inconsistency (Check 2) and the recognizable shared solidification-theory ancestry (Check 4c, advisory) are real, specifically-nameable, non-fatal issues, yielding an overall FLAG."
    failed_checks: []
    flagged_checks:
      - "Check 2: cryogenic suction ψ / Li electrochemical potential μ̃ mapping (Section 2) — Γ_A = 2γ_iw/ρ_i is a specific (per-mass) Gibbs-Thomson coefficient while Γ_B = Ω_Li γ_Li is a molar coefficient, so Π_A and Π_B sit on different physical bases that the entry never reconciles; K_w is also never given explicit units consistent with being used against a potential rather than a hydraulic head."
      - "Check 4c (Prior Art, advisory): Section 4's transfer direction and Section 3's free-boundary template — a Stefan-type moving boundary with a Gibbs-Thomson curvature term and kinetic (Robin) undercooling is a recognizable structure from classical solidification/crystal-growth theory, independently already applied to frost heave (segregation-potential / frozen-fringe theory) and to lithium dendrites (e.g., Monroe & Newman-style dendrite-growth analyses); this is advisory only and not grounds for rejection."
    quoted_evidence: []
    stage_3_watch_items:
      - "Confirm the intended physical basis (specific vs. molar) of ψ, Π_A, and K_w in Section 3, and whether Γ_A = 2γ_iw/ρ_i and Γ_B = Ω_Li γ_Li are meant to be put on a common basis before the Section 3 nondimensionalization."
      - "Search for prior literature directly pairing frost-heave segregation-potential theory with lithium-dendrite inception criteria, and check whether battery literature already contains a compact pore-curvature inception rule (e.g., beyond Monroe & Newman-style planar-front stability analysis), which would weaken Section 4's stated bottleneck claim."
      - "Verify the κ = 2/r hemispherical-tip curvature convention used in Section 4's falsifiable prediction matches whatever convention is implied for κ in Section 3's general Robin condition."
      - "Check how restrictive the 'locally constant K_w' assumption is against standard frozen-fringe treatments, where hydraulic conductivity is typically strongly suction- and temperature-dependent."
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "REJECT"
    verdict_rationale: "The lithium-side interface equation is dimensionally inconsistent: it adds a molar electrochemical potential to an overpotential (voltage) without conversion by the Faraday constant."
    failed_checks: ["Check 1: Lithium interface law Π_{B,i} = R_ct v_B + Γ_B κ mixes electrochemical potential and voltage units."]
    flagged_checks: []
    quoted_evidence:
      - "Define the local overpotential potential `Π_B = μ̃ - μ̃_eq`, where `μ̃_eq` is the equilibrium electrochemical potential of lithium metal."
      - "At the lithium/electrolyte interface, linearized Butler-Volmer kinetics plus capillarity give ... `Π_{B,i} = R_{ct} v_B + Γ_B κ`, ... where `v_B` is the normal plating velocity, `R_ct` is the linearized charge-transfer resistance expressed as an overpotential per unit velocity, and `Ω_Li` is the molar volume of lithium metal."
    stage_3_watch_items:
      - "Prior-art check for published frost-heave ↔ lithium-dendrite or ice-lens ↔ dendrite free-boundary analogies."
      - "Human reviewer should verify the correct linearized Butler-Volmer coefficient (F R_ct vs R_ct) if the entry is corrected."
      - "Human review of the frost-heave Gibbs-Thomson coefficient Γ_A = 2 γ_iw / ρ_i for dimensional consistency in the chosen water-potential convention."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "The entry demonstrates exceptional mathematical rigor, perfectly mapping the free-boundary Stefan problem across both domains with dimensionally consistent potentials, identical transport operators, and a highly specific falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: 
      - "Check recent literature on solid-state battery mechanics and dendrite propagation (e.g., works by Monroe, Newman, or modern phase-field studies) for prior conceptual or mathematical analogies to frost heave and ice lens segregation."
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are explicitly demonstrated with matched equations, all vocabulary pairs are mathematically type-compatible with specific shared structure claims, both sides belong to the same equation class (elliptic divergence-form transport with affine Robin free-boundary conditions and Stefan accretion laws), and the falsifiable prediction is specific and measurable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: [
      "The analogy between Stefan-type free-boundary models for solidification/frost-heave and electrochemical deposition has been explored in adjacent literature (phase-field models of electrodeposition, mushy-zone analogies). Stage 3 should verify whether this specific mapping — with frozen-fringe film flow and segregation-potential criteria imported to lithium dendrite inception — is novel or has prior art.",
      "The constitutive equivalence is rated 'medium' by the entry itself. The entry correctly notes the correspondence stops where constitutive physics diverges (heat equation, disjoining-pressure films, double-layer charging, etc.). Stage 3 should verify that the limited-parameter regime claimed (isothermal, dilute, quasi-steady, linearized-kinetics) is physically realizable in laboratory dendrite-inception experiments.",
      "The linearized charge-transfer resistance R_ct is defined as 'overpotential per unit velocity,' which is a specific (non-standard but internally consistent) parameterization of Butler-Volmer kinetics. Stage 3 should check that this parameterization has been validated experimentally at the relevant current densities."
    ]
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: both systems genuinely share the same elliptic divergence-form transport operator, Robin-type kinetic-capillary interface condition, and Stefan-type normal-flux accretion law, with all three correspondence vectors explicitly demonstrated and a specific falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify whether the specific frost-heave to lithium-dendrite Stefan-problem mapping has been previously published; the Gibbs-Thomson/capillary-kinetic interface condition is standard in solidification theory and its application to electrodeposition is known, so prior art may exist in the solidification-electrochemistry intersection."
      - "Confirm the dimensional convention for Γ_A = 2γ_iw/ρ_i against frost-heave literature: if Π_A is in pressure units (Pa) the prefactor appears inconsistent, but if Π_A is mass-specific (J/kg) it is consistent; the entry's nondimensionalization removes the issue but Stage 3 should verify the raw dimensional claim."
      - "Assess whether the falsifiable prediction η_rad(r) = 2Ω_Li γ_Li/(Fr) is genuinely novel or a standard Kelvin/Gibbs-Thomson result already known in the electrodeposition literature; the novelty claim rests on its use as a dendrite-inception design criterion, not the formula itself."
  sixth_adversarial_review:
    reviewer_model: "GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "REJECT"
    verdict_rationale: "Check 1 contains a genuine curvature-coefficient inconsistency: the frost-heave Gibbs-Thomson coefficient has an extra factor of 2 relative to the curvature convention used elsewhere in the entry, undermining the claimed shared capillary interface law."
    failed_checks: ["Check 1: The frost-heave capillary coefficient is inconsistent with the entry's stated curvature convention."]
    flagged_checks: []
    quoted_evidence: ["`\\Gamma_A = \\frac{2 \\gamma_{iw}}{\\rho_i}` together with `\\Pi_{A,i} = R_f v_A + \\Gamma_A \\kappa.`"]
    stage_3_watch_items: []
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "The entry demonstrates three mathematically consistent correspondences (divergence-form mobility operator, affine Robin capillary-kinetic interface, and Stefan/Faraday normal-flux accretion law) with matching equation classes and explicit derivations supporting each listed vector."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Check whether the claimed linearized charge-transfer resistance R_ct and the frozen-fringe interfacial resistance R_f are experimentally and dimensionally consistent across the nondimensionalization used; the entry states: \"Π_{A,i} = R_f v_A + Γ_A κ\" and \"Π_{B,i} = R_{ct} v_B + Γ_B κ.\""
      - "Verify prior-art overlap with canonical Stefan/Faraday moving-boundary formulations in electrochemistry and any existing Robin-type capillarity-kinetics interface laws applied to electrodeposition; the entry explicitly frames the mapping as: \"both systems reduce to the same Stefan-type free-boundary problem\" and uses the identity \"ρ_ph v_n = M ∂_n Π.\""
      - "Confirm experimental feasibility and measurement protocol for the falsifiable prediction relating hemispherical-tip curvature to overpotential: the entry gives the testable formula \"η_rad(r) = 2 Γ_B / (F r) = 2 Ω_{Li} γ_{Li} / (F r)\" and the ratio prediction \"η_rad(r)/η_rad(2r) = 2.\""
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are class-consistent and support the claimed Stefan free-boundary structure, vocabulary mappings are type-compatible with explicit shared operators, all three listed vectors are fully demonstrated by matching equations, and the transfer/prediction pair is asymmetric and quantitatively falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Confirm that the electrochemical-potential definition of Π_B (energy/mole) is consistently converted to voltage by the factor 1/F in experimental realizations of the predicted η_rad scaling.", "Verify that the quasi-steady dilute-limit assumptions used for both transport operators remain valid under the stated experimental conditions of the falsifiable prediction."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-15"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with matching elliptic divergence-form transport, affine Robin capillary-kinetic, and Stefan-Faraday flux accretion operators; vocabulary mappings are type-compatible with explicit nondimensionalization; transfer is asymmetric and prediction is quantitatively falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0034

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Geocryology / frost-heave mechanics: ice segregation and ice-lens growth in freezing colloidal or porous media, driven by cryogenic suction through unfrozen water films.
*   **Silo B (Field 2):** Lithium-metal battery electrodeposition: dendritic or filamentary lithium advance through a porous separator/electrolyte, driven by electrochemical potential gradients and sustained by Faradaic accretion.
*   **Mathematical Isomorphism:** In the isothermal, dilute, quasi-steady, linearized-kinetics limit in which a single mobile species supplies a growing phase through a confining layer, both systems reduce to the same Stefan-type free-boundary problem: a dimensionless chemical-potential field satisfies the same divergence-form mobility transport operator, the interface obeys the same affine Robin-type capillary-kinetic condition, and the normal interface velocity is given by the same normal-flux accretion law, with cryogenic suction mapped to electrochemical overpotential after the explicit nondimensionalization displayed in Section 3.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   `cryogenic suction ψ` ↔ `Li-ion electrochemical potential μ̃`
    *   *Operator Role:* The mapped driving potentials are `Π_A = ψ_m - ψ` and `Π_B = μ̃ - μ̃_eq`. After nondimensionalization `u_A = Π_A / ΔΠ_A` and `u_B = Π_B / ΔΠ_B`, they are dimensionless scalar potentials entering the same divergence-form mobility operator displayed in Section 3.

*   `hydraulic conductivity K_w` ↔ `ionic mobility M_B = D c / (R T)`
    *   *Operator Role:* These are the positive mobility coefficients multiplying the potential gradient in the same flux-divergence operator. With `M_A = ρ_w K_w` for the frost-heave mass flux and `M_B = D c / (R T)` for the lithium flux, the two transport operators coincide after the scaling in Section 3.

*   `ice-lens velocity v_A` ↔ `lithium plating velocity v_B`
    *   *Operator Role:* Both are the normal free-boundary velocities in the same accretion identity `ρ_ph v_n = M ∂_n Π` and in the same Robin interface law `Π_i = R v_n + Γ κ`.

*   `frozen-fringe interfacial resistance R_f` ↔ `charge-transfer resistance R_ct`
    *   *Operator Role:* Both are the coefficients of `v_n` in the affine Robin interface condition, converting interface velocity into a potential drop at the accreting boundary.

*   `Gibbs-Thomson ice coefficient Γ_A = 2 γ_iw / ρ_i` ↔ `lithium capillary coefficient Γ_B = Ω_Li γ_Li`
    *   *Operator Role:* Both multiply curvature `κ` in the same interface condition and produce the hemispherical-tip critical potential `2 Γ / r` used in the falsifiable prediction.

*   `segregation potential drop ΔΠ_A` ↔ `applied electrochemical overpotential ΔΠ_B`
    *   *Operator Role:* Both are the boundary driving potential differences across the transport length `L`; they set the far-field boundary value for the same one-dimensional transport solution used in the threshold derivation.

## 3. CORE MATHEMATICAL PARALLELISM

In frost-heave mechanics, ice segregation is modeled by water migration through an unfrozen fringe toward an ice lens. Let `ψ` be the cryogenic water potential and let `ψ_m` be the local melting-equilibrium potential. Define the suction potential `Π_A = ψ_m - ψ`, which is positive when water is drawn toward the ice lens. In the quasi-steady frozen-fringe limit, the water potential satisfies a divergence-form transport equation. For locally constant hydraulic conductivity `K_w`, this is

```math
\nabla \cdot \left(K_w \nabla \psi\right) = 0,
\qquad
\Pi_A = \psi_m - \psi,
\qquad
\nabla \cdot \left(K_w \nabla \Pi_A\right) = 0.
```

The ice-lens interface condition combines interfacial hydraulic resistance with Gibbs-Thomson curvature depression of the freezing potential. With normal velocity `v_A` and interface curvature `κ`,

```math
\Pi_{A,i} = R_f v_A + \Gamma_A \kappa,
\qquad
\Gamma_A = \frac{2 \gamma_{iw}}{\rho_i}.
```

The Stefan mass-balance condition equates ice accretion to the incoming water mass flux. With the normal `n` oriented so that positive flux is toward the growing ice phase,

```math
\rho_i v_A = \rho_w K_w \, \partial_n \Pi_A.
```

In lithium-metal electrodeposition, the relevant driving field is the electrochemical potential of lithium in the electrolyte or solid-ion conductor,

```math
\tilde{\mu} = \mu^0 + R T \ln\left(\frac{c}{c_{\mathrm{ref}}}\right) + F \phi.
```

Define the local overpotential potential `Π_B = μ̃ - μ̃_eq`, where `μ̃_eq` is the equilibrium electrochemical potential of lithium metal. In a dilute, isothermal, electroneutral transport layer of thickness `L`, the quasi-steady flux is written in terms of the mobility `M_B = D c / (R T)` as

```math
\nabla \cdot \left(M_B \nabla \tilde{\mu}\right) = 0,
\qquad
\Pi_B = \tilde{\mu} - \tilde{\mu}_{eq},
\qquad
\nabla \cdot \left(M_B \nabla \Pi_B\right) = 0.
```

At the lithium/electrolyte interface, linearized Butler-Volmer kinetics plus capillarity give

```math
\Pi_{B,i} = R_{ct} v_B + \Gamma_B \kappa,
\qquad
\Gamma_B = \Omega_{Li} \gamma_{Li},
```

where `v_B` is the normal plating velocity, `R_ct` is the linearized charge-transfer resistance expressed as an overpotential per unit velocity, and `Ω_Li` is the molar volume of lithium metal. Faradaic accretion gives the moving-boundary condition

```math
\frac{1}{\Omega_{Li}} v_B
=
M_B \, \partial_n \Pi_B,
\qquad
v_B
=
\Omega_{Li} M_B \, \partial_n \Pi_B
=
\frac{\Omega_{Li}}{F} i_n.
```

The explicit bridge is obtained by scaling the spatial coordinate and the two driving potentials:

```math
\hat{x} = \frac{x}{L},
\qquad
u_A = \frac{\Pi_A}{\Delta \Pi_A},
\qquad
u_B = \frac{\Pi_B}{\Delta \Pi_B},
```

and by introducing reference mobilities `K_w^0` and `M_B^0`:

```math
\hat{M}_A = \frac{K_w}{K_w^0},
\qquad
\hat{M}_B = \frac{M_B}{M_B^0}.
```

Under this transformation, both transport equations become

```math
\nabla_{\hat{x}} \cdot \left(\hat{M} \, \nabla_{\hat{x}} u\right) = 0.
```

The correspondence extends through the following three demonstrated vectors.

**Vector 1: chemical_potential_divergence_mobility_transport_operator.**  
For Silo A,

```math
\mathcal{L}_A[\Pi_A]
=
\nabla \cdot \left(K_w \nabla \Pi_A\right)
=
0.
```

For Silo B,

```math
\mathcal{L}_B[\Pi_B]
=
\nabla \cdot \left(M_B \nabla \Pi_B\right)
=
0.
```

After the nondimensionalization above, the two operators are identical in form:

```math
\mathcal{L}[u]
=
\nabla_{\hat{x}} \cdot \left(\hat{M} \nabla_{\hat{x}} u\right)
=
0.
```

**Vector 2: capillary_kinetic_robin_interface_condition.**  
For Silo A,

```math
\Pi_{A,i} = R_f v_A + \Gamma_A \kappa.
```

For Silo B,

```math
\Pi_{B,i} = R_{ct} v_B + \Gamma_B \kappa.
```

Both are the same affine Robin-type free-boundary condition,

```math
\Pi_i = R v_n + \Gamma \kappa,
```

with the parameter identifications

```math
(\Pi, R, \Gamma, v_n)_A
=
(\Pi_A, R_f, \Gamma_A, v_A),
\qquad
(\Pi, R, \Gamma, v_n)_B
=
(\Pi_B, R_{ct}, \Gamma_B, v_B).
```

**Vector 3: stefan_faraday_normal_flux_accretion_law.**  
For Silo A,

```math
\rho_i v_A
=
\rho_w K_w \, \partial_n \Pi_A.
```

For Silo B,

```math
\frac{1}{\Omega_{Li}} v_B
=
M_B \, \partial_n \Pi_B.
```

Both are the same normal-flux-to-velocity Stefan-type law,

```math
\rho_{\mathrm{ph}} v_n
=
M \, \partial_n \Pi,
```

with

```math
(\rho_{\mathrm{ph}}, M)_A
=
(\rho_i, \rho_w K_w),
\qquad
(\rho_{\mathrm{ph}}, M)_B
=
\left(\frac{1}{\Omega_{Li}}, \frac{D c}{R T}\right).
```

The correspondence stops where the constitutive physics diverges: frost heave may require a heat equation, disjoining-pressure films, and strong saturation-dependent permeability; lithium electrodeposition may require migration in non-dilute electrolytes, double-layer charging, convection, mechanical fracture, and electron tunneling. Those effects add operators not present in the minimal mapping above.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Geocryology / frost-heave mechanics → Lithium-metal battery dendrite electrodeposition.

*   **Asymmetric Maturity Rationale:** Frost-heave mechanics possesses a mature suite of ice-segregation criteria, frozen-fringe film-flow models, interfacial resistance laws, and curvature-dependent critical suction rules for confined porous media. Lithium-battery modeling is mature in porous-electrode transport, Newman-style continuum models, and phase-field dendrite simulations, but it lacks a compact, pore-scale free-boundary inception criterion that directly links separator pore curvature, interfacial kinetic resistance, and critical electrochemical driving force without resolving nanometer-scale double layers or running full phase-field simulations.

*   **Target Bottleneck Mitigation:** Importing the frost-heave segregation-potential criterion provides a reduced-order dendrite-inception rule for porous separators. The hypothesis is that dendrite penetration through a separator pore is governed at onset by the same capillary-kinetic Robin condition that controls ice-lens nucleation in a freezing pore. This rule can replace purely concentration-depletion criteria in separator design screens and can identify pore radii and interfacial resistances for which dendrite inception is suppressed at practical charging currents.

*   **Falsifiable Prediction:** Prepare cells with identical separator thickness `L`, porosity, tortuosity, electrolyte, and electrode chemistry, but with controlled cylindrical pore radii `r` and `2r`. At a fixed small plating velocity `v_0`, measure the additional overpotential beyond a planar-reference cell required to sustain plating. From the interface law with hemispherical tip curvature `κ = 2 / r`, the radius-dependent overpotential component is

```math
\eta_{\mathrm{rad}}(r)
=
\frac{2 \Gamma_B}{F r}
=
\frac{2 \Omega_{Li} \gamma_{Li}}{F r}.
```

Therefore,

```math
\frac{\eta_{\mathrm{rad}}(r)}{\eta_{\mathrm{rad}}(2r)}
=
2,
\qquad
\eta_{\mathrm{rad}}(r)
-
\eta_{\mathrm{rad}}(2r)
=
\frac{\Omega_{Li} \gamma_{Li}}{F r}.
```

The state-of-the-art Sand-time / Newman porous-electrode baseline, when held at fixed electrolyte and transport parameters, predicts no such pore-radius-dependent overpotential increment; its predicted radius-dependent component is zero, or equivalently a ratio of one after experimental noise is included. The prediction is falsified if the measured radius-dependent overpotential increment is statistically indistinguishable from zero, or if the measured scaling exponent in `η_rad ∝ r^{-α}` is not close to `α = 1` under conditions where the capillary term dominates the kinetic term.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"cryogenic suction" AND "ice segregation" AND "Stefan condition"`
*   `"electrochemical potential" AND "Butler-Volmer" AND "moving boundary" AND "lithium dendrite"`
*   `"frost heave" AND "lithium dendrite" AND "segregation potential"`
*   `"Gibbs-Thomson" AND "cryogenic suction" AND "Nernst-Planck"`
*   `"separator pore radius" AND "critical overpotential" AND "lithium plating"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos reduce to a quasi-steady, linearized divergence-form transport equation (`∇·(K_w∇Π_A)=0` / `∇·(M_B∇Π_B)=0`), a linear Robin interface condition, and a linear Stefan-type accretion law; the nondimensionalization in Section 3 (`u_A=Π_A/ΔΠ_A`, `u_B=Π_B/ΔΠ_B`, `M̂_A=K_w/K_w^0`, `M̂_B=M_B/M_B^0`) is carried out explicitly and reduces correctly to `∇_x̂·(M̂∇_x̂u)=0`, and the entry itself scopes out the regimes (non-dilute transport, double-layer effects, saturation-dependent permeability) where the linear correspondence would break down.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — In the pairing `Gibbs-Thomson ice coefficient Γ_A ↔ lithium capillary coefficient Γ_B` (Section 2), `Γ_A = 2γ_iw/ρ_i` is dimensionally a specific (per-unit-mass) coefficient while `Γ_B = Ω_Li γ_Li` is a molar coefficient; this implies `Π_A` and `Π_B` are on different physical bases that Section 2/3 never reconciles, even though it does not break the later nondimensionalized operator identity.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three YAML-listed vectors are demonstrated with explicit paired equations in Section 3: Vector 1 (`chemical_potential_divergence_mobility_transport_operator`) via `∇·(K_w∇Π_A)=0` and `∇·(M_B∇Π_B)=0` unified into `∇_x̂·(M̂∇_x̂u)=0`; Vector 2 (`capillary_kinetic_robin_interface_condition`) via the shared `Π_i=Rv_n+Γκ` form with explicit `(Π,R,Γ,v_n)_A` / `(Π,R,Γ,v_n)_B` identification; Vector 3 (`stefan_faraday_normal_flux_accretion_law`) via the shared `ρ_ph v_n=M∂_nΠ` form with explicit `(ρ_ph,M)_A` / `(ρ_ph,M)_B` identification.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (a) and falsifiability (b) are individually satisfied: the transfer direction targets a specific named capability gap (a compact pore-scale inception criterion) rather than a generic maturity claim, and Section 4's prediction (`η_rad(r)/η_rad(2r)=2`, correctly derived from `Γ_B` and `κ=2/r`) names a concrete measurable ratio against a stated null (Sand-time/Newman baseline predicting ratio 1). Prior art (c, advisory): both frost-heave theory and lithium-dendrite modeling are independently recognizable as drawing on classical Stefan/Gibbs–Thomson solidification theory (e.g., Monroe & Newman-style dendrite-growth analyses on the battery side, segregation-potential/frozen-fringe theory on the frost-heave side); this shared ancestry should be checked at Stage 3 and is not grounds for rejection.

#### Stage 3 Watch Items
- Reconcile the specific (per-mass) basis implied by `Γ_A = 2γ_iw/ρ_i` against the molar basis implied by `Γ_B = Ω_Li γ_Li`, and confirm the intended units of `ψ`, `Π_A`, and `K_w` given `K_w` is used against a potential gradient rather than a hydraulic-head gradient.
- Search for existing literature directly pairing frost-heave segregation-potential theory with lithium-dendrite inception criteria, and separately check whether battery literature already has a compact pore-curvature inception rule beyond planar-front stability analyses, which would weaken Section 4's stated bottleneck claim.
- Verify the `κ=2/r` hemispherical-tip curvature convention in Section 4 is applied consistently with whatever convention `κ` carries in Section 3's general Robin condition.
- Check how restrictive the "locally constant `K_w`" assumption is relative to standard frozen-fringe treatments, where hydraulic conductivity is typically strongly suction- and temperature-dependent.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The lithium interface law `Π_{B,i} = R_{ct} v_B + Γ_B κ` is written with `Π_{B,i} = μ̃ - μ̃_eq` in J/mol, while the entry defines `R_ct` as an overpotential per unit velocity, so `R_ct v_B` is a voltage; the equation adds a voltage to the molar-energy capillary term `Γ_B κ = Ω_Li γ_Li κ` and is missing the Faraday conversion factor.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are compatible mathematical types: potentials, mobility coefficients, velocities, interface resistances, curvature coefficients, and driving drops. No category error is apparent.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are explicitly assigned displayed equations in Section 3. The defect in Vector 2 is equation validity, already counted under Check 1, not absence of supporting body text.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The geocryology→electrodeposition direction is plausibly asymmetric as argued, and the radius-dependent overpotential prediction is quantitative and falsifiable. No canonical prior-art analogy is recognized here; bibliometric verification is still advised.

#### Stage 3 Watch Items
- Prior-art check for published frost-heave ↔ lithium-dendrite / ice-lens ↔ dendrite free-boundary analogies.
- Verify the corrected Butler-Volmer linearization coefficient (`F R_ct` vs `R_ct`) if the equation is repaired.
- Human review of the frost-heave Gibbs-Thomson coefficient `Γ_A = 2 γ_iw / ρ_i` for dimensional consistency in the chosen water-potential convention.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The equations exhibit flawlessly consistent physical dimensions and correctly identify identical operator classes (quasi-steady Laplace transport, affine Robin boundary conditions, and a linear Stefan accretion law) for both domains under the stated limits.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings correctly align parameters of identical mathematical type and physical role, successfully reconciling the domain-specific intensive variables (mass-specific chemical potential vs. molar electrochemical potential).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three correspondence vectors listed in the YAML (`chemical_potential_divergence_mobility_transport_operator`, `capillary_kinetic_robin_interface_condition`, and `stefan_faraday_normal_flux_accretion_law`) are explicitly derived and demonstrated in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction appropriately leverages the more mature interfacial curvature mechanics of geocryology to address a known gap in reduced-order battery separator design. The falsifiable prediction provides a highly specific, mathematically rigorous scaling law that directly contrasts with the standard porous-electrode baseline.

#### Stage 3 Watch Items
- Check recent literature on solid-state battery mechanics and dendrite propagation (e.g., works by Monroe, Newman, or modern phase-field studies) for prior conceptual or mathematical analogies to frost heave and ice lens segregation.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B equations are elliptic divergence-form transport operators, both interface conditions are affine Robin-type with kinetic resistance and Gibbs-Thomson curvature terms, and both accretion laws are normal-flux Stefan conditions. The nondimensionalization is explicit and reduces both to the same form.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six paired mappings connect objects of compatible mathematical type (scalar potentials ↔ scalar potentials, mobility coefficients ↔ mobility coefficients, velocity ↔ velocity, resistance coefficients ↔ resistance coefficients, Gibbs-Thomson coefficients ↔ Gibbs-Thomson coefficients, driving potential differences ↔ driving potential differences), and each Operator Role specifies a shared mathematical structure with explicit parameter identification.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (chemical_potential_divergence_mobility_transport_operator, capillary_kinetic_robin_interface_condition, stefan_faraday_normal_flux_accretion_law) are demonstrated in Section 3 with full equations on both sides, explicit parameter identifications, and nondimensionalization to a common form.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (frost heave → lithium dendrite) is asymmetric: frost heave has mature compact segregation-potential criteria for pore-scale inception, while lithium modeling lacks an equivalent reduced-order free-boundary inception rule. The falsifiable prediction names a specific measurable ratio (η_rad(r)/η_rad(2r) = 2), a specific scaling exponent (α = 1), and explicit falsification conditions. No canonical prior-art analogy recognized for this specific domain pairing.

#### Stage 3 Watch Items
- The Stefan/free-boundary template for electrochemical deposition has been explored in phase-field dendrite modeling and mushy-zone literature. Stage 3 should probe whether the specific frost-heave-to-lithium mapping (frozen-fringe film flow + segregation potential → dendrite inception criterion) is novel or has prior art.
- The entry's claimed validity regime (isothermal, dilute, quasi-steady, linearized-kinetics) should be verified as physically realizable in laboratory dendrite-inception experiments at the pore scales relevant to the prediction.
- The linearized charge-transfer resistance R_ct parameterized as overpotential-per-unit-velocity is internally consistent but non-standard; Stage 3 should check experimental validation at relevant current densities.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos present quasi-steady elliptic divergence-form transport equations (∇·(M∇Π)=0), Robin-type kinetic-capillary interface conditions (Π_i = R v_n + Γ κ), and Stefan-type normal-flux accretion laws (ρ_ph v_n = M ∂_n Π). No equation-class mismatch: both are elliptic free-boundary problems of the same structural type. The lithium electrochemical potential μ̃ = μ⁰ + RT ln(c/c_ref) + Fφ correctly yields the Nernst-Planck flux J = -M_B ∇μ̃ = -D∇c - (DFc/RT)∇φ when expanded, confirming the equation is genuinely from the electrochemistry domain rather than a relabeled equation from a third field. The frost-heave transport equation is the standard quasi-steady Darcy form. The two equations together support the claimed structural correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six paired mappings connect objects of compatible mathematical type: scalar thermodynamic potentials ↔ scalar thermodynamic potentials, mobility coefficients ↔ mobility coefficients, normal velocities ↔ normal velocities, kinetic resistance coefficients ↔ kinetic resistance coefficients, capillary coefficients ↔ capillary coefficients, and boundary driving differences ↔ boundary driving differences. Each Operator Role explanation specifies the shared mathematical structure (the divergence-form operator, the Robin condition, or the Stefan law) rather than relying on hedged analogy language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are explicitly demonstrated in Section 3 with paired equations and parameter identifications. Vector 1 (transport operator) is shown via ∇·(K_w∇Π_A)=0 and ∇·(M_B∇Π_B)=0 collapsing to the same nondimensional form ∇_{x̂}·(M̂∇_{x̂}u)=0. Vector 2 (Robin interface condition) is shown via Π_{A,i}=R_f v_A+Γ_A κ and Π_{B,i}=R_ct v_B+Γ_B κ with explicit parameter correspondences. Vector 3 (Stefan accretion) is shown via ρ_i v_A=ρ_w K_w ∂_n Π_A and (1/Ω_Li) v_B=M_B ∂_n Π_B with the unified form ρ_ph v_n = M ∂_n Π. No vector is merely named or gestured at.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetry is plausible: frost-heave mechanics possesses mature analytical segregation criteria (Miller-type frozen-fringe models, Rempel et al. premelting theory) that combine capillary, kinetic, and transport effects in compact form, while lithium-dendrite modeling relies primarily on phase-field simulations and Newman porous-electrode models that do not yield a compact pore-scale inception criterion. The transfer direction is not backwards. The falsifiable prediction is specific: it names a measurable quantity (radius-dependent overpotential increment η_rad), a specific experimental design (cells with pore radii r and 2r at fixed v_0), a quantitative threshold (η_rad(r)/η_rad(2r) = 2, or equivalently scaling exponent α = 1 in η_rad ∝ r^{-α}), and a clear falsification condition (statistically indistinguishable from zero, or α ≠ 1). This is not a template non-prediction. Advisory: the Stefan problem and Gibbs-Thomson effect are classical in both solidification theory and electrochemistry; Stage 3 should verify whether this specific cross-domain mapping has prior art.

#### Stage 3 Watch Items
- Check whether the frost-heave ↔ lithium-electrodeposition Stefan-problem mapping has been previously published. The Gibbs-Thomson/capillary-kinetic interface condition is standard in solidification theory, and its application to electrodeposition is known; prior art may exist at the solidification-electrochemistry intersection.
- Verify the dimensional convention for Γ_A = 2γ_iw/ρ_i: if Π_A is in pressure units (Pa), the prefactor 2γ_iw/ρ_i has units m³/s² rather than Pa·m, suggesting Π_A is mass-specific (J/kg). The nondimensionalization removes this, but the raw dimensional claim should be checked against frost-heave literature conventions.
- Assess whether the falsifiable prediction η_rad = 2Ω_Li γ_Li/(Fr) is genuinely novel. This is a standard Kelvin/Gibbs-Thomson result for curved electrode surfaces; the novelty claim rests on its deployment as a separator-pore dendrite-inception design criterion, not on the formula itself.
- Probe whether the claim "the state-of-the-art Sand-time / Newman porous-electrode baseline predicts no such pore-radius-dependent overpotential increment" is accurate: some Newman-type models can incorporate curvature corrections, and phase-field models of dendrite growth do include surface energy effects.

### Sixth Adversarial Review
**Reviewer:** GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-15

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The frost-heave interface law states “`\\Gamma_A = \\frac{2 \\gamma_{iw}}{\\rho_i}`” in “`\\Pi_{A,i} = R_f v_A + \\Gamma_A \\kappa`”; with the entry's curvature convention `κ = 2/r` for a hemispherical interface and the lithium coefficient `\\Gamma_B = \\Omega_{Li}\\gamma_{Li}`, the frost coefficient carries an extra factor of 2, so the two capillary terms do not actually implement the same Gibbs-Thomson curvature law.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped quantities are scalar potentials, mobility coefficients, interface velocities, resistance coefficients, capillary coefficients, and boundary driving potentials respectively, with the entry explicitly supplying nondimensionalization where needed.
* **CHECK 3 (Correspondence Vector Support):** PASS — `chemical_potential_divergence_mobility_transport_operator`, `capillary_kinetic_robin_interface_condition`, and `stefan_faraday_normal_flux_accretion_law` are each demonstrated for both silos by paired equations and explicit parameter identifications in Section 3.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction is presented as asymmetric on the entry's own maturity rationale, and the prediction specifies measurable radius-dependent overpotential scaling (`r^{-1}`), a quantitative ratio, and explicit falsification conditions.

#### Stage 3 Watch Items
None identified.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The transport equations in Section 3 for both silos are steady divergence-form elliptic equations \(\nabla\cdot(M\nabla\Pi)=0\), the interface laws are affine Robin-type conditions, and the normal-flux accretion laws are Stefan-type relations; these are the same equation class and the entry provides explicit equations for both silos supporting the claimed shared operator.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapped token pair in Section 2 is of compatible mathematical type (scalar driving potentials, positive mobility coefficients, normal interface velocities, interface resistances, curvature coefficients) and the Operator Role descriptions assert explicit shared structure rather than hedged analogy (e.g., both mobilities multiply gradients in the flux-divergence operator).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three YAML-listed vectors are demonstrated in the body with equations and identifications:  
  - **chemical_potential_divergence_mobility_transport_operator** — shown by \(\mathcal{L}_A[\Pi_A]=\nabla\cdot(K_w\nabla\Pi_A)=0\) and \(\mathcal{L}_B[\Pi_B]=\nabla\cdot(M_B\nabla\Pi_B)=0\) and the nondimensional form \(\nabla_{\hat{x}}\cdot(\hat{M}\nabla_{\hat{x}}u)=0\).  
  - **capillary_kinetic_robin_interface_condition** — shown by \(\Pi_{A,i}=R_f v_A+\Gamma_A\kappa\) and \(\Pi_{B,i}=R_{ct} v_B+\Gamma_B\kappa\) and the unified \(\Pi_i=R v_n+\Gamma\kappa\) identification.  
  - **stefan_faraday_normal_flux_accretion_law** — shown by \(\rho_i v_A=\rho_w K_w\,\partial_n\Pi_A\) and \(\tfrac{1}{\Omega_{Li}}v_B=M_B\,\partial_n\Pi_B\) and the unified \(\rho_{\mathrm{ph}} v_n = M\,\partial_n\Pi\).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric (frost-heave → electrodeposition) as argued, and the entry provides a concrete, measurable falsifiable prediction \(\eta_{\mathrm{rad}}(r)=2\Gamma_B/(F r)\) with an explicit ratio \(\eta_{\mathrm{rad}}(r)/\eta_{\mathrm{rad}}(2r)=2\), which specifies an experimentally testable scaling exponent \(\alpha\approx 1\).

#### Stage 3 Watch Items
- "Confirm whether the linearized kinetic coefficient \(R_{ct}\) used as an overpotential-per-velocity is consistent with standard electrochemical linearization conventions and with the nondimensionalization applied in Section 3."
- "Check for prior-art overlap with Stefan-type moving-boundary formulations applied to electrodeposition and any existing literature that already frames dendrite inception via capillarity-kinetic Robin conditions (advisory; do not use as grounds for rejection)."
- "Assess experimental practicality of isolating the capillary term in \(\eta_{\mathrm{rad}}(r)=2\Omega_{Li}\gamma_{Li}/(F r)\) from other contributions (kinetic, ohmic, transport) in real porous separators."

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides are quasi-steady elliptic divergence-form mobility operators closed by identical affine Robin capillary-kinetic conditions and normal-flux Stefan accretion laws; after the explicit nondimensionalization they coincide, supporting the claimed structural identity.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of matching mathematical type (scalar potential, mobility coefficient, free-boundary velocity, interfacial resistance, capillary coefficient, far-field driving drop) and the Operator Role statements name the shared operator or identity after scaling.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (chemical_potential_divergence_mobility_transport_operator, capillary_kinetic_robin_interface_condition, stefan_faraday_normal_flux_accretion_law) are demonstrated by side-by-side equations and the common nondimensional form in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric as argued (mature free-boundary criteria exist in frost-heave; lithium literature lacks the compact pore-scale inception rule); the prediction supplies a concrete, measurable ratio η_rad(r)/η_rad(2r)=2 and difference formula that the Sand/Newman baseline predicts to be unity/zero, with explicit statistical falsification criteria.

#### Stage 3 Watch Items
- Confirm that the electrochemical-potential definition of Π_B (energy/mole) is consistently converted to voltage by the factor 1/F in experimental realizations of the predicted η_rad scaling.
- Verify that the quasi-steady dilute-limit assumptions used for both transport operators remain valid under the stated experimental conditions of the falsifiable prediction.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-15

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A `∇·(K_w ∇Π_A)=0` and Silo B `∇·(M_B ∇Π_B)=0` are elliptic divergence-form mobility operators in the stated quasi-steady, dilute, linearized limit, with matching interface `Π_i = R v_n + Γ κ` and Stefan `ρ_ph v_n = M ∂_n Π` laws, supporting the claimed Stefan-type isomorphism after explicit nondimensionalization.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six mappings pair compatible types (scalar potential ↔ scalar potential, mobility coefficient ↔ mobility coefficient, normal velocity ↔ normal velocity, resistance ↔ resistance, capillary coefficient ↔ capillary coefficient, driving potential drop ↔ driving potential drop) with shared operator roles and stated nondimensionalization `u = Π/ΔΠ`, no category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three YAML vectors are demonstrated in Section 3: chemical_potential_divergence_mobility_transport_operator via `ℒ[u]=∇·(M̂∇u)=0`, capillary_kinetic_robin_interface_condition via `Π_i = R v_n + Γ κ` with `Γ_A=2γ_iw/ρ_i` and `Γ_B=Ω_Liγ_Li`, stefan_faraday_normal_flux_accretion_law via `ρ_ph v_n = M ∂_n Π` with both Silo A and Silo B forms and parameter identifications.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is justified: frost-heave mature segregation/curvature criteria → Li-battery lacks compact pore-scale inception rule without full phase-field. Falsifiability names measurable `η_rad(r)=2Γ_B/(F r)`, ratio `η_rad(r)/η_rad(2r)=2`, difference `Ω_Liγ_Li/(F r)`, and exponent `η_rad∝r^{-α}` with `α=1` vs baseline zero/ratio one. No canonical textbook prior-art pairing recognized; advisory none.

#### Stage 3 Watch Items
- None identified.